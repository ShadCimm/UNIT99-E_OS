# Installation Guide


## Before You Install

Pip-OS is distributed as an APK, not through the Play Store. You need:

- An Android 8 or newer device.
- A landscape-capable head unit or tablet.
- Enough free storage for the APK, radio files, and any offline maps you add.
- Optional: GPS enabled for speed/map features.
- Optional: Bluetooth enabled and an already-paired ELM327 adapter for OBD-II.

## Install the APK

1. Download the latest `UNIT99-E_OS_*.apk` from the release page.
2. Copy it to the Android device using USB, SD card, browser download, cloud storage, or file transfer.
3. Open the APK with the device's file manager.
4. If Android blocks the install, choose `Settings` and enable `Install unknown apps` for that file manager or browser.
5. Go back to the APK and tap `Install`.
6. Open Pip-OS after installation finishes.

## Set Pip-OS as the Home Launcher

For the intended car-launcher experience:

1. Press the Android Home button.
2. Select `Pip-OS` from the launcher choices.
3. Tap `Always`.

If Android does not ask, open Android settings and look for:

`Settings > Apps > Default apps > Home app`

Then choose `Pip-OS`.

## Optional: Install PipBooter for Boot Startup

Some generic Android head units do not open the selected Home launcher after boot. Instead, they restore the last-used app. If your unit has a setting that launches a navigation app or startup app when the unit boots, you can use `PipBooter.apk` as a helper.

PipBooter is a launcher for the launcher. When opened, it acts like the Android Home button was pressed. If `Pip-OS` is already set as the default Home app, PipBooter causes Android to open Pip-OS.

Setup:

1. Install `pipOS_*.apk`.
2. Set `Pip-OS` as the default Home app.
3. Install `PipBooter.apk`.
4. Open your head unit's settings.
5. Find the option for startup app, navigation app on boot, boot app, or similar.
6. Select `PipBooter`.
7. Reboot the head unit.

Expected boot chain:

```text
Head unit starts -> PipBooter opens -> Home is triggered -> Pip-OS opens
```

Do not set PipBooter as the default Home app. Pip-OS should stay as the default Home app.

See [PipBooter Setup](PIPBOOTER.md) for the full explanation.

## First Launch Checklist

On first launch, Android may request or open settings pages for several permissions. You do not need every permission for every feature, but these are the common setup choices:

- Allow location for GPS speed and maps.
- Allow audio/media file access for local radio stations.
- Allow all-files access if your Android version requires it for `PipCarRadio` folders and `station.ini`.
- Allow Bluetooth connect access for OBD-II.
- Enable notification access if you want external music metadata and controls.
- Enable accessibility only if you want the speed tap action to open Android Recents.
- Allow microphone only if you enable the live radio waveform visualizer.

See [Permissions Explained](PERMISSIONS.md) for the plain-English purpose of each permission.

## Recommended First Setup

1. Open `SET > DISPLAY` and choose your color theme.
2. Open `SET > HUD` and choose `MPH` or `KPH`.
3. Open `SET > MAP` and download or load your local map region.
4. Open `SET > APPS` and configure quick-launch shortcuts.
5. Open `SET > OBD-II` only if you use a Bluetooth ELM327 adapter.
6. Long-press either side of `DASH` to choose your preferred dashboard widgets.

## Updating

Install the newer APK over the older one. Android should keep your settings, map package records, station folders, and configured shortcuts.

If a new build behaves strangely after updating, fully close the app or reboot the device once. Some car head units keep launcher processes alive aggressively.
