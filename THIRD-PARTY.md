# Third-party components

## RtAudio ASIO host backend

RtAudio pinned revision `8ce4f2635a3b8f52687ec34625c8027e18024fe9`, from
https://github.com/thestk/rtaudio . RtAudio uses an MIT-style license; see its
`LICENSE` file. The bundled Steinberg interface sources in its `include/`
directory have separate ASIO SDK licensing requirements; see `asioinfo.txt`
and https://www.steinberg.net/developers/ . Local development does not select a
project-wide distribution license. No ASIO hardware driver is bundled.
The ASIO host sources require their applicable SDK license choice/agreement,
separately from any driver installed by an end user. A free preview does not by
itself settle those SDK requirements. Windows MIDI uses system WinRT APIs and no
external BLE driver.

## TONE3000 logo

`ui/assets/tone3000-logo.svg` and the corresponding PNG come from the official
integration logo pack at https://www.tone3000.com/TONE3000%20Logos.zip .
The artwork is unmodified and displayed on the library intro and library header.
TONE3000 retains ownership of its name and artwork; this does not imply a
commercial partnership or endorsement.

## NeuralAmpModelerCore 0.6.0

Native inference uses the official runtime at pinned commit
`0b3d3c97b0859a3a8c92a8628c4dd89a25eb5842` from
https://github.com/sdatkinson/NeuralAmpModelerCore . The runtime source is
unmodified; CENTAURI's wrapper lives in `engine/src/nam.cpp`.

- NAM: MIT, copyright Steven Atkinson; `licenses/NAM-MIT.txt` in desktop packages.
- Eigen: MPL 2.0 plus applicable per-file licenses; all upstream `COPYING*`
  files are included in `licenses/`. Unmodified source for the pinned Eigen
  revision is available at https://gitlab.com/libeigen/eigen/-/tree/bc3b39870ecb690a623a3f49149a358b95c5781d .
- nlohmann JSON 3.12.0: MIT, copyright Niels Lohmann; license included in `licenses/`.
- AudioDSPTools: MIT, copyright Steven Atkinson; pinned submodule revision
  `0827c6c2fc0deced568536142ea86f189e0b98a1`, source at
  https://github.com/sdatkinson/AudioDSPTools . License included in `licenses/`.

Downloaded NAM captures and IR files have their own creator licenses. They are
user assets and are not bundled as factory content. Upstream example models
are used for development tests only and are not shipped in the portable app.

## Microsoft WebView2 SDK 1.0.4314.35

The Windows desktop host uses WebView2 headers and distributes the x64 loader.
Audio processing does not run in WebView2.

- Official package: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.4314.35
- Package SHA-256: `90778deb1b77e36292828b4b5833c9255c27533f40e0ddd55891ae718944edc4`
- License: `engine/third_party/webview2/LICENSE.txt`, included as `WebView2-LICENSE.txt` in the portable desktop package.
- The Microsoft Edge WebView2 Runtime is a separate prerequisite, not bundled here.

## miniaudio 0.11.25

Native audio device I/O only; original CENTAURI DSP lives in `engine/src/dsp.cpp`.

- Source: https://github.com/mackron/miniaudio/tree/0.11.25
- Vendored file: `engine/third_party/miniaudio/miniaudio.h`
- SHA-256: `ac7af4de748b7e26b777f37e01cee313a308a7296a3eb080e2906b320cc55c89`
- License choice: MIT No Attribution. Full license text is included at the end of the header.

Copyright 2026 David Reid

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies
of the Software, and to permit persons to whom the Software is furnished to do
so.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Filter equations

The original biquad implementation follows the formulae in Robert Bristow-Johnson's
[Audio EQ Cookbook](https://www.w3.org/TR/audio-eq-cookbook/), published by W3C.

## PicoSHA2

PicoSHA2 by okdshin (MIT) supplies SHA-256 for Linux/headless OAuth PKCE.
Source and full license: engine/third_party/picosha2.h. Source URL and SHA-256
are recorded in engine/third_party/picosha2-source.txt.

## Optional CENTAURI OS graphical runtime

The unified OS preview adds Cage 0.2.0, wlroots 0.18.2 and seatd 0.9.1
(MIT); Mesa 24.0.9 (MIT, SGI and Khronos notices); GTK 3.24.51
(LGPL-2.0+); WebKitGTK 2.52.4 (LGPL-2.1+ and BSD notices); and DejaVu
2.37 fonts (Bitstream Vera and applicable DejaVu notices). These are
unmodified upstream packages selected through the pinned Buildroot tree.
Their dependencies retain their respective upstream licenses.

Audio remains in the native CENTAURI engine. Cage, GTK and WebKit are
separate runtime processes/libraries; the read-only Stage Display does not
load WebKit. Buildroot package recipes record exact source URLs, hashes and
license files. `make legal-info` in that Buildroot output directory generates
its license/source manifest for distribution preparation.
