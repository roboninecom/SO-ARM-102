<!-- translation-navigation -->
[English](../../en/docs/printing.md) · [Русский](../../ru/docs/printing.md) · [Español](../../es/docs/printing.md) · [Français](../../fr/docs/printing.md) · [Deutsch](printing.md) · [Português (Brasil)](../../pt-BR/docs/printing.md) · [简体中文](../../zh-CN/docs/printing.md) · [日本語](../../ja/docs/printing.md) · [हिन्दी](../../hi/docs/printing.md) · [العربية](../../ar/docs/printing.md)

[Englisches Original](../../../printing.md)

[Dokumentation](../README.md) · [Drucken](printing.md) · [Stückliste](bom.md) · [Montage](assembly-guide.md) · [Technische Daten](specifications.md) · [Modelle](../models/README.md) · [Mitwirken](../CONTRIBUTING.md) · [Lizenzen](../LICENSING.md) · [Übersetzungen](translations.md)

> Vollständige Übersetzung des Dokuments. Abbildungen und die ursprüngliche PDF-Anleitung werden gemeinsam genutzt. Mit KI übersetzt; noch nicht von Muttersprachlern geprüft.
<!-- /translation-navigation -->

<!-- translated-content -->
<a id="printing-the-parts"></a>
# Teile drucken

> Revision prüfen: Das Greifer-3MF bezeichnet die Klemmbacken als `RB9.01.062.024`, die aktuelle STEP/STL-Teileliste als `RB9.01.062.025`. Prüfen Sie die Geometrie vor dem Druck; die Namen allein belegen keinen Unterschied der Netze.

Jeder gedruckte Teil des SO-ARM 102-Baukastens ist in [`../models/stl/`](../../../../models/stl) Die editierbaren CAD Quellen mit den gleichen Namen sind in [`../models/step/`](../../../../models/step).

- `common/` — Gemeinsame Teile einschließlich Controllergehäuse.
- `follower/` — Parallelgreifer und Kamerahalterung.
- `leader/` — Griff, Abzug und Handgelenkrotation.

Alle Teile passen auf eine 180 × 180 mm 3D-Druckerbauplatte.Das größte Teil, die Basis, ist 160 × 112.5 mm.

![Alle gedruckten Teile des Bausatzes](../../../../assets/images/assembly/printed-parts.jpg)

<a id="material"></a>
## Material

| Einbauort | Material | Grund |
|---|---|---|
| Armglieder und Servohalter | PET-CF, wenn möglich geglüht | Steifste und hitzebeständigste Option, getestet in der Nähe von warmen Servomotoren |
| Greiferklemmen, Abdeckungen, Leiter Roboterarmgriff und Auslöser | PETG oder PET-CF | Härter gegen Stöße |

