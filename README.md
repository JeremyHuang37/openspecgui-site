# openspecgui-site

OpenSpecGUI 官网与 Mac 应用分发。

## 部署官网

站点为静态单页，位于项目根目录：

- **index.html** — 落地页（产品介绍 + 下载入口）
- **assets/** — 样式与图标
- **OpenSpecGUI.app** — Mac 应用（与页面同目录，供下载）

### 部署方式

- **GitHub Pages**：在仓库设置中将 Source 设为项目根（或 `main` 分支根目录），访问根即显示官网，`/OpenSpecGUI.app` 可作为下载链接（若托管方支持大文件）。
- **其他静态托管**（Vercel、Netlify 等）：将项目根作为站点根目录上传，默认文档设为 `index.html`。若需提供 .app 下载，可先将 `OpenSpecGUI.app` 打成 zip 并上传，将页面中的下载链接改为该 zip 的 URL。
