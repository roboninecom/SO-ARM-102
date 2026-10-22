<!-- translation-navigation -->
[English](README.md) · [Русский](../../ru/models/README.md) · [Español](../../es/models/README.md) · [Français](../../fr/models/README.md) · [Deutsch](../../de/models/README.md) · [Português (Brasil)](../../pt-BR/models/README.md) · [简体中文](../../zh-CN/models/README.md) · [日本語](../../ja/models/README.md) · [हिन्दी](../../hi/models/README.md) · [العربية](../../ar/models/README.md)

[English source](../../../../models/README.md)

[Documentation](../README.md) · [Printing](../docs/printing.md) · [BOM](../docs/bom.md) · [Assembly](../docs/assembly-guide.md) · [Specifications](../docs/specifications.md) · [Models](README.md) · [Contributing](../CONTRIBUTING.md) · [Licensing](../LICENSING.md) · [Translations](../docs/translations.md)

> English reference. Shared illustrations and the original PDF booklet are unchanged.
<!-- /translation-navigation -->

<!-- translated-content -->
<a id="3d-models"></a>
# 3D models

| Folder | Content |
|---|---|
| `3mf/` | Bambu Studio projects with saved plate layouts, orientation and support settings |
| `stl/` | Print-ready meshes, binary STL, millimetres |
| `step/` | CAD parts and assemblies |

The `stl/` and `step/` folders use the same split:

- `common/` — Shared parts, including controller cases.
- `follower/` — Parallel gripper and camera mount.
- `leader/` — Handle, trigger and wrist roll.

<a id="3mf-slicer-projects"></a>
## 3MF slicer projects

| Project | Contents | Saved filament profile |
|---|---|---|
| [SO102_leader.3mf](../../../../models/3mf/SO102_leader.3mf) | One leader: arm parts, handle, trigger, wrist roll and board case | Bambu PETG-CF |
| [SO102_follower_arms.3mf](../../../../models/3mf/SO102_follower_arms.3mf) | One follower's arm parts | Fiberon PET-CF17 |
| [SO102_follower_gripper_base.3mf](../../../../models/3mf/SO102_follower_gripper_base.3mf) | Follower gripper and base; Shared parts, including controller cases | Bambu PETG-CF |

Open these files as projects in **Bambu Studio** to retain the saved settings.
All three use the **Bambu Lab A1, 0.4 mm nozzle** profile and one **256 × 256 mm** plate each.
Select your printer, nozzle and filament before slicing. For a smaller bed, split the parts
across additional plates while preserving their orientations and support settings.

For one leader + one follower, print all three projects once. The arm projects each include
the common parts for one arm; there is no need to print a separate common set.

Saved settings and layout previews are in [docs/printing.md](../docs/printing.md#3mf-slicer-projects).

Part numbers, quantities and print settings are in [docs/printing.md](../docs/printing.md).
<!-- /translated-content -->
