---
name: ai-agent-pm-job-radar
description: Refresh and maintain the local AI / Agent product-manager job radar without relying on a fixed repository scraper. Use when the user asks to update, refresh, check, rebuild, or report AI/Agent 产品经理岗位 data, CSV/Markdown outputs, job change logs, source scraping behavior, or the static dashboard at ai_agent_pm_jobs.html.
---

# AI / Agent PM Job Radar

## Core Rule

Act as the scraper. Do not rely on a checked-in refresh script. For each refresh, write any needed Python/JS as temporary one-off code in the shell, run it, inspect results, and leave no durable scraper in the repository.

The persistent artifacts are only:

- `data/*_ai_agent_pm_jobs.csv`
- `data/*_ai_agent_pm_jobs.md`
- `data/ai_agent_pm_job_change_log.csv`
- `data/ai_agent_pm_job_change_log.md`
- `ai_agent_pm_jobs.html`

During a routine refresh, update data and the `jobData` JSON payload only. Do not change page styling or layout.

## Refresh Flow

1. Work from the repository root containing `ai_agent_pm_jobs.html`.
2. Read existing CSVs first so each source can fail open after retry.
3. For every source, fetch live data. If a source fails, retry that source once after a short delay. Only after the retry fails, keep the existing CSV under `data/` for that source and record the failure.
   - If a source fails after retry, do not modify that company's CSV/Markdown outputs in the eventual GitHub push. A failed source must remain byte-for-byte as it was before that source's refresh attempt unless the user explicitly asks to overwrite it.
4. Normalize rows to these logical fields: company/source, title, matched keywords, location, published time, official URL, JD.
   - If the official site does not disclose a publish time, use the first successful crawl time as the row's recorded time.
   - For existing no-publish-time jobs, preserve their previous recorded time on later refreshes; do not overwrite it every run.
5. Filter to product-manager roles:
   - title must include `产品经理`
   - source search keywords must be exactly two separate single-keyword searches: `AI` and `Agent`
   - title or JD must match at least one of: `AI`, `Agent`, `agent`
6. Write company CSV and Markdown outputs under `data/`.
7. Rebuild `data/ai_agent_pm_job_change_log.csv/.md`.
8. Replace only `<script id="jobData" type="application/json">...</script>` inside `ai_agent_pm_jobs.html`.
9. Verify JSON and frontend script syntax.
10. Report total jobs, source counts, new/delisted counts, and retry/failure details.

## Source Files

Use these current output files:

| Source | CSV |
|---|---|
| 快手 | `data/kuaishou_ai_agent_pm_jobs.csv` |
| 字节跳动 | `data/bytedance_ai_agent_pm_jobs.csv` |
| 腾讯 | `data/tencent_ai_agent_pm_jobs.csv` |
| 小米 | `data/xiaomi_ai_agent_pm_jobs.csv` |
| 百度 | `data/baidu_ai_agent_pm_jobs.csv` |
| 理想 | `data/lixiang_ai_agent_pm_jobs.csv` |
| 阿里云 | `data/aliyun_ai_agent_pm_jobs.csv` |
| 淘天集团 | `data/taotian_ai_agent_pm_jobs.csv` |
| 蚂蚁集团 | `data/antgroup_ai_agent_pm_jobs.csv` |
| 千问事业部 | `data/qianwen_ai_agent_pm_jobs.csv` |
| 通义 | `data/tongyi_ai_agent_pm_jobs.csv` |

## Scraping Techniques

Use browser-like headers for all requests:

```text
User-Agent: Mozilla/5.0
Accept: application/json,text/plain,*/*
```

## High-Failure Source Recovery Playbook

When a source that has failed before returns `0`, HTML, `illegal-visit`, `405`, a stale first page, or a response shape that does not contain jobs, do not immediately accept the result as empty. Use this recovery order:

1. Retry once with the exact current source technique below.
2. If direct HTTP is blocked, open the official search page in a real browser session, capture the successful list request from DevTools/network events, then replay that request with the same cookies, headers, token, signature, and pagination payload.
3. Search `AI` and `Agent` as two separate single keywords. Do not combine them into `AI Agent`.
4. Compare the recovered result with the existing company CSV. If a historically populated source suddenly returns zero or far fewer rows, inspect the response shape and retry through browser capture before overwriting the CSV.
5. If a source is intentionally capped or only partially paginated, such as first 10 pages only, never infer delisted jobs from missing rows. Merge captured rows with the existing CSV, record confirmed new jobs, and leave old rows that were outside the observed window in place. Only write delisted changes after a successful full crawl of that source.
6. If the retry still fails, keep that company's existing CSV/Markdown byte-for-byte and report the failure.

