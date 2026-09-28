# AI Translator

Entiende vocabulario, traduce pasajes y guarda notas bilingües dentro de Obsidian. Funciona con Markdown y texto seleccionable de PDF.

[English](README.md) · [简体中文](README.zh-CN.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Español](README.es.md) · [Français](README.fr.md) · [Deutsch](README.de.md)

## Mira cómo funciona

Cada GIF muestra una función con instrucciones en inglés, clics resaltados y atajos de teclado.

[**Ver las 12 demostraciones**](docs/demos.md) · [Guía completa en vídeo](https://github.com/skye1349/obsidian-ai-translator/releases/download/1.0.0/ai-translator-guide.mp4)

![Mira cómo funciona](https://github.com/skye1349/obsidian-ai-translator/releases/download/1.0.0/translate-passage.gif)

## Qué puedes hacer

- Traducir palabras y pasajes en Markdown o PDF con texto seleccionable.
- Entender vocabulario según el contexto.
- Conservar el original e insertar la traducción debajo.
- Traducir uno o varios archivos Markdown, al final o intercalando textos.
- Reunir extractos y traducciones en la nota que elijas.
- Escuchar texto con idioma y velocidad ajustables.

## Instalación

Requiere Obsidian de escritorio 1.13.7 o posterior. No admite dispositivos móviles.

1. Abre **Ajustes → Plugins de la comunidad** y actívalos si se solicita.
2. Pulsa **Explorar (Browse)** y busca **AI Translator**.
3. Pulsa **Instalar (Install)** y después **Activar (Enable)**.
4. Abre los ajustes del plugin para elegir idioma y servicio de IA.

## Tu primera traducción

1. Configura IA y **Learning / target language**.
2. Selecciona un pasaje y ejecuta **Translate selected text**.
3. Para el popup, activa **Auto translate selection** y mantén Command en macOS o Ctrl en Windows/Linux mientras seleccionas; puedes cambiarlo en ajustes.
4. Selecciona palabras para su significado y una explicación contextual con IA. Los PDF escaneados necesitan OCR primero.

## Configurar IA

En los ajustes del plugin, elige **AI backend**. Para OpenAI o Anthropic introduce tu propia clave API; el proveedor cobra el uso. Para **Codex / Claude Code** locales, instala e inicia sesión primero. Si no se detectan, indica la ruta en **Codex command / Claude command**. Un CLI local también puede enviar contenido a su proveedor de IA.

Empieza con **Automatic · Economy**: modelos ligeros admitidos, selección en caché durante una hora y sin salto automático a modelos premium. Elige **Manual** para un modelo concreto o una URL API personalizada. Usa **Test API connection** para comprobar la API.

## Guardar notas

**Insert translation below selected text** conserva el original. Los comandos de Markdown completo añaden la traducción al final o intercalan original y traducción; también hay lotes de varios archivos. Modifican tus notas: prueba primero sobre una copia.

Usa **Save selected text to excerpt note** y configura **Excerpt file**, si incluir la traducción y si abrir la nota después. **Read selected text aloud** lee con el idioma y velocidad elegidos.

## Privacidad y dudas

La traducción envía texto y contexto al proveedor; la traducción completa envía fragmentos del documento. La consulta básica de diccionario/traducción puede contactar Google por separado. Desactiva **Auto translate selection** para usar solo comandos. Si no responde, revisa la tecla modificadora. Para documentos largos ajusta **Timeout / Batch chunk size**.

Las claves API se guardan en los ajustes del plugin dentro de la bóveda. Protégelos al compartirla o sincronizarla. Si falla la IA, revisa el proveedor, la autenticación y el modelo. Los errores de cuota o red no cambian el modelo.

Para vídeo usa [Video Player (AI integrated)](https://github.com/skye1349/obsidian-video-player-ai).

## Ayuda

Informa en [GitHub Issues](https://github.com/skye1349/obsidian-ai-translator/issues) con la versión y el error. No incluyas claves API ni notas privadas.

Las integraciones IA locales leen el catálogo CLI y usan la sesión existente del directorio de usuario. El plugin no instala esas herramientas.

[MIT License](LICENSE) · © 2026 Taoye
