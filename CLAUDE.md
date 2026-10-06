# CLAUDE.md

Guidance for Claude Code when working in this repository.

## What this repository is

Open hardware: the SO-ARM 102 leader + follower robot arm by Robonine. There is no code.
Content is CAD (`models/step/`), print meshes (`models/stl/`), slicer projects (`models/3mf/`), docs (`docs/`) and images (`assets/`).

## Rules

- `models/step/` is the source of truth. Every STEP has an STL with the same base name in the same sub-folder (`common/`, `follower/`, `leader/`). `RB9.01.060.075 Camera holder` is the one STL without a STEP.
- Part numbers (`SO102.02.xxx`, `RB9.01.06x.xxx`) appear in `docs/printing.md`, `docs/bom.md` and `docs/assembly-guide.md`. Renaming or adding a part means updating all three.
- The README summarises bom, printing and specifications on purpose. Keep the numbers consistent.
- Every new file must be covered by `REUSE.toml`. CI runs `pre-commit run --all-files`, including `reuse lint`.
- The file size limit is 5 MB, with a scoped exception for `models/3mf/SO102_leader.3mf`. The preview video is re-encoded to stay under the limit.
- Do not add a `Co-Authored-By: Claude` line to commits.
