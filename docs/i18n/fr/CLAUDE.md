<!-- translation-navigation -->
[English](../en/CLAUDE.md) · [Русский](../ru/CLAUDE.md) · [Español](../es/CLAUDE.md) · [Français](CLAUDE.md) · [Deutsch](../de/CLAUDE.md) · [Português (Brasil)](../pt-BR/CLAUDE.md) · [简体中文](../zh-CN/CLAUDE.md) · [日本語](../ja/CLAUDE.md) · [हिन्दी](../hi/CLAUDE.md) · [العربية](../ar/CLAUDE.md)

[Original anglais](../../../CLAUDE.md)

[Documentation](README.md) · [Impression](docs/printing.md) · [Composants](docs/bom.md) · [Montage](docs/assembly-guide.md) · [Caractéristiques](docs/specifications.md) · [Modèles](models/README.md) · [Contribuer](CONTRIBUTING.md) · [Licences](LICENSING.md) · [Traductions](docs/translations.md)

> Traduction intégrale du document. Les illustrations et le livret PDF original sont communs aux langues. Traduction assistée par IA, pas encore relue par des locuteurs natifs.
<!-- /translation-navigation -->

<!-- translated-content -->
<a id="claudemd"></a>
# CLAUDE.md

Conseils pour Claude Code lorsque vous travaillez dans ce dépôt.

<a id="what-this-repository-is"></a>
## Qu'est-ce que ce dépôt

Matériel ouvert: le SO-ARM 102 Bras robot leader + bras robot follower bras robot par RobonineIl n'y a pas de code. Le contenu est CAD (`models/step/`), imprimer des mailles (`models/stl/`), projets de trancheur (`models/3mf/`), docs (`docs/`) et images (`assets/`).

<a id="rules"></a>
## Règles

- `models/step/` est la source de vérité. Chaque STEP a un STL avec le même nom de base dans le même sous-dossier (`common/`, `follower/`, `leader/`).
- Les numéros de pièce (`SO102.02.xxx`, `RB9.01.06x.xxx`) apparaissent dans `docs/printing.md`, `docs/bom.md` et `docs/assembly-guide.md`.Renommer ou ajouter une pièce signifie mettre à jour les trois.
- Le README résume les informations sur le bom, l'impression et les spécifications. Gardez les nombres cohérents.
- Chaque nouveau fichier doit être couvert par `REUSE.toml`. CI exécute `pre-commit run --all-files`, y compris `reuse lint`.
- La limite de taille du fichier est 5 MB, avec une exception d'étendue pour `models/3mf/SO102_leader.3mf`.La vidéo d'aperçu est recodée pour rester sous la limite.
- Ne pas ajouter une ligne `Co-Authored-By: Claude` aux commits.
<!-- /translated-content -->