Recent successful recoveries to preserve:

- 百度 succeeds through direct form POST only when `Content-Type` is form encoded, `Referer` is the social-list page, and `pageSize=10`. Larger page sizes or JSON payloads can fail.
- 蚂蚁集团 succeeds by capturing the browser-gated `hrcareersweb.antgroup.com/api/social/position/search?ctoken=...` request and reusing `front-user-id`, cookies, `ctoken`, and the same payload shape. Direct non-browser requests can return `405`.
- 阿里云、淘天集团、千问事业部、通义 succeed by extracting each host's `_csrf` token, then retrying `group_official_site` when the page-extracted off-campus channel returns `0`.
- 快手 succeeds by letting the frontend generate `sign` and `signTimestamp`; capture `GET /api/v1/open/positions/simple` from the browser instead of calling unsigned JSON.
- 字节跳动和小米 succeed by letting the frontend generate `_signature`; navigate/search in browser and click pagination rather than mutating `offset` manually.
- 字节跳动、快手、小米等限页或浏览器分页来源只能把已捕获列表作为“仍在线/新增”的证据，不能把未捕获到的旧岗位判定为下架。

### 腾讯

- List API: `https://careers.tencent.com/tencentcareer/api/post/Query`
- Query params: `keyword`, `pageIndex`, `pageSize=50`, `language=zh-cn`, `timestamp`
- Detail API: `https://careers.tencent.com/tencentcareer/api/post/ByPostId?postId=...&language=zh-cn`
- Include both `Responsibility` and `Requirement` in JD.
- Detail URL: `https://careers.tencent.com/jobdesc.html?postId={PostId}&language=zh-cn`
- Reliable refresh pattern:
  1. Search list pages with two separate single-keyword searches: `AI`, then `Agent`.
  2. Use list fields first to reduce detail calls; only call `ByPostId` for candidate rows whose title contains `产品经理` and whose title/list responsibility already hits the AI/Agent keyword set.
  3. Set a short detail timeout and fall back to list `Responsibility` if a detail request stalls, but when detail succeeds always merge `Responsibility` and `Requirement`.

### 百度

- API: `https://talent.baidu.com/httservice/getPostListNew`
- Method: `POST`, form encoded.
- Payload: `recruitType=SOCIAL`, `pageSize`, `keyWord`, `curPage`, `postType`, `workPlace`, `projectType`.
- Detail URL should be `https://talent.baidu.com/jobs/detail/SOCIAL/{postId}` when `postId` exists.
- JD fields: `workContent` and `serviceCondition`.
- This API may return an empty object or `illegal-visit` without browser-like request context. Use form encoding, not JSON, and include `Referer: https://talent.baidu.com/jobs/social-list?search=AI` plus `Content-Type: application/x-www-form-urlencoded; charset=UTF-8`. `Origin: https://talent.baidu.com` is accepted, but `Referer` and exact form content type are the critical headers.
- Keep `pageSize=10`. Larger values such as `50` can return `Illegal argument : pageSize`.
- Successful recovery pattern: for each of `AI` and `Agent`, POST the exact form payload, paginate by `curPage`, stop only after the response list is shorter than `pageSize` or empty, and normalize detail URLs from `postId`. Treat a sudden zero-row result as suspicious unless the browser replay also returns no list.
- If the enhanced request still returns no `data.list`, retry once through a browser session. If the page no longer emits the list request and direct browser `fetch` returns `illegal-visit`, keep the existing CSV and report the failure rather than overwriting with zero rows.

### 理想

- List API: `https://api-web.lixiang.com/osd-hr-recruitment-website/v1/recruit/social/job-page`
- Query params: `page`, `page_size=10`, `search`.
- Detail API: `https://api-web.lixiang.com/osd-hr-recruitment-website/v1/recruit/job/detail?job_id=...`
- Detail URL: `https://www.lixiang.com/employ/detail/{job_id}.html`
- JD fields: `description` and `requirements`.
- The list response uses `data.items` in the current portal. Treat `data.list` as only a fallback.
- The current list/detail API may not provide publish time. For each new official job with no publish time, set `发布时间` to the current successful crawl timestamp as its recorded/entry time. If the job already exists in `data/lixiang_ai_agent_pm_jobs.csv`, preserve the existing `发布时间`.

