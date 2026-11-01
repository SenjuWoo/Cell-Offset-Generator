<p align="center">
  <img src="assets/mark.svg" width="72" height="72" alt="Cell-Offset-Generator">
</p>

<div align="center">

# Cell-Offset-Generator

<p>
  <a href="https://github.com/SenjuWoo/Cell-Offset-Generator/actions/workflows/build.yml"><img src="https://github.com/SenjuWoo/Cell-Offset-Generator/actions/workflows/build.yml/badge.svg" alt="CI"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-GPL--3.0-8A7434?labelColor=0d1117" alt="GPL-3.0 License"></a>
  <a href="https://github.com/SenjuWoo/Cell-Offset-Generator/releases/latest"><img src="https://img.shields.io/github/v/release/SenjuWoo/Cell-Offset-Generator?label=release&color=8A7434&labelColor=0d1117" alt="latest release"></a>
</p>

</div>

Cell-offset table generator for Bethesda games. Speeds up ESP cell lookups by extending the OFST fast-path beyond masters — regenerates worldspace cell offset tables that tools like xEdit strip out.

> Fork of [1001Bits/Cell-Offset-Generator](https://github.com/1001Bits/Cell-Offset-Generator).

## Layout

| Directory | Game | Notes |
| --- | --- | --- |
| `Skyrim/` | Skyrim SE/AE | SKSE plugin, CMake presets (`vs2022-windows-vcpkg`, …), CommonLibVR submodule under `extern/` |
| `Fallout 4/` | Fallout 4 | F4SE variant |
| `Starfield/` | Starfield | SFSE variant |

## Building (Skyrim)

Requirements: Visual Studio 2022 (C++ workload), CMake 3.21+, vcpkg (`VCPKG_ROOT` set). Clone with submodules:

```powershell
git clone --recurse-submodules <this-repo>
cd Skyrim
cmake --preset vs2022-windows-vcpkg
cmake --build build --config Release
```

## License

See [LICENSE](LICENSE).
