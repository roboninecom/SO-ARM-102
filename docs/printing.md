# Printing the parts

<!-- documentation-languages -->
[English](i18n/en/docs/printing.md) · [Русский](i18n/ru/docs/printing.md) · [Español](i18n/es/docs/printing.md) · [Français](i18n/fr/docs/printing.md) · [Deutsch](i18n/de/docs/printing.md) · [Português (Brasil)](i18n/pt-BR/docs/printing.md) · [简体中文](i18n/zh-CN/docs/printing.md) · [日本語](i18n/ja/docs/printing.md) · [हिन्दी](i18n/hi/docs/printing.md) · [العربية](i18n/ar/docs/printing.md)
<!-- /documentation-languages -->

Every printed part of the SO-ARM 102 kit is in [`../models/stl/`](../models/stl/).
The editable CAD sources with the same names are in [`../models/step/`](../models/step/).

- `common/` — Shared parts, including controller cases.
- `follower/` — Parallel gripper and camera mount.
- `leader/` — Handle, trigger and wrist roll.

All parts fit a 180 × 180 mm bed. The largest part, the base, is 160 × 112.5 mm.

![All printed parts of the kit](../assets/images/assembly/printed-parts.jpg)

## Material

| Where | Material | Why |
|---|---|---|
| Follower arm links and servo holders | PET-CF, annealed if possible | Stiffest and most heat-resistant option tested near warm servos |
| Follower gripper and base | PETG-CF | Tougher against knocks |
| Leader | PLA+ | Optimal cheap material |

The prototype was printed in **Fiberon PET-CF17**. In our filament tests, annealing cut PET-CF17
deflection after one hour at 65–70 °C from 3.4 mm to 0.3 mm. Annealing also makes the part more brittle,
so do not anneal parts that take impacts. Details:
[Choosing a filament for robotic arms](https://robonine.com/choosing-filament-for-robotic-arm-applications/).

## 3MF slicer projects

The [3MF projects](../models/README.md#3mf-slicer-projects) include saved part orientations,
plate layouts and support settings. Open them as projects in **Bambu Studio**, select your
printer and filament, then slice and review the support preview.

| Project | Saved filament profile | Layer height | Walls | Top / bottom layers | Infill | Weight | Time |
|---|---|---|:-:|:-:|---|:-:|:-:|
| [Follower arm links](../models/3mf/SO102.1.01_Follower_table_arm_links_PET-CF.3mf.3mf) | Fiberon PET-CF17 | 0.20 mm | 6 | 6 / 6 | 30 % cubic | 394 gr | 15,5 h |
| [Follower gripper and base](../models/3mf/SO102.2.01_Follower_table_base_PETG-CF.3mf) | Bambu PETG-CF | 0.20 mm | 6 | 6 / 6 | 30 % cubic | 287 gr | 14 h |
| [Leader](../models/3mf/SO102.3.01_Leader_table_PLA+.3mf) | Bambu PLA+ | 0.20 mm | 3 | 5 / 4 | 15 % gyroid | 457 gr | 23 h |

All three save a **Bambu Lab A1, 0.4 mm nozzle** profile on a **256 × 256 mm** bed.
Individual parts still fit a 180 × 180 mm bed, but the supplied layouts need to be split
across more plates for that size. Automatic tree supports are the global default;
some parts have support overrides, manual support settings or support blockers.

| Leader layout | Follower arm links | Follower gripper and base |
|:-:|:-:|:-:|
| ![Leader slicer layout](../assets/images/3d%20print/leader_3dprint_layout.png) | ![Follower arms](../assets/images/3d%20print/follower_3dprint_layout.png) | ![Follower gripper and base](../assets/images/3d%20print/gripper_3dprint.png) |

For the gripper gear and gear racks use 100 % infill.

**More infill makes the follower stiffer.** With 100 % infill on all links and 35 % on the base,
the gripper deflection under 300 g dropped from 3.4 mm to 2.34 mm. The cost is filament and time:
about 720 g and 27 h instead of 500 g and 21 h, gripper not included.
For the leader, keep the infill low. It only has to be light and quick to print.

**Orientation matters.** Upper arms print best tilted, so the surface
comes out clean and the thin section does not crack. Lay long parts so the layer lines run
along the length of the part.

## Part list

Quantities are for one complete kit: one follower and one leader.

### Common parts, both arms

| Part number | Name | Qty |
|---|---|:-:|
| SO102.02.010 | Base | 2 |
| SO102.02.020 | Base ring | 2 |
| SO102.02.030 | Base washer | 2 |
| SO102.02.040 | Bottom top plate | 2 |
| SO102.02.050 | Bottom ring | 2 |
| SO102.02.060 | Bottom servo holder | 2 |
| SO102.02.070 | Bottom arm | 4 |
| SO102.02.080 | Upper arm left | 2 |
| SO102.02.080-01 | Upper arm right | 2 |
| SO102.02.090 | Wrist holder | 2 |
| SO102.02.101 | Board holder | 2 |
| SO102.02.101-01 | Board cap | 2 |
| SO102.02.130 | Cable snap | 2 |

### Follower only

| Part number | Name | Qty |
|---|---|:-:|
| RB9.01.062.012 | Main frame (D6.1) | 1 |
| RB9.01.062.025 | Clamp (D6.1) | 2 |
| RB9.01.062.030 | Gear rack | 2 |
| RB9.01.062.040 | Gear for gripper | 1 |
| RB9.01.062.050 | Washer | 2 |
| RB9.01.062.075 | Camera holder | 1 |
| RB9.01.062.090 | Camera spacer | 1 |
| RB9.01.062.100 | Nail | 2 |

`(D6.1)` means the rod bores are sized for 6.1 mm. See the known issues in the main README if the gripper runs tight.

### Leader only

| Part number | Name | Qty |
|---|---|:-:|
| — | SO102 Handle | 1 |
| — | SO102 Trigger | 1 |
| — | SO102 Washer | 1 |
| — | SO102 Wrist roll | 1 |

## About the STL files

The STL files were exported from the STEP sources with a chord tolerance of 0.02 mm.
If you change a part, edit the STEP and export a new STL with the same name.
