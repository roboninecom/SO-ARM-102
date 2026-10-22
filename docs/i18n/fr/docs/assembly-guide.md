<!-- translation-navigation -->
[English](../../en/docs/assembly-guide.md) · [Русский](../../ru/docs/assembly-guide.md) · [Español](../../es/docs/assembly-guide.md) · [Français](assembly-guide.md) · [Deutsch](../../de/docs/assembly-guide.md) · [Português (Brasil)](../../pt-BR/docs/assembly-guide.md) · [简体中文](../../zh-CN/docs/assembly-guide.md) · [日本語](../../ja/docs/assembly-guide.md) · [हिन्दी](../../hi/docs/assembly-guide.md) · [العربية](../../ar/docs/assembly-guide.md)

[Original anglais](../../../assembly-guide.md)

[Documentation](../README.md) · [Impression](printing.md) · [Composants](bom.md) · [Montage](assembly-guide.md) · [Caractéristiques](specifications.md) · [Modèles](../models/README.md) · [Contribuer](../CONTRIBUTING.md) · [Licences](../LICENSING.md) · [Traductions](translations.md)

> Traduction intégrale du document. Les illustrations et le livret PDF original sont communs aux langues. Traduction assistée par IA, pas encore relue par des locuteurs natifs.
<!-- /translation-navigation -->

<!-- translated-content -->
<a id="assembly-guide"></a>
# Guide de montage

> Ancien guide : le livret et les illustrations montrent le matériel HAT précédent. La nomenclature et le guide d’impression v0.2.0 utilisent des Bus Servo Adapter sur les deux bras, des pièces de pince révisées et d’autres vis. Ne suivez pas les anciennes étapes de pince ou de contrôleur pour les pièces révisées ; le livret actualisé reste à publier.

Ce guide suit le livret imprimé [SO-ARM102_assembly_A5_v0.6.pdf](../../../SO-ARM102_assembly_A5_v0.6.pdf) page par page, imprimé sur A5 paysage si vous préférez du papier.

Avant de commencer :

- Imprimez toutes les pièces à partir de [printing.md](printing.md) et récupérez le matériel à partir de [bom.md](bom.md).
- Vous avez besoin des clés hexadécimales 1.5 mm (M2) et 2 mm (M3).
- Deux endroits dans l'ordre actuel sont mal placés, voir [Problèmes connus](../README.md#-known-issues) pour plus d'informations.

> ⚠️ **Le bras maître fonctionne sous 5 V, le bras suiveur sous 12 V.** Gardez leurs alimentations séparées.

![Outils et avertissement de tension](../../../../assets/images/assembly/tools-and-voltage.jpg)

<a id="order-of-work"></a>
## Ordre des opérations

<a id="reading-the-illustrations"></a>
### Lecture des illustrations

La vignette de la pièce et la quantité indiquent ce qui doit être ajouté. Le cercle numéroté représente l'étape d'assemblage, les points indiquent le progrès. Les numéros de pièces, les tailles des fixations et les ID des servomoteurs sont identiques dans toutes les langues.

<a id="assembly-sequence"></a>
### Séquence d'assemblage

1. Montez les cornes sur les servomoteurs.
2. Construisez le corps du bras robotique **deux fois**, une fois pour le bras robotique suiveur et une fois pour le bras robotique leader (étapes 1–11).
3. Construire la pince parallèle (étapes de pince 1–6).
4. Terminer le bras robotique suivant: pince, caméra, contrôleur (bras robotique suivant étapes 1-5).
5. Terminer le bras robotique du leader: poignée, déclencheur, contrôleur (bras robotique du leader étapes 1–4).

<a id="servo-ids"></a>
## Identifiants des servos

