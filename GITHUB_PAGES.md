# GitHub Pages 发布说明

本项目已经准备为独立仓库 `future-mind-organoid` 通过 GitHub Actions 自动构建和发布。每次向 `main` 分支推送，工作流将使用 Node.js 22、pnpm 10 构建静态产物，并发布到 GitHub Pages。

## 自定义域名

发布配置会把 `www.organoid-chip.com` 写入最终站点的 `CNAME` 文件。请在域名的 DNS 服务商处添加以下记录：

| 主机记录 | 类型 | 记录值 |
| --- | --- | --- |
| `www` | `CNAME` | `leolzk.github.io` |

可选地，如需让裸域 `organoid-chip.com` 也可访问，可在 DNS 服务商添加 GitHub Pages 的四条 A 记录：`185.199.108.153`、`185.199.109.153`、`185.199.110.153`、`185.199.111.153`。域名 DNS 生效后，再在 GitHub 仓库的 **Settings → Pages** 确认自定义域名并启用 HTTPS。

## 路由兼容

发布工作流会把构建后的 `index.html` 复制为 `404.html`，使 `/chips`、`/cro` 等前端路由在 GitHub Pages 刷新后仍能加载应用。
