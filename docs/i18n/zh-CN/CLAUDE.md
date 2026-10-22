<!-- translation-navigation -->
[English](../en/CLAUDE.md) · [Русский](../ru/CLAUDE.md) · [Español](../es/CLAUDE.md) · [Français](../fr/CLAUDE.md) · [Deutsch](../de/CLAUDE.md) · [Português (Brasil)](../pt-BR/CLAUDE.md) · [简体中文](CLAUDE.md) · [日本語](../ja/CLAUDE.md) · [हिन्दी](../hi/CLAUDE.md) · [العربية](../ar/CLAUDE.md)

[英文原文](../../../CLAUDE.md)

[文档](README.md) · [打印](docs/printing.md) · [物料清单](docs/bom.md) · [装配](docs/assembly-guide.md) · [规格](docs/specifications.md) · [模型](models/README.md) · [参与贡献](CONTRIBUTING.md) · [许可说明](LICENSING.md) · [翻译](docs/translations.md)

> 本文为完整译文。各语言共用插图和原始 PDF 手册。翻译由人工智能辅助完成，尚未经母语使用者审校。
<!-- /translation-navigation -->

<!-- translated-content -->
<a id="claudemd"></a>
# CLAUDE.md

Claude Code 在此仓库工作时的指导。

<a id="what-this-repository-is"></a>
## 这个储存库是什么

开放硬件: SO-ARM 102 领导机器人臂 + Robonine 的跟随机器人臂 没有代码。 内容是 CAD (`models/step/`) 、 打印网格 (`models/stl/`) 、 切片项目 (`models/3mf/`) 、 文档 (`docs/`) 和图像 (`assets/`) 。

<a id="rules"></a>
## 规则

- `models/step/` 是真理的来源。 每个 STEP 在同一个子文件夹(`common/`, `follower/`, `leader/`)中都有一个具有相同基名的 STL 。
- 零件编号(`SO102.02.xxx`, `RB9.01.06x.xxx`)出现在 `docs/printing.md`、`docs/bom.md` 和 `docs/assembly-guide.md` 中。 重命名或添加一个零件意味着更新所有三个。
- README 总结了 bom、打印和规格的目的。 保持数字一致。
- 每个新文件必须由 `REUSE.toml` 覆盖。 CI 运行 `pre-commit run --all-files` , 包括 `reuse lint` 。
- 文件大小限制为 5 MB,对 `models/3mf/SO102_leader.3mf` 进行了范围异常处理。 预览视频将重新编码以保持在限制内。
- 不要在提交中添加 `Co-Authored-By: Claude` 行。
<!-- /translated-content -->
