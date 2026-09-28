# AI Translator

在 Obsidian 内理解词义、翻译段落并保存双语笔记。支持 Markdown 和可选择文本的 PDF，不必每次把内容复制到另一个聊天应用。

[English](README.md) · [简体中文](README.zh-CN.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Español](README.es.md) · [Français](README.fr.md) · [Deutsch](README.de.md)

## 功能演示

每个 GIF 演示一个功能，包含英文操作步骤、鼠标点击高亮和键盘快捷键提示。

[**查看全部 12 个功能演示**](docs/demos.md) · [完整视频教程](https://github.com/skye1349/obsidian-ai-translator/releases/download/1.0.0/ai-translator-guide.mp4)

![功能演示](https://github.com/skye1349/obsidian-ai-translator/releases/download/1.0.0/translate-passage.gif)

## 能做什么

- 翻译 Markdown 或可选文字 PDF 中的单词和段落。
- 结合上下文理解词义，而不只是查看字面翻译。
- 保留原文，在下方插入译文，制作双语笔记。
- 翻译单篇或多篇 Markdown，选择文末追加或原文译文交错排列。
- 把选中内容及译文收集到指定摘录笔记。
- 朗读选中文字，并调整语音语言和速度。

## 安装

需要桌面版 Obsidian 1.13.7 或更新版本，不支持手机和平板。

1. 打开 Obsidian 的**设置 → 第三方插件**，如有提示先启用第三方插件。
2. 点击**浏览**，搜索 **AI Translator**。
3. 点击**安装**，然后**启用**。
4. 打开插件设置，选择语言和 AI 服务。

## 翻译第一段文字

1. 按下方说明配置 AI，在 **Learning / target language** 中选择目标语言。
2. 选中笔记文字，从命令面板执行 **Translate selected text**。
3. 想在阅读时显示弹窗，保留 **Auto translate selection**，按住 macOS 的 Command 或 Windows/Linux 的 Ctrl 再选择文字；可在设置中修改这一要求。
4. 选择单词查看释义，并请求结合上下文的 AI 解释。PDF 必须能选中文字，扫描件需要先做 OCR。

## 配置 AI

打开本插件设置，在 **AI backend** 中选择服务。使用 OpenAI 或 Anthropic 时填写自己的 API key，费用由对应服务商收取。使用本地 **Codex** 或 **Claude Code** 时，先安装并登录对应程序；若无法自动找到，填写 **Codex command** 或 **Claude command** 路径。本地运行这些程序仍可能把内容发送给其 AI 服务商。

建议保留 **Automatic · Economy / 自动选择 · 经济型**，优先使用支持的轻量模型，缓存选择一小时，不自动升级旗舰模型。需要固定型号时切换 **Manual / 手动指定**；自定义 API 地址也请使用手动模式。API 用户可以点击 **Test API connection** 测试连接。两个插件的设置相互独立。

## 把结果整理成笔记

执行 **Insert translation below selected text**，可保留原文并在下面插入译文。翻译整篇 Markdown 时，可以选择在文末追加译文，也可以选择原文与译文交错排列；批量命令支持多篇 Markdown。这些命令会修改笔记，建议先在副本上试用。

执行 **Save selected text to excerpt note** 收集摘录。在 **Excerpt file** 中设置摘录文件，并选择是否附带译文、保存后是否打开文件。**Read selected text aloud** 可按设置的语音语言和速度朗读。

## 隐私与常见问题

翻译和 AI 解释会把选中文字及相关上下文发送给所选服务商；整篇翻译会发送文档分段。基础在线词典/翻译查询可能独立连接 Google。自动翻译会在你触发设定的选词手势时运行；只想手动操作时关闭 **Auto translate selection**。

选中文字后没反应时，检查修饰键要求，或直接使用命令面板。PDF 无法选字时先做 OCR。长文档可以增加 **Timeout**，或调整 **Batch chunk size**。

API key 保存在笔记库内的插件设置中，共享或同步笔记库时请保护这些设置。AI 无法使用时，检查服务商、登录/API key 和模型；额度不足或网络故障不会触发自动换模型。

视频播放、字幕和截图笔记请使用 [Video Player (AI integrated)](https://github.com/skye1349/obsidian-video-player-ai)。两个插件独立使用。本插件不会替换旧 Read and Watch with AI，也不会自动导入其设置。若同时启用两个翻译插件，请关闭其中一个的选词弹窗，避免重复响应。

## 获取帮助

请到 [GitHub Issues](https://github.com/skye1349/obsidian-ai-translator/issues)反馈，附上插件版本和错误信息，不要上传 API key 或私人笔记。

本地 AI 集成也会读取用户目录中的 CLI 模型目录，并使用已有登录。插件不会自行安装这些工具。

[MIT License](LICENSE) · © 2026 Taoye
