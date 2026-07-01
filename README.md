# 国内互联网大厂 AI 岗位监控 Skill

为了方便及时跟进和了解市场上 AI 或 Agent 相关的产品经理岗位，我编写了这样一个 skill：

1. 能够从各家招聘网站中，根据相关关键词找到对应的岗位 JD
2. 能够以网页看板的形式，将所有岗位统一展示出来

目前该 skill 已支持 11 个公司。

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
| 快手 | 44 | +1 -0 | 2026/07/01 23:13:00 |
| 字节跳动 | 669 | +110 -60 | 2026/07/01 23:13:00 |
| 腾讯 | 72 | +0 -3 | 2026/07/01 23:13:00 |
| 小米 | 22 | +1 -1 | 2026/07/01 23:13:00 |
| 百度 | 151 | +2 -1 | 2026/07/01 23:13:00 |
| 理想 | 14 | +0 -0 | 2026/07/01 23:13:00 |
| 阿里云 | 14 | +0 -0 | 2026/07/01 23:13:00 |
| 淘天集团 | 59 | +1 -0 | 2026/07/01 23:13:00 |
| 蚂蚁集团 | 27 | +3 -0 | 2026/07/01 23:13:00 |
| 千问事业部 | 21 | +1 -0 | 2026/07/01 23:13:00 |
| 通义 | 3 | +0 -0 | 2026/07/01 23:13:00 |

## 近 7 日岗位变更

> 注：这里的日期是抓取变动日期，不是岗位发布时间。当前仓库从 2026-07-01 这轮刷新开始记录新的明细格式，所以目前只有 2026-07-01；后续持续更新后会累积最近 7 天的变更。

