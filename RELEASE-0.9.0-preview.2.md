# CENTAURI 0.9.0-preview.2

A faster pitch response and a cleaner way to shape your sound.

- Fast Pitch (beta) uses a 384-sample active window: measured wet impulse delay
  of 8 ms at 48 kHz, versus the original Poly Pitch’s 42.7 ms. Device latency is
  additional. The owner tested and approved the Linux 8 ms candidate.
- Pitch defaults start at zero interval and zero Glide. Saved intervals/scenes
  remain unchanged. Short windows can thin low notes; bass and complex chord
  quality remain beta.
- AI chat, clear generation progress, eight-scene result cards and temporary
  audition. Gemini or pinned OpenRouter Nemotron Free with zero-price ceilings
  and no paid fallback. Your own key/internet and provider quota are required.
- Linux keys use the desktop Secret Service keyring. Android keys use Keystore.
  Windows is excluded from this release; its next native build is deferred.
- Android voice dictation appends text for review before Send. No spoken AI
  replies. Speech recognition uses the phone service, which can use internet;
  actual microphone recognition remains a device test.
- Cleaner inline trial status, compact MIDI settings and aligned four-column
  preset picker. Android has a compact landscape header and effect settings
  overlay. Desktop retains its parameter panel.
- OS includes the qualified touchpad/input support and visible USB boot choices.
  Headless, Stage Display and Full GUI remain available.

Windows is deliberately excluded from this update. Linux and Android are public preview downloads. The OS image is on GitHub with
a MEGA alternative. Windows remains a private preview, with no public Windows
updater asset. Never reinstall an existing OS just for this application update;
use a compatible update path and back up sounds first.

Validation and limits

Automated evidence is recorded with the release. Synthetic pitch measurements
are not physical round-trip latency. No broad Celeron/bass/GPU/thermal guarantee.
Linux candidate listening approval does not qualify every device/edition.
Live OpenRouter/Gemini generation quality remains untested with a release key.

## Downloads and setup

Get the correct edition at https://centauri.iceiy.com/downloads.html.
GitHub Releases is the primary host. CENTAURI OS also has a MEGA mirror.

### Linux standalone

Use the branded .run installer on an x86-64 Linux desktop. On Debian/Ubuntu the
runtime packages are python3-gi, gir1.2-gtk-3.0, gir1.2-webkit2-4.1, openssl and
ca-certificates. AI key storage additionally needs gir1.2-secret-1 and an unlocked
Secret Service desktop keyring, such as GNOME Keyring. Missing keyring support
does not disable the editor. Run the installer as your normal user.

Select the input/output devices and an appropriate buffer in Audio settings.
Use a compatible interface and its own headphone/output connection. Updates
preserve your preset collections and activation data. Settings → Updates verifies
the signed manifest and installer before offering installation/restart.

### Android companion

Android8 or later; this is a Bluetooth companion, not a phone guitar-audio engine.
Pair/connect to CENTAURI OS, then edit, browse supported catalog content, generate
a temporary AI preset or control scenes. The release uses the same signing
identity as the previous public APK and has versionCode21. It can update an
existing release-signed install in place. Debug-signed development installs may
need a separate migration; save settings first.

AI → key icon selects Gemini or OpenRouter Free only. A blank key field retains
that provider’s saved key. Credentials remain on the phone. A saved key is not
proof of provider access; quotas and free-endpoint capacity can still fail.
Voice dictation is Android-only; typed input remains available everywhere AI
is supported. No preset is automatically saved by generating or auditioning.

### CENTAURI OS

The compressed image is about106MB and expands to2,484,097,024 bytes. Compression
was verified by restoring and hashing the complete raw byte stream. Use a
compatible x86-64 UEFI computer with SSE4.2 and a USB of at least4GB. Intel
graphics are the initial GUI target; other hardware is not broadly qualified.

The USB boot menu offers the live modes, internal installation and compatible
installed-system update choices. All choices are visible. Installed systems use
a short hidden menu and CENTAURI logo; Esc reveals recovery choices.

- Headless: Android/foot-controller operation without the desktop graphics stack.
- Stage Display: native read-only display of preset/scenes.
- Full GUI: local editing with supported mouse, touchpad or touchscreen input.

Writing an image erases the selected USB. Internal installation erases the
selected target drive. Back up first and check the drive carefully. For an
existing compatible CENTAURI installation, use its update path rather than
erasing/reinstalling just for this application update. Wi-Fi management, a file
manager and a touch-only on-screen keyboard are not introduced in this release.

## Presets, licensing and data

All32 factory slots1A–8D remain protected, including the owner’s7D Live Variety.
Save your own sounds in Custom collections. One license covers one OS board and
one standalone computer, with the existing Safe/Permanent policy. Trial length
and current activation status appear in the app. Purchases are not offered by
this release repository. See https://centauri.iceiy.com/licensing.html.

Processing is local. AI requests contact your chosen provider; catalog downloads
contact TONE3000/storage providers; update downloads contact GitHub or MEGA.
Provider terms and availability apply independently of CENTAURI licensing.

## Integrity and third-party sources

SHA-256 lists, RSA signatures, the signed update manifest and a verification
summary accompany this release. Native apps verify the update trust key bundled
with them; do not replace that key with an untrusted download.

The OS third-party dependency/source bundle is unchanged from preview.1 and
remains linked on the downloads page. This update changes CENTAURI’s proprietary
application and bundled UI; it does not introduce a new OS third-party dependency.
The original application source is private. Bundled third-party notices retain
their own terms.

Guides: https://centauri.iceiy.com/learn.html
Documentation: https://centauri.iceiy.com/docs.html
Community: https://www.facebook.com/centaurimultifx/
