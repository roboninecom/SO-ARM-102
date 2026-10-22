<!-- translation-navigation -->
[English](../../en/docs/printing.md) · [Русский](../../ru/docs/printing.md) · [Español](../../es/docs/printing.md) · [Français](../../fr/docs/printing.md) · [Deutsch](../../de/docs/printing.md) · [Português (Brasil)](../../pt-BR/docs/printing.md) · [简体中文](printing.md) · [日本語](../../ja/docs/printing.md) · [हिन्दी](../../hi/docs/printing.md) · [العربية](../../ar/docs/printing.md)

[英文原文](../../../printing.md)

[文档](../README.md) · [打印](printing.md) · [物料清单](bom.md) · [装配](assembly-guide.md) · [规格](specifications.md) · [模型](../models/README.md) · [参与贡献](../CONTRIBUTING.md) · [许可说明](../LICENSING.md) · [翻译](translations.md)

> 本文为完整译文。各语言共用插图和原始 PDF 手册。翻译由人工智能辅助完成，尚未经母语使用者审校。
<!-- /translation-navigation -->

<!-- translated-content -->
<a id="printing-the-parts"></a>
# 打印零件

> 版本检查：夹爪 3MF 将夹爪滑块标为 `RB9.01.062.024`，而当前 STEP/STL 零件清单使用 `RB9.01.062.025`。打印前请核对几何版本；仅凭名称不能确定网格是否不同。

SO-ARM 102套件的每个印刷部分都在[`../models/stl/` ](../../../../models/stl)中。 同名的可编辑源文件CAD位于[`../models/step/` ](../../../../models/step)中。

- `common/` — 共用零件，包括控制器外壳.
- `follower/` — 平行夹爪和相机支架.
- `leader/` — 手柄、扳机和腕部旋转件.

所有部件都适合 180 × 180 mm 3D 打印机建模板。 最大的部件,即底座,是 160 × 112.5 mm。

![套件的所有打印部件](../../../../assets/images/assembly/printed-parts.jpg)

<a id="material"></a>
## 材料

| 位置 | 材料 | 原因 |
|---|---|---|
| 机械臂连杆和舵机支架 | PET-CF，如有可能则退火 | 在温暖的伺服电机附近测试了最刚性和耐热的选项 |
| 抓具夹,盖子,领导机器人臂手柄和触发器 | PETG或PET-CF | 更坚固耐撞击 |