| 日期 | 公司 | 岗位名 | URL |
|---|---|---|---|
| 2026-07-01 | 腾讯 | 产品经理（人-Agent 协作编辑器方向） | https://careers.tencent.com/jobdesc.html?postId=2061646301208162304&language=zh-cn |
| 2026-07-01 | 腾讯 | ima-AI Agent 策略产品经理(深圳/北京) | https://careers.tencent.com/jobdesc.html?postId=1998225333643530240&language=zh-cn |
| 2026-07-01 | 腾讯 | 腾讯会议-AI产品经理-AI应用体验方向 | https://careers.tencent.com/jobdesc.html?postId=2045074510201389056&language=zh-cn |
| 2026-07-01 | 字节跳动 | 账号产品经理-AI创新业务 | https://jobs.bytedance.com/experienced/position/7657457002419194165/detail |
| 2026-07-01 | 字节跳动 | 网管平台运维产品经理-基础设施 | https://jobs.bytedance.com/experienced/position/7657441316938680581/detail |
| 2026-07-01 | 淘天集团 | 营销平台及市场部-中后台AI产品经理-杭州 | https://talent.taotian.com/off-campus/position-detail?positionId=100013640012 |
| 2026-07-01 | 字节跳动 | AI产品经理-国际化业务 | https://jobs.bytedance.com/experienced/position/7657406421592590645/detail |
| 2026-07-01 | 千问事业部 | 千问事业部-千问策略产品经理-北京/杭州 | https://talent.quark.cn/off-campus/position-detail?positionId=100010300008 |
| 2026-07-01 | 快手 | AI 数据产品经理（运营方向）-【主站】 | https://zhaopin.kuaishou.cn/recruit/e/#/official/social/job-info/31401 |
| 2026-07-01 | 百度 | 产品经理（基础设施供应链与资源运营）（J101289） | https://talent.baidu.com/jobs/detail/SOCIAL/505473ed-ffdd-476e-a809-64ff86c510f3 |
| 2026-07-01 | 百度 | AI产品经理（企业效能方向）（J101301） | https://talent.baidu.com/jobs/detail/SOCIAL/ad3bf79c-557c-495a-a6ee-2d90f42014f8 |
| 2026-07-01 | 字节跳动 | AI产品经理（ToB方向）-中国广告产品（北京/上海） | https://jobs.bytedance.com/experienced/position/7657172655967406341/detail |
| 2026-07-01 | 字节跳动 | AI策略产品经理（豆包办公）-飞书 | https://jobs.bytedance.com/experienced/position/7657104355999140101/detail |
| 2026-07-01 | 蚂蚁集团 | 蚂蚁数字科技-数字科技线-客服助理智能体产品经理 | https://talent.antgroup.com/off-campus-position/25121107972489 |
| 2026-07-01 | 字节跳动 | 策略安全产品经理-TikTok安全产品 | https://jobs.bytedance.com/experienced/position/7657052865140164917/detail |
| 2026-07-01 | 小米 | 硬件产品经理 | https://xiaomi.jobs.f.mioffice.cn/index/position/7656647737086232838/detail |
| 2026-07-01 | 字节跳动 | AI产品经理（评测方向）-TikTok | https://jobs.bytedance.com/experienced/position/7656316786938136885/detail |
| 2026-07-01 | 字节跳动 | OS软件产品经理-AI创新业务 | https://jobs.bytedance.com/experienced/position/7655638973901818117/detail |
| 2026-07-01 | 字节跳动 | AI Agent产品经理-剪映CapCut | https://jobs.bytedance.com/experienced/position/7655610311870351621/detail |
| 2026-07-01 | 字节跳动 | AI投稿产品经理（订阅方向）-抖音 | https://jobs.bytedance.com/experienced/position/7655582718345267509/detail |
| 2026-07-01 | 字节跳动 | 豆包AI大模型训练平台产品经理-火山方舟MaaS | https://jobs.bytedance.com/experienced/position/7655530707158534405/detail |
| 2026-07-01 | 字节跳动 | 豆包AI大模型训练平台产品经理-火山方舟MaaS | https://jobs.bytedance.com/experienced/position/7655530367665064197/detail |
| 2026-07-01 | 字节跳动 | 可观测产品经理-算力基础设施 | https://jobs.bytedance.com/experienced/position/7655311908937681157/detail |
| 2026-07-01 | 字节跳动 | 商家经营治理策略产品经理（健康分方向）-TikTok Shop | https://jobs.bytedance.com/experienced/position/7654564211297782069/detail |
| 2026-07-01 | 字节跳动 | 商家达人AI智能触达产品经理-TikTok Shop | https://jobs.bytedance.com/experienced/position/7654562997887453445/detail |
| 2026-07-01 | 蚂蚁集团 | 财富海外业务-AI 产品经理-深圳 | https://talent.antgroup.com/off-campus-position/25102707311650 |
| 2026-07-01 | 字节跳动 | 产品经理（People）-集团信息系统 | https://jobs.bytedance.com/experienced/position/7654470750275094837/detail |
| 2026-07-01 | 字节跳动 | 网管平台运维产品经理-基础设施 | https://jobs.bytedance.com/experienced/position/7654055256297490741/detail |
| 2026-07-01 | 字节跳动 | IT专家产品经理-Next | https://jobs.bytedance.com/experienced/position/7652665661643196677/detail |
| 2026-07-01 | 字节跳动 | Next-IT高级产品经理-IT | https://jobs.bytedance.com/experienced/position/7652664426181593397/detail |
| 2026-07-01 | 字节跳动 | 营销产品经理（投放优化方向）-技术中台 | https://jobs.bytedance.com/experienced/position/7652661591710288133/detail |
| 2026-07-01 | 字节跳动 | IT高级产品经理-Next | https://jobs.bytedance.com/experienced/position/7652661356095588613/detail |
| 2026-07-01 | 字节跳动 | 商家服务平台产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7652342434347321605/detail |
| 2026-07-01 | 字节跳动 | 创作者产品经理（达人孵化方向）-TikTok Shop | https://jobs.bytedance.com/experienced/position/7652259662441924869/detail |
| 2026-07-01 | 字节跳动 | 创作者产品经理（达人孵化方向）-TikTok Shop | https://jobs.bytedance.com/experienced/position/7652258771961350405/detail |
| 2026-07-01 | 字节跳动 | 商家经营治理策略产品经理（健康分方向）-TikTok Shop | https://jobs.bytedance.com/experienced/position/7651841128621132037/detail |
| 2026-07-01 | 字节跳动 | 商家达人AI智能触达产品经理-TikTok Shop | https://jobs.bytedance.com/experienced/position/7651841129605712133/detail |
| 2026-07-01 | 字节跳动 | 抖音钱包产品经理（账单方向）-财经 | https://jobs.bytedance.com/experienced/position/7651508063779064117/detail |
| 2026-07-01 | 字节跳动 | 用户增长产品经理-AI数据与安全 | https://jobs.bytedance.com/experienced/position/7651504030311418117/detail |
| 2026-07-01 | 字节跳动 | 商家治理教育产品经理（AI智能化建设）-TikTok Shop | https://jobs.bytedance.com/experienced/position/7650386102826780933/detail |
| 2026-07-01 | 字节跳动 | DMP数据产品经理（人群画像方向）-抖音生活服务 | https://jobs.bytedance.com/experienced/position/7648917634620672309/detail |
| 2026-07-01 | 字节跳动 | 风控AI产品经理-链接安全 | https://jobs.bytedance.com/experienced/position/7647006248021264693/detail |
| 2026-07-01 | 字节跳动 | 风控AI产品经理-链接安全 | https://jobs.bytedance.com/experienced/position/7646331547399358725/detail |
| 2026-07-01 | 字节跳动 | 抖音电商站外CPS业务产品经理（电商联盟）-穿山甲（北京/上海） | https://jobs.bytedance.com/experienced/position/7644530984033913141/detail |
| 2026-07-01 | 字节跳动 | AI硬件产品经理（交易履约方向）-抖音生活服务 | https://jobs.bytedance.com/experienced/position/7644524053193836853/detail |
| 2026-07-01 | 字节跳动 | AI产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7644122084184475957/detail |
| 2026-07-01 | 字节跳动 | 店铺产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7642260688628123909/detail |
| 2026-07-01 | 字节跳动 | 搜索产品经理-TikTok旗下图文独立端 | https://jobs.bytedance.com/experienced/position/7642194999950346549/detail |
| 2026-07-01 | 字节跳动 | 直播间用户产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7641517040751659269/detail |
| 2026-07-01 | 字节跳动 | 策略产品经理（内容治理）-TikTok安全产品 | https://jobs.bytedance.com/experienced/position/7640028583914342709/detail |
| 2026-07-01 | 字节跳动 | 虚拟人产品经理（游戏引擎&虚拟形象方向）-抖音 | https://jobs.bytedance.com/experienced/position/7640005631806490885/detail |
| 2026-07-01 | 蚂蚁集团 | 蚂蚁数字科技-数字科技线-具身智能数据产品经理 | https://talent.antgroup.com/off-campus-position/26031909227216 |
| 2026-07-01 | 字节跳动 | 社交产品经理-TikTok | https://jobs.bytedance.com/experienced/position/7638517648654387509/detail |
| 2026-07-01 | 字节跳动 | 用户产品经理（电商图文方向）-TikTok Shop | https://jobs.bytedance.com/experienced/position/7638482545135175989/detail |
| 2026-07-01 | 字节跳动 | 红果短剧变现产品经理（AI方向）-中国广告产品（北京/上海） | https://jobs.bytedance.com/experienced/position/7638474435041970437/detail |
| 2026-07-01 | 字节跳动 | 店铺产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7637413019261897013/detail |
| 2026-07-01 | 字节跳动 | 商品库平台产品经理-中国广告产品 | https://jobs.bytedance.com/experienced/position/7633422277548509445/detail |
| 2026-07-01 | 字节跳动 | AI产品经理-抖音生活服务 | https://jobs.bytedance.com/experienced/position/7633287502036551941/detail |
| 2026-07-01 | 字节跳动 | 营销C端产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7633273928761510197/detail |
| 2026-07-01 | 字节跳动 | 高级数据产品经理（内容理解方案）-国际化数据生产平台 | https://jobs.bytedance.com/experienced/position/7633268081309370677/detail |
| 2026-07-01 | 字节跳动 | 数据产品经理（内容理解方案）-国际化数据生产平台 | https://jobs.bytedance.com/experienced/position/7632176919911549237/detail |
| 2026-07-01 | 字节跳动 | AI音乐工具产品经理-抖音 | https://jobs.bytedance.com/experienced/position/7631928601329731845/detail |
| 2026-07-01 | 字节跳动 | AI产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7631862247841597701/detail |
| 2026-07-01 | 字节跳动 | 选品产品经理（拉美市场）-TikTok Shop | https://jobs.bytedance.com/experienced/position/7631488780272273669/detail |
| 2026-07-01 | 字节跳动 | 平台产品经理（AI方向）-TikTok直播 | https://jobs.bytedance.com/experienced/position/7631251704113580341/detail |
| 2026-07-01 | 字节跳动 | AI产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7631129293118638341/detail |
| 2026-07-01 | 字节跳动 | AI产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7631127110056675589/detail |
| 2026-07-01 | 字节跳动 | AI产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7631124636152154373/detail |
| 2026-07-01 | 字节跳动 | 软件产品经理-豆包手机助手 | https://jobs.bytedance.com/experienced/position/7631098115112159493/detail |
| 2026-07-01 | 字节跳动 | 商家服务平台产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7629623290512181557/detail |
| 2026-07-01 | 字节跳动 | 反欺诈策略产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7628876717684361525/detail |
| 2026-07-01 | 字节跳动 | OS基础体验产品经理-PICO | https://jobs.bytedance.com/experienced/position/7628824127614535941/detail |
| 2026-07-01 | 字节跳动 | 交易搜索营销产品经理-抖音搜索 | https://jobs.bytedance.com/experienced/position/7628512643581659445/detail |
| 2026-07-01 | 字节跳动 | 价格力产品经理-TikTok Shop | https://jobs.bytedance.com/experienced/position/7628501722295781637/detail |
| 2026-07-01 | 字节跳动 | 抖音高级平台产品经理-抖音 | https://jobs.bytedance.com/experienced/position/7628457788331559221/detail |
| 2026-07-01 | 字节跳动 | 平台产品经理-TikTok直播 | https://jobs.bytedance.com/experienced/position/7628447375792933125/detail |
| 2026-07-01 | 字节跳动 | 商家增长AI产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7628084252005140741/detail |
| 2026-07-01 | 字节跳动 | 联盟产品经理（拉美市场）-TikTok Shop | https://jobs.bytedance.com/experienced/position/7628072455828867333/detail |
| 2026-07-01 | 字节跳动 | 用户增长高级产品经理-剪映CapCut（北京/深圳） | https://jobs.bytedance.com/experienced/position/7628067517120284933/detail |
| 2026-07-01 | 字节跳动 | AI产品经理（搜索方向）-飞书项目 | https://jobs.bytedance.com/experienced/position/7627125252828481845/detail |
| 2026-07-01 | 字节跳动 | AI产品经理-抖音生活服务 | https://jobs.bytedance.com/experienced/position/7627117718337308981/detail |
| 2026-07-01 | 字节跳动 | AI产品经理（生成式广告）-中国广告产品（北京/上海） | https://jobs.bytedance.com/experienced/position/7626572184251287813/detail |
| 2026-07-01 | 字节跳动 | 商家IM产品经理-TikTok Shop | https://jobs.bytedance.com/experienced/position/7626287567147288837/detail |
| 2026-07-01 | 字节跳动 | 撮合平台产品经理（商家经营方向）-抖音电商（北京） | https://jobs.bytedance.com/experienced/position/7621477643783178549/detail |
| 2026-07-01 | 字节跳动 | AI剧行业产品经理（出海全自动转产分发方向）-中国广告产品（北京） | https://jobs.bytedance.com/experienced/position/7621206460016363781/detail |
| 2026-07-01 | 字节跳动 | AI短剧产品经理-TikTok | https://jobs.bytedance.com/experienced/position/7621082075197901109/detail |
| 2026-07-01 | 字节跳动 | 隐私合规产品经理-AI创新业务 | https://jobs.bytedance.com/experienced/position/7618160617182578997/detail |
| 2026-07-01 | 字节跳动 | AI产品经理（国际电商方向）-剪映CapCut | https://jobs.bytedance.com/experienced/position/7617839326168844549/detail |
| 2026-07-01 | 字节跳动 | 商家触达产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7617809994370402565/detail |
| 2026-07-01 | 字节跳动 | 硬件产品经理-AI创新业务 | https://jobs.bytedance.com/experienced/position/7616334070452734261/detail |
| 2026-07-01 | 字节跳动 | AI产品经理-ArkClaw | https://jobs.bytedance.com/experienced/position/7615914486223603973/detail |
| 2026-07-01 | 字节跳动 | 风控策略产品经理-火山方舟 | https://jobs.bytedance.com/experienced/position/7614032464814410037/detail |
| 2026-07-01 | 字节跳动 | 国际化商业AI策略产品经理-AIGC广告创意 | https://jobs.bytedance.com/experienced/position/7613224542970104117/detail |
| 2026-07-01 | 字节跳动 | 商品供给产品经理（AI智能化建设）-TikTok Shop | https://jobs.bytedance.com/experienced/position/7611441225568209205/detail |
| 2026-07-01 | 字节跳动 | 增长策略产品经理（独立端方向）-抖音 | https://jobs.bytedance.com/experienced/position/7611068912851863861/detail |
| 2026-07-01 | 字节跳动 | 数据安全产品经理-AI创新业务 | https://jobs.bytedance.com/experienced/position/7610639456902908165/detail |
| 2026-07-01 | 字节跳动 | AI应用产品经理-抖音生活服务 | https://jobs.bytedance.com/experienced/position/7605531121644652805/detail |
| 2026-07-01 | 字节跳动 | 语言学习类AI产品经理-Gauth | https://jobs.bytedance.com/experienced/position/7605138439006685445/detail |
| 2026-07-01 | 字节跳动 | 豆包大模型语音交互产品经理-Data 语音 | https://jobs.bytedance.com/experienced/position/7602941919246862597/detail |
| 2026-07-01 | 字节跳动 | 内容产品经理-TikTok生活服务 | https://jobs.bytedance.com/experienced/position/7602929425096886533/detail |
