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
4. Normalize rows to these logical fields: company/source, title, matched keywords, location, published time, official URL, JD.
   - If the official site does not disclose a publish time, use the first successful crawl time as the row's recorded time.
   - For existing no-publish-time jobs, preserve their previous recorded time on later refreshes; do not overwrite it every run.
5. Filter to product-manager roles:
   - title must include `产品经理`
   - title or JD must match at least one of: `AI`, `人工智能`, `大模型`, `AIGC`, `Agent`, `agent`, `智能体`
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

### 腾讯

- List API: `https://careers.tencent.com/tencentcareer/api/post/Query`
- Query params: `keyword`, `pageIndex`, `pageSize=50`, `language=zh-cn`, `timestamp`
- Detail API: `https://careers.tencent.com/tencentcareer/api/post/ByPostId?postId=...&language=zh-cn`
- Include both `Responsibility` and `Requirement` in JD.
- Detail URL: `https://careers.tencent.com/jobdesc.html?postId={PostId}`

### 百度

- API: `https://talent.baidu.com/httservice/getPostListNew`
- Method: `POST`, form encoded.
- Payload: `recruitType=SOCIAL`, `pageSize`, `keyWord`, `curPage`, `postType`, `workPlace`, `projectType`.
- Detail URL should be `https://talent.baidu.com/jobs/detail/SOCIAL/{postId}` when `postId` exists.
- JD fields: `workContent` and `serviceCondition`.

### 理想

- List API: `https://www.lixiang.com/osd-hr-recruitment-website/v1/recruit/social/job-page`
- Query params: `page`, `page_size=10`, `search`.
- Detail API: `https://www.lixiang.com/osd-hr-recruitment-website/v1/recruit/job/detail?job_id=...`
- Detail URL: `https://www.lixiang.com/employ/detail/{job_id}.html`
- JD fields: `description` and `requirements`.
- The current list/detail API may not provide publish time. For each new official job with no publish time, set `发布时间` to the current successful crawl timestamp as its recorded/entry time. If the job already exists in `data/lixiang_ai_agent_pm_jobs.csv`, preserve the existing `发布时间`.

### 阿里云 / 淘天集团 / 千问事业部 / 通义

These share the Alibaba CPO portal pattern:

1. GET the page URL.
2. Extract `window.__sysconfig.__token__`.
3. Extract `window.__sysconfig.channelCodeMap.offCampus`; fallback to the known channel.
4. POST `{host}/position/search?_csrf={token}` as JSON:

```json
{"channel":"...","language":"zh","pageIndex":1,"pageSize":50,"key":"AI"}
```

Repeat for `Agent`, paginate by `totalCount`, and use list fields `name`, `description`, `requirement`, `workLocations`, `publishTime`, `positionUrl`.

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

- The search response already includes `description`, `requirement`, `workLocations`, `publishTime`, and `id`; merge `description` and `requirement` into JD.
- Detail URL format: `https://talent.antgroup.com/off-campus-position/{id}`.
- Do not treat a non-browser `405` as empty results; fall back to browser-captured requests first.

### 快手 / 字节跳动 / 小米

Use the latest known public APIs if still accessible, but expect some to block or return non-JSON. Always retry once before fail-open:

- 快手 known endpoint: `https://zhaopin.kuaishou.cn/recruit/e/api/v1/open/positions/simple`
- 字节 known endpoint: `https://jobs.bytedance.com/api/v1/search/job/posts`
- 小米 known endpoint: `https://xiaomi.jobs.f.mioffice.cn/api/v1/search/job/posts`

If blocked after retry, keep existing CSV and report the reason.

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

Build `dashboard.jobChanges` from the latest 7 distinct job dates/recorded dates, not 3.

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
