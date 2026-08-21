# 芯启蔚来旗舰官网自定义说明

> 当前版本未保存为新检查点、未发布，也没有推送到 GitHub。所有文字和视觉更改会在开发预览中实时生效。

## 内容与双语文案

公司的中英文名称、口号、电话、页面导航与服务名称集中位于 `client/src/lib/futureMindContent.ts`。每段可切换内容均以 `zh` 与 `en` 成对维护；更新时请同步修改两个字段，确保中英界面信息一致。

| 调整目标 | 位置 | 说明 |
| --- | --- | --- |
| 公司名称、口号、电话 | `company` | 供页首、页尾、联系模块共用 |
| Logo 与主视觉 | `ASSETS` | 使用已上传的安全静态资源 URL |
| 首页四项服务 | `solutions` | 修改名称、简介与跳转地址 |
| 服务页首屏文案 | `serviceCopy` | 修改标题、说明与页面主视觉 |

## Logo 与旗舰视觉

用户提供的 Logo 已裁切为正方形品牌印记，当前地址为 `ASSETS.logo`。这个处理仅改善网页中的比例、圆形容器呈现与清晰度，不重绘或改动 Logo 主体图形。首页旗舰主视觉、芯片页和 CRO 页使用独立的深空 AI 生物科技图像；不建议将同一张图用于多个核心页面。

网站主色变量位于 `client/src/index.css` 的顶部。`--blue` 为离子青，`--red` 为决策信号红，`--paper` 为深空底色。调整颜色时应同时检查按钮、正文、导航与图片叠层上的文字对比度。

## 字体与指针交互

网站现已使用两套**本地自托管的开源字体**：`FM Songti`（Noto Serif CJK SC，宋体风格标题）与 `FM Heiti`（Noto Sans CJK SC，黑体风格正文和界面）。字体文件与 `OFL.txt` 许可证均位于 `client/public/fonts/`，采用 SIL Open Font License 1.1。`index.html` 不加载 Google Fonts、Adobe Fonts 或其他外部字体服务；CSS 也不再列出操作系统商业字体名称。

旗舰鼠标磁场、扫描环、数据流与粒子逻辑位于 `client/src/components/BioField.tsx`，样式位于 `index.css` 的 “AI BIO COMMAND CENTER” 区块。它们是纯前端视觉效果，不会收集用户数据；系统开启“减少动态效果”时会自动关闭。
