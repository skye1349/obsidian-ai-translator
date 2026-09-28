# AI Translator

Obsidian内で語句の意味を調べ、文章を翻訳して対訳ノートを保存します。Markdownと文字を選択できるPDFに対応します。

[English](README.md) · [简体中文](README.zh-CN.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Español](README.es.md) · [Français](README.fr.md) · [Deutsch](README.de.md)

## 使い方を動画で見る

各 GIF で一つの機能を紹介します。英語の手順、クリック位置の強調、キーボード操作の表示が付いています。

[**12 個の機能デモを見る**](docs/demos.md) · [動画ガイド全編](https://github.com/skye1349/obsidian-ai-translator/releases/download/1.0.0/ai-translator-guide.mp4)

![使い方を動画で見る](https://github.com/skye1349/obsidian-ai-translator/releases/download/1.0.0/translate-passage.gif)

## できること

- Markdownや選択可能なPDFの単語・文章を翻訳。
- 文脈に沿った語句の説明を確認。
- 原文を残し、その下に訳文を挿入。
- 単一・複数のMarkdownを末尾追加または対訳形式で翻訳。
- 抜粋と訳文を指定したノートに収集。
- 言語と速度を調整して選択文を読み上げ。

## インストール

デスクトップ版 Obsidian 1.13.7 以降が必要です。モバイルには対応していません。

1. Obsidian の**設定 → コミュニティプラグイン**を開き、必要なら有効にします。
2. **閲覧（Browse）**で **AI Translator** を検索します。
3. **インストール（Install）**、**有効化（Enable）**の順に選びます。
4. プラグイン設定で言語とAIサービスを選びます。

## 最初の翻訳

1. AIを設定し、**Learning / target language** を選びます。
2. ノートの文章を選択して **Translate selected text** を実行します。
3. ポップアップを使う場合は **Auto translate selection** を有効にし、macOSはCommand、Windows/LinuxはCtrlを押しながら選択します。設定で変更できます。
4. 単語を選ぶと意味を確認し、文脈に沿ったAI説明を頼めます。スキャンPDFは先にOCRが必要です。

## AI の設定

本プラグインの **AI backend** でサービスを選びます。OpenAI / Anthropic はご自身の API キーを入力してください。利用料金はサービス側で発生します。ローカルの **Codex / Claude Code** は先にインストールしてログインします。見つからない場合は **Codex command / Claude command** にパスを指定してください。ローカルCLIでも内容がAIサービスへ送られる場合があります。

通常は **Automatic · Economy** を使用します。対応する軽量モデルを選び、選択を1時間キャッシュし、高価格モデルへ自動変更しません。固定モデルや独自APIアドレスには **Manual** を選びます。API接続は **Test API connection** で確認できます。

## ノートに残す

**Insert translation below selected text** で原文の下に訳文を追加します。Markdown全体は末尾追加または原文と交互の翻訳を選べます。複数ファイルの一括翻訳も可能です。ノートを変更するため、最初はコピーで試してください。

**Save selected text to excerpt note** で抜粋を集め、**Excerpt file** で保存先を指定します。訳文の追加や保存後に開く動作も設定できます。**Read selected text aloud** で読み上げます。

## プライバシーと困ったとき

選択文と文脈、全文翻訳では文書の分割内容がAIへ送られます。基本辞書・翻訳検索はAIとは別にGoogleへ接続する場合があります。手動だけで使う場合は **Auto translate selection** を無効にします。反応しない場合は修飾キーかコマンドパレットを確認してください。大きな文書には **Timeout / Batch chunk size** を調整します。

APIキーは保管庫内のプラグイン設定に保存されます。保管庫の共有・同期時は設定を保護してください。AIエラー時はサービス、認証、モデルを確認します。残高・通信エラーではモデルを自動変更しません。

動画には [Video Player (AI integrated)](https://github.com/skye1349/obsidian-video-player-ai) を使用できます。

## サポート

[GitHub Issues](https://github.com/skye1349/obsidian-ai-translator/issues)にバージョンとエラーを報告してください。APIキーや非公開ノートは添付しないでください。

ローカルAI連携はユーザーディレクトリのCLIモデル情報と既存ログインを使用します。ツールの自動インストールは行いません。

[MIT License](LICENSE) · © 2026 Taoye
