# AI Translator

在 Obsidian 内理解词义、翻译段落并保存双语笔记。支持 Markdown 和可选择文本的 PDF，不必每次把内容复制到另一个聊天应用。

[English](README.md) · [简体中文](README.zh-CN.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Español](README.es.md) · [Français](README.fr.md) · [Deutsch](README.de.md)

## 安装

需要桌面版 Obsidian 1.13.7 或更新版本，不支持手机和平板。

社区插件目录正在等待审核。安装按钮开放前，请按下面的方法手动安装。

从[最新版本](https://github.com/skye1349/obsidian-ai-translator/releases/latest)下载 **main.js**、**manifest.json** 和 **styles.css**。在笔记库中创建 `<笔记库>/.obsidian/plugins/ai-translator/`，放入这三个文件，重启 Obsidian，然后在**设置 → 第三方插件**中启用 **AI Translator**。目录审核通过后，也可以在「浏览」中搜索 **AI Translator**，安装并启用。

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

你选择的本地视频可以位于笔记库之外。本地 AI 集成也会读取用户目录中的 CLI 模型目录，并使用已有登录。插件不会自行安装这些工具。

[MIT License](LICENSE) · © 2026 Taoye
