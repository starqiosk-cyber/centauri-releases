# CENTAURI 0.9.0-preview.1 — build your dream multi-FX rig

CENTAURI turns a compatible computer and audio interface into a guitar rig:
native audio processing, an amp/cab/effect editor, eight scenes per preset and
MIDI control. This is the first public preview, with a Linux installer, an Android Bluetooth companion and a separate three-mode OS image.

## Downloads

* Windows standalone: private preview, shared directly by the creator.
* [Linux x86-64 installer](https://github.com/starqiosk-cyber/centauri-releases/releases/download/v0.9.0-preview.1/CENTAURI-Setup-0.9.0-preview.1-linux-x86_64.run)
* [Android companion APK](https://github.com/starqiosk-cyber/centauri-releases/releases/download/v0.9.0-preview.1/CENTAURI-Remote-0.9.0-preview.1-release.apk)
* **[Get CENTAURI OS → official website](https://centauri.iceiy.com/downloads.html#os)**

OS image downloads, requirements and corresponding third-party sources are linked
from the website. This repository distributes releases and documentation; the
original CENTAURI application source is private. Portable ZIP builds are not the
public standalone distribution.

## Your computer. Your sound.

The editor provides three signal paths, up to 12 processing blocks per path and
36 total, with up to two amps and two cabinets. Native processing supports the
built-in models, supported NAM captures and cabinet IRs. The TONE3000 experience
stays inside the application for sign-in and catalog browsing; loading indicators
show when a request is in progress. Online AI-assisted preset drafting supports
auditioning before saving, using a supported provider account/API key.

The factory collection has 32 protected slots, 1A–8D, and 256 scenes. Create and
rename Custom collections to make your own banks. Blank collections include all
32 positions. Factory presets remain starting points that cannot be overwritten
through normal save/rename/delete commands.

**7D is the creator's owner-tuned Live Variety**, opening on Clean Dry. Its eight
scenes are Clean Dry, Boosted Clean Solo, Boosted Clean Cloud, Heavy Rhythm
Distortion, Heavy Lead Semi Warm, Heavy Lead Hall Warm, Heavy Lead Semi Warm Auto
Wah and Boosted Clean Solo Auto Wah. No external NAM/IR files are required.
Ambient Beta stays at 7A. Cloud and Shimmer retain their beta labels.

## A shared interface across editions

Portrait pedal-shaped effects, stronger borders, fixed processing positions,
compact small-window icons and Move/Copy to A/B/C simplify chain editing. Portrait
layouts keep the pedal shape and allow horizontal swiping. Landscape fits all
12 positions. Stage mode dims unselected scene colors so the active scene stands
out; the header remains black and uses CENTAURI's orange branding.

Settings group controls under General, Presets, Devices and About. Activation
status, trial awareness, online unlink, official website/Facebook links, compact
audio controls and confirmed destructive actions are included.

On Android, tapping the preset header in Stage mode opens a full-screen sliding
chooser. Portrait shows four square preset buttons per row with their slot and
name; landscape uses six. The companion controls the OS processor; Android does
not process the guitar audio. It can relay supported TONE3000 and license
requests using the phone's internet connection.

## Branded installers and built-in standalone updates

Windows installs for the current user and keeps application data under
`%LOCALAPPDATA%\GMFX`. It checks for WebView2 Runtime and provides its official
download when needed. Linux installs under `~/.local/opt/centauri`, adds an
application-menu entry and keeps presets/activation outside the program files.

Open Settings → Updates to check GitHub Releases. Update metadata is signed;
downloads must match the signed size and SHA-256. Save edits before installation.
Audio stops before setup opens, and the updated application can restart after
installation. The Windows installer is not Authenticode-signed in this preview.
Detached release signatures and checksums accompany the downloads.

## Activation without losing your sounds

Start the trial shown in the activation screen, or enter a code immediately in
Settings → License. The default trial is seven days. An administrator can change
the period for new trials, reset a synthetic/approved device trial or remove its
record. Changing the default does not alter existing trial expiry dates.

One activation code includes **one OS board and one standalone computer**, usable
at the same time. Standalone and OS Safe use signed seven-day offline permissions
and check at most once per day following successful verification. Offline/server
errors retain an existing valid permission. Expiry blocks new audio starts;
network failures do not cut off an existing performance.

OS Safe supports explicit lost/broken-device recovery. The old activation ends
on its next online check or when its remaining offline permission expires. OS
Permanent stays valid offline indefinitely; moving it requires online unlink
from the activated hardware. Lost/stolen Permanent hardware cannot be reset from
the website alone; its separate standalone entitlement remains available.
Read the [licensing policy](https://centauri.iceiy.com/licensing.html).

## CENTAURI OS: choose the interface your hardware needs

One installer offers Headless, native read-only Stage Display and Full GUI.
Headless is the default. Display-mode changes keep the supervised audio/MIDI
engine running. Installed boot uses the CENTAURI logo and a hidden recovery menu;
firmware vendor logos before the OS bootloader are outside CENTAURI's control.

Use an x86-64 UEFI computer with SSE4.2. Intel graphics are the initial target.
Writing a USB image or installing internally erases the chosen target: keep
backups and verify the drive. Do not erase an existing internal installation
just to try the preview. Full-system OTA migration, a Wi-Fi manager, a file
explorer and a touch-only keyboard are not included in this release.

## Requirements and qualification

* Windows 10/11 x86-64, WebView2 Runtime and a compatible audio interface/driver.
  WASAPI and installed compatible ASIO drivers are supported. CENTAURI has no
  hardware-brand allowlist. The legacy Behringer driver guard applies only to
  that driver's supported hardware.
* Linux x86-64, Python 3.12+, GTK 3, WebKitGTK 4.1 and OpenSSL 3. On Debian/Ubuntu:
  `python3-gi gir1.2-gtk-3.0 gir1.2-webkit2-4.1 openssl ca-certificates`.
* Android 8+ with Bluetooth/Nearby Devices permission. The release APK uses a new
  private publisher key; it cannot update an earlier debug-signed app in place.
  Back up app settings/API keys before manually replacing a development APK.

The creator built and tested Windows audio and its installer. Automated protocol,
collection, capacity, remote, native licensing, signed-update validation and
responsive UI checks cover the release candidates. Trial administration and OS/
standalone seat isolation were tested against synthetic backend records.

The OS is a public preview: service/display/installer VM checks are separate from
physical GPU, Bluetooth, touch, thermal, sustained audio and measured round-trip
latency qualification. No measured latency number is claimed. A complete live
signed-upgrade cycle on Windows remains to be qualified. Software licensing does
not make an administrator-controlled computer uncrackable; Secure Boot, TPM-backed
activation and verified-root protection are not configured.

The private Windows preview is the creator-built, audio-tested installer. The newest
native launch fix for the website/Facebook links is in the synced source for its
next rebuild; if those Settings links do not open, use the links on this page.

## Verify, learn and keep a backup

Compare each download's `.sha256` file before installing. The `.sig` files use
the accompanying public update key; built-in updaters verify signed metadata.
Back up presets before upgrades. Factory reset and unlink have confirmations;
uninstalling does not automatically erase personal sounds or unlink a license.

[Website](https://centauri.iceiy.com/) ·
[Downloads & checksums](https://centauri.iceiy.com/downloads.html) ·
[Tutorials](https://centauri.iceiy.com/learn.html) ·
[Documentation](https://centauri.iceiy.com/docs.html) ·
[Official Facebook](https://www.facebook.com/centaurimultifx/)

Third-party names belong to their owners. Downloaded captures/IRs have their own
licenses. Included open-source components retain their original notices and
source-availability obligations; see the bundled notices and OS source link.

OS downloads use GitHub Releases as the primary host, with a MEGA mirror on the official downloads page. Windows is a private preview shared directly by the creator.
