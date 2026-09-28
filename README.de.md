# AI Translator

Verstehe Wörter im Kontext, übersetze Abschnitte und speichere zweisprachige Notizen in Obsidian. Unterstützt Markdown und auswählbaren PDF-Text.

[English](README.md) · [简体中文](README.zh-CN.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Español](README.es.md) · [Français](README.fr.md) · [Deutsch](README.de.md)

## Installation

Benötigt Obsidian für Desktop ab Version 1.13.7. Mobilgeräte werden nicht unterstützt.

Die Prüfung im Community-Verzeichnis steht noch aus. Verwende bis zur Freigabe die manuelle Installation.

Lade **main.js**, **manifest.json** und **styles.css** aus der [neuesten Version](https://github.com/skye1349/obsidian-ai-translator/releases/latest) herunter und lege sie unter `<vault>/.obsidian/plugins/ai-translator/` ab. Starte Obsidian neu und aktiviere **AI Translator** unter **Einstellungen → Community-Erweiterungen**. Nach der Freigabe kannst du **AI Translator** auch über Browse suchen und installieren.

## Erste Übersetzung

1. Richte KI und **Learning / target language** ein.
2. Markiere Text und starte **Translate selected text**.
3. Für das Popup aktiviere **Auto translate selection** und halte beim Markieren Command auf macOS oder Ctrl auf Windows/Linux. Die Voraussetzung lässt sich ändern.
4. Wähle ein Wort für seine Bedeutung und eine KI-Kontexterklärung. Gescannte PDFs benötigen vorher OCR.

## KI einrichten

Wähle **AI backend** in den Plugin-Einstellungen. OpenAI oder Anthropic benötigen deinen eigenen API-Schlüssel; die Nutzung wird vom Anbieter berechnet. Installiere lokale **Codex / Claude Code** zuerst und melde dich an. Falls nötig, gib den Pfad unter **Codex command / Claude command** an. Auch lokale CLIs können Inhalte an ihren KI-Anbieter senden.

Beginne mit **Automatic · Economy**: unterstützte leichte Modelle, eine Stunde Zwischenspeicherung und kein automatischer Wechsel zu Premium. Für ein bestimmtes Modell oder eigene API-Adressen nutze **Manual**. Prüfe die API mit **Test API connection**. Beide Plugins haben getrennte Einstellungen.

## Notizen behalten

**Insert translation below selected text** behält den Originaltext. Befehle für ganze Markdown-Dateien hängen die Übersetzung an oder wechseln Original und Übersetzung ab; mehrere Dateien lassen sich im Stapel verarbeiten. Dabei werden Notizen geändert: Probiere es zuerst mit einer Kopie.

Nutze **Save selected text to excerpt note** und stelle **Excerpt file**, Übersetzung im Auszug und Öffnen nach dem Speichern ein. **Read selected text aloud** liest mit gewählter Sprache und Geschwindigkeit vor.

## Datenschutz und Fragen

Übersetzung sendet Text und Kontext an den Anbieter; ganze Dokumente werden abschnittsweise gesendet. Einfache Wörterbuch-/Übersetzungsabfragen können separat Google kontaktieren. Deaktiviere **Auto translate selection** für reine Befehlsnutzung. Prüfe bei ausbleibender Reaktion die Modifikatortaste. Für lange Dokumente passe **Timeout / Batch chunk size** an.

API-Schlüssel werden in den Plugin-Einstellungen im Vault gespeichert. Schütze diese beim Teilen oder Synchronisieren. Prüfe bei KI-Fehlern Anbieter, Anmeldung und Modell. Kontingent- oder Netzwerkfehler lösen keinen Modellwechsel aus.

Für Videos nutze [Video Player (AI integrated)](https://github.com/skye1349/obsidian-video-player-ai). Dieses Plugin ersetzt das alte nicht und importiert keine Einstellungen. Bei zwei aktiven Übersetzern deaktiviere ein automatisches Popup gegen doppelte Antworten.

## Hilfe

Melde Probleme in [GitHub Issues](https://github.com/skye1349/obsidian-ai-translator/issues) mit Version und Fehlermeldung, aber ohne API-Schlüssel oder private Notizen.

Ausgewählte lokale Videos können außerhalb des Vaults liegen. Lokale KI-Anbindungen lesen den CLI-Modellkatalog und nutzen die vorhandene Anmeldung im Benutzerverzeichnis. Das Plugin installiert diese Werkzeuge nicht.

[MIT License](LICENSE) · © 2026 Taoye
