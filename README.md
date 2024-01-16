# kwin-effect-hide-cursor

Hide mouse cursor on inactivity or typing.

Duration of inactivity and when hide on typing can be configured in `System Settings - Window Management - Desktop Effects`.

## Installation

Extract the following package into `/usr/lib/qt6/plugins/`:

## Build

```bash
cmake -B build -S . -DCMAKE_BUILD_TYPE=Release
cmake --build build
sudo cmake --install build
```