### 阿里云 / 淘天集团 / 千问事业部 / 通义

These share the Alibaba CPO portal pattern:

1. GET the page URL.
2. Extract `window.__sysconfig.__token__`.
3. Extract `window.__sysconfig.channelCodeMap.offCampus`; fallback to the known channel.
   - If the extracted off-campus channel returns `totalCount=0` for obvious populated searches, retry with `group_official_site` before treating the source as empty. Some Alibaba portals expose a source-specific channel in the page config while the public search results are returned only for `group_official_site`.
   - In the successful recovery, `group_official_site` was the useful fallback for sources that looked empty through the page-extracted channel.
4. POST `{host}/position/search?_csrf={token}` as JSON:

```json
{"channel":"...","language":"zh","pageIndex":1,"pageSize":50,"key":"AI"}
```

Repeat the same flow for the separate single keyword `Agent`, paginate by `totalCount`, and use list fields `name`, `description`, `requirement`, `workLocations`, `publishTime`, `positionUrl`. Do not use `大模型`, `AIGC`, `智能体`, `人工智能`, combined `AI Agent`, or other keywords as source search terms unless the user explicitly changes the scope.

For each Alibaba-family source, keep the token/cookie scoped to that source host. Do not reuse an Aliyun token or cookie for Taotian, Quark/Qianwen, or Tongyi.

If search returns unexpectedly empty results or the user provides an official Alibaba detail URL, fetch the detail page directly as a fallback:

1. Reuse the same cookie/session from the initial GET.
2. Parse `positionId` from `/position-detail?...positionId=...`.
3. POST `{host}/position/detail?_csrf={token}` with JSON:

```json
{"id": 100014403005, "channel": "...", "language": "zh"}
```

Use `id`, not `positionId`, in the detail payload. Sending `positionId` may return a successful response with null fields.

For detail rows, merge `description` and `requirement` into JD, keep the official detail URL, and normalize `publishTime` from milliseconds using Asia/Shanghai time.

Known pages and fallback channels:

| Source | Page | Host | Fallback channel |
|---|---|---|---|
| 阿里云 | `https://careers.aliyun.com/off-campus/position-list?lang=zh&search=ai` | `https://careers.aliyun.com` | `group_official_site` |
| 淘天集团 | `https://talent.taotian.com/off-campus/position-list?lang=zh&search=ai` | `https://talent.taotian.com` | `group_official_site` |
| 千问事业部 | `https://talent.quark.cn/off-campus/position-list` | `https://talent.quark.cn` | `group_official_site` |
| 通义 | `https://careers-tongyi.alibaba.com/off-campus/position-list?lang=zh&search=ai` | `https://careers-tongyi.alibaba.com` | `group_official_site` |

Empty results are valid for these sources; write a header-only CSV and show count `0`.

### 蚂蚁集团

- Page: `https://talent.antgroup.com/off-campus?categories=97&search=ai`
- This site uses a separate browser-gated API host, not the Alibaba CPO `/position/search` host.
- Use a real browser session when direct requests return `405`:
  1. Open the page URL.
  2. Capture the first `POST https://hrcareersweb.antgroup.com/api/social/position/search?ctoken=...` request.
  3. Reuse that request URL, `front-user-id` header, cookies, and browser context.
  4. Paginate with `pageSize=10` and increment `pageIndex` until fewer than 10 rows return.
- Working payload shape:

```json
{"key":"ai","regions":"","categories":"97","subCategories":"97,98,99,100,101,102,403,404,405,406","bgCode":"","socialQrCode":"","pageIndex":1,"pageSize":10,"channel":"group_official_site","language":"zh"}
```

- Replace `key` with the current single keyword (`AI` or `Agent`) while preserving the rest of the captured payload shape.
- The search response may return the list directly under `content`, not `data.list`; inspect both. The rows already include `description`, `requirement`, `workLocations`, `publishTime`, and `id`; merge `description` and `requirement` into JD.
- Detail URL format: `https://talent.antgroup.com/off-campus-position/{id}`.
- Do not treat a non-browser `405` as empty results; fall back to browser-captured requests first.

### 快手

The public list endpoint requires the frontend-generated signature headers. Do not call it with unsigned `POST` JSON.

- Page: `https://zhaopin.kuaishou.cn/recruit/e/#/official/social/?workLocationCode=domestic`
- Signed list endpoint: `GET https://zhaopin.kuaishou.cn/recruit/e/api/v1/open/positions/simple`
- Required query params:
  - `name=AI` or `name=Agent`
  - `pageNum`
  - `pageSize=10`
  - `positionNatureCode=C001`
  - `recruitProject=socialr`
  - `workLocationCode=domestic`
