<!-- translation-navigation -->
[English](../en/CLAUDE.md) · [Русский](../ru/CLAUDE.md) · [Español](../es/CLAUDE.md) · [Français](../fr/CLAUDE.md) · [Deutsch](../de/CLAUDE.md) · [Português (Brasil)](CLAUDE.md) · [简体中文](../zh-CN/CLAUDE.md) · [日本語](../ja/CLAUDE.md) · [हिन्दी](../hi/CLAUDE.md) · [العربية](../ar/CLAUDE.md)

[Original em inglês](../../../CLAUDE.md)

[Documentação](README.md) · [Impressão](docs/printing.md) · [Materiais](docs/bom.md) · [Montagem](docs/assembly-guide.md) · [Especificações](docs/specifications.md) · [Modelos](models/README.md) · [Contribuir](CONTRIBUTING.md) · [Licenças](LICENSING.md) · [Traduções](docs/translations.md)

> Tradução completa do documento. As ilustrações e o manual PDF original são compartilhados entre os idiomas. Tradução feita com auxílio de IA; ainda não revisada por falantes nativos.
<!-- /translation-navigation -->

<!-- translated-content -->
<a id="claudemd"></a>
# CLAUDE.md

Orientação para Claude Code ao trabalhar neste repositório.

<a id="what-this-repository-is"></a>
## O que é este repositório

Hardware aberto: o SO-ARM 102 braço robô líder + braço robô seguidor braço robô por Robonine. Não há código. Conteúdo é CAD (`models/step/`), malhas de impressão (`models/stl/`), projetos slicer (`models/3mf/`), documentos (`docs/`) e imagens (`assets/`).

<a id="rules"></a>
## Regras

- `models/step/` é a fonte da verdade. Cada STEP tem um STL com o mesmo nome de base na mesma subpasta (`common/`, `follower/`, `leader/`).
- Os números de peça (`SO102.02.xxx`, `RB9.01.06x.xxx`) aparecem em `docs/printing.md`, `docs/bom.md` e `docs/assembly-guide.md`.Renomear ou adicionar uma peça significa atualizar todos os três.
- O README resume bom, impressão e especificações de propósito. Mantenha os números consistentes.
- Cada novo arquivo deve ser coberto por `REUSE.toml`. CI executa `pre-commit run --all-files`, incluindo `reuse lint`.
- O limite de tamanho do arquivo é 5 MB, com uma exceção de escopo para `models/3mf/SO102_leader.3mf`.O vídeo de visualização é recodificado para permanecer abaixo do limite.
- Não adicione uma linha `Co-Authored-By: Claude` aos commits.
<!-- /translated-content -->
