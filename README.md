# 国内互联网大厂 AI 岗位监控 Skill

为了方便及时跟进和了解市场上 AI 或 Agent 相关的产品经理岗位，我编写了这样一个 skill：

1. 能够从各家招聘网站中，根据相关关键词找到对应的岗位 JD
2. 能够以网页看板的形式，将所有岗位统一展示出来

目前该 skill 已接入 11 个公司/事业部，其中 10 个来源在本轮抓取中返回了岗位数据。

## 项目文件

- `ai_agent_pm_jobs.html`：静态岗位看板，直接用浏览器打开即可查看
- `*_ai_agent_pm_jobs.csv`：各公司岗位明细数据
- `*_ai_agent_pm_jobs.md`：各公司岗位明细 Markdown 版本
- `.codex/skills/ai-agent-pm-job-radar/SKILL.md`：Codex Skill，记录抓取、重试、归一化和页面更新规则
- `ai_agent_pm_job_change_log.csv` / `.md`：岗位变更日志

## 当前已支持公司

| 公司名 | 岗位数量 | 更新时间 |
|---|---:|---|
| 快手 | 43 | 2026/06/28 11:59:56 |
| 字节跳动 | 619 | 2026/06/28 11:59:56 |
| 腾讯 | 64 | 2026/06/28 11:59:56 |
| 小米 | 22 | 2026/06/28 11:59:56 |
| 百度 | 85 | 2026/06/28 11:59:56 |
| 理想 | 8 | 2026/06/28 11:59:56 |
| 阿里云 | 18 | 2026/06/28 11:59:56 |
| 淘天集团 | 61 | 2026/06/28 11:59:56 |
| 蚂蚁集团 | 0 | 2026/06/28 11:59:56 |
| 千问事业部 | 23 | 2026/06/28 11:59:56 |
| 通义 | 3 | 2026/06/28 11:59:56 |

> 注：蚂蚁集团官网本轮直接请求未打通，当前保留为 0；不代表官网确定没有 AI/Agent 产品经理岗位。

## 近 7 日岗位变更

