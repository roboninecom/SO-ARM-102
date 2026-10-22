<!-- translation-navigation -->
[English](CLAUDE.md) · [Русский](../ru/CLAUDE.md) · [Español](../es/CLAUDE.md) · [Français](../fr/CLAUDE.md) · [Deutsch](../de/CLAUDE.md) · [Português (Brasil)](../pt-BR/CLAUDE.md) · [简体中文](../zh-CN/CLAUDE.md) · [日本語](../ja/CLAUDE.md) · [हिन्दी](../hi/CLAUDE.md) · [العربية](../ar/CLAUDE.md)

[English source](../../../CLAUDE.md)

[Documentation](README.md) · [Printing](docs/printing.md) · [BOM](docs/bom.md) · [Assembly](docs/assembly-guide.md) · [Specifications](docs/specifications.md) · [Models](models/README.md) · [Contributing](CONTRIBUTING.md) · [Licensing](LICENSING.md) · [Translations](docs/translations.md)

> English reference. Shared illustrations and the original PDF booklet are unchanged.
<!-- /translation-navigation -->

<!-- translated-content -->
<a id="claudemd"></a>
# CLAUDE.md

Guidance for Claude Code when working in this repository.

<a id="what-this-repository-is"></a>
## What this repository is

Open hardware: the SO-ARM 102 leader + follower robot arm by Robonine. There is no code.
Content is CAD (`models/step/`), print meshes (`models/stl/`), slicer projects (`models/3mf/`), docs (`docs/`) and images (`assets/`).

<a id="rules"></a>
## Rules

- `models/step/` is the source of truth. Every STEP has an STL with the same base name in the same sub-folder (`common/`, `follower/`, `leader/`).
- Part numbers (`SO102.02.xxx`, `RB9.01.06x.xxx`) appear in `docs/printing.md`, `docs/bom.md` and `docs/assembly-guide.md`. Renaming or adding a part means updating all three.
- The README summarises bom, printing and specifications on purpose. Keep the numbers consistent.
- Every new file must be covered by `REUSE.toml`. CI runs `pre-commit run --all-files`, including `reuse lint`.
- The file size limit is 5 MB, with a scoped exception for `models/3mf/SO102_leader.3mf`. The preview video is re-encoded to stay under the limit.
- Do not add a `Co-Authored-By: Claude` line to commits.
<!-- /translated-content -->
