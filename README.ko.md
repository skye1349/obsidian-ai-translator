# AI Translation Assistant

Obsidian 안에서 단어 뜻을 이해하고 문장을 번역하여 이중 언어 노트를 만드세요. Markdown과 텍스트 선택이 가능한 PDF를 지원합니다.

[English](README.md) · [简体中文](README.zh-CN.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Español](README.es.md) · [Français](README.fr.md) · [Deutsch](README.de.md)

## 사용 방법 살펴보기

각 GIF는 한 가지 기능을 보여 줍니다. 영어 안내, 마우스 클릭 강조, 키보드 단축키 표시가 포함되어 있습니다.

[**12개 기능 데모 보기**](docs/demos.md) · [전체 동영상 가이드](https://github.com/skye1349/obsidian-ai-translator/releases/download/1.0.0/ai-translator-guide.mp4)

![사용 방법 살펴보기](https://github.com/skye1349/obsidian-ai-translator/releases/download/1.0.0/translate-passage.gif)

## 주요 기능

- Markdown과 선택 가능한 PDF 텍스트의 단어와 문장을 번역합니다.
- 문맥에 맞는 어휘 설명을 확인합니다.
- 원문을 유지하고 아래에 번역을 넣습니다.
- Markdown 한 개 또는 여러 개를 끝에 추가하거나 교차 배치해 번역합니다.
- 발췌와 번역을 원하는 노트에 모읍니다.
- 언어와 속도를 조정해 선택한 텍스트를 읽습니다.

## 설치

데스크톱 Obsidian 1.13.7 이상이 필요합니다. 모바일은 지원하지 않습니다.

1. Obsidian **설정 → 커뮤니티 플러그인**을 열고 필요한 경우 활성화합니다.
2. **탐색(Browse)**에서 **AI Translation Assistant**을 검색합니다.
3. **설치(Install)** 후 **활성화(Enable)**를 누릅니다.
4. 플러그인 설정에서 언어와 AI 서비스를 선택합니다.

## 첫 번역

1. AI를 설정하고 **Learning / target language**를 고릅니다.
2. 노트의 텍스트를 선택하고 **Translate selected text**를 실행합니다.
3. 팝업을 쓰려면 **Auto translate selection**을 켜고 macOS에서는 Command, Windows/Linux에서는 Ctrl을 누른 채 선택합니다. 이 조건은 설정에서 바꿀 수 있습니다.
4. 단어를 선택해 뜻과 문맥에 맞는 AI 설명을 확인합니다. 스캔 PDF는 먼저 OCR이 필요합니다.

## AI 설정

플러그인 설정의 **AI backend**에서 서비스를 고릅니다. OpenAI 또는 Anthropic은 본인의 API 키를 입력하며 사용료는 해당 업체에서 청구합니다. 로컬 **Codex / Claude Code**는 먼저 설치하고 로그인하세요. 찾지 못하면 **Codex command / Claude command** 경로를 지정하세요. 로컬 CLI도 내용을 AI 서비스로 전송할 수 있습니다.

기본 **Automatic · Economy**는 지원되는 경량 모델을 선택하고 한 시간 캐시하며 고가 모델로 자동 변경하지 않습니다. 특정 모델 또는 사용자 지정 API 주소는 **Manual**을 사용하세요. API는 **Test API connection**으로 확인할 수 있습니다.

## 노트로 저장

**Insert translation below selected text**는 원문 아래에 번역을 넣습니다. Markdown 전체는 끝에 추가하거나 원문과 번역을 번갈아 배치할 수 있고, 여러 파일을 일괄 번역할 수 있습니다. 노트를 수정하므로 먼저 복사본에서 시험하세요.

**Save selected text to excerpt note**로 발췌하고 **Excerpt file**에서 저장 위치를 정합니다. 번역 포함과 저장 후 열기도 설정할 수 있습니다. **Read selected text aloud**로 읽어 줍니다.

## 개인정보와 문제 해결

선택 텍스트와 문맥, 전체 번역 시 문서 조각이 AI로 전송됩니다. 기본 사전/번역 조회는 AI와 별도로 Google에 연결할 수 있습니다. 명령만 사용하려면 **Auto translate selection**을 끄세요. 반응이 없으면 수정 키 설정 또는 명령 팔레트를 확인하세요. 긴 문서는 **Timeout / Batch chunk size**를 조절하세요.

API 키는 보관함 안의 플러그인 설정에 저장됩니다. 보관함 공유·동기화 시 설정을 보호하세요. AI 오류가 나면 서비스, 로그인/키, 모델을 확인하세요. 할당량과 네트워크 오류는 모델 변경을 유발하지 않습니다.

영상에는 [Video Player (AI integrated)](https://github.com/skye1349/obsidian-video-player-ai)를 사용하세요.

## 도움말

[GitHub Issues](https://github.com/skye1349/obsidian-ai-translator/issues)에 버전과 오류를 남겨 주세요. API 키나 개인 노트는 올리지 마세요.

로컬 AI 연동은 사용자 폴더의 CLI 모델 정보와 기존 로그인을 사용합니다. 도구를 자동 설치하지 않습니다.

[MIT License](LICENSE) · © 2026 Taoye
