# Licensing

Copyright (c) 2026 Robonine

This project releases different kinds of material under different licences.
Every file in this repository is covered by exactly one of them.

| Material | Licence | Text |
|---|---|---|
| Hardware designs (CAD, manufacturable geometry) | CERN-OHL-P-2.0 | [`HARDWARE-LICENSE.txt`](HARDWARE-LICENSE.txt) |
| Software (configuration, CI) | Apache-2.0 | [`SOFTWARE-LICENSE.txt`](SOFTWARE-LICENSE.txt) |
| Documentation, renders and photographs | CC-BY-4.0 | [`DOCS-LICENSE.txt`](DOCS-LICENSE.txt) |

The machine-readable version of this map is [`REUSE.toml`](REUSE.toml).
`LICENSES/` holds the same three texts under their SPDX names, as the REUSE Specification requires.
The copies at the root are the ones GitHub's licence detection reads.

## 1. Hardware: CERN-OHL-P-2.0

```
models/step/    *.STEP
models/stl/     *.stl
```

`models/README.md` is documentation and falls under CC-BY-4.0.

Recommended notice when reusing this hardware:

```
Copyright (c) 2026 Robonine

This source describes Open Hardware and is licensed under the CERN-OHL-P v2.
You may redistribute and modify this source and make products using it under
the terms of the CERN-OHL-P v2 (https://ohwr.org/cern_ohl_p_v2.txt).

This source is distributed WITHOUT ANY EXPRESS OR IMPLIED WARRANTY, INCLUDING
OF MERCHANTABILITY, SATISFACTORY QUALITY AND FITNESS FOR A PARTICULAR PURPOSE.

SPDX-License-Identifier: CERN-OHL-P-2.0
```

## 2. Software: Apache-2.0

```
.github/    .pre-commit-config.yaml    .gitignore    .gitattributes
```

## 3. Documentation: CC-BY-4.0

```
README.md, CONTRIBUTING.md, LICENSING.md, CLAUDE.md, NOTICE
docs/             *.md, *.pdf
assets/images/    *.jpg
every other README.md in the repository
```

Attribution for reuse: "Robonine, SO-ARM 102, https://github.com/roboninecom/SO-ARM-102, CC BY 4.0".

## 4. Third-party material

No file in this repository is copied from a third party.
See [`NOTICE`](NOTICE) for the projects this design builds on.
