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
| 快手 | 24 | +0 -0 | 2026/07/03 01:30:00 |
| 字节跳动 | 18 | +0 -0 | 2026/07/03 01:30:00 |
| 腾讯 | 71 | +0 -0 | 2026/07/03 01:30:00 |
| 小米 | 15 | +0 -0 | 2026/07/03 01:30:00 |
| 百度 | 140 | +0 -0 | 2026/07/03 01:30:00 |
| 理想 | 13 | +0 -0 | 2026/07/03 01:30:00 |
| 阿里云 | 12 | +0 -0 | 2026/07/03 01:30:00 |
| 淘天集团 | 35 | +0 -0 | 2026/07/03 01:30:00 |
| 蚂蚁集团 | 26 | +0 -0 | 2026/07/03 01:30:00 |
| 千问事业部 | 8 | +0 -0 | 2026/07/03 01:30:00 |
| 通义 | 3 | +0 -0 | 2026/07/03 01:30:00 |

## 近 7 日岗位变更

> 注：这里的日期是抓取变动日期，不是岗位发布时间。本次 2026-07-03 更新调整为两个单关键词 `AI`、`Agent` 的抓取口径，口径变化不计入岗位新增/下架；表格仅展示历史抓取中已确认的近 7 日变动。

| 日期 | 变动 | 公司 | 岗位名 | URL |
|---|---|---|---|---|
| 2026-07-02 | 下架 | 蚂蚁集团 | 财富海外业务-AI 产品经理-深圳 | https://talent.antgroup.com/off-campus-position/25102707311650 |
| 2026-07-02 | 下架 | 阿里云 | 阿里云智能-产品经理-供应链管理方向-杭州 | https://careers.aliyun.com/off-campus/position-detail?positionId=100015503003 |
| 2026-07-02 | 下架 | 百度 | Agent增长产品经理（J100513） | https://talent.baidu.com/jobs/detail/SOCIAL/4548d19c-0217-41de-afc1-432ea1dd7599 |
| 2026-07-02 | 下架 | 阿里云 | 诚云科技-资深产品经理-国际 | https://careers.aliyun.com/off-campus/position-detail?positionId=100014323002 |
| 2026-07-02 | 下架 | 百度 | 用户产品经理（国际化方向）（J97851） | https://talent.baidu.com/jobs/detail/SOCIAL/f6494e67-8aa7-44fc-94f4-07c3bf41e4de |
| 2026-07-02 | 新增 | 百度 | 用户增长产品经理（J97221） | https://talent.baidu.com/jobs/detail/SOCIAL/602f9a0f-c479-4183-ad68-c92e3e453073 |
| 2026-07-01 | 新增 | 百度 | 产品经理（基础设施供应链与资源运营）（J101289） | https://talent.baidu.com/jobs/detail/SOCIAL/505473ed-ffdd-476e-a809-64ff86c510f3 |
| 2026-07-01 | 新增 | 百度 | AI产品经理（企业效能方向）（J101301） | https://talent.baidu.com/jobs/detail/SOCIAL/ad3bf79c-557c-495a-a6ee-2d90f42014f8 |
| 2026-07-01 | 新增 | 淘天集团 | 营销平台及市场部-中后台AI产品经理-杭州 | https://talent.taotian.com/off-campus/position-detail?positionId=100013640012 |
| 2026-07-01 | 新增 | 快手 | AI 数据产品经理（运营方向）-【主站】 | https://zhaopin.kuaishou.cn/recruit/e/#/official/social/job-info/31401 |
| 2026-07-01 | 新增 | 字节跳动 | 账号产品经理-AI创新业务 | https://jobs.bytedance.com/experienced/position/7657457002419194165/detail |
| 2026-07-01 | 新增 | 字节跳动 | 网管平台运维产品经理-基础设施 | https://jobs.bytedance.com/experienced/position/7657441316938680581/detail |
| 2026-07-01 | 新增 | 字节跳动 | AI产品经理-国际化业务 | https://jobs.bytedance.com/experienced/position/7657406421592590645/detail |
| 2026-07-01 | 新增 | 千问事业部 | 千问事业部-千问策略产品经理-北京/杭州 | https://talent.quark.cn/off-campus/position-detail?positionId=100010300008 |
| 2026-07-01 | 新增 | 蚂蚁集团 | 蚂蚁数字科技-数字科技线-客服助理智能体产品经理 | https://talent.antgroup.com/off-campus-position/25121107972489 |
| 2026-07-01 | 新增 | 字节跳动 | 策略安全产品经理-TikTok安全产品 | https://jobs.bytedance.com/experienced/position/7657052865140164917/detail |
| 2026-07-01 | 新增 | 字节跳动 | AI策略产品经理（豆包办公）-飞书 | https://jobs.bytedance.com/experienced/position/7657104355999140101/detail |
| 2026-07-01 | 新增 | 字节跳动 | AI产品经理（ToB方向）-中国广告产品（北京/上海） | https://jobs.bytedance.com/experienced/position/7657172655967406341/detail |
| 2026-07-01 | 下架 | 腾讯 | 产品经理（人-Agent 协作编辑器方向） | https://careers.tencent.com/jobdesc.html?postId=2061646301208162304&language=zh-cn |
| 2026-07-01 | 新增 | 小米 | 硬件产品经理 | https://xiaomi.jobs.f.mioffice.cn/index/position/7656647737086232838/detail |
| 2026-07-01 | 新增 | 字节跳动 | AI产品经理（评测方向）-TikTok | https://jobs.bytedance.com/experienced/position/7656316786938136885/detail |
| 2026-07-01 | 新增 | 字节跳动 | 豆包AI大模型训练平台产品经理-火山方舟MaaS | https://jobs.bytedance.com/experienced/position/7655530707158534405/detail |
| 2026-07-01 | 新增 | 字节跳动 | 豆包AI大模型训练平台产品经理-火山方舟MaaS | https://jobs.bytedance.com/experienced/position/7655530367665064197/detail |
| 2026-07-01 | 新增 | 字节跳动 | OS软件产品经理-AI创新业务 | https://jobs.bytedance.com/experienced/position/7655638973901818117/detail |
| 2026-07-01 | 新增 | 字节跳动 | AI投稿产品经理（订阅方向）-抖音 | https://jobs.bytedance.com/experienced/position/7655582718345267509/detail |
| 2026-07-01 | 新增 | 字节跳动 | AI Agent产品经理-剪映CapCut | https://jobs.bytedance.com/experienced/position/7655610311870351621/detail |
| 2026-07-01 | 新增 | 字节跳动 | 可观测产品经理-算力基础设施 | https://jobs.bytedance.com/experienced/position/7655311908937681157/detail |
| 2026-07-01 | 新增 | 蚂蚁集团 | 财富海外业务-AI 产品经理-深圳 | https://talent.antgroup.com/off-campus-position/25102707311650 |
| 2026-07-01 | 新增 | 字节跳动 | 商家达人AI智能触达产品经理-TikTok Shop | https://jobs.bytedance.com/experienced/position/7654562997887453445/detail |
| 2026-07-01 | 新增 | 字节跳动 | 产品经理（People）-集团信息系统 | https://jobs.bytedance.com/experienced/position/7654470750275094837/detail |
| 2026-07-01 | 下架 | 字节跳动 | 商家经营治理策略产品经理（健康分方向）-TikTok Shop | https://jobs.bytedance.com/experienced/position/7654564211297782069/detail |
| 2026-07-01 | 下架 | 字节跳动 | 网管平台运维产品经理-基础设施 | https://jobs.bytedance.com/experienced/position/7654055256297490741/detail |
| 2026-07-01 | 新增 | 字节跳动 | Next-IT高级产品经理-IT | https://jobs.bytedance.com/experienced/position/7652664426181593397/detail |
| 2026-07-01 | 新增 | 字节跳动 | IT高级产品经理-Next | https://jobs.bytedance.com/experienced/position/7652661356095588613/detail |
| 2026-07-01 | 新增 | 字节跳动 | IT专家产品经理-Next | https://jobs.bytedance.com/experienced/position/7652665661643196677/detail |
| 2026-07-01 | 下架 | 字节跳动 | 营销产品经理（投放优化方向）-技术中台 | https://jobs.bytedance.com/experienced/position/7652661591710288133/detail |
| 2026-07-01 | 新增 | 字节跳动 | 商家服务平台产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7652342434347321605/detail |
| 2026-07-01 | 下架 | 字节跳动 | 创作者产品经理（达人孵化方向）-TikTok Shop | https://jobs.bytedance.com/experienced/position/7652259662441924869/detail |
| 2026-07-01 | 下架 | 字节跳动 | 创作者产品经理（达人孵化方向）-TikTok Shop | https://jobs.bytedance.com/experienced/position/7652258771961350405/detail |
| 2026-07-01 | 新增 | 字节跳动 | 商家达人AI智能触达产品经理-TikTok Shop | https://jobs.bytedance.com/experienced/position/7651841129605712133/detail |
| 2026-07-01 | 下架 | 字节跳动 | 商家经营治理策略产品经理（健康分方向）-TikTok Shop | https://jobs.bytedance.com/experienced/position/7651841128621132037/detail |
| 2026-07-01 | 新增 | 字节跳动 | 用户增长产品经理-AI数据与安全 | https://jobs.bytedance.com/experienced/position/7651504030311418117/detail |
| 2026-07-01 | 新增 | 字节跳动 | 抖音钱包产品经理（账单方向）-财经 | https://jobs.bytedance.com/experienced/position/7651508063779064117/detail |
| 2026-07-01 | 新增 | 字节跳动 | 商家治理教育产品经理（AI智能化建设）-TikTok Shop | https://jobs.bytedance.com/experienced/position/7650386102826780933/detail |
| 2026-07-01 | 下架 | 腾讯 | ima-AI Agent 策略产品经理(深圳/北京) | https://careers.tencent.com/jobdesc.html?postId=1998225333643530240&language=zh-cn |
| 2026-07-01 | 新增 | 字节跳动 | DMP数据产品经理（人群画像方向）-抖音生活服务 | https://jobs.bytedance.com/experienced/position/7648917634620672309/detail |
| 2026-07-01 | 下架 | 字节跳动 | 风控AI产品经理-链接安全 | https://jobs.bytedance.com/experienced/position/7647006248021264693/detail |
| 2026-07-01 | 下架 | 字节跳动 | 风控AI产品经理-链接安全 | https://jobs.bytedance.com/experienced/position/7646331547399358725/detail |
| 2026-07-01 | 下架 | 腾讯 | 腾讯会议-AI产品经理-AI应用体验方向 | https://careers.tencent.com/jobdesc.html?postId=2045074510201389056&language=zh-cn |
| 2026-07-01 | 下架 | 字节跳动 | 抖音电商站外CPS业务产品经理（电商联盟）-穿山甲（北京/上海） | https://jobs.bytedance.com/experienced/position/7644530984033913141/detail |
| 2026-07-01 | 下架 | 字节跳动 | AI硬件产品经理（交易履约方向）-抖音生活服务 | https://jobs.bytedance.com/experienced/position/7644524053193836853/detail |
| 2026-07-01 | 新增 | 字节跳动 | AI产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7644122084184475957/detail |
| 2026-07-01 | 新增 | 字节跳动 | 搜索产品经理-TikTok旗下图文独立端 | https://jobs.bytedance.com/experienced/position/7642194999950346549/detail |
| 2026-07-01 | 新增 | 字节跳动 | 店铺产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7642260688628123909/detail |
| 2026-07-01 | 下架 | 字节跳动 | 直播间用户产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7641517040751659269/detail |
| 2026-07-01 | 新增 | 字节跳动 | 策略产品经理（内容治理）-TikTok安全产品 | https://jobs.bytedance.com/experienced/position/7640028583914342709/detail |
| 2026-07-01 | 下架 | 字节跳动 | 虚拟人产品经理（游戏引擎&虚拟形象方向）-抖音 | https://jobs.bytedance.com/experienced/position/7640005631806490885/detail |
| 2026-07-01 | 新增 | 蚂蚁集团 | 蚂蚁数字科技-数字科技线-具身智能数据产品经理 | https://talent.antgroup.com/off-campus-position/26031909227216 |
| 2026-07-01 | 新增 | 字节跳动 | 红果短剧变现产品经理（AI方向）-中国广告产品（北京/上海） | https://jobs.bytedance.com/experienced/position/7638474435041970437/detail |
| 2026-07-01 | 下架 | 字节跳动 | 社交产品经理-TikTok | https://jobs.bytedance.com/experienced/position/7638517648654387509/detail |
| 2026-07-01 | 下架 | 字节跳动 | 用户产品经理（电商图文方向）-TikTok Shop | https://jobs.bytedance.com/experienced/position/7638482545135175989/detail |
| 2026-07-01 | 新增 | 字节跳动 | 店铺产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7637413019261897013/detail |
| 2026-07-01 | 新增 | 字节跳动 | 高级数据产品经理（内容理解方案）-国际化数据生产平台 | https://jobs.bytedance.com/experienced/position/7633268081309370677/detail |
| 2026-07-01 | 新增 | 字节跳动 | 商品库平台产品经理-中国广告产品 | https://jobs.bytedance.com/experienced/position/7633422277548509445/detail |
| 2026-07-01 | 新增 | 字节跳动 | AI产品经理-抖音生活服务 | https://jobs.bytedance.com/experienced/position/7633287502036551941/detail |
| 2026-07-01 | 下架 | 字节跳动 | 营销C端产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7633273928761510197/detail |
| 2026-07-01 | 新增 | 字节跳动 | 数据产品经理（内容理解方案）-国际化数据生产平台 | https://jobs.bytedance.com/experienced/position/7632176919911549237/detail |
| 2026-07-01 | 新增 | 字节跳动 | AI产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7631862247841597701/detail |
| 2026-07-01 | 下架 | 字节跳动 | AI音乐工具产品经理-抖音 | https://jobs.bytedance.com/experienced/position/7631928601329731845/detail |
| 2026-07-01 | 新增 | 字节跳动 | 选品产品经理（拉美市场）-TikTok Shop | https://jobs.bytedance.com/experienced/position/7631488780272273669/detail |
| 2026-07-01 | 新增 | 字节跳动 | 平台产品经理（AI方向）-TikTok直播 | https://jobs.bytedance.com/experienced/position/7631251704113580341/detail |
| 2026-07-01 | 新增 | 字节跳动 | AI产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7631129293118638341/detail |
| 2026-07-01 | 新增 | 字节跳动 | AI产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7631127110056675589/detail |
| 2026-07-01 | 新增 | 字节跳动 | AI产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7631124636152154373/detail |
| 2026-07-01 | 下架 | 字节跳动 | 软件产品经理-豆包手机助手 | https://jobs.bytedance.com/experienced/position/7631098115112159493/detail |
| 2026-07-01 | 新增 | 字节跳动 | 商家服务平台产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7629623290512181557/detail |
| 2026-07-01 | 新增 | 字节跳动 | 反欺诈策略产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7628876717684361525/detail |
| 2026-07-01 | 新增 | 字节跳动 | OS基础体验产品经理-PICO | https://jobs.bytedance.com/experienced/position/7628824127614535941/detail |
| 2026-07-01 | 新增 | 字节跳动 | 平台产品经理-TikTok直播 | https://jobs.bytedance.com/experienced/position/7628447375792933125/detail |
| 2026-07-01 | 新增 | 字节跳动 | 价格力产品经理-TikTok Shop | https://jobs.bytedance.com/experienced/position/7628501722295781637/detail |
| 2026-07-01 | 下架 | 字节跳动 | 抖音高级平台产品经理-抖音 | https://jobs.bytedance.com/experienced/position/7628457788331559221/detail |
| 2026-07-01 | 下架 | 字节跳动 | 交易搜索营销产品经理-抖音搜索 | https://jobs.bytedance.com/experienced/position/7628512643581659445/detail |
| 2026-07-01 | 新增 | 字节跳动 | 联盟产品经理（拉美市场）-TikTok Shop | https://jobs.bytedance.com/experienced/position/7628072455828867333/detail |
| 2026-07-01 | 新增 | 字节跳动 | 用户增长高级产品经理-剪映CapCut（北京/深圳） | https://jobs.bytedance.com/experienced/position/7628067517120284933/detail |
| 2026-07-01 | 下架 | 字节跳动 | 商家增长AI产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7628084252005140741/detail |
| 2026-07-01 | 新增 | 字节跳动 | AI产品经理-抖音生活服务 | https://jobs.bytedance.com/experienced/position/7627117718337308981/detail |
| 2026-07-01 | 下架 | 字节跳动 | AI产品经理（搜索方向）-飞书项目 | https://jobs.bytedance.com/experienced/position/7627125252828481845/detail |
| 2026-07-01 | 新增 | 字节跳动 | AI产品经理（生成式广告）-中国广告产品（北京/上海） | https://jobs.bytedance.com/experienced/position/7626572184251287813/detail |
| 2026-07-01 | 新增 | 字节跳动 | 商家IM产品经理-TikTok Shop | https://jobs.bytedance.com/experienced/position/7626287567147288837/detail |
| 2026-07-01 | 下架 | 字节跳动 | 撮合平台产品经理（商家经营方向）-抖音电商（北京） | https://jobs.bytedance.com/experienced/position/7621477643783178549/detail |
| 2026-07-01 | 新增 | 字节跳动 | AI剧行业产品经理（出海全自动转产分发方向）-中国广告产品（北京） | https://jobs.bytedance.com/experienced/position/7621206460016363781/detail |
| 2026-07-01 | 下架 | 字节跳动 | AI短剧产品经理-TikTok | https://jobs.bytedance.com/experienced/position/7621082075197901109/detail |
| 2026-07-01 | 下架 | 字节跳动 | 隐私合规产品经理-AI创新业务 | https://jobs.bytedance.com/experienced/position/7618160617182578997/detail |
| 2026-07-01 | 新增 | 字节跳动 | 商家触达产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7617809994370402565/detail |
| 2026-07-01 | 下架 | 字节跳动 | AI产品经理（国际电商方向）-剪映CapCut | https://jobs.bytedance.com/experienced/position/7617839326168844549/detail |
| 2026-07-01 | 下架 | 字节跳动 | 硬件产品经理-AI创新业务 | https://jobs.bytedance.com/experienced/position/7616334070452734261/detail |
| 2026-07-01 | 下架 | 字节跳动 | AI产品经理-ArkClaw | https://jobs.bytedance.com/experienced/position/7615914486223603973/detail |
| 2026-07-01 | 新增 | 字节跳动 | 风控策略产品经理-火山方舟 | https://jobs.bytedance.com/experienced/position/7614032464814410037/detail |
| 2026-07-01 | 新增 | 字节跳动 | 国际化商业AI策略产品经理-AIGC广告创意 | https://jobs.bytedance.com/experienced/position/7613224542970104117/detail |
| 2026-07-01 | 新增 | 字节跳动 | 商品供给产品经理（AI智能化建设）-TikTok Shop | https://jobs.bytedance.com/experienced/position/7611441225568209205/detail |
| 2026-07-01 | 下架 | 字节跳动 | 增长策略产品经理（独立端方向）-抖音 | https://jobs.bytedance.com/experienced/position/7611068912851863861/detail |
| 2026-07-01 | 下架 | 字节跳动 | 数据安全产品经理-AI创新业务 | https://jobs.bytedance.com/experienced/position/7610639456902908165/detail |
| 2026-07-01 | 下架 | 字节跳动 | AI应用产品经理-抖音生活服务 | https://jobs.bytedance.com/experienced/position/7605531121644652805/detail |
| 2026-07-01 | 下架 | 字节跳动 | 语言学习类AI产品经理-Gauth | https://jobs.bytedance.com/experienced/position/7605138439006685445/detail |
| 2026-07-01 | 新增 | 字节跳动 | 豆包大模型语音交互产品经理-Data 语音 | https://jobs.bytedance.com/experienced/position/7602941919246862597/detail |
| 2026-07-01 | 下架 | 字节跳动 | 内容产品经理-TikTok生活服务 | https://jobs.bytedance.com/experienced/position/7602929425096886533/detail |
| 2026-07-01 | 新增 | 字节跳动 | 商品AI产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7602570046460807477/detail |
| 2026-07-01 | 下架 | 百度 | 用户增长产品经理（J97221） | https://talent.baidu.com/jobs/detail/SOCIAL/602f9a0f-c479-4183-ad68-c92e3e453073 |
| 2026-07-01 | 新增 | 字节跳动 | 用户产品经理-AI创新产品 | https://jobs.bytedance.com/experienced/position/7601072811857217797/detail |
| 2026-07-01 | 新增 | 字节跳动 | 供给增长产品经理（内容方向）-抖音电商 | https://jobs.bytedance.com/experienced/position/7601034900205357365/detail |
| 2026-07-01 | 新增 | 字节跳动 | AI创作产品经理-火山引擎 | https://jobs.bytedance.com/experienced/position/7600664438863399173/detail |
| 2026-07-01 | 下架 | 字节跳动 | 投稿功能产品经理-TikTok旗下图文独立端 | https://jobs.bytedance.com/experienced/position/7600628951331834117/detail |
| 2026-07-01 | 下架 | 字节跳动 | 投稿功能产品经理-TikTok旗下图文独立端 | https://jobs.bytedance.com/experienced/position/7600626006446377269/detail |
| 2026-07-01 | 下架 | 字节跳动 | 商家产品经理（招商入驻）-TikTok生活服务 | https://jobs.bytedance.com/experienced/position/7600604192977389829/detail |
| 2026-07-01 | 下架 | 字节跳动 | 运营项目平台产品经理（AI应用方向）-抖音 | https://jobs.bytedance.com/experienced/position/7600376071956318517/detail |
| 2026-07-01 | 下架 | 字节跳动 | 人才系统AI产品经理-管理研究院 | https://jobs.bytedance.com/experienced/position/7597663577026447669/detail |
| 2026-07-01 | 新增 | 字节跳动 | 商品信息产品经理（图谱方向）-抖音生活服务 | https://jobs.bytedance.com/experienced/position/7595494559024384309/detail |
| 2026-07-01 | 新增 | 字节跳动 | 账号产品经理-AI创新业务 | https://jobs.bytedance.com/experienced/position/7594318925060868405/detail |
| 2026-07-01 | 新增 | 字节跳动 | AI产品经理（通用Agent方向）-Aime | https://jobs.bytedance.com/experienced/position/7594409781193804085/detail |
| 2026-07-01 | 新增 | 字节跳动 | 产品经理（平台应用）-TikTok | https://jobs.bytedance.com/experienced/position/7587379992544217397/detail |
| 2026-07-01 | 新增 | 字节跳动 | 软件产品经理-豆包手机助手 | https://jobs.bytedance.com/experienced/position/7585095373407979781/detail |
| 2026-07-01 | 新增 | 字节跳动 | AI产品经理（一方应用方向）-AI创新业务 | https://jobs.bytedance.com/experienced/position/7584328223313299765/detail |
| 2026-07-01 | 新增 | 字节跳动 | 安全运营产品经理-安全与风控 | https://jobs.bytedance.com/experienced/position/7581803131965770037/detail |
| 2026-07-01 | 新增 | 字节跳动 | 推荐策略产品经理-抖音 | https://jobs.bytedance.com/experienced/position/7581392237222037813/detail |
| 2026-07-01 | 下架 | 字节跳动 | AI策略产品经理（大模型应用方向）-抖音UGC | https://jobs.bytedance.com/experienced/position/7576862126063634693/detail |
| 2026-07-01 | 新增 | 字节跳动 | 贷后平台产品经理-国际支付 | https://jobs.bytedance.com/experienced/position/7574362303903516981/detail |
| 2026-07-01 | 新增 | 字节跳动 | 商家AI产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7570987149207832885/detail |
| 2026-07-01 | 新增 | 字节跳动 | 商家AI产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7570986292770310405/detail |
| 2026-07-01 | 新增 | 字节跳动 | AI应用产品经理（广告后链路风险治理方向）-国际化广告审核风控业务 | https://jobs.bytedance.com/experienced/position/7568341860274997509/detail |
| 2026-07-01 | 下架 | 字节跳动 | AI商业化产品经理-剪映CapCut | https://jobs.bytedance.com/experienced/position/7566558149944232197/detail |
| 2026-07-01 | 新增 | 字节跳动 | 消费品行业产品经理-巨量星图（北京/上海） | https://jobs.bytedance.com/experienced/position/7565789079940253957/detail |
| 2026-07-01 | 下架 | 字节跳动 | AIGC模型产品经理（生成式广告）-中国广告产品 | https://jobs.bytedance.com/experienced/position/7560987484038039869/detail |
| 2026-07-01 | 下架 | 字节跳动 | 数据基建产品经理-集团信息系统 | https://jobs.bytedance.com/experienced/position/7559852733760243975/detail |
| 2026-07-01 | 新增 | 字节跳动 | 语音大模型产品经理-Data语音 | https://jobs.bytedance.com/experienced/position/7559515401470822674/detail |
| 2026-07-01 | 新增 | 字节跳动 | 平台产品经理（机器审核）-TikTok安全产品 | https://jobs.bytedance.com/experienced/position/7550201606065113362/detail |
| 2026-07-01 | 新增 | 字节跳动 | 营收分发策略产品经理（主播方向）-抖音直播 | https://jobs.bytedance.com/experienced/position/7548846967108028680/detail |
| 2026-07-01 | 下架 | 字节跳动 | 数据基建产品经理-集团信息系统 | https://jobs.bytedance.com/experienced/position/7548744081137535250/detail |
| 2026-07-01 | 新增 | 字节跳动 | 直播安全产品经理-国际化 | https://jobs.bytedance.com/experienced/position/7546521350170118408/detail |
| 2026-07-01 | 下架 | 字节跳动 | 互动策略产品经理-红果短剧 | https://jobs.bytedance.com/experienced/position/7539816205835946248/detail |
| 2026-07-01 | 下架 | 字节跳动 | 创作者工具产品经理-抖音生活服务 | https://jobs.bytedance.com/experienced/position/7537166145301694727/detail |
| 2026-07-01 | 新增 | 字节跳动 | AI产品经理（用户方向）-TikTok直播 | https://jobs.bytedance.com/experienced/position/7535784517489264904/detail |
| 2026-07-01 | 新增 | 字节跳动 | LLM策略产品经理-AI创新产品 | https://jobs.bytedance.com/experienced/position/7532485605025286407/detail |
| 2026-07-01 | 新增 | 字节跳动 | 内容生态平台产品经理-抖音电商 | https://jobs.bytedance.com/experienced/position/7530624370278369543/detail |
| 2026-07-01 | 下架 | 字节跳动 | 高级AI产品经理-飞书 | https://jobs.bytedance.com/experienced/position/7527871379245795592/detail |
| 2026-07-01 | 新增 | 字节跳动 | 商品平台产品经理-抖音生活服务 | https://jobs.bytedance.com/experienced/position/7527702519792748818/detail |
| 2026-07-01 | 新增 | 字节跳动 | 治理策略产品经理-抖音生活服务 | https://jobs.bytedance.com/experienced/position/7522373588897646866/detail |
| 2026-07-01 | 新增 | 字节跳动 | 资深产品经理-AI漏洞修复 | https://jobs.bytedance.com/experienced/position/7514260989933750546/detail |
| 2026-07-01 | 新增 | 字节跳动 | 智能审核策略产品经理-商业安全（北京/上海） | https://jobs.bytedance.com/experienced/position/7509747812536748295/detail |
| 2026-07-01 | 新增 | 字节跳动 | LLM大模型评估产品经理-豆包 | https://jobs.bytedance.com/experienced/position/7497188463336065288/detail |
| 2026-07-01 | 下架 | 字节跳动 | 商业化产品经理（广告平台&策略）-国际化 | https://jobs.bytedance.com/experienced/position/7494499736948656392/detail |
| 2026-07-01 | 新增 | 字节跳动 | 高级AI产品经理（妙记/音视频方向）-飞书 | https://jobs.bytedance.com/experienced/position/7493572774875678984/detail |
| 2026-07-01 | 下架 | 字节跳动 | 内容社区产品经理-抖音搜索 | https://jobs.bytedance.com/experienced/position/7493828480070633736/detail |
| 2026-07-01 | 下架 | 小米 | 产品经理 | https://xiaomi.jobs.f.mioffice.cn/index/position/7493440141990920300/detail |
| 2026-07-01 | 新增 | 字节跳动 | 欧洲商家治理策略产品经理（AI智能化方向）-TikTok Shop | https://jobs.bytedance.com/experienced/position/7490819392198019346/detail |
| 2026-07-01 | 新增 | 字节跳动 | 商家域解决方案产品经理-TikTok Shop | https://jobs.bytedance.com/experienced/position/7490416895222417672/detail |
| 2026-07-01 | 新增 | 字节跳动 | 混合云高级产品经理-火山引擎 | https://jobs.bytedance.com/experienced/position/7488548949344438536/detail |
| 2026-07-01 | 下架 | 字节跳动 | 小游戏产品经理-抖音 | https://jobs.bytedance.com/experienced/position/7488557298413144327/detail |
| 2026-07-01 | 新增 | 字节跳动 | 语音交互大模型产品经理-Data语音 | https://jobs.bytedance.com/experienced/position/7485326381946620178/detail |
| 2026-07-01 | 下架 | 字节跳动 | 用户产品经理（职人成长方向）-抖音生活服务 | https://jobs.bytedance.com/experienced/position/7481302578857396498/detail |
| 2026-07-01 | 新增 | 字节跳动 | 产品经理（中台产品方向）-中国用户增长 | https://jobs.bytedance.com/experienced/position/7480093288046889224/detail |
| 2026-07-01 | 下架 | 字节跳动 | AI策略产品经理-国际化业务 | https://jobs.bytedance.com/experienced/position/7474950346042034439/detail |
| 2026-07-01 | 下架 | 字节跳动 | 研发平台AI产品经理-Dev Infra | https://jobs.bytedance.com/experienced/position/7470432989257959698/detail |
| 2026-07-01 | 新增 | 字节跳动 | AI产品经理-AI创新业务 | https://jobs.bytedance.com/experienced/position/7470046983894812935/detail |
| 2026-07-01 | 下架 | 字节跳动 | AI产品经理-AI创新业务 | https://jobs.bytedance.com/experienced/position/7470062770294655239/detail |
| 2026-07-01 | 新增 | 字节跳动 | 资深搜索策略产品经理-TikTok | https://jobs.bytedance.com/experienced/position/7468635772272331026/detail |
| 2026-07-01 | 新增 | 字节跳动 | 高级AI产品经理-飞书IM | https://jobs.bytedance.com/experienced/position/7450501406907500807/detail |
| 2026-07-01 | 新增 | 字节跳动 | 视觉模型策略与评测产品经理-Seed | https://jobs.bytedance.com/experienced/position/7449654995466946823/detail |
| 2026-07-01 | 新增 | 字节跳动 | 数据产品经理（CDP方向）-火山引擎 | https://jobs.bytedance.com/experienced/position/7441841110853011719/detail |
| 2026-07-01 | 新增 | 字节跳动 | AI创作产品经理-TikTok | https://jobs.bytedance.com/experienced/position/7431463752770177319/detail |
| 2026-07-01 | 新增 | 字节跳动 | AI搜索产品经理-火山方舟MaaS | https://jobs.bytedance.com/experienced/position/7429315484883470655/detail |
| 2026-07-01 | 新增 | 字节跳动 | 产品经理（AI大模型效果方向）-抖音 | https://jobs.bytedance.com/experienced/position/7424062645269449010/detail |
| 2026-07-01 | 下架 | 字节跳动 | AI策略产品经理-Gauth | https://jobs.bytedance.com/experienced/position/7400736893523249445/detail |
| 2026-07-01 | 新增 | 字节跳动 | 营收礼物玩法产品经理（AI应用方向）-抖音直播 | https://jobs.bytedance.com/experienced/position/7376171219186829605/detail |
| 2026-07-01 | 下架 | 字节跳动 | 商家端产品经理（体验优化）-抖音生活服务 | https://jobs.bytedance.com/experienced/position/7374385842502879539/detail |
| 2026-07-01 | 下架 | 字节跳动 | 商家端产品经理（体验优化）-抖音生活服务 | https://jobs.bytedance.com/experienced/position/7374385623858268454/detail |
| 2026-07-01 | 下架 | 字节跳动 | 生态平台产品经理-火山引擎（北京/上海/深圳） | https://jobs.bytedance.com/experienced/position/7373565710050511114/detail |
| 2026-07-01 | 新增 | 字节跳动 | 座舱大模型产品经理-火山引擎 | https://jobs.bytedance.com/experienced/position/7370931403174988058/detail |
| 2026-07-01 | 下架 | 字节跳动 | 数据产品经理（商家方向）-抖音生活服务 | https://jobs.bytedance.com/experienced/position/7367339421547563314/detail |
| 2026-07-01 | 下架 | 字节跳动 | 商家端产品经理-抖音生活服务 | https://jobs.bytedance.com/experienced/position/7351304460650891558/detail |
| 2026-07-01 | 新增 | 字节跳动 | 国际化产品经理-商业内容审核流程 | https://jobs.bytedance.com/experienced/position/7346161091770976549/detail |
| 2026-07-01 | 新增 | 字节跳动 | 研发平台AI产品经理-Dev Infra | https://jobs.bytedance.com/experienced/position/7321252497531521330/detail |
| 2026-07-01 | 下架 | 字节跳动 | 风控策略产品经理-AI创新业务 | https://jobs.bytedance.com/experienced/position/7319709842402658598/detail |
| 2026-07-01 | 新增 | 字节跳动 | 高级AI工具产品经理-剪映CapCut | https://jobs.bytedance.com/experienced/position/7298568941759416603/detail |
| 2026-07-01 | 新增 | 字节跳动 | 高级数据产品经理-抖音 | https://jobs.bytedance.com/experienced/position/7280525588996081975/detail |
| 2026-07-01 | 新增 | 字节跳动 | 直播产品经理（付费体系方向）-抖音直播 | https://jobs.bytedance.com/experienced/position/7244746617290426685/detail |
| 2026-07-01 | 新增 | 字节跳动 | 今日头条策略产品经理（安全方向）-今日头条 | https://jobs.bytedance.com/experienced/position/7194275187881314616/detail |
| 2026-07-01 | 新增 | 字节跳动 | 向量数据库高级产品经理-Data AML | https://jobs.bytedance.com/experienced/position/7155360670261922078/detail |
| 2026-07-01 | 新增 | 字节跳动 | 数据产品经理-中国商业产品与技术 | https://jobs.bytedance.com/experienced/position/7091613732409395487/detail |
| 2026-07-01 | 新增 | 字节跳动 | 智能体身份安全产品经理-云安全 | https://jobs.bytedance.com/experienced/position/6974604323511847181/detail |
| 2026-07-01 | 下架 | 字节跳动 | 资深C端产品经理-Gauth | https://jobs.bytedance.com/experienced/position/6864836370575640846/detail |
