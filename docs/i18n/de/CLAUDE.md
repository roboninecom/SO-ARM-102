<!-- translation-navigation -->
[English](../en/CLAUDE.md) · [Русский](../ru/CLAUDE.md) · [Español](../es/CLAUDE.md) · [Français](../fr/CLAUDE.md) · [Deutsch](CLAUDE.md) · [Português (Brasil)](../pt-BR/CLAUDE.md) · [简体中文](../zh-CN/CLAUDE.md) · [日本語](../ja/CLAUDE.md) · [हिन्दी](../hi/CLAUDE.md) · [العربية](../ar/CLAUDE.md)

[Englisches Original](../../../CLAUDE.md)

[Dokumentation](README.md) · [Drucken](docs/printing.md) · [Stückliste](docs/bom.md) · [Montage](docs/assembly-guide.md) · [Technische Daten](docs/specifications.md) · [Modelle](models/README.md) · [Mitwirken](CONTRIBUTING.md) · [Lizenzen](LICENSING.md) · [Übersetzungen](docs/translations.md)

> Vollständige Übersetzung des Dokuments. Abbildungen und die ursprüngliche PDF-Anleitung werden gemeinsam genutzt. Mit KI übersetzt; noch nicht von Muttersprachlern geprüft.
<!-- /translation-navigation -->

<!-- translated-content -->
<a id="claudemd"></a>
# CLAUDE.md

Anleitung für Claude Code bei der Arbeit in diesem Repository.

<a id="what-this-repository-is"></a>
## Was dieses Repository ist

Open Hardware: der SO-ARM 102 Leader Roboterarm + Follower Roboterarm Roboterarm von Robonine. Es gibt keinen Code. Inhalt ist CAD (`models/step/`), Drucknetze (`models/stl/`), Slicer-Projekte (`models/3mf/`), Dokumente (`docs/`) und Bilder (`assets/`).

<a id="rules"></a>
## Regeln

- `models/step/` ist die Quelle der Wahrheit. Jedes STEP hat ein STL mit dem gleichen Basisnamen im selben Unterordner (`common/`, `follower/`, `leader/`).
- Teilenummern (`SO102.02.xxx`, `RB9.01.06x.xxx`) erscheinen in `docs/printing.md`, `docs/bom.md` und `docs/assembly-guide.md`.Wenn Sie ein Teil umbenennen oder hinzufügen, werden alle drei aktualisiert.
- Die README fasst Bom, Druck und Spezifikationen absichtlich zusammen. Halten Sie die Zahlen konsistent.
- Jede neue Datei muss von `REUSE.toml` abgedeckt werden. CI läuft `pre-commit run --all-files`, einschließlich `reuse lint`.
- Die Dateigrößenbeschränkung beträgt 5 MB, mit einer Ausnahme für `models/3mf/SO102_leader.3mf`.Das Vorschauvideo wird neu codiert, um unter der Begrenzung zu bleiben.
- Fügen Sie den Commits keine `Co-Authored-By: Claude`-Zeile hinzu.
<!-- /translated-content -->
