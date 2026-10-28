<!-- translation-navigation -->
[English](../../en/models/README.md) · [Русский](../../ru/models/README.md) · [Español](../../es/models/README.md) · [Français](../../fr/models/README.md) · [Deutsch](../../de/models/README.md) · [Português (Brasil)](../../pt-BR/models/README.md) · [简体中文](../../zh-CN/models/README.md) · [日本語](README.md) · [हिन्दी](../../hi/models/README.md) · [العربية](../../ar/models/README.md)

[英語原文](../../../../models/README.md)

[ドキュメント](../README.md) · [印刷](../docs/printing.md) · [部品表](../docs/bom.md) · [組立](../docs/assembly-guide.md) · [仕様](../docs/specifications.md) · [モデル](README.md) · [貢献方法](../CONTRIBUTING.md) · [ライセンス](../LICENSING.md) · [翻訳](../docs/translations.md)

> この文書の全文翻訳です。図と元のPDF冊子は各言語で共用します。AIを使用した翻訳であり、母語話者による確認は未実施です。
<!-- /translation-navigation -->

<!-- translated-content -->
<a id="3d-models"></a>
# 3Dモデル

| フォルダー | 内容 |
|---|---|
| `3mf/` | 保存されたプレートレイアウト、方向、サポート設定を持つプロジェクト Bambu Studio |
| `stl/` | 印刷可能なメッシュ、二進法 STL、ミリメートル |
| `step/` | CAD 部品とアセンブリ |

フォルダ `stl/` と `step/` は同じスプリットを使用しています:

- `common/` — コントローラーケースを含む共通部品.
- `follower/` — 平行グリッパーとカメラマウント.
- `leader/` — ハンドル、トリガー、手首回転部品.

<a id="3mf-slicer-projects"></a>
## 3MF スライサープロジェクト

| プロジェクト | 内容 | 保存済みフィラメントプロファイル |
|---|---|---|
| [SO102_leader.3mf](../../../../models/3mf/SO102_leader.3mf) | ワンリーダーロボットアーム：ロボットアーム部品，ハンドル，トリガー，手首ロール，ボードケース | Bambu PETG-CF |
| [SO102_follower_arms.3mf](../../../../models/3mf/SO102_follower_arms.3mf) | ワンフォローロボットアームのロボットアーム部分 | Fiberon PET-CF17 |
| [SO102_follower_gripper_base.3mf](../../../../models/3mf/SO102_follower_gripper_base.3mf) | フォロワーのグリッパーとベース; コントローラーケースを含む共通部品 | Bambu PETG-CF |

これらのファイルを **Bambu Studio**でプロジェクトとして開き、保存した設定を保持します。すべてのファイルは**Bambu Lab A1, 0.4 mm ノズルプロファイルと **256 × 256 mm** プレートを使用しています。スライスする前にプリンタ、ノズル、フィラメントを選択してください。小さな 3D プリンタビルドプレートの場合は、配向とサポート設定を保持しながら部品を追加のプレートに分割してください。

１つのリーダーロボットアームと１つのフォローアームに対して，３つのプロジェクトを一度に印刷する。ロボットアームプロジェクトはそれぞれ１つのロボットアームの共通部品を含み，別々の共通セットを印刷する必要はない。

保存された設定とレイアウトのプレビューは [docs/printing.md](../docs/printing.md#3mf-slicer-projects)にあります。

部品番号、数量、印刷設定は [docs/printing.md](../docs/printing.md).

クランプと同じ材料・設定で[ガイドロッドのはめあいテスト板](../../../../models/stl/test/Gripper%20test%20plate%20star%20holes%206.0-6.3.STL)を印刷してください。6.0–6.3 mm の穴を大きい順に試し、滑らかに動き、がたつきが最小になる寸法を選びます。このリポジトリには D6.1 クランプのみ含まれます。結果が異なる場合は、印刷前に対応するクランプ版が必要です。テスト板は確認用工具で、キット部品ではありません。
<!-- /translated-content -->
