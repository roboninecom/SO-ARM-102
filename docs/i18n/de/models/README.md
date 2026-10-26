<!-- translation-navigation -->
[English](../../en/models/README.md) · [Русский](../../ru/models/README.md) · [Español](../../es/models/README.md) · [Français](../../fr/models/README.md) · [Deutsch](README.md) · [Português (Brasil)](../../pt-BR/models/README.md) · [简体中文](../../zh-CN/models/README.md) · [日本語](../../ja/models/README.md) · [हिन्दी](../../hi/models/README.md) · [العربية](../../ar/models/README.md)

[Englisches Original](../../../../models/README.md)

[Dokumentation](../README.md) · [Drucken](../docs/printing.md) · [Stückliste](../docs/bom.md) · [Montage](../docs/assembly-guide.md) · [Technische Daten](../docs/specifications.md) · [Modelle](README.md) · [Mitwirken](../CONTRIBUTING.md) · [Lizenzen](../LICENSING.md) · [Übersetzungen](../docs/translations.md)

> Vollständige Übersetzung des Dokuments. Abbildungen und die ursprüngliche PDF-Anleitung werden gemeinsam genutzt. Mit KI übersetzt; noch nicht von Muttersprachlern geprüft.
<!-- /translation-navigation -->

<!-- translated-content -->
<a id="3d-models"></a>
# 3D-Modelle

| Ordner | Inhalt |
|---|---|
| `3mf/` | Bambu Studio Projekte mit gespeicherten Plattenlayouts, Ausrichtung und Stützeinstellungen |
| `stl/` | Druckfertige Netze, binär STL, Millimeter |
| `step/` | CAD-Einzelteile und Baugruppen |

Die Ordner `stl/` und `step/` verwenden die gleiche Aufteilung:

- `common/` — Gemeinsame Teile einschließlich Controllergehäuse.
- `follower/` — Parallelgreifer und Kamerahalterung.
- `leader/` — Griff, Abzug und Handgelenkrotation.

<a id="3mf-slicer-projects"></a>
## 3MF Slicer-Projekte

| Projekt | Inhalt | Gespeichertes Filamentprofil |
|---|---|---|
| [SO102_leader.3mf](../../../../models/3mf/SO102_leader.3mf) | Ein Führer Roboterarm: Roboterarmteile, Griff, Abzug, Handgelenkrolle und Brettfall | Bambu PETG-CF |
| [SO102_follower_arms.3mf](../../../../models/3mf/SO102_follower_arms.3mf) | Roboterarmteile eines Anhängerroboterarms | Fiberon PET-CF17 |
| [SO102_follower_gripper_base.3mf](../../../../models/3mf/SO102_follower_gripper_base.3mf) | Greifer und Basis des Followers; Gemeinsame Teile einschließlich Controllergehäuse | Bambu PETG-CF |

Öffnen Sie diese Dateien als Projekte in **Bambu Studio**, um die gespeicherten Einstellungen beizubehalten. Alle drei verwenden das Düsenprofil **Bambu Lab A1, 0.4 mm und jeweils eine Platte **256 × 256 mm**. Wählen Sie vor dem Schneiden Drucker, Düse und Filament aus. Für eine kleinere 3D-Druckerbauplatte teilen Sie die Teile auf zusätzliche Platten auf, wobei ihre Orientierungen und Stützeinstellungen beibehalten werden.

Für einen Leader-Roboterarm + einen Follower-Roboterarm drucken Sie alle drei Projekte einmal aus. Die Roboterarmprojekte enthalten jeweils die gemeinsamen Teile für einen Roboterarm. Es ist nicht erforderlich, ein separates gemeinsames Set zu drucken.

Gespeicherte Einstellungen und Layout-Vorschauen sind in [docs/printing.md](../docs/printing.md#3mf-slicer-projects).

Teilenummern, Mengen und Druckeinstellungen finden Sie in [docs/printing.md](../docs/printing.md).

Drucken Sie die [Prüfplatte für Führungsstangen](../../../../models/stl/test/Gripper%20test%20plate%20star%20holes%206.0-6.3.STL) mit demselben Material und denselben Einstellungen wie die Greifbacken. Prüfen Sie die Bohrungen von 6.0–6.3 mm von groß nach klein auf leichtgängigen Sitz mit minimalem Spiel. Enthalten sind nur D6.1-Greifbacken; andere Ergebnisse erfordern vor dem Druck eine passende Version. Die Prüfplatte ist kein Bausatzteil.
<!-- /translated-content -->
