<!-- translation-navigation -->
[English](../../en/docs/assembly-guide.md) · [Русский](../../ru/docs/assembly-guide.md) · [Español](../../es/docs/assembly-guide.md) · [Français](../../fr/docs/assembly-guide.md) · [Deutsch](assembly-guide.md) · [Português (Brasil)](../../pt-BR/docs/assembly-guide.md) · [简体中文](../../zh-CN/docs/assembly-guide.md) · [日本語](../../ja/docs/assembly-guide.md) · [हिन्दी](../../hi/docs/assembly-guide.md) · [العربية](../../ar/docs/assembly-guide.md)

[Englisches Original](../../../assembly-guide.md)

[Dokumentation](../README.md) · [Drucken](printing.md) · [Stückliste](bom.md) · [Montage](assembly-guide.md) · [Technische Daten](specifications.md) · [Modelle](../models/README.md) · [Mitwirken](../CONTRIBUTING.md) · [Lizenzen](../LICENSING.md) · [Übersetzungen](translations.md)

> Vollständige Übersetzung des Dokuments. Abbildungen und die ursprüngliche PDF-Anleitung werden gemeinsam genutzt. Mit KI übersetzt; noch nicht von Muttersprachlern geprüft.
<!-- /translation-navigation -->

<!-- translated-content -->
<a id="assembly-guide"></a>
# Montageanleitung

> Veraltete Anleitung: Heft und Abbildungen zeigen die frühere HAT-Hardware. Stückliste und Druckanleitung für v0.2.0 verwenden Bus Servo Adapter an beiden Armen, überarbeitete Greiferteile und andere Schrauben. Die alten Greifer- und Controller-Schritte gelten nicht für die überarbeiteten Teile; ein aktualisiertes Montageheft steht noch aus.

Diese Anleitung folgt der gedruckten Broschüre [SO-ARM102_assembly_A5_v0.6.pdf](../../../SO-ARM102_assembly_A5_v0.6.pdf) Seite für Seite und druckt die Broschüre auf A5 Querformat aus, wenn Sie Papier bevorzugen.

Vor dem Beginn:

