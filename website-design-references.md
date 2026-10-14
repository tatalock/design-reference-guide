# 网站设计参考：结构、视觉与配色

用于设计新官网、营销首页和 Landing Page，也供 agent 按需查阅。

核心分工：**Relume 做骨架，其他网站做皮肉，配色工具把视觉方向落实为可复用的颜色系统。**

工具用途与个人偏好分栏记录。“暂未评价”表示尚未给出个人反馈。

站点与功能核对日期：2026-10-14。功能、访问限制和收费方案可能调整，以各站点当前说明为准。

## 一、页面结构与视觉参考

| 站点 | 类型 | 主要用途 | 适合参考的内容 | 我的建议 |
| --- | --- | --- | --- | --- |
| [Relume Library](https://www.relume.ai/page-templates) | 页面模板与组件库 | 设定页面骨架 | section 选择与顺序、信息层级、图文关系、列数、CTA 位置；组件类别包括 Hero、Features、Navbar、Footer、CTA | 适合设定页面的 Layout 结构，作为骨架参考。 |
| [Landbook](https://land-book.com/) | 网站与 section 灵感库 | 确定视觉方向与局部排版 | 字体、配色、间距、画面、质感；可从 Sections 入口找区块，并按行业和风格筛选 | 这类站点适合做站点的皮肉，参考视觉与表达。 |
| [Lapa Ninja](https://www.lapa.ninja/category/saas/) | 真实网站案例库 | 研究整页表达 | 完整页面截图、section 顺序、内容比例与阅读节奏；链接直达 SaaS 分类 | 这类站点适合做站点的皮肉，参考视觉与表达。 |
| [SaaSFrame](https://www.saasframe.io/) | SaaS 页面与 UI 案例库 | 查具体页面与区块 | Hero、使用场景、价格比较、Footer，以及文案、产品界面和用户流程 | 这类站点适合做站点的皮肉，参考视觉与表达。 |
| [Framer Templates](https://www.framer.com/marketplace/templates/categories/saas/) | 可使用的整站模板 | 找一套完整视觉方案 | SaaS 首页、字体搭配、图文编排、交互；另有 [AI 模板分类](https://www.framer.com/marketplace/templates/categories/ai/) | 这类站点适合做站点的皮肉，参考视觉与表达。 |
| [Webflow Templates](https://webflow.com/templates) | 可使用的整站模板 | 参考多页面网站体系 | 首页、价格、博客、联系等页面的结构与一致性 | 这类站点适合做站点的皮肉，参考视觉与表达。 |

### 如何分工

- **骨架**：优先参考 Relume。先决定每个 section 的目的、真实内容、顺序和布局，再进入视觉设计。
- **皮肉**：从 Landbook、Lapa Ninja、Framer、Webflow 或同类产品官网选择一个主要视觉参考，再按需补充局部案例。
- **局部查询**：需要 Hero、价格比较或使用场景等特定表达时，可查 Landbook 的 Sections 或 SaaSFrame 的对应分类。
- **统一表达**：将借鉴的局部设计转成同一套字体、色彩、间距、图像和动效语言。

灵感库适合研究案例；Framer、Webflow 和 Relume 也提供可使用的模板或组件。参考设计不要求购买模板或采用其发布平台。部分功能可能需要账户或付费。

## 二、网站配色工具

| 站点 | 主要用途 | 适合的阶段 | 重点功能 | 我的建议 |
| --- | --- | --- | --- | --- |
| [Happy Hues](https://www.happyhues.co/) | 参考现成的配色应用 | 探索配色方向 | 成套配色应用在实际示例页面中，标明背景、标题、正文、按钮、卡片等颜色角色 | 暂未评价。 |
| [Color Hunt](https://colorhunt.co/) | 浏览色板灵感 | 探索品牌气质 | 按 Pastel、Vintage、Dark、Warm 等标签浏览配色组合 | 暂未评价。 |
| [Realtime Colors](https://www.realtimecolors.com/) | 实时验证页面配色 | 从色板进入网页效果 | 调整背景、文字、主色、辅助色与强调色；支持明暗切换、对比度检查和 CSS 等格式导出 | 暂未评价。 |
| [UI Colors](https://uicolors.app/generate) | 生成色阶并预览 UI | 建立代码中的色彩系统 | Tailwind 色阶、网站与组件预览、中性色和成功、提示、警告、错误等状态色 | 暂未评价。 |
| [Radix Colors](https://www.radix-ui.com/colors) | 使用有明确用途的 UI 色阶 | 建立完整产品界面配色 | 背景、交互状态、边框、文字等用途分级，以及暗色和透明色方案 | 我觉得 Radix Colors 挺好。 |

### 配色要落实为颜色角色

最终确定以下角色，并按项目需要映射为语义 token：

| 角色 | 使用位置 |
| --- | --- |
| 页面背景 | 页面基础底色 |
| 表面色 | 卡片、面板、弹出层 |
| 正文色 | 标题与主要文本 |
| 弱化文字色 | 说明、辅助信息 |
| 边框色 | 分隔线、输入框、卡片边界 |
| 品牌主色 | 主要按钮和关键强调 |
| 交互状态色 | Hover、Active、Focus、Disabled |
| 业务状态色 | 成功、提示、警告、错误 |

在实际文字、按钮、边框和背景组合上检查对比度；若产品支持明暗主题，分别验证。色板的最终效果取决于各颜色的角色、面积和所在背景。

## 三、推荐使用流程

1. **真实内容**：确定目标用户、主要行动、核心价值、使用场景、价格和已有证据。
2. **Relume 定结构**：选择需要的 section，用真实内容填充，确认目的、顺序、信息层级和图文关系。
3. **选择主要视觉参考**：在案例库或模板站中选一个主方向，确定字体、图像、间距、质感和动效。
4. **寻找配色方向**：用 Happy Hues 或 Color Hunt 探索；已有品牌色时，以品牌色为起点。
5. **预览页面效果**：用 Realtime Colors 验证文字、背景、卡片、按钮的关系。
6. **落实色彩系统**：按需使用 UI Colors 或 Radix Colors，将颜色角色映射到项目 token 和交互状态。
7. **完成检查**：每个 section 都服务于访客的理解或行动；全页视觉语言一致；页面上的文案、截图和证据与实际产品相符。

按任务需要选工具即可，不要求每次访问所有站点。若参考源不可访问，说明缺口并使用可访问的等价参考；已有页面的局部调整保持原有结构和视觉身份。

## 四、按问题快速查阅

| 当前问题 | 优先查阅 |
| --- | --- |
| 首页需要哪些 section，如何排列？ | Relume、同类产品的真实内容结构 |
| Hero 或功能区怎么排版？ | Landbook、SaaSFrame、Relume |
| 想看完整页面如何讲清楚产品？ | Lapa Ninja、同类产品官网 |
| 想找一套完整模板？ | Framer、Webflow |
| 还没有配色方向？ | Happy Hues、Color Hunt |
| 想看配色落在网页上的效果？ | Realtime Colors |
| 已有主色，需要完整色阶和 UI 状态？ | UI Colors、Radix Colors |
