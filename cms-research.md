# CMS 调研：官网、博客、案例与 FAQ

适用于自己开发前端的 SaaS、AI 产品和开发者工具官网，用 CMS 管理首页内容、博客、案例、FAQ 和多语言文案。

官方资料核对日期：2026-10-14。整理日期：2026-10-15。价格与功能是核对时的资料，选型前按官方页面复核。

**当前候选：Sanity、Payload、Strapi、Decap CMS。尚未选定或接入具体 CMS。** 本页的选型建议来自调研，未视为维护者的使用评价。

## 一、候选对比

| CMS | 适合的场景 | 免费方案与成本 | 主要取舍 | 官方来源 |
| --- | --- | --- | --- | --- |
| **Sanity** | 希望托管省心，运营成员经常维护结构化内容 | Free 含 20 个席位、10,000 文档、2 个公开 dataset；Growth $15/席位/月 | 免费角色仅 Administrator 和 Viewer；需要细分编辑权限或私有 dataset 时考虑 Growth。内容基础设施由服务商托管 | [套餐与权限](https://www.sanity.io/pricing) |
| **Payload** | 开发者主导，希望内容模型、代码与数据由自己掌控 | MIT 开源，软件免费；部署、数据库和文件存储成本自行承担 | 基于 TypeScript / Next.js，配置生成后台、API 与内容模型；适合愿意维护应用后端的团队 | [官方仓库与许可证](https://github.com/payloadcms/payload)、[产品架构](https://payloadcms.com/docs/getting-started/what-is-payload) |
| **Strapi** | 需要独立 CMS 后台，通过 API 接自己的前端 | Community 免费、MIT 开源；自托管有基础设施成本。付费 CMS 功能与 Cloud 托管分别计费 | 有内容管理后台、REST / GraphQL API、内容类型和组件；可与 Vue、React 等前端配合。付费功能按当前套餐核对 | [CMS 套餐](https://strapi.io/pricing-cms)、[Cloud 套餐](https://strapi.io/pricing-cloud) |
| **Decap CMS** | 静态官网、博客或文档，内容跟随 Git 管理 | MIT 开源免费；Git、认证和网站构建部署按所选平台承担成本 | 提供编辑界面，将内容保存到仓库；适合更新频率不高、已有静态构建流程的站点 | [官方说明与许可证](https://decapcms.org/docs/intro/) |

## 二、按维护方式选择

| 实际需求 | 优先考虑 | 理由 |
| --- | --- | --- |
| 运营成员经常改内容，自己希望减少 CMS 服务维护 | Sanity | 托管内容基础设施，按字段管理内容；先核对编辑权限与席位成本 |
| Next.js / TypeScript 项目，需要深度定制内容模型 | Payload | 内容配置与应用代码放在同一开发流程中 |
| 前端独立，需要一个专门的 CMS 后台 | Strapi | 用内容后台与 API 连接前端，CMS 可独立部署 |
| 主要由开发者或 agent 维护，内容更新不多 | Markdown；需要编辑后台时加 Decap | 复用 Git、版本记录和现有发布流程 |

Payload 的 CMS 应用使用 Next.js；其他前端可以通过它的 REST / GraphQL API 获取内容。这两种部署方式在选型时分开评估。[Payload 架构说明](https://payloadcms.com/docs/getting-started/what-is-payload)

## 三、成本与稳定性

本次调研核对公开产品资料，未做跨服务长期可用性测量。以下比较针对保障与维护责任，具体可用性按所选部署和合同评估。

| 方案 | 成本与保障 | 稳定性判断 |
| --- | --- | --- |
| Sanity Free / Growth | 有免费用量或按席位收费；公开套餐表均未包含 uptime SLA | Growth 的主要升级价值是权限、协作和容量，不能仅凭付费推导故障率更低 |
| Sanity Enterprise | 列出专属支持与 uptime SLA，具体合同报价 | 需要明确可用性与恢复支持时核对 SLA 范围、排除项和支持响应条件 |
| Payload / Strapi 自托管 | 软件可免费使用，运行资源和维护由自己承担 | 根据应用部署、数据库、存储、监控和恢复流程评估；软件许可证价格无法代表部署的稳定性 |
| Strapi Cloud | 托管费与 CMS 功能费分别看；核对时 Starter 会闲置休眠，Pro / Business 常驻；Business 列 99.9% uptime SLA | 有实时内容 API 依赖时关注休眠行为；付费档位的保障仅适用于对应 Cloud 套餐 |
| Decap + 静态网站 | CMS 软件免费，依赖 Git 和构建发布平台 | 构建发布后，访客阅读静态页面通常不依赖 CMS 编辑后台在线；编辑与发布仍依赖 Git、认证和部署流程 |

套餐事实来源：[Sanity 定价](https://www.sanity.io/pricing)、[Strapi Cloud 对比](https://strapi.io/pricing-cloud)、[Decap 的 Git 工作流](https://decapcms.org/docs/intro/)。自托管与静态发布的维护责任说明属于基于上述架构的选型判断。

## 四、在 Section 设计流程中如何使用

先用 Relume 确定页面结构，再参考视觉站点与配色工具完成组件设计。CMS 管理这些组件所需的真实内容。

| CMS 管理的内容 | 页面组件负责的表现 |
| --- | --- |
| 标题、正文、按钮文案与目标链接 | 排版、间距、按钮样式与交互 |
| 图片、视频与说明 | 图文关系、裁切规则与展示方式 |
| 功能、使用场景、FAQ 与客户案例 | 卡片、列表、问答展开与区块布局 |
| Section 类型、启用状态和排列顺序 | 已实现的组件与布局规则 |
| 多语言内容 | 对应语言下的内容呈现 |

建议先围绕实际需要维护的内容建模，给每种 section 明确字段。编辑成员通过已有组件调整内容和顺序，页面保持统一的视觉表达。

内容读取方式也影响稳定性：低频内容可在构建时生成页面；需要实时更新的内容再使用 API，并按项目需要配置缓存。

## 五、选型前要明确的决定

- 谁维护内容：开发者、agent、运营成员，还是多人协作。
- 更新频率：低频发布，还是需要立即生效。
- 内容范围：博客和 FAQ，还是整页的 section 内容与顺序。
- 部署方式：服务商托管，还是自己维护 CMS 应用。
- 权限需求：编辑、查看、审批与私有内容的实际范围。
- 成本口径：席位、API、存储、带宽、数据库、托管和支持分别计算。

相关资料：[首页 Section 拆分](homepage-sections.md)、[结构、视觉与配色参考](website-design-references.md)、[业务服务候选清单](homepage-services.md#cms)。
