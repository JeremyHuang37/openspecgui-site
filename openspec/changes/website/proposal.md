## Why

OpenSpecGUI 已作为 Mac 应用开发完成并放在项目中，但缺少对外展示与分发入口。需要有一个官网页面介绍这款 App 的功能与价值，并让用户能方便地下载安装，提升发现率和采用率。

## What Changes

- 新增一个面向公众的网站（可部署在项目内或独立域名）。
- 网站包含对 OpenSpecGUI Mac App 的介绍：产品定位、核心功能、适用场景。
- 提供明确的下载入口：用户可从该页面获取 Mac 版安装包（如 .app 或 .dmg）。
- 可选：展示版本号、系统要求、更新说明等基础信息。

## Capabilities

### New Capabilities

- `app-intro`: 介绍 OpenSpecGUI 的页面或区块，包括产品说明、主要功能、使用场景与价值，以及必要的视觉呈现（如截图、图标）。
- `download`: 下载能力——在页面上提供 Mac 版 OpenSpecGUI 的下载入口（链接到可下载的 .app/.dmg 或发布资源），并可选展示当前版本、系统要求与简要更新说明。

### Modified Capabilities

- （无：当前无已有 spec 需要修改。）

## Impact

- 新增网站相关代码与静态资源（如放在 `my-website/` 或独立目录）。
- 下载入口需指向现有或后续的构建产物（如 `OpenSpecGUI.app` 或打包后的 .dmg）。
- 若通过 CDN/静态托管部署，需配置构建与发布流程；不改变现有 OpenSpec 工作流或 CLI 行为。
