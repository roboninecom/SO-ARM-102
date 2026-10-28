<!-- translation-navigation -->
[English](../../en/models/README.md) · [Русский](../../ru/models/README.md) · [Español](../../es/models/README.md) · [Français](../../fr/models/README.md) · [Deutsch](../../de/models/README.md) · [Português (Brasil)](../../pt-BR/models/README.md) · [简体中文](README.md) · [日本語](../../ja/models/README.md) · [हिन्दी](../../hi/models/README.md) · [العربية](../../ar/models/README.md)

[英文原文](../../../../models/README.md)

[文档](../README.md) · [打印](../docs/printing.md) · [物料清单](../docs/bom.md) · [装配](../docs/assembly-guide.md) · [规格](../docs/specifications.md) · [模型](README.md) · [参与贡献](../CONTRIBUTING.md) · [许可说明](../LICENSING.md) · [翻译](../docs/translations.md)

> 本文为完整译文。各语言共用插图和原始 PDF 手册。翻译由人工智能辅助完成，尚未经母语使用者审校。
<!-- /translation-navigation -->

<!-- translated-content -->
<a id="3d-models"></a>
# 3D模型

| 文件夹 | 内容 |
|---|---|
| `3mf/` | Bambu Studio 项目已保存板材布局、方向和支撑设置 |
| `stl/` | 打印准备网格,二进制STL,毫米 |
| `step/` | CAD 零件和装配体 |

`stl/` 和 `step/` 文件夹使用相同的分割:

- `common/` — 共用零件，包括控制器外壳.
- `follower/` — 平行夹爪和相机支架.
- `leader/` — 手柄、扳机和腕部旋转件.

<a id="3mf-slicer-projects"></a>
## 3MF 切片器项目

| 项目 | 内容 | 保存的耗材配置 |
|---|---|---|
| [SO102_leader.3mf](../../../../models/3mf/SO102_leader.3mf) | 机器人臂:机器人臂部件,手柄,触发器,腕轮和板箱 | Bambu PETG-CF |
| [SO102_follower_arms.3mf](../../../../models/3mf/SO102_follower_arms.3mf) | 机器人手臂零部件 | Fiberon PET-CF17 |
| [SO102_follower_gripper_base.3mf](../../../../models/3mf/SO102_follower_gripper_base.3mf) | 从动臂夹爪与底座; 共用零件，包括控制器外壳 | Bambu PETG-CF |

将这些文件作为 **Bambu Studio**中的项目打开,以保留已保存的设置。 这三个文件都使用** Bambu Lab A1 、 0.4 mm喷嘴**配置文件和一个**256 × 256 mm** 板。 在切片之前选择您的打印机、喷嘴和丝材。

对于一个领导机器人手臂+一个跟随机器人手臂,打印三个项目一次。 机器人手臂项目每个都包含一个机器人手臂的共同部件,无需单独打印共同集合。

保存的设置和布局预览在 [docs/printing.md ](../docs/printing.md#3mf-slicer-projects) 中。

零件编号、数量和打印设置见[docs/printing.md ](../docs/printing.md) 。

使用与夹爪相同的材料和设置打印[导杆配合测试板](../../../../models/stl/test/Gripper%20test%20plate%20star%20holes%206.0-6.3.STL)。从大到小测试 6.0–6.3 mm 孔，选择滑动顺畅且间隙最小的尺寸。仓库目前仅提供 D6.1 夹爪；若测试结果不同，打印前需要相应尺寸的夹爪版本。测试板是检测工具，不是套件零件。
<!-- /translated-content -->
