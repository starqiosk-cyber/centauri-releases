# CENTAURI OS 0.9.0-preview.3

This OS-only preview adds the Full GUI tools requested for CENTAURI's dedicated appliance. Linux standalone and Android remain at their previously published preview versions. Windows is not part of this public release.

## What's new in CENTAURI OS

- Full GUI Settings includes the CENTAURI file manager. It browses CENTAURI data and mounted removable media, shows used/free capacity, and routes supported preset, WAV cabinet IR and NAM selections into the existing import screens. System directories are not exposed.
- Full GUI Settings → Devices includes Wi-Fi controls when the system detects a wireless adapter. The image enables common Intel and Realtek wireless drivers and firmware, including RTL8821CE, with scan/connect/disconnect/forget controls. Exact adapter and firmware support varies.
- Full GUI's Cage/libinput setup explicitly enables two-finger touchpad scrolling on devices that advertise that method. Tap-to-click and tap-drag are retained.
- The engine already uses the approved shared Fast Pitch 384-sample active window for new builds. Its 8 ms wet impulse delay at 48 kHz is a synthetic processing measurement, not complete input-to-output latency. Low-note, bass and complex-chord quality remains beta.
- Headless, Stage Display and Full GUI stay in one image. The matching Android companion remains preview.2 inside the image; this release does not update the companion APK.

## Updating

The existing installed-system update is still a matching-kernel application update booted from CENTAURI USB. It cannot update the kernel, wireless drivers or compositor. Full-system updates over the internet and a Bluetooth transfer fallback through Android are not implemented. The intended policy is OS internet update first, Android Bluetooth transfer only when the OS has no internet; a verified A/B boot/update flow is needed before either path can update an installed system safely.

Do not reinstall an existing installation just to update. Back up first. Use the USB update entry for a supported matching-kernel application update; otherwise wait for a full-system update path.

## Installation and limits

This raw x86-64 UEFI image is for a compatible computer with SSE4.2. Writing the image erases the selected USB. Internal installation erases the selected target drive. Read the installation guide and verify the target carefully.

VM and build checks do not certify a physical Wi-Fi adapter, laptop touchpad, audio latency, thermals, Bluetooth coexistence or every GPU. The update flow remains a preview and requires hardware qualification.

The image embeds the already released Android preview.2 companion. Get Linux standalone and Android downloads from the previous public release; Windows remains private and excluded.
