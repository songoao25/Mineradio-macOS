# Mineradio macOS

> ⚠️ **重要声明**：本项目是 [Mineradio](https://github.com/XxHuberrr/Mineradio) 的 macOS 适配分支，**原作者为 XxHuberrr**。本仓库仅对 macOS 平台进行适配构建，不改变原有功能与架构。如果你觉得这个项目对你有价值，请前往[原仓库](https://github.com/XxHuberrr/Mineradio)给作者 Star ⭐。

Mineradio 是一款桌面沉浸式音乐播放器，把天气电台、搜索播放、歌词舞台、粒子视觉和 3D 歌单架组合成一个更接近现场感的私人音乐空间。本仓库为 macOS 适配版本。

1.1.0 的核心目标是把 Mineradio 重新整理成一份可公开下载的纯净安装版。

## 当前版本

当前版本：`1.1.1`

## 下载安装

- **macOS**（Apple Silicon / Intel）→ 从 [GitHub Releases](../../releases) 下载 `Mineradio-1.1.1-arm64.dmg`，打开后将 Mineradio 拖入 Applications 即可
- **Windows** → 从 [原仓库 XxHuberrr/Mineradio](https://github.com/XxHuberrr/Mineradio/releases) 下载 `Mineradio-1.1.1-Setup.exe`

## 核心特性

- Open-Meteo 天气电台，根据当前位置、城市和天气 mood 生成更合适的播放队列
- 首页包含天气电台、每日推荐、私人电台、继续听、听歌画像和我的歌单入口
- Wallpaper 银河首页背景，未播放状态保持干净的星河氛围
- 播放后切换到 Emily / 默认播放态视觉，歌词舞台与粒子舞台同步工作
- 基于节奏的电影镜头视觉系统
- 面向长播客和 DJ 曲目的专属视觉模式
- 歌词舞台、自定义歌词、歌词位置与视觉控制
- 自定义专辑封面上传与裁剪
- 右键唤起 3D 歌单架，支持歌单队列浏览
- 网易云音乐账号、搜索、歌单、播客等体验接入
- QQ 音乐搜索、登录态与音源补充接入
- GitHub Releases 更新检测与下载入口
- 首次启动内置「默认测试」视觉用户存档，软件内默认视觉参数与该存档一致

## 使用说明

### macOS

从 GitHub Releases 下载 `Mineradio-1.1.1-arm64.dmg` → 双击打开 → 将 Mineradio 拖入 Applications 文件夹 → 首次打开时右键选择「打开」以绕过未签名提示。也可在终端执行：

```bash
xattr -cr /Applications/Mineradio.app
```

### Windows

从原仓库 Releases 下载 `Mineradio-1.1.1-Setup.exe` 安装。

## 开发运行

```bash
npm install
npm start
npm run build:mac   # 生成 macOS DMG，产物位于 dist/
npm run build:win   # 生成 Windows NSIS 安装包，产物位于 dist/
```

桌面版入口由 Electron 主进程加载本地服务。

## 更新机制

Mineradio 会请求 GitHub Releases latest 检测新版本。远端版本高于本地版本时，应用内更新入口会展示 Release 内容、下载安装包到本机用户数据目录，并通过系统打开安装包。

本地验证更新链路时，可以通过 `MINERADIO_UPDATE_MANIFEST` 指向一个本地 manifest JSON 或 HTTP 地址来模拟线上 Release。

## 第三方音乐平台说明

Mineradio 不是网易云音乐、QQ 音乐或腾讯音乐娱乐集团的官方客户端，也不隶属于任何音乐平台。

项目中的第三方平台接入仅用于个人学习、本地客户端体验和用户自有账号的播放辅助。请遵守对应平台的用户协议、版权规则和会员权益规则。项目不会提供绕过付费、绕过会员、破解音质或重新分发音乐内容的能力。

## 用户数据与隐私

登录 Cookie、搜索历史、自定义封面、自定义歌词、节奏分析缓存等数据只应保存在本机用户数据目录或浏览器本地存储中，不应提交到仓库。

更多说明见 [PRIVACY.md](./PRIVACY.md)。

## 作者支持

如果 Mineradio 陪你多听了一首歌，也欢迎请作者一杯咖啡。

[查看完整支持页](./docs/SUPPORT.md)

![Mineradio 作者支持渠道](./docs/assets/support/mineradio-author-support-poster.png)

## 致谢

Mineradio 由 XxHuberrr 主要设计与打造。emily 作为早期视觉底层想法与 `emily` 视觉预设改进方向的共创者和灵感来源之一，特此感谢。

同时感谢小天才e宝、应春日、锋将军、軌跡、林中、骊、风痕、花椰菜🥦在早期体验、测试反馈和发布准备中的帮助。

## 版权与授权

本项目为 [Mineradio](https://github.com/XxHuberrr/Mineradio) 的 macOS 适配版本，基于原作者 XxHuberrr 的代码适配，遵循 GPL-3.0 授权。详见 [LICENSE](./LICENSE)。

原作 Copyright (C) 2026 XxHuberrr.

MR Logo、Mineradio 名称、界面视觉设计与原创视觉表达归作者所有；第三方依赖和第三方服务分别遵循其各自授权与服务条款。