原型使用 **Fiberon PET-CF17** 打印。在我们的耗材测试中，PET-CF17 在 65–70 °C 下放置一小时后的挠度，经退火处理后从 3.4 mm 降至 0.3 mm。退火也会使零件更脆，因此不要对需要承受冲击的零件退火。详情：[为机械臂选择打印耗材](https://robonine.com/choosing-filament-for-robotic-arm-applications/)。

领导机器人手臂没有载荷,所以 PLA 应该足够。 这还没有被测试过。

<a id="3mf-slicer-projects"></a>
## 3MF 切片器项目

[3MF项目 ](../models/README.md#3mf-slicer-projects)包含保存的零件方向、板布局和支架设置。 在 **Bambu Studio** 中将其作为项目打开,选择您的打印机和纤维,然后切片并查看支架预览。

| 项目 | 保存的耗材配置 | 层高 | 壁数 | 顶层 / 底层 | 填充 | 重量 | 时间 |
|---|---|---|:-:|:-:|---|:-:|:-:|
| [主臂](../../../../models/3mf/SO102_leader.3mf) | Bambu PETG-CF | 0.20 mm | 3 | 5 / 4 | 15% 螺旋体 | 457 gr | 23 h |
| [追随者机器人臂](../../../../models/3mf/SO102_follower_arms.3mf) | Fiberon PET-CF17 | 0.20 mm | 6 | 6 / 6 | 30%立方米 | 394 gr | 15,5 h |
| [从动臂夹爪与底座](../../../../models/3mf/SO102_follower_gripper_base.3mf) | Bambu PETG-CF | 0.20 mm | 6 | 6 / 6 | 30%立方米 | 287 gr | 14 h |

使用这些设置,您将需要: Fiberon PET-CF17 394 gr, Bambu PETG-CF 744 gr。

所有三种方法都将 **Bambu Lab A1, 0.4 mm 喷嘴轮廓保存在 **256 × 256 mm ** 3D 打印机构造板上。 单个零件仍然适合 180 × 180 mm 3D 打印机构造板,但所提供的布局需要分割到多个板中以满足该尺寸。 自动树支撑是全局默认设置;某些零件具有支撑覆盖、手动支撑设置或支撑阻止器。

| Leader 机器人手臂布局 | 从动臂连杆 | 从动臂夹爪与底座 |
|:-:|:-:|:-:|
| ![机器人手臂切片机布局](../../../../assets/images/3d%20print/leader_3dprint_layout.png) | ![从动臂连杆](../../../../assets/images/3d%20print/follower_3dprint_layout.png) | ![从动臂夹爪与底座](../../../../assets/images/3d%20print/gripper_3dprint.png) |

<a id="test-arm-slicer-settings"></a>
## 测试机器人臂切片设置

这些是测试机器人手臂打印时的设置。 上面提供的 3MF 项目使用不同的配置文件;使用 3D 打印切片器再次切割它们,以获得纤维和打印时间估计值。

| 设置 | 值 |
|---|---|
| 壁数 | 4 |
| 顶层和底层 | 4 |
| 填充 | 25% 螺旋体 |
| 支撑 | 按需使用 |

对于夹具齿轮和齿条,使用 100 %的填充。

**更多的填充使跟随机器人臂更加刚性。** 在所有链条上填充 100 % , 在底座上填充 35 % , 300 g 下的抓具偏转从 3.4 mm 降至 2.34 mm。 成本是纤维和时间:约 720 g 和 27 h 而不是 500 g 和 21 h,不包括抓具。

**方向很重要。** 上部机器人臂打印最好倾斜,这样表面会干净出来,薄片不会裂开。 铺放长件时,层线应沿着零件的长度流动。

<a id="part-list"></a>
## 零件清单

数量为一个完整的套件:一个跟随机器人臂和一个领导机器人臂。

<a id="common-parts-both-arms"></a>
### 两个机器人臂的共同部件

| 零件编号 | 名称 | 数量 |
|---|---|:-:|
| SO102.02.010 | 底座 | 2 |
| SO102.02.020 | 底座环 | 2 |
| SO102.02.030 | 底座垫圈 | 2 |
| SO102.02.040 | 底座上板 | 2 |
| SO102.02.050 | 下环 | 2 |
| SO102.02.060 | 下部舵机支架 | 2 |
| SO102.02.070 | 下臂 | 4 |
| SO102.02.080 | 上臂左侧 | 2 |
| SO102.02.080-01 | 上臂右侧 | 2 |
| SO102.02.090 | 腕部支架 | 2 |
| SO102.02.110 | 主臂电路板支架 | 2 |
| SO102.02.110-01 | 主臂电路板盖 | 2 |
| SO102.02.130 | 线缆卡扣 | 4 |

<a id="follower-only"></a>
### 仅有跟踪机器人臂

| 零件编号 | 名称 | 数量 |
|---|---|:-:|
| RB9.01.062.012 | 主框架 (D6.1) | 1 |
| RB9.01.062.025 | 夹爪 (D6.1) | 2 |
| RB9.01.062.030 | 齿条 | 2 |
| RB9.01.062.040 | 夹爪齿轮 | 1 |
| RB9.01.062.050 | 垫圈 | 2 |
| RB9.01.062.100 | 销钉 | 2 |
| RB9.01.062.075 | 相机支架 | 1 |
| RB9.01.062.090 | 相机垫块 | 1 |

`(D6.1)` 表示杆孔尺寸为 6.1 mm。 如果夹持器运行紧凑,请参阅主 README 中的已知问题。

<a id="leader-only"></a>
### 仅 Leader 机器人臂

| 零件编号 | 名称 | 数量 |
|---|---|:-:|
| — | SO102手柄 | 1 |
| — | SO102触发器 | 1 |
| — | SO102 手腕滚动 | 1 |

<a id="about-the-stl-files"></a>
## 关于 STL 文件

STL 文件是从 STEP 源导出的,和弦公差为 0.02 mm。 如果您更改了一个部分,请编辑 STEP 并导出新的 STL,名称相同。
<!-- /translated-content -->