- Drucken Sie alle Teile aus [printing.md](printing.md) und sammeln Sie die Hardware aus [bom.md](bom.md).
- Sie benötigen die Hex-Schlüssel 1.5 mm (M2) und 2 mm (M3).
- Lesen Sie zwei Schritte voraus, bevor Sie etwas festziehen. Zwei Stellen in der aktuellen Reihenfolge sind umständlich, siehe [Bekannte Probleme](../README.md#-known-issues).

> ⚠️ **Der Leader-Arm wird mit 5 V betrieben, der Follower-Arm mit 12 V.** Halten Sie die Netzteile getrennt.

![Werkzeug- und Spannungswarnung](../../../../assets/images/assembly/tools-and-voltage.jpg)

<a id="order-of-work"></a>
## Arbeitsreihenfolge

<a id="reading-the-illustrations"></a>
### Lesen der Illustrationen

Beigefarbene Markierungen kennzeichnen neue Teile, graue Teile sind bereits montiert. Das Teil-Thumbnail und die Menge zeigen, was hinzugefügt werden muss. Der nummerierte Kreis ist der Montageschritt, die Punkte zeigen den Fortschritt. Teilenummern, Verbindungsgrößen und Servomotor-IDs sind in allen Sprachen gleich.

<a id="assembly-sequence"></a>
### Montagereihenfolge

1. Montieren Sie die Hörner auf den Servomotoren.
2. Bauen Sie den Roboterarmkörper **zweimal**, einmal für den Nachfolgerroboterarm und einmal für den Anführerroboterarm (Schritte 1–11).
3. Bauen Sie den Parallelgreifer (Greiferschritte 1–6).
4. Fertigstellung des Follower-Roboterarms: Greifer, Kamera, Steuerung (Folger-Roboterarm Schritte 1–5).
5. Fertigstellung des Leiterroboterarms: Griff, Trigger, Controller (Leiterroboterarm Schritte 1–4).

<a id="servo-ids"></a>
## Servo-IDs

Stellen Sie die ID jedes Servomotors ein, bevor er in den Roboterarm gelangt. Tools zum Setzen von IDs und Kalibrieren finden Sie unter [lab.robonine.com](https://lab.robonine.com).

![Servo IDs](../../../../assets/images/assembly/servo-ids.jpg)

| ID | Gelenk | Follower-Servo | Leader-Servo |
|:-:|---|---|---|
| 1 | Basisdrehung | STS3235 | STS3215 |
| 2 | Schulterhub | STS3250 | STS3215 |
| 3 | Ellbogenbeugung | STS3250 | STS3215 |
| 4 | Handgelenkbeugung | STS3235 | STS3215 |
| 5 | Handgelenkrotation | STS3215 | STS3215 |
| 6 | Greifer / Abzug | STS3215 | STS3215 |

<a id="0-servo-horns"></a>
## 0. Servohörner

Ein Horn wird mit einer M3 × 6 Schraube am Servomotor ID 1 befestigt. Die Servos ID 2, 3 und 4 erhalten auf beiden Seiten ein Horn.

Wenn Sie O-Ringe an den Roboterarm des Leiters anbringen, setzen Sie sie jetzt zwischen Servomotor und Horn ein, da eine falsche Reihenfolge dazu führen kann, dass der Ring zwischen Servomotorgehäuse und Horn verklemmt.

<a id="111-arm-body-follower-and-leader"></a>
## 1–11. Armkörper, Roboterarm und Leiterroboterarm

Wiederholen Sie diese Schritte für beide Roboterarme.

| Schritt | Teile | Befestigungsmittel |
|:-:|---|---|
| 1 | SO102.02.060 Servomotorhalter unten, SO102.02.040 Bodenplatte oben | 3 × M3×16, 3 × M3 Mutter |
| 2 | — | 3 × M3×16, 3 × M3 Mutter |
| 3 | Servo ID 1 | 4 × M2×6 |
| 4 | SO102.02.020 Grundring, Lager 6812, SO102.02.050 Unterer Ring, SO102.02.010 Basis | 6 × M3×16, 6 × M3 Mutter |
| 5 | SO102.02.030 Unterlegscheibe | 4 × M3×10, 6 × M3×16 |
| 6 | Servos ID 2 und ID 3, 2 × SO102.02.070 Roboterarm unten, 2 kurze Kabel, 1 langes Kabel | 16 × M2×6 |
| 7 | Servo ID 4, SO102.02.080-01 Roboterarm oben rechts, 1 kurze Leitung | 4 × M2×6 |
| 8 | SO102.02.080 Oberer Roboterarm links, 2 × SO102.02.130 Kabelverschluss | 4 × M2×6, 8 × M3×10 |
| 9 | Servo ID 5, SO102.02.090 Handgelenkhalterung, Servomotorhorn | 1 × M3×6, 4 × 2×6 selbstschneidend |
| 10 | 1 Kurzes Kabel | 8 × M3×10 |
| 11 | — | 8 × M3×10 |

| | | |
|:-:|:-:|:-:|
| ![Schritt 1](../../../../assets/images/assembly/steps/shared-01.jpg) | ![Schritt 2](../../../../assets/images/assembly/steps/shared-02.jpg) | ![Schritt 3](../../../../assets/images/assembly/steps/shared-03.jpg) |
| ![Schritt 4](../../../../assets/images/assembly/steps/shared-04.jpg) | ![Schritt 5](../../../../assets/images/assembly/steps/shared-05.jpg) | ![Schritt 6](../../../../assets/images/assembly/steps/shared-06.jpg) |
| ![Schritt 7](../../../../assets/images/assembly/steps/shared-07.jpg) | ![Schritt 8](../../../../assets/images/assembly/steps/shared-08.jpg) | ![Schritt 9](../../../../assets/images/assembly/steps/shared-09.jpg) |
| ![Schritt 10](../../../../assets/images/assembly/steps/shared-10.jpg) | ![Schritt 11](../../../../assets/images/assembly/steps/shared-11.jpg) |  |

Prüfen Sie, ob jedes Servomotorkabel die nächste Verbindung mit etwas Spiel erreicht, bevor Sie die Verbindung schließen.

<a id="gripper-16-follower-only"></a>
## Greifer 1–6, nur Roboterarm

| Schritt | Teile | Befestigungsmittel |
|:-:|---|---|
| 1 | RB9.01.062.040 Getriebe für Greifer am Servomotorhorn, Servomotor ID 6 | 4 × M3×4 Stellschraube, 1 × M3×6 |
| 2 | 2 × RB9.01.062.024 Klammer, 2 × RB9.01.062.030 Zahnstange, 2 × RB9.01.062.100 Nagel | — |
| 3 | 2 × Stab Ø6 × 125 mm | — |
| 4 | RB9.01.062.011 Hauptrahmen, 2 × Lager MF106ZZ | 2 × M4×8 |
| 5 | Schnappen Sie die Stangen in den Hauptrahmen | — |
| 6 | Die Klemmen auf ihre äußeren Anschläge schieben, den Servomotor einsetzen | 3 × 2×6 selbstschneidend |

Ziehen Sie die Gewindestifte von der Seite des Servohorns in Richtung Zahnrad fest, damit dazwischen kein Spalt entsteht. Stellen Sie vor Schritt 6 den Servo mit ID 6 auf seine Minimalposition, damit der Greifer vollständig schließt und sich auf die vollen 85 mm öffnet. Schieben Sie beide Klemmbacken vor dem Schließen des Gehäuses von Hand entlang der Stangen. Sie müssen sich frei und ohne Verklemmen bewegen.

| | | |
|:-:|:-:|:-:|
| ![Gripper 1](../../../../assets/images/assembly/steps/gripper-01.jpg) | ![Gripper 2](../../../../assets/images/assembly/steps/gripper-02.jpg) | ![Gripper 3](../../../../assets/images/assembly/steps/gripper-03.jpg) |
| ![Gripper 4](../../../../assets/images/assembly/steps/gripper-04.jpg) | ![Gripper 5](../../../../assets/images/assembly/steps/gripper-05.jpg) | ![Gripper 6](../../../../assets/images/assembly/steps/gripper-06.jpg) |

<a id="follower-15"></a>
## Roboterarm mit Nachfolger 1–5

| Schritt | Teile | Befestigungsmittel |
|:-:|---|---|
| 1 | RB9.01.062.075 Kamerahalter | 4 × M3×10 |
| 2 | Greifermontage am Handgelenk | 4 × 2×6 selbstschneidend |
| 3 | RB9.01.062.090 Kamera-Abstandshalter, USB-Kamera | 4 × M2×8, 4 × M2 Mutter |
| 4 | SO102.02.100 Roboterarm für Bretthalter, Waveshare Bus Servo Driver HAT | 4 × M2×8, 4 × M2 Mutter |
| 5 | SO102.02.100-01 Board Cap Follower Roboterarm, langes Kabel | — |

| | | |
|:-:|:-:|:-:|
| ![Nachfolger Roboterarm 1](../../../../assets/images/assembly/steps/follower-01.jpg) | ![Nachfolger Roboterarm 2](../../../../assets/images/assembly/steps/follower-02.jpg) | ![Nachfolger Roboterarm 3](../../../../assets/images/assembly/steps/follower-03.jpg) |
| ![Nachfolger Roboterarm 4](../../../../assets/images/assembly/steps/follower-04.jpg) | ![Nachfolger Roboterarm 5](../../../../assets/images/assembly/steps/follower-05.jpg) |  |

<a id="leader-14"></a>
## Leader Roboterarm 1–4

| Schritt | Teile | Befestigungsmittel |
|:-:|---|---|
| 1 | SO102 Handgriff, SO102 Handgelenkrolle | 4 × M3×6, 1 × 2×6 selbstschneidend |
| 2 | SO102 Trigger, Servomotor ID 6 | 4 × M3×6, 4 × 2×6 selbstschneidend |
| 3 | SO102.02.110 Roboterarm für Leiterplattenhalter, Waveshare Bus Servo Adapter | 4 × M2×8, 4 × M2 Mutter |
| 4 | SO102.02.110-01 Board Cap Leader Roboterarm, langes Kabel | — |

| | |
|:-:|:-:|
| ![Anführer Roboterarm 1](../../../../assets/images/assembly/steps/leader-01.jpg) | ![Anführer Roboterarm 2](../../../../assets/images/assembly/steps/leader-02.jpg) |
| ![Anführer Roboterarm 3](../../../../assets/images/assembly/steps/leader-03.jpg) | ![Anführer Roboterarm 4](../../../../assets/images/assembly/steps/leader-04.jpg) |

<a id="mounting-and-first-start"></a>
## Befestigung und erste Inbetriebnahme

1. Klemmen Sie jede Basis mit zwei C-Klemmen an den Tisch.
2. Schließen Sie die Steuerung des Follower-Arms an das 12 V-Netzteil und die Steuerung des Leader-Arms an das 5 V-Netzteil an.
3. Verbinden Sie beide Controller mit USB-C mit dem Computer.
4. Kalibrieren Sie beide Roboterarme und starten Sie die Teleoperation unter [lab.robonine.com](https://lab.robonine.com) oder mit dem LeRobot SO-101-Workflow.
<!-- /translated-content -->