- Required headers are generated by the frontend: `sign` and `signTimestamp`.
- Reliable refresh pattern:
  1. Use a real browser session and navigate to hash URLs such as `https://zhaopin.kuaishou.cn/recruit/e/#/official/social/?workLocationCode=domestic&name=AI&pageNum=1`.
  2. Listen for `GET /api/v1/open/positions/simple` responses and parse `result.total` plus `result.list`.
  3. Repeat pages for the two separate single-keyword searches `AI` and `Agent`; the browser will sign each page request. For routine refreshes, capture up to the first 10 pages per keyword unless the user asks for deeper pagination.
  4. The list response already includes `description`, `positionDemand`, `workLocationsCode`, `updateTime`, and `id`; merge `description` and `positionDemand` into JD.
  5. Detail URL format: `https://zhaopin.kuaishou.cn/recruit/e/#/official/social/job-info/{id}`.

### 字节跳动 / 小米

Use the latest known public APIs if still accessible, but expect some to block or return non-JSON. Always retry once before fail-open:

- 字节 known endpoint: `https://jobs.bytedance.com/api/v1/search/job/posts`
- 小米 known endpoint: `https://xiaomi.jobs.f.mioffice.cn/api/v1/search/job/posts`

The list endpoints require frontend-generated `_signature` query params. Directly changing `offset` with an old signature returns HTML instead of JSON.

Reliable refresh pattern:

1. Use a real browser session.
2. Open the search page:
   - 字节: `https://jobs.bytedance.com/experienced/position?keywords=AI`
   - 小米: `https://xiaomi.jobs.f.mioffice.cn/index?keywords=AI`
3. Listen for `GET /api/v1/search/job/posts` JSON responses and collect `data.job_post_list`.
4. Scroll the main `section.atsx-layout` to the bottom so the pagination is visible.
5. Click `.atsx-pagination-item` page numbers or `.atsx-pagination-next`; the frontend will generate a valid `_signature` for each offset.
6. For 字节, capture only the first 10 pages for the single keyword `AI` and the first 10 pages for the single keyword `Agent`, then merge by `id`.
7. For 小米, capture only the two separate single-keyword searches `AI` and `Agent`, then merge by `id`.
8. Detail URL formats:
   - 字节: `https://jobs.bytedance.com/experienced/position/{id}/detail`
   - 小米: `https://xiaomi.jobs.f.mioffice.cn/index/position/{id}/detail`

When validating Xiaomi detail URLs with direct HTTP requests, use full browser-like HTML headers including `Accept: text/html...` and `Accept-Language`; minimal request headers can be misreported as `404` even when the URL opens in a normal browser.

If blocked after retry or pagination is incomplete, keep existing CSV and report the reason.

## HTML Payload Contract

`ai_agent_pm_jobs.html` stores all data in:

```html
<script id="jobData" type="application/json">...</script>
```

Build payload with:

- `generatedAt`
- `changeSummary`
- `dashboard.sourceCounts`
- `dashboard.keywordCounts`
- `dashboard.cityTop`
- `dashboard.dateTrend` for the latest 12 months only
- `dashboard.monthTrend` for the latest 12 months only
- `dashboard.wordCloud`
- `dashboard.jobChanges`
- `jobs`

Build `dashboard.jobChanges` as near-3-day additions only: use change-log rows whose `变动类型` is `新增` and whose `变动日期` falls within the latest 3 calendar days. Do not include delisted rows in this dashboard module.

Preserve existing JS/CSS unless the user explicitly asks for UI changes.

## Validation

After each refresh, run equivalent checks:

```bash
python3 - <<'PY'
from pathlib import Path
import json, re
text = Path("ai_agent_pm_jobs.html").read_text(encoding="utf-8")
payload = json.loads(re.search(r'<script id="jobData" type="application/json">(.*?)</script>', text, re.S).group(1))
print(payload["generatedAt"], len(payload["jobs"]), payload["dashboard"]["sourceCounts"])
PY
node --check <(python3 - <<'PY'
from pathlib import Path
import re
text = Path("ai_agent_pm_jobs.html").read_text(encoding="utf-8")
print(re.search(r'<script>(.*)</script></body></html>', text, re.S).group(1))
PY
)
```

Do not commit, tag, or push unless the user explicitly asks.
