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
| [快手](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/kuaishou_ai_agent_pm_jobs.csv) | 25 | +0 -0 | 2026/07/10 23:59:59 |
| [字节跳动](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/bytedance_ai_agent_pm_jobs.csv) | 30 | +0 -0 | 2026/07/10 23:59:59 |
| [腾讯](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/tencent_ai_agent_pm_jobs.csv) | 58 | +0 -0 | 2026/07/10 23:59:59 |
| [小米](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/xiaomi_ai_agent_pm_jobs.csv) | 16 | +0 -0 | 2026/07/10 23:59:59 |
| [百度](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/baidu_ai_agent_pm_jobs.csv) | 135 | +1 -0 | 2026/07/10 23:59:59 |
| [理想](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/lixiang_ai_agent_pm_jobs.csv) | 10 | +0 -0 | 2026/07/10 23:59:59 |
| [阿里云](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/aliyun_ai_agent_pm_jobs.csv) | 12 | +0 -0 | 2026/07/10 23:59:59 |
| [淘天集团](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/taotian_ai_agent_pm_jobs.csv) | 35 | +0 -2 | 2026/07/10 23:59:59 |
| [蚂蚁集团](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/antgroup_ai_agent_pm_jobs.csv) | 23 | +0 -1 | 2026/07/10 23:59:59 |
| [千问事业部](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/qianwen_ai_agent_pm_jobs.csv) | 9 | +0 -0 | 2026/07/10 23:59:59 |
| [通义](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/tongyi_ai_agent_pm_jobs.csv) | 2 | +0 -0 | 2026/07/10 23:59:59 |


## 近 3 日新增

> 注：这里的日期是抓取变动日期，不是岗位发布时间；仅展示近 3 日内确认的新增岗位，不包含下架记录。

| 日期 | 公司 | 岗位名 | URL |
|---|---|---|---|
| 2026-07-10 | 百度 | 百度网盘APP-AI产品经理（工具体验方向）（J97004） | https://talent.baidu.com/jobs/detail/SOCIAL/84cbba90-c72e-4047-ab6f-d8a0e12946c1 |
| 2026-07-09 | 蚂蚁集团 | 蚂蚁集团-芝麻信用商业产品经理-芝麻信用 | https://talent.antgroup.com/off-campus-position/260709010851063 |
| 2026-07-09 | 百度 | 百度文库 PC 端高级产品经理（J81716） | https://talent.baidu.com/jobs/detail/SOCIAL/e83a0eeb-36f2-4b3c-92bd-fbf07d036d25 |
| 2026-07-09 | 百度 | 搜索策略产品经理（医院决策方向）（J100597） | https://talent.baidu.com/jobs/detail/SOCIAL/3aec4215-cdd7-4be0-a860-df969b953c7f |
| 2026-07-09 | 百度 | 平台供给引入产品经理（生活服务方向）​​（J85108） | https://talent.baidu.com/jobs/detail/SOCIAL/78d10ce7-78f5-48d7-bf14-7781fd933830 |
| 2026-07-09 | 百度 | 健康AI产品经理（J101199） | https://talent.baidu.com/jobs/detail/SOCIAL/40f97291-9468-4c96-9a2e-c8a358328984 |
| 2026-07-09 | 百度 | 产品经理（J100962） | https://talent.baidu.com/jobs/detail/SOCIAL/7cc6a8b2-24af-4f83-8b58-72eca83dcfb9 |
| 2026-07-09 | 百度 | C端用户产品经理（J90816） | https://talent.baidu.com/jobs/detail/SOCIAL/a029e532-a22d-4430-b108-14b08bb64288 |
| 2026-07-09 | 百度 | AI产品经理（企业效能方向）（J101407） | https://talent.baidu.com/jobs/detail/SOCIAL/645aeeb5-f2a7-4df3-b13c-d90a6006aac3 |
| 2026-07-09 | 快手 | 内容风控策略产品经理（版权IP方向）-【可灵AI专项】 | https://zhaopin.kuaishou.cn/recruit/e/#/official/social/job-info/31524 |
| 2026-07-08 | 腾讯 | 智能体套件-高级产品经理-CodeBuddy/WorkBuddy | https://careers.tencent.com/jobdesc.html?postId=2074756585305059328&language=zh-cn |
| 2026-07-08 | 百度 | 车载语音产品经理（J78057） | https://talent.baidu.com/jobs/detail/SOCIAL/b66645b2-1162-4c78-8537-8ea36b966105 |
| 2026-07-08 | 淘天集团 | 平台及用户产品事业部-商品详情产品经理-AI/垂类方向 | https://talent.taotian.com/off-campus/position-detail?positionId=7000043120 |
| 2026-07-08 | 淘天集团 | M&T事业部-商家工具AI产品经理-杭州 | https://talent.taotian.com/off-campus/position-detail?positionId=100022940005 |
