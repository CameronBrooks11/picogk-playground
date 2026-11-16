# picogk-playground

<img src="peacock-logo.png" alt="Peacock logo" width="160" align="right">

A place for experimenting with [PicoGK](https://github.com/leap71/PicoGK), LEAP 71's
voxel-based geometry kernel for computational engineering, and the libraries built on it.

**Status: parked.** It runs one ShapeKernel example today. I plan to come back to it
for real work with PicoGK.

## What's here

| Path | What it is |
| --- | --- |
| `Program.cs` | The entry point: runs ShapeKernel's `BaseCylinderShowCase` at a 0.1 mm voxel size and writes its output to `out/`. A commented-out block runs PicoGK's `BooleanShowCase` instead. |
| `PicoGK/` | [leap71/PicoGK](https://github.com/leap71/PicoGK), the geometry kernel. |
| `ShapeKernel/` | [leap71/LEAP71_ShapeKernel](https://github.com/leap71/LEAP71_ShapeKernel), shapes and modulations on top of PicoGK. |
| `LatticeLibrary/` | [leap71/LEAP71_LatticeLibrary](https://github.com/leap71/LEAP71_LatticeLibrary), lattice structures. |
| `LEAP71_HelixHeatX/` | [leap71/LEAP71_HelixHeatX](https://github.com/leap71/LEAP71_HelixHeatX), a helical heat exchanger design. |
| `QuasiCrystals/` | [leap71/LEAP71_QuasiCrystals](https://github.com/leap71/LEAP71_QuasiCrystals), Penrose patterns and quasi-crystals. |

The five libraries are git submodules, each pinned to the commit it was tried at.

## Running it

You need the [.NET 8 SDK](https://dotnet.microsoft.com/download), and PicoGK's native
runtime for your platform (see PicoGK's README).

```sh
git clone --recurse-submodules https://github.com/CameronBrooks11/picogk-playground
cd picogk-playground
dotnet run
```

In a clone made without `--recurse-submodules`, run `git submodule update --init` first.
To try another example, point `PicoGK.Library.Go` in `Program.cs` at a different task.

The project and solution files are still named `Peacock-Engineering-Playground`, from the
repo's earlier name.

## Licence

[Apache-2.0](LICENSE), like the LEAP 71 libraries it uses. Each submodule carries its own
licence.
