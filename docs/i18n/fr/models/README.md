<!-- translation-navigation -->
[English](../../en/models/README.md) · [Русский](../../ru/models/README.md) · [Español](../../es/models/README.md) · [Français](README.md) · [Deutsch](../../de/models/README.md) · [Português (Brasil)](../../pt-BR/models/README.md) · [简体中文](../../zh-CN/models/README.md) · [日本語](../../ja/models/README.md) · [हिन्दी](../../hi/models/README.md) · [العربية](../../ar/models/README.md)

[Original anglais](../../../../models/README.md)

[Documentation](../README.md) · [Impression](../docs/printing.md) · [Composants](../docs/bom.md) · [Montage](../docs/assembly-guide.md) · [Caractéristiques](../docs/specifications.md) · [Modèles](README.md) · [Contribuer](../CONTRIBUTING.md) · [Licences](../LICENSING.md) · [Traductions](../docs/translations.md)

> Traduction intégrale du document. Les illustrations et le livret PDF original sont communs aux langues. Traduction assistée par IA, pas encore relue par des locuteurs natifs.
<!-- /translation-navigation -->

<!-- translated-content -->
<a id="3d-models"></a>
# Modèles 3D

| Dossier | Contenu |
|---|---|
| `3mf/` | Bambu Studio projets avec des configurations de plaques, d'orientation et de support sauvegardées |
| `stl/` | Maillages prêts à imprimer, binaire STL, millimètres |
| `step/` | Pièces et assemblages CAO |

Les dossiers `stl/` et `step/` utilisent la même division:

- `common/` — Pièces communes, dont les boîtiers de contrôleur.
- `follower/` — Pince parallèle et support de caméra.
- `leader/` — Poignée, gâchette et rotation du poignet.

<a id="3mf-slicer-projects"></a>
## 3MF projets de slicer

| Projet | Contenu | Profil de filament enregistré |
|---|---|---|
| [SO102_leader.3mf](../../../../models/3mf/SO102_leader.3mf) | Un bras robotique leader: pièces de bras robot, poignée, déclencheur, rouleau de poignet et boîtier | Bambu PETG-CF |
| [SO102_follower_arms.3mf](../../../../models/3mf/SO102_follower_arms.3mf) | Pièces de bras robotique d'un bras robotique | Fiberon PET-CF17 |
| [SO102_follower_gripper_base.3mf](../../../../models/3mf/SO102_follower_gripper_base.3mf) | Pince et base du suiveur; Pièces communes, dont les boîtiers de contrôleur | Bambu PETG-CF |

Ouvrez ces fichiers en tant que projets dans **Bambu Studio**pour conserver les paramètres enregistrés. Tous trois utilisent le profil de buse**Bambu Lab A1, 0.4 mm et une plaque **256 × 256 mm chacune. Sélectionnez votre imprimante, votre buse et votre filament avant de couper. Pour une petite plaque de construction d'imprimante 3D, divisez les pièces sur des plaques supplémentaires tout en préservant leurs orientations et leurs paramètres de support.

Pour un bras robotique leader + un bras robotique suiveur, imprimez les trois projets une fois. Les projets de bras robotiques incluent chacun les pièces communes pour un bras robotique. Il n'est pas nécessaire d'imprimer un ensemble commun séparé.

Les paramètres enregistrés et les aperçus de mise en page sont dans [docs/printing.md](../docs/printing.md#3mf-slicer-projects).

Les numéros de pièce, les quantités et les paramètres d'impression sont dans [docs/printing.md](../docs/printing.md).
<!-- /translated-content -->
