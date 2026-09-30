# Contributing

Thank you for helping improve SO-ARM 102.

## Report a problem

Open an issue and include:

- what you were building or printing, with the part number;
- printer, material and slicer settings for print problems;
- photos, if something does not fit.

Build reports are especially welcome, even when everything worked.

## Change a part

1. Edit the STEP file in `models/step/`.
2. Export a binary STL with the same name into `models/stl/`.
3. Update `docs/printing.md` and `docs/assembly-guide.md` if names, quantities or fasteners change.
4. Print and fit the part before opening a pull request, and say in the pull request what you tested.

## Licence of contributions

Your change is licensed under the licence that already covers the file.

| You are changing | Your contribution is licensed |
|---|---|
| CAD and meshes in `models/` | CERN-OHL-P-2.0 |
| Configuration and CI | Apache-2.0 |
| Documentation and images | CC BY 4.0 |

If a contribution contains material you did not create, say so in the pull request so it can be recorded in `NOTICE`.
New files must be covered by `REUSE.toml`. CI runs `reuse lint` and fails otherwise.