| 日期 | 公司 | 岗位名 | URL |
|---|---|---|---|
| 2026-06-28 | 理想 | AI应用主交互产品经理 | [官网详情](https://www.lixiang.com/employ/detail/18741.html) |
| 2026-06-28 | 理想 | 【人形机器人】商业化产品经理 | [官网详情](https://www.lixiang.com/employ/detail/19219.html) |
| 2026-06-28 | 理想 | 充电体验产品经理 | [官网详情](https://www.lixiang.com/employ/detail/19251.html) |
| 2026-06-28 | 理想 | 具身Agent安全产品经理 (Safety PM) | [官网详情](https://www.lixiang.com/employ/detail/18788.html) |
| 2026-06-28 | 理想 | 智能驾驶AI高级产品经理 | [官网详情](https://www.lixiang.com/employ/detail/15783.html) |
| 2026-06-28 | 理想 | 理想汽车App车控产品经理 | [官网详情](https://www.lixiang.com/employ/detail/18817.html) |
| 2026-06-28 | 理想 | 空间AI产品经理（AI Operator） | [官网详情](https://www.lixiang.com/employ/detail/18922.html) |
| 2026-06-28 | 理想 | 车载控制器产品经理（自动驾驶/AI方向） | [官网详情](https://www.lixiang.com/employ/detail/19003.html) |
| 2026-06-27 | 淘天集团 | 阿里妈妈-AIGC产品经理-杭州/北京 | [官网详情](https://talent.taotian.com/off-campus/position-detail?positionId=100021080002) |
| 2026-06-27 | 淘天集团 | 阿里妈妈-内容广告产品经理-北京/杭州 | [官网详情](https://talent.taotian.com/off-campus/position-detail?positionId=100021080003) |
| 2026-06-26 | 百度 | AI产品经理（J101168） | [官网详情](https://talent.baidu.com/jobs/detail/SOCIAL/1c3db307-c38a-41e1-91aa-761a3579f60f) |
| 2026-06-26 | 百度 | 推荐策略产品经理（J101167） | [官网详情](https://talent.baidu.com/jobs/detail/SOCIAL/d9b55b5d-a9a2-46b7-915e-942d4a0669fe) |
| 2026-06-26 | 腾讯 | 混元大模型平台产品经理（北京/深圳） | [官网详情](http://careers.tencent.com/jobdesc.html?postId=2070472100677857280) |
| 2026-06-26 | 腾讯 | 腾讯混元大模型数据产品经理 | [官网详情](http://careers.tencent.com/jobdesc.html?postId=2064244091922853888) |
| 2026-06-26 | 腾讯 | 腾讯视频-AI 产品经理 | [官网详情](http://careers.tencent.com/jobdesc.html?postId=2046845261342470144) |
| 2026-06-26 | 阿里云 | 阿里云智能-AI原生数据库产品经理-北京/杭州 | [官网详情](https://careers.aliyun.com/off-campus/position-detail?lang=zh&positionId=100014403005) |
| 2026-06-25 | 千问事业部 | 千问事业部-UC浏览器产品经理-会员产品-广州 | [官网详情](https://talent.quark.cn/off-campus/position-detail?positionId=100020840003) |
| 2026-06-25 | 淘天集团 | 阿里妈妈-流量机制产品经理-杭州/北京 | [官网详情](https://talent.taotian.com/off-campus/position-detail?positionId=100020640004) |
| 2026-06-25 | 百度 | 健康档案产品经理（J101063） | [官网详情](https://talent.baidu.com/jobs/detail/SOCIAL/d49c9738-527a-4fe1-b6a1-546daef61416) |
| 2026-06-25 | 腾讯 | 元宝- AI策略产品经理 | [官网详情](http://careers.tencent.com/jobdesc.html?postId=1925398818564710400) |
| 2026-06-25 | 腾讯 | 元宝- AI策略产品经理（图片理解方向） | [官网详情](http://careers.tencent.com/jobdesc.html?postId=2021846191561666560) |
| 2026-06-25 | 腾讯 | 元宝-大模型策略产品经理（AIGC方向） | [官网详情](http://careers.tencent.com/jobdesc.html?postId=2021054129127981056) |
| 2026-06-25 | 腾讯 | 元宝-大模型策略产品经理（AIGC方向） | [官网详情](http://careers.tencent.com/jobdesc.html?postId=2021054127102132224) |
| 2026-06-25 | 腾讯 | 大数据产品经理（深圳/北京） | [官网详情](http://careers.tencent.com/jobdesc.html?postId=2013806539382611968) |
| 2026-06-25 | 腾讯 | 微信-产品经理-AI方向 | [官网详情](http://careers.tencent.com/jobdesc.html?postId=2037392058448248832) |
| 2026-06-25 | 腾讯 | 腾讯云文字识别高级产品经理 | [官网详情](http://careers.tencent.com/jobdesc.html?postId=2037377907856408576) |
| 2026-06-25 | 腾讯 | 腾讯会议-AI产品经理-企业应用方向 | [官网详情](http://careers.tencent.com/jobdesc.html?postId=2036620119203020800) |
| 2026-06-24 | 字节跳动 | AI Coding产品经理-TRAE | [官网详情](https://jobs.bytedance.com/experienced/position/7654847592895351093/detail) |
| 2026-06-24 | 字节跳动 | AI资深产品经理（商家经营方向）-TikTok Shop | [官网详情](https://jobs.bytedance.com/experienced/position/7654845775078115589/detail) |
| 2026-06-24 | 字节跳动 | AI资深产品经理（商家经营方向）-TikTok Shop | [官网详情](https://jobs.bytedance.com/experienced/position/7654845572276553989/detail) |
| 2026-06-24 | 快手 | AI Infra 成本运营产品经理-【可灵AI专项】 | [官网详情](https://zhaopin.kuaishou.cn/recruit/e/#/official/social/job-info/30981) |
| 2026-06-24 | 快手 | AIGC产品经理-【生活服务】 | [官网详情](https://zhaopin.kuaishou.cn/recruit/e/#/official/social/job-info/31053) |
| 2026-06-24 | 快手 | AIGC产品经理（号生态方向）-【生活服务】 | [官网详情](https://zhaopin.kuaishou.cn/recruit/e/#/official/social/job-info/28798) |
| 2026-06-24 | 快手 | AIGC产品经理（直播方向）-【生活服务】 | [官网详情](https://zhaopin.kuaishou.cn/recruit/e/#/official/social/job-info/31052) |
| 2026-06-24 | 快手 | AIGC产品经理（短视频方向）-【生活服务】 | [官网详情](https://zhaopin.kuaishou.cn/recruit/e/#/official/social/job-info/23556) |
| 2026-06-24 | 快手 | AI产品经理-【生活服务】 | [官网详情](https://zhaopin.kuaishou.cn/recruit/e/#/official/social/job-info/30717) |
| 2026-06-24 | 快手 | AI产品经理（AI外呼）—【生活服务】 | [官网详情](https://zhaopin.kuaishou.cn/recruit/e/#/official/social/job-info/30863) |
| 2026-06-24 | 快手 | AI产品经理（诊断任务）—【生活服务】 | [官网详情](https://zhaopin.kuaishou.cn/recruit/e/#/official/social/job-info/30864) |
| 2026-06-24 | 快手 | B端产品经理（AI方向）-【生活服务】 | [官网详情](https://zhaopin.kuaishou.cn/recruit/e/#/official/social/job-info/30895) |
| 2026-06-24 | 快手 | 商业私信产品经理（AI方向）-【生活服务】 | [官网详情](https://zhaopin.kuaishou.cn/recruit/e/#/official/social/job-info/30143) |
| 2026-06-24 | 快手 | 广告投放AI Agent产品经理-【生活服务】 | [官网详情](https://zhaopin.kuaishou.cn/recruit/e/#/official/social/job-info/30688) |
| 2026-06-24 | 快手 | 智能客服产品经理（AI方向）-【生活服务】 | [官网详情](https://zhaopin.kuaishou.cn/recruit/e/#/official/social/job-info/28344) |
| 2026-06-24 | 快手 | 高级数据产品经理-【可灵AI专项】 | [官网详情](https://zhaopin.kuaishou.cn/recruit/e/#/official/social/job-info/30556) |
| 2026-06-24 | 淘天集团 | 智能算法产品事业部-拍立淘产品经理-杭州 | [官网详情](https://talent.taotian.com/off-campus/position-detail?positionId=7000046108) |
| 2026-06-24 | 淘天集团 | 淘宝平台事业部-智能产品经理-商家服务 | [官网详情](https://talent.taotian.com/off-campus/position-detail?positionId=100010040045) |
| 2026-06-24 | 百度 | 生态产品经理（Skill 方向）（J101048） | [官网详情](https://talent.baidu.com/jobs/detail/SOCIAL/72b0e209-eb41-4408-85e4-f0c78104ed27) |
| 2026-06-24 | 腾讯 | 游戏美术 AIGC 产品经理 | [官网详情](http://careers.tencent.com/jobdesc.html?postId=2036274661179944960) |
| 2026-06-24 | 腾讯 | 证券-AI产品经理-金融AI应用体验方向 | [官网详情](http://careers.tencent.com/jobdesc.html?postId=2052527703940313088) |
| 2026-06-24 | 阿里云 | ATH事业群-产品经理-AI应用（杭州/北京） | [官网详情](https://careers.aliyun.com/off-campus/position-detail?lang=zh&positionId=100015523014) |
| 2026-06-24 | 阿里云 | ATH事业群-产品经理-AI解决方案（北京/杭州/深圳） | [官网详情](https://careers.aliyun.com/off-campus/position-detail?lang=zh&positionId=100015463013) |
| 2026-06-24 | 阿里云 | 阿里云智能-AI Native 应用产品经理 - AI Coding / Agent 方向-专有云（北京&杭州） | [官网详情](https://careers.aliyun.com/off-campus/position-detail?lang=zh&positionId=100015463012) |
| 2026-06-23 | 字节跳动 | AI投稿产品经理-红果短剧 | [官网详情](https://jobs.bytedance.com/experienced/position/7654560585702508805/detail) |
| 2026-06-23 | 字节跳动 | 商家经营治理策略产品经理（健康分方向）-TikTok Shop | [官网详情](https://jobs.bytedance.com/experienced/position/7654564211297782069/detail) |
| 2026-06-23 | 快手 | AI 标注平台产品经理（可灵AI专项） | [官网详情](https://zhaopin.kuaishou.cn/recruit/e/#/official/social/job-info/31280) |
| 2026-06-23 | 淘天集团 | M&T事业部-淘工厂-agent产品经理 | [官网详情](https://talent.taotian.com/off-campus/position-detail?positionId=100017780002) |
| 2026-06-23 | 淘天集团 | 天猫事业部-手机天猫搜索产品经理-杭州 | [官网详情](https://talent.taotian.com/off-campus/position-detail?positionId=100013760008) |
| 2026-06-23 | 腾讯 | 混元AIGC模型产品经理（多模态方向）（北京/上海） | [官网详情](http://careers.tencent.com/jobdesc.html?postId=1930452494366932992) |
| 2026-06-22 | 千问事业部 | 千问事业部-商业化产品经理（夸克/UC/书旗）-北京 | [官网详情](https://talent.quark.cn/off-campus/position-detail?positionId=100012140001) |
| 2026-06-22 | 字节跳动 | 网管平台产品经理（开发者方向）-基础设施 | [官网详情](https://jobs.bytedance.com/experienced/position/7654056429055887621/detail) |
| 2026-06-22 | 字节跳动 | 网管平台产品经理（开发者方向）-基础设施 | [官网详情](https://jobs.bytedance.com/experienced/position/7654056402500225333/detail) |
| 2026-06-22 | 字节跳动 | 网管平台运维产品经理-基础设施 | [官网详情](https://jobs.bytedance.com/experienced/position/7654055256297490741/detail) |
| 2026-06-22 | 字节跳动 | 网管平台运维产品经理-基础设施 | [官网详情](https://jobs.bytedance.com/experienced/position/7654055117743884549/detail) |
| 2026-06-22 | 小米 | 高级产品经理（行政方向） | [官网详情](https://xiaomi.jobs.f.mioffice.cn/index/position/7654059093745715498) |
| 2026-06-22 | 小米 | 高级产品经理（资产、工程管理方向） | [官网详情](https://xiaomi.jobs.f.mioffice.cn/index/position/7654058914586036523) |
| 2026-06-22 | 淘天集团 | 平台及用户产品事业部-产品经理-杭州 | [官网详情](https://talent.taotian.com/off-campus/position-detail?positionId=100019420007) |
| 2026-06-22 | 淘天集团 | 搜推智能产品事业部-搜索机制策略产品经理-杭州 | [官网详情](https://talent.taotian.com/off-campus/position-detail?positionId=100006520002) |
| 2026-06-22 | 百度 | IaaS异构计算产品经理（J100957） | [官网详情](https://talent.baidu.com/jobs/detail/SOCIAL/5a935bc7-9fd6-4aa9-bc37-799efd3d8079) |
| 2026-06-22 | 百度 | Iaas计算产品经理（J100956） | [官网详情](https://talent.baidu.com/jobs/detail/SOCIAL/db85e2df-a2ce-4b72-a39b-40a130778601) |
| 2026-06-22 | 百度 | 产品经理（J100962） | [官网详情](https://talent.baidu.com/jobs/detail/SOCIAL/7cc6a8b2-24af-4f83-8b58-72eca83dcfb9) |
| 2026-06-22 | 百度 | 大模型高级AI产品经理（J100663） | [官网详情](https://talent.baidu.com/jobs/detail/SOCIAL/2bdc6bd4-52bd-4b80-b0f6-7df7e5af78d5) |
| 2026-06-22 | 百度 | 政务交通行业-服务售前产品经理（J98509） | [官网详情](https://talent.baidu.com/jobs/detail/SOCIAL/102cc837-d083-4ba4-adfe-93f34f7968f0) |
| 2026-06-22 | 腾讯 | 元宝-整合营销产品经理 | [官网详情](http://careers.tencent.com/jobdesc.html?postId=2035265036687142912) |
| 2026-06-22 | 腾讯 | 元宝-整合营销产品经理 | [官网详情](http://careers.tencent.com/jobdesc.html?postId=2035265034589995008) |
| 2026-06-22 | 腾讯 | 腾讯云数据智能平台-资深产品经理-出海方向 | [官网详情](http://careers.tencent.com/jobdesc.html?postId=2047219127009050624) |
| 2026-06-22 | 腾讯 | 腾讯云数据智能平台-资深产品经理-数据治理方向 | [官网详情](http://careers.tencent.com/jobdesc.html?postId=2047218784430882816) |
| 2026-06-22 | 腾讯 | 腾讯游戏-产品经理（游戏发行AI方向）-新星引力计划 | [官网详情](http://careers.tencent.com/jobdesc.html?postId=1966332041217859584) |
| 2026-06-22 | 通义 | Token Foundry-语音AI产品经理-通义百聆 | [官网详情](https://careers-tongyi.alibaba.com/off-campus/position-detail?positionId=100011240002) |

## 抓取规则摘要

- 只保留岗位名包含 `产品经理` 的岗位
- 岗位名或 JD 需命中 `AI`、`人工智能`、`大模型`、`AIGC`、`Agent`、`智能体` 等关键词
- JD 合并岗位职责和岗位要求
- 官网未披露发布时间时，使用首次成功抓取时间作为录入时间
- 单个来源失败时先自主重试一次，仍失败则保留旧数据继续更新其它来源
- 日常刷新只更新数据和 HTML 内的 `jobData`，不改页面样式

## 本地查看

```bash
open ai_agent_pm_jobs.html
```

## 数据概览

- 生成时间：2026/06/28 11:59:56
- 总岗位数：946
- 近 7 个岗位日期明细数：77

## License

MIT
