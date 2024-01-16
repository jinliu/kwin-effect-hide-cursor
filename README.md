# kwin-effect-hide-cursor

Hide mouse cursor on inactivity or typing.

Duration of inactivity and when hide on typing can be configured in `System Settings - Window Management - Desktop Effects`.

## Installation

Extract the following package into `/usr/lib/qt6/plugins/`:

KDE 6 RC1

https://github.com/jinliu/kwin-effect-hide-cursor/releases/download/v0.1/kwin-effect-hide-cursor-0.1.tar.gz

## Build

```bash
cmake -B build -S . -DCMAKE_BUILD_TYPE=Release
cmake --build build
sudo cmake --install build
```
