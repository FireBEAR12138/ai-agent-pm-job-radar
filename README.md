# 国内互联网大厂 AI 岗位监控 Skill

为了方便及时跟进和了解市场上 AI 或 Agent 相关的产品经理岗位，我编写了这样一个 skill：

1. 能够从各家招聘网站中，根据相关关键词找到对应的岗位 JD
2. 能够以网页看板的形式，将所有岗位统一展示出来

目前该 skill 已支持 11 个公司。

当前抓取口径：分别用两个单关键词 `AI`、`Agent` 抓取招聘官网结果，并过滤岗位标题包含“产品经理”的岗位；不使用组合词 `AI Agent`，也不使用 `大模型`、`AIGC`、`智能体`、`人工智能` 等额外搜索词。

## 项目文件

- `ai_agent_pm_jobs.html`：静态岗位看板页面，可直接用浏览器打开，也可通过 GitHub Pages 访问。
- `data/`：岗位 CSV、Markdown 明细和岗位变动记录。
- `.codex/skills/ai-agent-pm-job-radar/SKILL.md`：Codex Skill 使用说明，记录各招聘站抓取技巧、重试策略和页面更新规则。

## 页面截图

### 看板视图

![AI / Agent 产品经理岗位看板截图](assets/ai-agent-pm-dashboard.png)

### 岗位列表

![AI / Agent 产品经理岗位列表截图](assets/ai-agent-pm-jobs-list.png)

## 当前已支持公司

| 公司名 | 岗位数量 | 本次更新 | 更新时间 |
|---|---:|---:|---|
| [快手](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/kuaishou_ai_agent_pm_jobs.csv) | 24 | +0 -0 | 2026/07/06 23:17:33 |
| [字节跳动](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/bytedance_ai_agent_pm_jobs.csv) | 29 | +0 -0 | 2026/07/06 23:17:33 |
| [腾讯](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/tencent_ai_agent_pm_jobs.csv) | 58 | +0 -0 | 2026/07/06 23:17:33 |
| [小米](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/xiaomi_ai_agent_pm_jobs.csv) | 15 | +0 -0 | 2026/07/06 23:17:33 |
| [百度](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/baidu_ai_agent_pm_jobs.csv) | 135 | +0 -2 | 2026/07/06 23:17:33 |
| [理想](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/lixiang_ai_agent_pm_jobs.csv) | 14 | +1 -0 | 2026/07/06 23:17:33 |
| [阿里云](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/aliyun_ai_agent_pm_jobs.csv) | 12 | +0 -0 | 2026/07/06 23:17:33 |
| [淘天集团](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/taotian_ai_agent_pm_jobs.csv) | 35 | +1 -1 | 2026/07/06 23:17:33 |
| [蚂蚁集团](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/antgroup_ai_agent_pm_jobs.csv) | 23 | +0 -0 | 2026/07/06 23:17:33 |
| [千问事业部](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/qianwen_ai_agent_pm_jobs.csv) | 9 | +0 -0 | 2026/07/06 23:17:33 |
| [通义](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/tongyi_ai_agent_pm_jobs.csv) | 2 | +0 -0 | 2026/07/06 23:17:33 |

## 近 3 日新增

> 注：这里的日期是抓取变动日期，不是岗位发布时间；仅展示近 3 日内确认的新增岗位，不包含下架记录。

| 日期 | 公司 | 岗位名 | URL |
|---|---|---|---|
| 2026-07-06 | 理想 | 充电体验产品经理 | https://www.lixiang.com/employ/detail/19413.html |
| 2026-07-06 | 淘天集团 | 1688-AI金融产品经理（商户洞察方向）-杭州 | https://talent.taotian.com/off-campus/position-detail?positionId=100019260008 |
