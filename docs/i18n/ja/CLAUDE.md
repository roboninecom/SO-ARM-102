<!-- translation-navigation -->
[English](../en/CLAUDE.md) · [Русский](../ru/CLAUDE.md) · [Español](../es/CLAUDE.md) · [Français](../fr/CLAUDE.md) · [Deutsch](../de/CLAUDE.md) · [Português (Brasil)](../pt-BR/CLAUDE.md) · [简体中文](../zh-CN/CLAUDE.md) · [日本語](CLAUDE.md) · [हिन्दी](../hi/CLAUDE.md) · [العربية](../ar/CLAUDE.md)

[英語原文](../../../CLAUDE.md)

[ドキュメント](README.md) · [印刷](docs/printing.md) · [部品表](docs/bom.md) · [組立](docs/assembly-guide.md) · [仕様](docs/specifications.md) · [モデル](models/README.md) · [貢献方法](CONTRIBUTING.md) · [ライセンス](LICENSING.md) · [翻訳](docs/translations.md)

> この文書の全文翻訳です。図と元のPDF冊子は各言語で共用します。AIを使用した翻訳であり、母語話者による確認は未実施です。
<!-- /translation-navigation -->

<!-- translated-content -->
<a id="claudemd"></a>
# CLAUDE.md

このリポジトリで作業するときの Claude Code のガイドライン。

<a id="what-this-repository-is"></a>
## このリポジトリは何ですか

オープンハードウェア: SO-ARM 102 リーダーロボットアーム + Robonine によるフォローアームロボットアーム。コードはありません。内容は CAD (`models/step/`)、メッシュ印刷 (`models/stl/`)、スライサープロジェクト (`models/3mf/`)、ドキュメント (`docs/`)、画像 (`assets/`)です。

<a id="rules"></a>
## 規則

- `models/step/` は真実のソースです。STEP には同じサブフォルダ (`common/`, `follower/`, `leader/`) に同じベース名を持つ STL があります。
- パーツ番号 (`SO102.02.xxx`, `RB9.01.06x.xxx`) は `docs/printing.md`, `docs/bom.md`, `docs/assembly-guide.md` に表示されます。パーツの名前を変更するか追加すると、それらすべてがアップデートされます。
- README は目的に応じて bom、印刷および仕様をまとめています。数字を一貫させてください。
- 新しいファイルは必ず `REUSE.toml`. CIが走る `pre-commit run --all-files`それは `reuse lint`.
- ファイルサイズ制限は 5 MB で、`models/3mf/SO102_leader.3mf` に対してスコープ例外があります。プレビュービデオを再エンコーディングして制限以下にします。
- コミットに `Co-Authored-By: Claude` 行を追加しない。
<!-- /translated-content -->
