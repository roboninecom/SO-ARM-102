<!-- translation-navigation -->
[English](../en/CLAUDE.md) · [Русский](CLAUDE.md) · [Español](../es/CLAUDE.md) · [Français](../fr/CLAUDE.md) · [Deutsch](../de/CLAUDE.md) · [Português (Brasil)](../pt-BR/CLAUDE.md) · [简体中文](../zh-CN/CLAUDE.md) · [日本語](../ja/CLAUDE.md) · [हिन्दी](../hi/CLAUDE.md) · [العربية](../ar/CLAUDE.md)

[Английский оригинал](../../../CLAUDE.md)

[Документация](README.md) · [Печать](docs/printing.md) · [Комплектующие](docs/bom.md) · [Сборка](docs/assembly-guide.md) · [Характеристики](docs/specifications.md) · [Модели](models/README.md) · [Участие](CONTRIBUTING.md) · [Лицензирование](LICENSING.md) · [Переводы](docs/translations.md)

> Полный перевод документа. Изображения и исходный PDF-буклет общие для всех языков. Перевод подготовлен с помощью ИИ; проверка носителями языка ещё не проведена.
<!-- /translation-navigation -->

<!-- translated-content -->
<a id="claudemd"></a>
# CLAUDE.md

Правила для Claude Code при работе с репозиторием.

<a id="what-this-repository-is"></a>
## О репозитории

Открытая аппаратная разработка: ведущая и ведомая роботизированные руки SO-ARM 102 от Robonine. Программного кода нет. Содержимое: CAD (`models/step/`), сетки для печати (`models/stl/`), проекты слайсера (`models/3mf/`), документы (`docs/`) и изображения (`assets/`).

<a id="rules"></a>
## Правила

- Источник истины — `models/step/`. Для каждого STEP есть STL с тем же базовым именем в соответствующей подпапке (`common/`, `follower/`, `leader/`).
- Номера деталей (`SO102.02.xxx`, `RB9.01.06x.xxx`) указаны в `docs/printing.md`, `docs/bom.md` и `docs/assembly-guide.md`. При переименовании или добавлении детали обновите все три документа.
- README намеренно кратко повторяет BOM, печать и характеристики. Числа должны совпадать.
- Каждый новый файл должен быть покрыт `REUSE.toml`. CI запускает `pre-commit run --all-files`, включая `reuse lint`.
- Ограничение размера файла — 5 MB, с отдельным исключением для `models/3mf/SO102_leader.3mf`. Видео перекодировано, чтобы уложиться в лимит.
- Не добавляйте в коммиты строку `Co-Authored-By: Claude`.
<!-- /translated-content -->