Réglez l'ID de chaque servomoteur avant qu'il ne passe dans le bras du robot.Les outils pour régler les ID et calibrer sont disponibles sur [lab.robonine.com](https://lab.robonine.com).

![Servo IDs](../../../../assets/images/assembly/servo-ids.jpg)

| ID | Articulation | Servo du suiveur | Servo du leader |
|:-:|---|---|---|
| 1 | Rotation de la base | STS3235 | STS3215 |
| 2 | Élévation de l’épaule | STS3250 | STS3215 |
| 3 | Flexion du coude | STS3250 | STS3215 |
| 4 | Flexion du poignet | STS3235 | STS3215 |
| 5 | Rotation du poignet | STS3215 | STS3215 |
| 6 | Pince / gâchette | STS3215 | STS3215 |

<a id="0-servo-horns"></a>
## 0. Servo klaxons

Montez une corne avec une vis M3 × 6 sur le servomoteur ID 1. Les servos ID 2, 3 et 4 reçoivent une corne des deux côtés.

Si vous ajoutez des joints toriques au bras du robot leader, placez-les maintenant entre le servomoteur et la corne.Si vous ne respectez pas cet ordre, l'anneau entre la coque du servomoteur et la corne risque de se coincer.

<a id="111-arm-body-follower-and-leader"></a>
## 1–11. Corps du bras, bras robotique suiveur et bras robotique leader

Répétez ces étapes pour les deux bras robotiques.

| Étape | Pièces | Fixations |
|:-:|---|---|
| 1 | SO102.02.060 Support de servomoteur inférieur, SO102.02.040 Plaque supérieure inférieure | Écrou 3 × M3×16, 3 × M3 |
| 2 | — | Écrou 3 × M3×16, 3 × M3 |
| 3 | Numéro de service 1 | 4 × M2×6 |
| 4 | SO102.02.020 Bague de base, roulement 6812, SO102.02.050 Anneau inférieur, SO102.02.010 Base | Écrou 6 × M3×16, 6 × M3 |
| 5 | SO102.02.030 Rondelle de base | 4 × M3×10, 6 × M3×16 |
| 6 | Servos ID 2 et ID 3, 2 × SO102.02.070 bras robot inférieur, 2 câbles courts, 1 câble long | 16 × M2×6 |
| 7 | Servo ID 4, SO102.02.080-01 bras robot supérieur droit, 1 câble court | 4 × M2×6 |
| 8 | SO102.02.080 Bras robot supérieur gauche, 2 × SO102.02.130 Mousqueton de câble | 4 × M2×6, 8 × M3×10 |
| 9 | Servo ID 5, SO102.02.090 Support de poignet, klaxon servomoteur | 1 × M3×6, 4 × 2×6 autotaraudeurs |
| 10 | 1 câble court | 8 × M3×10 |
| 11 | — | 8 × M3×10 |

| | | |
|:-:|:-:|:-:|
| ![Step 1](../../../../assets/images/assembly/steps/shared-01.jpg) | ![Step 2](../../../../assets/images/assembly/steps/shared-02.jpg) | ![Step 3](../../../../assets/images/assembly/steps/shared-03.jpg) |
| ![Step 4](../../../../assets/images/assembly/steps/shared-04.jpg) | ![Step 5](../../../../assets/images/assembly/steps/shared-05.jpg) | ![Step 6](../../../../assets/images/assembly/steps/shared-06.jpg) |
| ![Step 7](../../../../assets/images/assembly/steps/shared-07.jpg) | ![Step 8](../../../../assets/images/assembly/steps/shared-08.jpg) | ![Step 9](../../../../assets/images/assembly/steps/shared-09.jpg) |
| ![Step 10](../../../../assets/images/assembly/steps/shared-10.jpg) | ![Step 11](../../../../assets/images/assembly/steps/shared-11.jpg) |  |

Vérifiez que chaque câble de servomoteur atteigne le prochain joint avec un certain jeu avant de fermer le joint.

<a id="gripper-16-follower-only"></a>
## Pince 1–6, bras robotique suiveur uniquement

| Étape | Pièces | Fixations |
|:-:|---|---|
| 1 | RB9.01.062.040 Engrenage pour préhenseur sur le klaxon du servomoteur, servomoteur ID 6 | 4 × M3×4 vis de réglage, 1 × M3×6 |
| 2 | Pince 2 × RB9.01.062.024, crémaillère 2 × RB9.01.062.030, clou 2 × RB9.01.062.100 | — |
| 3 | 2 × tige Ø6 × 125 mm | — |
| 4 | RB9.01.062.011 Cadre principal, 2 × roulement MF106ZZ | 2 × M4×8 |
| 5 | Encliquetez les tiges dans le cadre principal | — |
| 6 | Poussez les pinces à leurs butées extérieures, insérez le servomoteur | 3 × 2×6 autotaraudeurs |

Serrez les vis de pression du côté du palonnier vers l'engrenage afin de ne laisser aucun jeu entre eux. Avant l'étape 6, placez le servo d'ID 6 en position minimale afin que la pince se ferme complètement et s'ouvre sur toute la course de 85 mm. Avant de refermer l'ensemble, faites coulisser les deux mâchoires à la main le long des tiges. Elles doivent se déplacer librement, sans coincer.

| | | |
|:-:|:-:|:-:|
| ![Gripper 1](../../../../assets/images/assembly/steps/gripper-01.jpg) | ![Gripper 2](../../../../assets/images/assembly/steps/gripper-02.jpg) | ![Gripper 3](../../../../assets/images/assembly/steps/gripper-03.jpg) |
| ![Gripper 4](../../../../assets/images/assembly/steps/gripper-04.jpg) | ![Gripper 5](../../../../assets/images/assembly/steps/gripper-05.jpg) | ![Gripper 6](../../../../assets/images/assembly/steps/gripper-06.jpg) |

<a id="follower-15"></a>
## Bras robotique de suivi 1–5

| Étape | Pièces | Fixations |
|:-:|---|---|
| 1 | RB9.01.062.075 Support pour appareil photo | 4 × M3×10 |
| 2 | Montage de la pince sur le poignet | 4 × 2×6 autotaraudeurs |
| 3 | RB9.01.062.090 Entretoise de caméra, caméra USB | Écrou 4 × M2×8, 4 × M2 |
| 4 | SO102.02.100 Bras robotique pour porte-cartes, Waveshare Bus Servo Driver HAT | Écrou 4 × M2×8, 4 × M2 |
| 5 | SO102.02.100-01 Bras robotique de suivi de chapeau de carte, câble long | — |

| | | |
|:-:|:-:|:-:|
| ![Suivant bras robotique 1](../../../../assets/images/assembly/steps/follower-01.jpg) | ![Suivant bras robotique 2](../../../../assets/images/assembly/steps/follower-02.jpg) | ![Suivant bras robotique 3](../../../../assets/images/assembly/steps/follower-03.jpg) |
| ![Suivant bras robotique 4](../../../../assets/images/assembly/steps/follower-04.jpg) | ![Suivant bras robotique 5](../../../../assets/images/assembly/steps/follower-05.jpg) |  |

<a id="leader-14"></a>
## Bras robotique de leader 1-4

| Étape | Pièces | Fixations |
|:-:|---|---|
| 1 | SO102 Poignée, SO102 Rouleau de poignet | 4 × M3×6, 1 × 2×6 autotaraudeurs |
| 2 | SO102 Déclencheur, servomoteur ID 6 | 4 × M3×6, 4 × 2×6 autotaraudeurs |
| 3 | SO102.02.110 Bras robotique de chef de porte-cartes, Waveshare Bus Servo Adapter | Écrou 4 × M2×8, 4 × M2 |
| 4 | SO102.02.110-01 Bras robotique de leader de chapeau de carte, câble long | — |

| | |
|:-:|:-:|
| ![Leader robot arm 1](../../../../assets/images/assembly/steps/leader-01.jpg) | ![Leader robot arm 2](../../../../assets/images/assembly/steps/leader-02.jpg) |
| ![Leader robot arm 3](../../../../assets/images/assembly/steps/leader-03.jpg) | ![Leader robot arm 4](../../../../assets/images/assembly/steps/leader-04.jpg) |

<a id="mounting-and-first-start"></a>
## Fixation et première mise en service

1. Fixez chaque base à la table avec deux pinces en C.
2. Branchez le contrôleur du bras suiveur à l'alimentation de 12 V et celui du bras maître à l'alimentation de 5 V.
3. Connectez les deux manettes à l'ordinateur avec USB-C.
4. Étalonnez les deux bras du robot et démarrez la téléopération sur [lab.robonine.com](https://lab.robonine.com), ou avec le flux de travail LeRobot SO-101.
<!-- /translated-content -->
