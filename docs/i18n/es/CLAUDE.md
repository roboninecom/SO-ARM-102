<!-- translation-navigation -->
[English](../en/CLAUDE.md) · [Русский](../ru/CLAUDE.md) · [Español](CLAUDE.md) · [Français](../fr/CLAUDE.md) · [Deutsch](../de/CLAUDE.md) · [Português (Brasil)](../pt-BR/CLAUDE.md) · [简体中文](../zh-CN/CLAUDE.md) · [日本語](../ja/CLAUDE.md) · [हिन्दी](../hi/CLAUDE.md) · [العربية](../ar/CLAUDE.md)

[Original en inglés](../../../CLAUDE.md)

[Documentación](README.md) · [Impresión](docs/printing.md) · [Materiales](docs/bom.md) · [Montaje](docs/assembly-guide.md) · [Especificaciones](docs/specifications.md) · [Modelos](models/README.md) · [Contribuir](CONTRIBUTING.md) · [Licencias](LICENSING.md) · [Traducciones](docs/translations.md)

> Traducción completa del documento. Las ilustraciones y el manual PDF original se comparten entre idiomas. Traducción realizada con ayuda de IA; aún no revisada por hablantes nativos.
<!-- /translation-navigation -->

<!-- translated-content -->
<a id="claudemd"></a>
# CLAUDE.md

Guía para Claude Code al trabajar en este repositorio.

<a id="what-this-repository-is"></a>
## Qué es este repositorio

Hardware abierto: el brazo robótico líder SO-ARM 102 + brazo robótico seguidor brazo robótico por Robonine. No hay código. El contenido es CAD (`models/step/`), mallas de impresión (`models/stl/`), proyectos slicer (`models/3mf/`), documentos (`docs/`) e imágenes (`assets/`).

<a id="rules"></a>
## Reglas

- `models/step/` es la fuente de verdad. Cada STEP tiene un STL con el mismo nombre base en la misma subcarpeta (`common/`, `follower/`, `leader/`).
- Los números de pieza (`SO102.02.xxx`, `RB9.01.06x.xxx`) aparecen en `docs/printing.md`, `docs/bom.md` y `docs/assembly-guide.md`.Cambiar el nombre o añadir una pieza significa actualizar las tres.
- El README resume bom, impresión y especificaciones a propósito. Mantenga los números consistentes.
- Cada nuevo archivo debe estar cubierto por `REUSE.toml`. CI ejecuta `pre-commit run --all-files`, incluyendo `reuse lint`.
- El límite de tamaño de archivo es 5 MB, con una excepción de ámbito para `models/3mf/SO102_leader.3mf`.El vídeo de vista previa se recodifica para mantenerse por debajo del límite.
- No añada una línea `Co-Authored-By: Claude` a los commits.
<!-- /translated-content -->
