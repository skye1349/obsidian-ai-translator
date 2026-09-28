# AI Translator

Understand words in context, translate passages and keep bilingual notes inside Obsidian. Work with Markdown and selectable PDF text without copying everything into a separate chat app.

[English](README.md) · [简体中文](README.zh-CN.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Español](README.es.md) · [Français](README.fr.md) · [Deutsch](README.de.md)

## Install

Desktop Obsidian 1.13.7 or later is required. Mobile is not supported.

Community-directory review is pending. Until the Install button is available, use the manual installation below.

Download **main.js**, **manifest.json**, and **styles.css** from the [latest release](https://github.com/skye1349/obsidian-ai-translator/releases/latest). Create `<vault>/.obsidian/plugins/ai-translator/`, put the three files there, restart Obsidian, then enable **AI Translator** in **Settings → Community plugins**. When the directory listing is approved, you can instead search for **AI Translator** under **Browse**, install and enable it.

## Translate your first passage

1. Configure AI below and choose **Learning / target language**.
2. Select text in a note, then run **Translate selected text** from the command palette.
3. For a popup while reading, keep **Auto translate selection** enabled and hold Command on macOS or Ctrl on Windows/Linux while selecting. You can change this requirement in settings.
4. Select a word to see its meaning and request an AI explanation in context. PDF text must be selectable; scanned pages need OCR first.

## Set up AI

Open this plugin’s settings and choose **AI backend**. For OpenAI or Anthropic, enter your own API key. API usage is billed by that provider. For local **Codex** or **Claude Code**, install and sign in to that application first; set **Codex command** or **Claude command** if it is not found automatically. Local CLI use can still send your content to its AI provider.

Start with **Automatic · Economy** for supported lightweight models. It caches selections for one hour and never automatically upgrades to a flagship model. Use **Manual** to choose a specific model; custom API base URLs require Manual mode. If using an API, run **Test API connection**. Each plugin has its own settings.

## Keep a useful note

Use **Insert translation below selected text** to retain the original passage. For a whole Markdown note, choose the command that appends a translation or interleaves it with the original. Batch commands work with multiple Markdown files. These commands modify your notes, so try them on a copy first.

Use **Save selected text to excerpt note** to collect passages. Choose **Excerpt file**, whether to include the translation, and whether to open it after saving. **Read selected text aloud** uses the configured speech language and rate.

## Privacy and common questions

Translation and AI explanations send the selected text and relevant context—or document chunks for full-file translation—to your chosen provider. Basic online dictionary/translation lookup can contact Google independently of the AI backend. Automatic selection translation runs when its configured gesture is triggered; disable **Auto translate selection** to use commands only.

If a selection does nothing, check the modifier-key setting or use the command palette. If PDF text cannot be selected, apply OCR first. For large documents, allow more time or adjust **Batch chunk size** and **Timeout**.

API keys are saved in this plugin’s settings in your vault. Keep those settings private, including when sharing or syncing your vault. If AI fails, check the selected backend, login/API key and model; quota or network errors do not cause an automatic model switch.

For YouTube/local playback, subtitles and screenshot notes, use [Video Player (AI integrated)](https://github.com/skye1349/obsidian-video-player-ai). Both work independently. This new plugin does not replace or import settings from Read and Watch with AI. If both translators are enabled, disable one selection popup to avoid duplicate responses.

## Help

Report a problem on [GitHub Issues](https://github.com/skye1349/obsidian-ai-translator/issues); include the plugin version and error message, but never an API key or private notes.

Local video files you choose may be outside your vault. Local AI integrations also read the CLI’s model catalog and use its existing login in your user directory. The plugin does not install these tools for you.

[MIT License](LICENSE) · © 2026 Taoye
