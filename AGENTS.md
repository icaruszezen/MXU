# MXU 项目指南

本文档旨在帮助开发者（包括 AI）快速了解 MXU 项目结构，以便参与开发。

## 项目概述

**MXU** 是一个基于 [MaaFramework ProjectInterface V2](https://github.com/MaaXYZ/MaaFramework/blob/main/docs/zh_cn/3.3-ProjectInterfaceV2协议.md) 协议的通用 GUI 客户端，使用 Tauri 2 + React 19 + TypeScript 构建。

它解析符合 PI V2 标准的 `interface.json` 文件，为 MaaFramework 生态中的自动化项目提供开箱即用的图形界面。

## 注意事项

- 请尽量复用项目中的组件、Utils 等，减少冗余。若发现原先代码即存在冗余，请再不改变软件行为的前提下，进行一定的抽象和重构。
- 修改 UI 涉及窗口权限问题时，请检查 `src-tauri/capabilities/default.json` 是否需要新增权限。
- 添加本文请同步检查 `src/i18n/locales` 中各语言的翻译，避免硬编码文本。
- 涉及更新下载相关功能，请十分慎重，仔细检查代码。因为其他功能若有问题，发布新版本修复即可；但更新功能一旦出错，用户可能无法正常获取新版本从而修复该问题，从而永久停留在该异常版本中。

## 相关资源

- [MaaFramework](https://github.com/MaaXYZ/MaaFramework) - 底层自动化框架
- [ProjectInterface V2 协议](https://github.com/MaaXYZ/MaaFramework/blob/main/docs/en_us/3.3-ProjectInterfaceV2.md)
- [Tauri 文档](https://tauri.app/v2/)
- [React 文档](https://react.dev/)
- [Zustand 文档](https://zustand-demo.pmnd.rs/)
