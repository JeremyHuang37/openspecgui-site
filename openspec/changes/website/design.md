## Context

OpenSpecGUI 已作为 Mac 应用存在于 `my-website/OpenSpecGUI.app`，当前仓库无对外官网。需要新增一个静态网站：介绍产品并提供 Mac 版下载入口，便于用户发现与安装。受众为使用 OpenSpec 工作流的开发者与团队。

## Goals / Non-Goals

**Goals:**

- 提供单一落地页，清晰介绍 OpenSpecGUI 的用途、功能与价值。
- 提供明确的 Mac 版下载入口（链接到可下载的 .app 或 .dmg）。
- 站点可独立部署（如 GitHub Pages、Vercel、Netlify 等），无需后端服务。
- 与现有 `my-website/` 目录结构兼容，便于把 App 与网站一起发布。

**Non-Goals:**

- 不做用户系统、登录、付费或版本管理后台。
- 不做自动构建/签名流水线（下载物可先用手动构建产物）。
- 不承诺多语言或深度 SEO 优化（首版以单页、清晰为主）。

## Decisions

1. **站点形态：单页静态站**
   - 采用单页（或极少量页面），减少路由与部署复杂度，首屏即介绍 + 下载。
   - 备选：多页站点（如 /features、/download）——首版不采纳，避免过度设计。

2. **技术选型：纯 HTML/CSS/JS 或轻量框架**
   - 推荐：纯 HTML + CSS + 少量 JS，无构建依赖，直接放在仓库即可部署。
   - 备选：Next.js / Astro 等——若后续需要博客、多语言再引入；当前以简单可维护为准。

3. **站点与 App 的共置**
   - 网站源码与静态资源放在 `my-website/` 下（例如 `my-website/index.html`、`my-website/assets/`），与 `OpenSpecGUI.app` 同目录，便于同一部署根路径提供「页面 + 下载」。
   - 下载链接指向同域下的 App 包（如 `/OpenSpecGUI.app` 或 `/releases/OpenSpecGUI-1.0.0.dmg`），由托管方提供静态文件服务即可。

4. **下载物形式**
   - 首版：直接提供 `.app` 的 zip 或目录链接，或后续增加 `.dmg`；具体文件名与版本号在实现时由 tasks 确定。
   - 页面上可展示当前版本号、最低 macOS 版本等文案，数据可写死在 HTML 或单文件 JS 中，无需后端。

5. **样式与品牌**
   - 使用简洁、可读的版式与配色，与 OpenSpec 文档风格大致一致即可；不依赖重型 UI 库，便于长期维护。

## Risks / Trade-offs

- **[Risk] 直接提供 .app 下载可能被浏览器或托管方限制**  
  →  mitigation：可改为提供 zip 包或 .dmg；若托管不支持大文件，可外链到 GitHub Releases 等，页面仅保留「下载」按钮与跳转。

- **[Risk] 版本号与更新说明需手动更新**  
  →  mitigation：接受首版手动维护；在 README 或 tasks 中注明发布时需更新版本号与下载链接。

- **[Trade-off] 单页信息密度有限**  
  →  首版优先保证「介绍 + 下载」清晰；若后续需要功能详解、截图轮播等再扩展版面或增加子页。

## Migration Plan

- 在 `my-website/` 下新增 `index.html`（及可选 `assets/`），不移动或删除现有 `OpenSpecGUI.app`。
- 若使用 GitHub Pages：将站点根设为 `my-website/` 或配置发布分支与目录，使访问根即看到官网，`/OpenSpecGUI.app` 或 `/releases/...` 可下载。
- 若使用其他静态托管：上传 `my-website/` 内容并配置默认文档为 `index.html`。
- 回滚：删除或还原新增的网页文件即可，不影响已有 .app。

## Open Questions

- 是否需要在首版提供 .dmg（安装体验更好），还是仅 .app/zip。
- 版本号与「当前版本」文案的更新流程（是否与 release 脚本或 CHANGELOG 联动）。
