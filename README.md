# SillyTavern 角色卡自动更新扩展 (AutoCardUpdaterExtension)

[![版本](https://img.shields.io/badge/version-3.8.6-blue.svg)](manifest.json)
[![许可证](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

一个为 [SillyTavern](https://github.com/SillyTavern/SillyTavern) 设计的强大扩展，旨在通过与自定义AI服务集成，自动分析对话历史，并动态生成和更新角色的世界书（Lorebook）条目，确保角色在互动中保持深度和一致性。

---

## 核心功能

-   **🤖 自动更新**: 在对话达到设定阈值时，自动调用AI，根据最新聊天内容生成或更新角色卡。
-   **👆 手动触发**: 提供“手动更新”按钮，让您随时可以捕捉角色的最新状态。
-   **🔧 高度可配置**:
    -   **自定义AI**: 支持任何与OpenAI兼容的API（如SillyTavern extras, LM Studio, Oobabooga等）。
    -   **自定义提示词**: 允许用户完全自定义用于破甲和生成角色卡的系统提示词。
-   **✨ 角色卡查看器**:
    -   提供一个可拖动的浮动按钮，一键打开角色卡编辑器。
    -   支持在同一个弹窗内，通过Tab标签页轻松查看和编辑所有已生成的角色卡。
-   **🔄 自动版本检查**: 扩展会自动检查GitHub仓库中的新版本，并提供一键更新功能，让您始终保持最新。

## 演示

*（这里可以放置一个GIF或截图来展示扩展的UI和核心功能）*

![演示截图](https://user-images.githubusercontent.com/your-id/your-image.png)

---

## 安装指南

### 方法一：通过SillyTavern扩展安装器 (推荐)

1.  在SillyTavern主界面，进入 **扩展 (Extensions)** 菜单。
2.  在 **下载扩展 (Download Extension)** 标签页中，粘贴本仓库的URL：
    ```
    https://github.com/1830488003/AutoCardUpdaterExtension
    ```
3.  点击下载并等待安装完成。

### 方法二：手动安装

1.  点击本仓库页面右上角的 **Code** -> **Download ZIP**。
2.  解压下载的ZIP文件。
3.  将解压后的 `AutoCardUpdaterExtension` 文件夹，完整地移动到您的SillyTavern安装目录下的 `public/scripts/extensions/third-party/` 文件夹中。
4.  重新启动SillyTavern。

---

## 使用说明

1.  **打开设置**: 安装并启用扩展后，在 **扩展 (Extensions)** 菜单中找到“角色卡自动更新”，点击齿轮图标⚙️进入设置面板。

2.  **API配置**:
    -   **API URL**: 填入您的AI服务的URL（例如 `http://127.0.0.1:5001`）。
    -   **API Key**: (可选) 如果您的服务需要，请填入API密钥。
    -   **加载模型**: 点击 **加载模型列表** 按钮，然后从下拉菜单中选择您要用于生成角色卡的模型。
    -   **保存配置**: 点击 **保存API配置**。

3.  **功能设置**:
    -   **自动更新阈值**: 设置进行一次自动更新需要累积多少条新消息。
    -   **启用自动更新**: 勾选此项以启用自动更新功能。
    -   **启用角色卡查看器**: 控制浮动按钮的显示与隐藏。

4.  **开始使用**:
    -   **自动**: 正常进行对话，当消息量达到阈值时，扩展会自动在后台工作。
    -   **手动**: 在设置面板中点击 **立即更新所有角色描述**，或在主聊天界面点击浮动按钮打开查看器并进行操作。

## 版本历史

详细的版本更新日志请参阅项目内的 `项目文档.txt` 文件。

-   **v3.8.6**: 重大UI修复，彻底解决移动端弹窗的布局和定位问题。
-   **v3.8.0**: UI风格统一，修复API调用和解析器的兼容性问题。
-   **v3.5.0**: 关键BUG修复，解决`include_swipes`导致上下文错误的问题。
-   **v3.0.0**: 架构定型，重写渲染器和解析器，确保数据流稳定。
-   **v2.0.0**: 重大架构重构，放弃YAML，引入可靠的自定义`[key]:value`数据格式。

## 贡献

欢迎通过提交 **Issues** 来报告BUG或提出功能建议。
如果您想直接贡献代码，也欢迎提交 **Pull Requests**。

## 许可证

本项目采用 [MIT](LICENSE) 许可证。