Der Prototyp wurde in **Fiberon PET-CF17** gedruckt. In unseren Filamenttests reduzierte das Glühen die PET-CF17-Ablenkung nach einer Stunde bei 65–70 °C von 3.4 mm auf 0.3 mm. Das Glühen macht das Teil auch brüchiger, daher sollten keine Teile geglüht werden, die Stöße empfangen. Details: [Auswahl eines Filament für Roboterroboterarme](https://robonine.com/choosing-filament-for-robotic-arm-applications/).

Der Roboterarm des Leaders trägt keine Last, PLA sollte also ausreichend sein, was noch nicht getestet wurde.

<a id="3mf-slicer-projects"></a>
## 3MF Slicer-Projekte

Die [3MF Projekte](../models/README.md#3mf-slicer-projects) enthalten gespeicherte Teileorientierungen, Plattenlayouts und Supporteinstellungen. Öffnen Sie sie als Projekte in **Bambu Studio**, wählen Sie Ihren Drucker und Filament aus, schneiden Sie dann und sehen Sie sich die Supportvorschau an.

| Projekt | Gespeichertes Filamentprofil | Schichthöhe | Wände | Obere / untere Schichten | Füllung | Gewicht | Dauer |
|---|---|---|:-:|:-:|---|:-:|:-:|
| [Leader-Arm](../../../../models/3mf/SO102_leader.3mf) | Bambu PETG-CF | 0.20 mm | 3 | 5 / 4 | 15 % Gyroid | 457 gr | 23 h |
| [Nachfolger Roboterarm](../../../../models/3mf/SO102_follower_arms.3mf) | Fiberon PET-CF17 | 0.20 mm | 6 | 6 / 6 | 30 % Kubik | 394 gr | 15,5 h |
| [Greifer und Basis des Followers](../../../../models/3mf/SO102_follower_gripper_base.3mf) | Bambu PETG-CF | 0.20 mm | 6 | 6 / 6 | 30 % Kubik | 287 gr | 14 h |

Mit diesen Einstellungen benötigen Sie: Fiberon PET-CF17 394 gr, Bambu PETG-CF 744 gr.

Alle drei speichern ein **Bambu Lab A1, 0.4 mm Düsenprofil**auf einer**256 × 256 mm** 3D-Druckerbauplatte. Einzelne Teile passen immer noch auf eine 180 × 180 mm 3D-Druckerbauplatte, aber die mitgelieferten Layouts müssen für diese Größe auf mehrere Platten aufgeteilt werden. Automatische Baum-Unterstützungen sind der globale Standard; einige Teile haben Unterstützungsüberschreibungen, manuelle Unterstützungseinstellungen oder Unterstützungsblocker.

| Leader Roboterarm-Layout | Follower-Arme | Greifer und Basis des Followers |
|:-:|:-:|:-:|
| ![Leader Roboterarm Schneidemaschine Layout](../../../../assets/images/3d%20print/leader_3dprint_layout.png) | ![Follower-Arme](../../../../assets/images/3d%20print/follower_3dprint_layout.png) | ![Greifer und Basis des Followers](../../../../assets/images/3d%20print/gripper_3dprint.png) |

<a id="test-arm-slicer-settings"></a>
## Test-Roboterarm Slicer Einstellungen

Dies sind die Einstellungen, mit denen die Test-Roboterarme gedruckt wurden. Die oben bereitgestellten 3MF Projekte verwenden unterschiedliche Profile. Schneiden Sie sie erneut mit dem 3D-Druck-Slicer auf, um Schätzungen für Filament und Druckzeit zu erhalten.

| Einstellung | Wert |
|---|---|
| Wände | 4 |
| Obere und untere Schichten | 4 |
| Füllung | 25 % Gyroid |
| Stützen | Ja, bei Bedarf |

Für das Greifergetriebe und die Zahnstangen 100 % Füllung verwenden.

**Mehr Füllung macht den Follower Roboterarm steifer.** Mit 100 % Füllung an allen Gliedern und 35 % auf der Basis sinkt die Greiferablenkung unter 300 g von 3.4 mm auf 2.34 mm. Die Kosten sind Filament und Zeit: etwa 720 g und 27 h statt 500 g und 21 h, Greifer nicht inbegriffen. Für den Leader Roboterarm halten Sie die Füllung niedrig. Es muss nur leicht und schnell zu drucken sein.

**Die Ausrichtung ist wichtig.** Die oberen Roboterarme drucken am besten geneigt, damit die Oberfläche sauber herauskommt und der dünne Abschnitt nicht reißt.Legen Sie lange Teile so auf, dass die Schichtlinien entlang der Länge des Teils verlaufen.

<a id="part-list"></a>
## Teileliste

Die Angaben beziehen sich auf ein komplettes Kit: einen Roboterarm und einen Leiterroboterarm.

<a id="common-parts-both-arms"></a>
### Gemeinsame Teile, beide Roboterarme

| Teilenummer | Name | Anzahl |
|---|---|:-:|
| SO102.02.010 | Basis | 2 |
| SO102.02.020 | Basisring | 2 |
| SO102.02.030 | Basisscheibe | 2 |
| SO102.02.040 | Obere Basisplatte | 2 |
| SO102.02.050 | Unterer Ring | 2 |
| SO102.02.060 | Unterer Servohalter | 2 |
| SO102.02.070 | Unterarmglied | 4 |
| SO102.02.080 | Oberarm links | 2 |
| SO102.02.080-01 | Oberarm rechts | 2 |
| SO102.02.090 | Handgelenkhalter | 2 |
| SO102.02.110 | Platinenhalter Leader | 2 |
| SO102.02.110-01 | Platinenabdeckung Leader | 2 |
| SO102.02.130 | Kabelclip | 4 |

<a id="follower-only"></a>
### Roboterarm nur für Nachfolger

| Teilenummer | Name | Anzahl |
|---|---|:-:|
| RB9.01.062.012 | Hauptrahmen (D6.1) | 1 |
| RB9.01.062.025 | Klemmbacke (D6.1) | 2 |
| RB9.01.062.030 | Zahnstange | 2 |
| RB9.01.062.040 | Greiferzahnrad | 1 |
| RB9.01.062.050 | Unterlegscheibe | 2 |
| RB9.01.062.100 | Stift | 2 |
| RB9.01.062.075 | Kamerahalter | 1 |
| RB9.01.062.090 | Kameraabstandshalter | 1 |

`(D6.1)` bedeutet, dass die Stangenbohrungen für 6.1 mm dimensioniert sind.Siehe die bekannten Probleme in der Haupt README, wenn der Greifer eng läuft.

<a id="leader-only"></a>
### Leader Roboterarm nur

| Teilenummer | Name | Anzahl |
|---|---|:-:|
| — | SO102-Handle | 1 |
| — | SO102 Trigger | 1 |
| — | SO102 Handgelenkrolle | 1 |

<a id="about-the-stl-files"></a>
## Über die STL-Dateien

Die STL Dateien wurden aus den STEP Quellen mit einer Akkordtoleranz von 0.02 mm exportiert.Wenn Sie einen Part ändern, bearbeiten Sie die STEP und exportieren eine neue STL mit dem gleichen Namen.
<!-- /translated-content -->
