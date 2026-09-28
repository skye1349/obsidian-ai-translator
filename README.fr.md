# AI Translator

Comprenez le vocabulaire, traduisez des passages et gardez des notes bilingues dans Obsidian. Compatible avec Markdown et le texte sélectionnable des PDF.

[English](README.md) · [简体中文](README.zh-CN.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Español](README.es.md) · [Français](README.fr.md) · [Deutsch](README.de.md)

## Voir le plugin en action

Chaque GIF présente une fonction, avec des instructions en anglais, les clics mis en évidence et les raccourcis clavier.

[**Voir les 12 démonstrations**](docs/demos.md) · [Guide vidéo complet](https://github.com/skye1349/obsidian-ai-translator/releases/download/1.0.0/ai-translator-guide.mp4)

![Voir le plugin en action](https://github.com/skye1349/obsidian-ai-translator/releases/download/1.0.0/translate-passage.gif)

## Ce que vous pouvez faire

- Traduire mots et passages dans Markdown ou les PDF à texte sélectionnable.
- Comprendre le vocabulaire dans son contexte.
- Conserver l’original et insérer la traduction en dessous.
- Traduire un ou plusieurs Markdown, en ajout final ou en alternance.
- Rassembler extraits et traductions dans la note de votre choix.
- Écouter un texte avec langue et vitesse réglables.

## Installation

Nécessite Obsidian pour ordinateur 1.13.7 ou ultérieur. Le mobile n’est pas pris en charge.

1. Ouvrez **Paramètres → Modules complémentaires** et activez-les si nécessaire.
2. Cliquez sur **Parcourir (Browse)** et recherchez **AI Translator**.
3. Cliquez sur **Installer (Install)**, puis **Activer (Enable)**.
4. Ouvrez les paramètres du module pour choisir la langue et le service IA.

## Première traduction

1. Configurez l’IA et **Learning / target language**.
2. Sélectionnez un passage puis lancez **Translate selected text**.
3. Pour la fenêtre flottante, activez **Auto translate selection** et maintenez Command sur macOS ou Ctrl sur Windows/Linux pendant la sélection ; ce réglage est modifiable.
4. Sélectionnez un mot pour son sens et une explication IA en contexte. Les PDF scannés nécessitent un OCR préalable.

## Configurer l’IA

Choisissez **AI backend** dans les paramètres du module. OpenAI et Anthropic nécessitent votre propre clé API ; leur utilisation est facturée par le fournisseur. Pour **Codex / Claude Code** locaux, installez le logiciel et connectez-vous d’abord. Si nécessaire, indiquez son chemin dans **Codex command / Claude command**. Un CLI local peut aussi envoyer le contenu à son fournisseur IA.

Commencez avec **Automatic · Economy** : modèles légers pris en charge, choix conservé une heure, sans passage automatique au premium. Utilisez **Manual** pour fixer un modèle ou une URL API personnalisée. Vérifiez l’API avec **Test API connection**. Chaque module a ses propres réglages.

## Garder une note

**Insert translation below selected text** conserve l’original. Les commandes Markdown complet ajoutent la traduction à la fin ou alternent original et traduction ; le traitement par lot accepte plusieurs fichiers. Ces commandes modifient vos notes : essayez sur une copie.

Utilisez **Save selected text to excerpt note**, puis réglez **Excerpt file**, l’ajout de la traduction et l’ouverture après sauvegarde. **Read selected text aloud** utilise la langue et la vitesse choisies.

## Confidentialité et questions

La traduction envoie le texte et le contexte au fournisseur ; la traduction complète transmet des parties du document. La recherche de définition/traduction simple peut contacter Google séparément. Désactivez **Auto translate selection** pour utiliser uniquement les commandes. Sans résultat, vérifiez la touche requise. Pour les longs documents, ajustez **Timeout / Batch chunk size**.

Les clés API sont enregistrées dans les paramètres du module dans le coffre. Protégez-les lors du partage ou de la synchronisation. En cas d’erreur, vérifiez le fournisseur, l’authentification et le modèle. Les erreurs de quota ou de réseau ne changent pas le modèle.

Pour les vidéos, utilisez [Video Player (AI integrated)](https://github.com/skye1349/obsidian-video-player-ai). Ce module ne remplace pas l’ancien et n’importe pas ses réglages. Avec deux traducteurs actifs, désactivez une fenêtre automatique pour éviter les doublons.

## Aide

Signalez les problèmes dans [GitHub Issues](https://github.com/skye1349/obsidian-ai-translator/issues) avec la version et le message d’erreur, sans clé API ni note privée.

L’intégration IA locale lit le catalogue CLI et utilise la connexion existante du dossier utilisateur. Le module n’installe pas ces outils.

[MIT License](LICENSE) · © 2026 Taoye
