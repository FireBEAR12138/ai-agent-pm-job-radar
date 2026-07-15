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
| [快手](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/kuaishou_ai_agent_pm_jobs.csv) | 26 | +1 -0 | 2026/07/16 00:06:21 |
| [字节跳动](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/bytedance_ai_agent_pm_jobs.csv) | 35 | +0 -0 | 2026/07/16 00:06:21 |
| [腾讯](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/tencent_ai_agent_pm_jobs.csv) | 58 | +0 -1 | 2026/07/16 00:06:21 |
| [小米](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/xiaomi_ai_agent_pm_jobs.csv) | 20 | +2 -0 | 2026/07/16 00:06:21 |
| [百度](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/baidu_ai_agent_pm_jobs.csv) | 128 | +0 -1 | 2026/07/16 00:06:21 |
| [理想](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/lixiang_ai_agent_pm_jobs.csv) | 10 | +0 -0 | 2026/07/16 00:06:21 |
| [阿里云](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/aliyun_ai_agent_pm_jobs.csv) | 15 | +1 -0 | 2026/07/16 00:06:21 |
| [淘天集团](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/taotian_ai_agent_pm_jobs.csv) | 35 | +1 -1 | 2026/07/16 00:06:21 |
| [蚂蚁集团](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/antgroup_ai_agent_pm_jobs.csv) | 23 | +1 -1 | 2026/07/16 00:06:21 |
| [千问事业部](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/qianwen_ai_agent_pm_jobs.csv) | 8 | +0 -0 | 2026/07/16 00:06:21 |
| [通义](https://github.com/FireBEAR12138/ai-agent-pm-job-radar/blob/main/data/tongyi_ai_agent_pm_jobs.csv) | 2 | +0 -0 | 2026/07/16 00:06:21 |


## 近 3 日新增

> 注：这里的日期是抓取变动日期，不是岗位发布时间；仅展示近 3 日内确认的新增岗位，不包含下架记录。

| 日期 | 公司 | 岗位名 | URL |
|---|---|---|---|
| 2026-07-16 | 快手 | AIGC产品经理（电商广告）-【电商】 | https://zhaopin.kuaishou.cn/recruit/e/#/official/social/job-info/31559 |
| 2026-07-16 | 小米 | 财务数据产品经理 | https://xiaomi.jobs.f.mioffice.cn/index/position/7661947261148301618/detail |
| 2026-07-16 | 小米 | 高级产品经理（AI 漫剧创作平台） | https://xiaomi.jobs.f.mioffice.cn/index/position/7662654539741055268/detail |
| 2026-07-16 | 阿里云 | ATH事业群-AI原生应用产品经理-杭州 | https://careers.aliyun.com/off-campus/position-detail?positionId=100011383005 |
| 2026-07-16 | 淘天集团 | M&T事业部-玩美生活 & 企业服务-AI产品经理 | https://talent.taotian.com/off-campus/position-detail?positionId=100024520005 |
| 2026-07-16 | 蚂蚁集团 | 蚂蚁集团-企业助手B端产品经理-芝麻企业信用 | https://talent.antgroup.com/off-campus-position/26010908319892 |
| 2026-07-15 | 字节跳动 | Coding Agent产品经理-扣子 | https://jobs.bytedance.com/experienced/position/7650041514577316101/detail |
| 2026-07-15 | 字节跳动 | 企业级Agent应用产品经理-数据平台 | https://jobs.bytedance.com/experienced/position/7568396650255911173/detail |
| 2026-07-15 | 腾讯 | 腾讯游戏-多模态数据策略产品经理-视频生成方向 | https://careers.tencent.com/jobdesc.html?postId=2073970041505890304&language=zh-cn |
| 2026-07-15 | 腾讯 | 腾讯游戏-多模态数据策略产品经理-视频生成方向 | https://careers.tencent.com/jobdesc.html?postId=2073970038867668992&language=zh-cn |
| 2026-07-15 | 腾讯 | 腾讯游戏-多模态数据策略产品经理-视频生成方向 | https://careers.tencent.com/jobdesc.html?postId=2073970036510470144&language=zh-cn |
| 2026-07-15 | 淘天集团 | 天猫事业部-商家AI数据产品经理-杭州 | https://talent.taotian.com/off-campus/position-detail?positionId=100023960006 |
| 2026-07-15 | 淘天集团 | 营销平台及市场部-AI产品经理（中台）-杭州 | https://talent.taotian.com/off-campus/position-detail?positionId=100024300001 |
