# Panda builds

Download mirror of the editor of the [Panda](https://github.com/toyship-studio/Panda) game engine.
This repository carries no source code: the release workflow of the engine publishes every build
here and to the object storage of pandaengine.dev. Nothing is committed by hand.

## Download

The `preview` channel is rolling: the release [preview](../../releases/tag/preview) always holds the
newest build and the one before it. Pick the file of your platform:

| Platform | File | Install |
| --- | --- | --- |
| macOS, Apple Silicon | `PandaEditor-<version>-macos-arm64.dmg` | open the image and drag Panda Editor to Applications |
| Windows 10 or newer, x86_64 | `PandaEditor-<version>-windows-x86_64.zip` | unpack anywhere and run `PandaEditor\PandaEditor.exe` |
| Linux, x86_64 (Ubuntu 22.04 or newer) | `PandaEditor-<version>-linux-x86_64.tar.gz` | unpack anywhere and run `PandaEditor/PandaEditor`; needs X11, OpenGL and GTK 3 |

The version is `0.1.0-preview.<build>`; the build number grows with every run of the workflow, and
the release notes name the commit of the engine the build was made from. The SDK for the scripts of
a project is inside every build.

## Manifest

`manifests/preview.json` describes the current build of the channel: version, build number, commit,
date, notes and the files with their size, SHA-256 and download addresses (the object storage first,
this repository second). The updater of the editor and the Download page of pandaengine.dev read it;
the raw address is
`https://raw.githubusercontent.com/toyship-studio/panda-builds/main/manifests/preview.json`.

## License

Panda is free and source-available under the Panda Engine License 1.0. The license and the
third-party notices are inside every build (`LICENSE.txt`, `THIRD_PARTY_NOTICES.txt`). Issues and
discussions live in the engine repository.
