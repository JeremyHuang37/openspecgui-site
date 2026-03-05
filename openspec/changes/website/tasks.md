## 1. 站点结构与基础页面

- [x] 1.1 在 `my-website/` 下新增 `index.html`，包含基础 HTML5 结构、`<title>` 与 viewport meta，不移动或删除现有 `OpenSpecGUI.app`
- [x] 1.2 如需独立样式与资源，在 `my-website/` 下新增 `assets/` 目录（或等价路径），用于放置 CSS、图片等

## 2. 产品介绍（app-intro）

- [x] 2.1 在首屏展示产品名称 "OpenSpecGUI" 与一句简短 tagline/描述，保证首屏可见（above the fold）
- [x] 2.2 添加「Why」或「What」区块，用简明文案说明产品用途与目标用户（OpenSpec 工作流用户、开发者/团队）
- [x] 2.3 列出至少两项主要功能或能力（如管理变更、查看规范、运行工作流等），便于访客判断是否适用
- [x] 2.4 在页面中至少加入一处产品视觉（App 图标、截图或示意图），可从 `OpenSpecGUI.app/Contents/Resources/AppIcon.icns` 或现有资源复用/导出

## 3. 下载入口（download）

- [x] 3.1 在页面上添加一个明显的下载按钮或链接，点击后能发起或跳转到 Mac 版安装包下载
- [x] 3.2 将下载入口指向有效的 Mac 安装物（如 `OpenSpecGUI.app` 的 zip、或同目录下的 .app/.dmg 路径），确保在目标部署环境下可下载并安装
- [x] 3.3 在常见桌面视口下，下载入口无需横向滚动即可看到

## 4. 版本与系统要求（可选）

- [x] 4.1 若展示版本号或系统要求，在页面中以可读文案形式写出（如「Version 1.0.0」「macOS 12+」），数据可写死在 HTML 或单文件 JS 中

## 5. 样式与部署

- [x] 5.1 为页面添加简洁、可读的版式与配色（可与 OpenSpec 文档风格一致），不引入重型 UI 库
- [x] 5.2 在 README 或项目文档中说明如何部署该站点（如 GitHub Pages 根目录设为 `my-website/`、或上传至其他静态托管并设置默认文档为 `index.html`）
