# 首页业务服务候选清单：免费额度与稳定性

配合 [产品首页常见 Section 拆分](homepage-sections.md) 的「可选业务服务与引入条件」使用。这里整理预约、留资、媒体托管等运行时服务；Layout、视觉效果与配色参考见 [网站设计参考](website-design-references.md)。按实际需要选择业务服务，优先复用产品已有能力。

**核对日期：2026-10-14。** 以下免费项为持续免费计划或按月免费额度，付费计划的短期试用不计入。价格仅供预算参考，美元标价及年付条件按对应官方页面说明；选型时重新核对额度与套餐。

本页的选型建议来自资料整理，个人偏好仍以 [参考站点文档的「我的建议」](website-design-references.md) 为准。

## 一、按服务类别查找

| 服务类别 | 常见关联 Section | 候选项 |
| --- | --- | --- |
| [表单与线索](#forms) | Hero、Final CTA、Footer | Tally、Formspree |
| [预约演示](#booking) | Hero、How It Works、Final CTA | Cal.com、Calendly |
| [邮件与订阅](#email) | CTA、Footer；按钮后的注册或通知流程 | Resend、Brevo |
| [评价收集](#testimonials) | Social Proof、Customer Stories | Senja |
| [交互 Demo](#demos) | Product Demo、功能展开、How It Works | Storylane、Arcade |
| [图片与视频素材](#media) | Hero、Demo、功能、案例 | Cloudinary、Cloudflare R2 |
| [内容 CMS](#cms) | 功能、场景、案例、FAQ | Sanity；低频更新可用本地 Markdown |
| [账号与登录](#auth) | Header、注册 CTA 后的产品流程 | Clerk、Supabase Auth |
| [在线客服](#chat) | FAQ、联系入口、全站浮层 | tawk.to |
| [流量与转化分析](#analytics) | 全站；跟踪 section 与 CTA 的效果 | Cloudflare Web Analytics、Umami |
| [状态页与监控](#status) | Footer 的服务状态入口 | Instatus、UptimeRobot |
| [支付入口](#payments) | Pricing、购买 CTA 后的结账流程 | Stripe；属于收费补充项 |
| [防机器人](#anti-bot) | 自建表单、注册或订阅流程 | Cloudflare Turnstile |

## 二、服务候选与免费限制

<a id="forms"></a>
### 1. 表单与线索

| 服务 | 持续免费额度与关键限制 | 付费价值 / 稳定性依据 | 适合的用法 |
| --- | --- | --- | --- |
| **Tally** | 无限表单与提交，受合理使用规则约束；免费上传单文件上限 10 MB。[定价](https://tally.so/pricing)、[合理使用](https://tally.so/help/fair-use-policy) | Pro 主要增加去品牌、自定义域名和协作。核对页未列可量化可用性 SLA，付费价值主要在功能与运营控制。[Business 说明](https://tally.so/help/tally-business) | 快速做联系表单、候补名单或需求收集；可嵌入，也可用独立链接。 |
| **Formspree** | 50 次提交/月，历史保留 30 天。超额仍保存提交，但暂停通知与插件处理。[套餐](https://formspree.io/plans)、[超限行为](https://help.formspree.io/articles/form-and-project-settings/over-limit-submissions) | 付费增加额度与保留期；Business 有优先支持，Custom 列出 SLA，具体范围需确认合同。 | 保留自己页面的表单 UI，只使用托管提交后端；发布活动前核对突发流量额度。 |

表单提交记录是主要依据，通知邮件作为提醒。外部嵌入不可用时保留独立链接或联系邮箱。

<a id="booking"></a>
### 2. 预约演示

| 服务 | 持续免费额度与关键限制 | 付费价值 / 稳定性依据 | 适合的用法 |
| --- | --- | --- | --- |
| **Cal.com** | Individual 单用户免费；事件类型、连接日历与会议数量不限。团队套餐试用另算。[套餐](https://cal.com/pricing) | Teams 增加轮询分配与路由；Enterprise 列出 SLA、可用性保障和专属支持，具体数值需确认合同。 | 单人销售、创始人演示预约；多人分配时再考虑团队套餐。 |
| **Calendly** | Free 提供一个事件类型、一个连接日历、不限会议，可嵌入网站。[套餐说明](https://calendly.com/help/choose-the-right-calendly-plan-for-your-team) | Standard 增加日历、事件类型、提醒和 24/7 聊天支持；Enterprise 有专属支持。核对页未确认通用的可用性 SLA 数值。 | 一个标准演示预约入口；复杂团队路由再比较付费选项。 |

预约还依赖日历同步与会议平台。保留普通预约链接和联系邮箱，便于嵌入组件异常时继续联系。

<a id="email"></a>
### 3. 邮件与订阅

| 服务 | 持续免费额度与关键限制 | 付费价值 / 稳定性依据 | 适合的用法 |
| --- | --- | --- | --- |
| **Resend** | 事务邮件 3,000 封/月，同时最多 100 封/日。营销邮件是独立套餐。[定价](https://resend.com/pricing) | Pro $20/月起，增加月量并取消日限；Enterprise 列出 99.99% uptime SLA 和保证响应时间。服务可用性与最终进收件箱的成功率分别评估。 | 有后端/API 的确认、通知、登录邮件；Newsletter 使用对应营销产品与额度。 |
| **Brevo** | 300 封/日，未用额度不结转。事务邮件撞日限后的重试队列最多 1,000 封。[免费限制](https://help.brevo.com/hc/en-us/articles/208580669-FAQs-What-are-the-limits-of-the-Free-plan) | Starter $9/月起取消日限，仍有月量和联系人限制；Standard 有优先邮件支持，Professional / Enterprise 有电话支持，Enterprise 列 SLA。[套餐](https://help.brevo.com/hc/en-us/articles/208589409-About-Brevo-s-pricing-plans)、[支持](https://help.brevo.com/hc/en-us/articles/360020434360-Contact-the-support-team) | 带订阅管理和编辑器的 Newsletter；群发人数与当天其他邮件共同计算。 |

按日的免费额度无法集中成一次月度群发。选型时分别估算平时用量和上线当天的峰值；关键提交先保存业务记录，再发送确认邮件。

<a id="testimonials"></a>
### 4. 评价收集

| 服务 | 持续免费额度与关键限制 | 付费价值 / 稳定性依据 | 适合的用法 |
| --- | --- | --- | --- |
| **Senja** | 免费共 15 条文字/视频评价，累计计数，删除不释放；一个表单、一个项目，带品牌标识。[套餐区别](https://support.senja.io/what-are-the-differences-between-the-free-and-paid-plans-sdcfs)、[超限行为](https://support.senja.io/what-happens-after-i-collect-more-than-15-testimonials-sar4p) | Starter $29/月、Pro $59/月，主要增加评价数量、去品牌及集成能力；核对页未列可用性 SLA。 | 少量初期评价的收集与展示。关键获授权评价也可直接静态展示。 |

<a id="demos"></a>
### 5. 交互 Demo

| 服务 | 持续免费额度与关键限制 | 付费价值 / 稳定性依据 | 适合的用法 |
| --- | --- | --- | --- |
| **Storylane** | 1 个席位、1 个已发布 Demo，观看次数不限，免费支持截图/视频式交互演示。[套餐](https://www.storylane.io/plans) | Starter 标价 $50/月起，增加已发布 Demo 数量、品牌与集成能力；核对页未列可用性 SLA，升级主要解决内容规模与功能需求。 | 一个核心产品流程的引导演示。 |
| **Arcade** | 1 个已发布 Demo、1 个已发布视频、不限观看，200 AI credits/月。[定价](https://www.arcade.software/pricing) | Growth 月付标价 $50/席位/月，增加发布与导出能力；Enterprise 有专属 CSM/Slack。核对页未列可用性 SLA。 | 产品演示与素材制作；单独核对 AI 生成额度。 |

Demo 嵌入失败时可显示静态截图与文字说明。免费发布数量、视频导出、去品牌和团队席位是不同限制。

<a id="media"></a>
### 6. 图片与视频素材

| 服务 | 持续免费额度与关键限制 | 付费价值 / 稳定性依据 | 适合的用法 |
| --- | --- | --- | --- |
| **Cloudinary Image and Video APIs** | 每月 25 credits，3 个用户/1 个账号；credits 按存储、转换与交付用量计算。此免费计划与 Assets DAM 的短期试用分别看待。[定价](https://cloudinary.com/pricing) | Plus 月付 $99/月，增加额度和加速支持；Enterprise 列企业 SLA、支持和 multi-CDN 能力，需核对合同。 | 需要图片转换、视频转码与 CDN 交付的页面。 |
| **Cloudflare R2** | Standard 每月 10 GB-month 存储、100 万 Class A 和 1,000 万 Class B 请求；R2 直接出口流量免费。[价格与免费额度](https://developers.cloudflare.com/r2/pricing/) | 超额按量计费，例如存储 $0.015/GB-month；该价格页未列免费/付费的可用性差异，不能套用其他 Cloudflare 产品的 SLA。 | 托管已处理好的图片与视频文件；若需要转码或自适应视频，可另选媒体平台。 |

少量核心图像可随网站发布。媒体量增长或需要转换能力时再选托管服务；R2 接入其他按量计费产品时，该产品可能另收费。

<a id="cms"></a>
### 7. 内容 CMS

| 服务 | 持续免费额度与关键限制 | 付费价值 / 稳定性依据 | 适合的用法 |
| --- | --- | --- | --- |
| **Sanity** | Free 提供 20 个席位、2 个公开 dataset、10,000 文档；每月 100 万 CDN API 和 25 万 API 请求。[定价](https://www.sanity.io/pricing) | Growth $15/席位/月，增加编辑权限与超额付费能力；Enterprise 才列专属支持及 uptime SLA。普通 Growth 的主要价值是内容协作与容量。 | 非开发成员频繁维护案例、FAQ、场景和内容；公开 dataset 只放可公开的内容。 |

低频更新可用本地 Markdown 或现有配置，无新增服务费。若用外部 CMS，可在构建时生成内容或使用缓存，降低 CMS 短暂异常对首页阅读的影响。

<a id="auth"></a>
### 8. 账号与登录

| 服务 | 持续免费额度与关键限制 | 付费价值 / 稳定性依据 | 适合的用法 |
| --- | --- | --- | --- |
| **Clerk** | Hobby 每应用 50,000 MRU，即月留存用户；用户注册 24 小时后返回才计入此口径。包含现成登录 UI。[定价与计数说明](https://clerk.com/pricing) | Pro 标价 $20/月按年付，增加会话控制、日志等能力；Enterprise 列 99.99% uptime SLA 和支持响应 SLA。 | 新产品需要独立托管认证；额度与 MAU 不可直接等同。 |
| **Supabase Auth** | Free 50,000 MAU，最多 2 个活跃项目；项目闲置一周会暂停。[定价](https://supabase.com/pricing) | Pro $25/月起，官方明确不会因闲置暂停，并有邮件支持；Team 有支持 SLA，Enterprise 列 uptime SLA。[生产可用性说明](https://supabase.com/docs/guides/deployment/going-into-prod) | 已使用或准备使用 Supabase 的产品；认证邮件需另核对 SMTP 和发送额度。 |

已有账号系统时直接链接并复用。首页重做本身不构成迁移认证系统的理由；登录是核心产品依赖，选择时同时看限制、支持和恢复能力。

<a id="chat"></a>
### 9. 在线客服

| 服务 | 持续免费额度与关键限制 | 付费价值 / 稳定性依据 | 适合的用法 |
| --- | --- | --- | --- |
| **tawk.to** | 人工 live chat 免费，席位、聊天量和站点不限，并提供 24/7/365 聊天/邮件支持。AI Assist 单独计费与限额。[官方 FAQ](https://www.tawk.to/faqs/) | Whitelabel $29/月/站点，AI Assist $29/月起；去品牌主要购买品牌控制，核对页未列可用性 SLA。[附加服务](https://www.tawk.to/add-ons/) | 有人接待的在线咨询；无人值守时显示回复时间并提供邮箱。 |

<a id="analytics"></a>
### 10. 流量与转化分析

| 服务 | 持续免费额度与关键限制 | 付费价值 / 稳定性依据 | 适合的用法 |
| --- | --- | --- | --- |
| **Cloudflare Web Analytics** | 官方提供免费的网站分析。[产品页](https://www.cloudflare.com/web-analytics/) | 核对页没有为此工具列独立付费 SLA；购买其他 Cloudflare 套餐不自动改变此产品的保障。 | 基础流量和页面表现观察；需要详细产品事件时另选事件分析工具。 |
| **Umami Cloud** | Hobby 每月 100,000 events、1 个站点、6 个月保留、社区支持。[定价](https://umami.is/pricing) | Pro $20/月，增加用量、保留和邮件支持；Enterprise 列 uptime SLA 与企业支持，需确认具体数值。 | CTA 点击和自定义事件分析；自托管软件免费，但基础设施与维护由自己承担。 |

分析加载失败时，页面和主要行动仍应可用。计数口径按工具定义核对，例如 Umami 将页面访问与事件属性也纳入用量。

<a id="status"></a>
### 11. 状态页与监控

| 服务 | 持续免费额度与关键限制 | 付费价值 / 稳定性依据 | 适合的用法 |
| --- | --- | --- | --- |
| **Instatus** | Starter 15 个 monitor、2 分钟检测、公开状态页、200 个订阅者、无自定义域名。[定价](https://instatus.com/pricing) | Pro/Business 增加检测频率、通知和域名；Enterprise 列 99.99% uptime SLA 与优先支持，价格需核对当前报价。 | Footer 放服务状态链接；付费可提升故障发现和通知能力。 |
| **UptimeRobot** | Free 50 个 monitor、5 分钟检测、基础状态页。价格页定位爱好/非营利项目；服务条款允许包括商业用途，但仍受合理使用规则约束。[定价](https://uptimerobot.com/pricing/)、[条款](https://uptimerobot.com/terms/) | 付费增加检测频率、通知和功能；核对页未确认统一可用性 SLA。检测更快主要缩短发现故障的时间。 | 初期 HTTP/API 监控与状态展示；使用前核对免费状态页和通知的实际限制。 |

监控工具能发现问题和展示状态；自身产品的恢复能力仍由产品架构与运维承担。

<a id="payments"></a>
### 12. 支付入口：收费补充项

| 服务 | 免费范围 / 收费方式 | 稳定性与付费说明 | 适合的用法 |
| --- | --- | --- | --- |
| **Stripe** | Standard 无设置费、月费，真实支付按交易计费，属于收费服务。费率按地区、支付方式和具体产品核对。[定价](https://stripe.com/pricing) | 核对的 Standard 价格页未列统一可用性 SLA。交易手续费是支付处理费用，不能据此推导某个套餐更稳定；选定产品后核对支持及合同。 | 购买 CTA 后的托管结账或订阅；仅显示价格时无需引入。 |

只有明确需要收款时才选支付服务。网站的付款完成状态要以支付确认结果为依据；价格展示继续使用产品的实际价格来源。

<a id="anti-bot"></a>
### 13. 防机器人

| 服务 | 持续免费额度与关键限制 | 付费价值 / 稳定性依据 | 适合的用法 |
| --- | --- | --- | --- |
| **Cloudflare Turnstile** | Free 最多 20 个 widget，每个 10 个 hostname，验证请求不限，7 天分析回看。[套餐](https://developers.cloudflare.com/turnstile/plans/) | Enterprise 增加域名、回看时间和控制能力；核对页未列此产品的可用性 SLA。 | 自建表单或注册流程遇到机器提交时使用；现有托管表单已经覆盖的能力可以复用。 |

## 三、如何从稳定性判断付费价值

本次核对的是公开套餐与官方文档，未做跨服务长期可用性测量。以下是比较依据，选型时结合服务状态历史与目标用户所在地区的实际访问情况。

| 比较项 | 要看什么 | 如何理解付费价值 |
| --- | --- | --- |
| 可用性 SLA | 覆盖哪个产品、套餐、故障类型、排除项和赔付条件 | Enterprise 或 Custom 的承诺按合同确认；SLA 是承诺与补偿机制 |
| 支持 SLA | 首次响应时间、支持渠道、工作时间和升级路径 | 更快找到负责团队，有助于缩短故障处理时间；响应时间与恢复时间分别看 |
| 超额处理 | 日限、月限、超额计费、限流、暂停、通知失效 | 增加额度可减少因流量增长造成的运营中断 |
| 服务历史 | 官方状态页中的事故频率、持续时间和复盘 | 当前正常状态仅说明当前情况；长期表现需要历史证据 |
| 恢复与迁移 | 数据导出、保留期、静态替代、普通链接和重试能力 | 保障业务继续运行需要同时考虑自己的页面与数据流程 |

**建议的付费顺序**：先处理已经影响注册、留资、预约或邮件发送的额度与暂停限制，再为需要明确恢复支持的核心依赖购买对应支持或 SLA。评价展示、分析、去品牌等需求按业务价值决定。

## 四、起步组合示例

以下是按需选取的组合，实际账单取决于各自额度、流量和附加服务。

- **简单营销首页**：静态内容 + Tally 留资 + Cal.com 预约；需要流量观察时加 Cloudflare Web Analytics。
- **开发者产品首页**：现有登录系统 + 自有价格配置 + Formspree 表单或现有 API + Resend 通知；有复杂演示需要时试用 Storylane 或 Arcade 的免费计划。
- **内容持续运营**：Sanity 管内容 + Brevo 管订阅 + Instatus 提供状态入口；需要评价收集时加 Senja。

每个服务在引入前记录：用途、免费限制、升级条件、支持/SLA依据和失败时的替代路径。全部候选项按实际需求逐项选择。
