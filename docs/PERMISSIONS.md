# Permissions Explained

Pip-OS asks for broad permissions because it is a launcher, media controller, map viewer, radio player, and optional vehicle dashboard. You can deny permissions for features you do not use, but those features may not work.


## Location

Used for:

- GPS speedometer.
- Top-bar speed readout.
- GPS info widget.
- Current position on the offline map.
- Heading/course information when available.

Permissions:

- `ACCESS_FINE_LOCATION`
- `ACCESS_COARSE_LOCATION`
- `FOREGROUND_SERVICE_LOCATION`

Precise location is recommended because approximate location is not accurate enough for a driving speedometer.

## Storage and Media

Used for:

- Scanning `Music/PipCarRadio/` and `Downloads/PipCarRadio/`.
- Reading local audio files.
- Reading `station.ini` files.
- Loading map files selected by the user.

Permissions:

- `READ_EXTERNAL_STORAGE` on older Android versions.
- `WRITE_EXTERNAL_STORAGE` for legacy compatibility.
- `READ_MEDIA_AUDIO` on Android 13+.
- `READ_MEDIA_IMAGES` and `READ_MEDIA_VIDEO` may appear on some Android versions because the app declares media access.
- `MANAGE_EXTERNAL_STORAGE` may be requested on Android 11+ so the app can scan normal folders and read `station.ini` files.

## Internet and Network State

Used for:

- Downloading offline map packages from the in-app map catalog.
- Checking network availability.

Permissions:

- `INTERNET`
- `ACCESS_NETWORK_STATE`

Offline maps do not require internet after the package is downloaded or manually loaded.

## Bluetooth

Used for:

- Listing already-paired Bluetooth devices.
- Connecting to a selected ELM327 OBD-II adapter.
- Monitoring Bluetooth on/off state for the HUD.

Permissions:

- `BLUETOOTH` and `BLUETOOTH_ADMIN` on older Android versions.
- `BLUETOOTH_CONNECT` on Android 12+.
- `BLUETOOTH_SCAN` is declared for Bluetooth discovery compatibility, but the app expects you to pair the adapter in Android settings first.

## Microphone / Audio Capture

Used for:

- Optional live radio waveform visualizer.

Permission:

- `RECORD_AUDIO`

This is only needed when `SET > EFFECTS > LIVE RADIO WAVEFORM` is enabled. Without it, the radio screen still shows a synthetic waveform.

## Notification Access

Used for:

- Reading active Android media sessions.
- Showing external music app title, artist, and album art.
- Sending play/pause/next/previous commands to external media apps.

This is enabled through Android's notification listener settings, not a normal permission dialog.

## Accessibility

Used for:

- Opening Android Recents through the `OPEN SYSTEM RECENTS` speed tap action.

Service name:

- `Pip-OS System Recents Control`

The accessibility service does not inspect app content. It exists so Pip-OS can call Android's global Recents action.

## Usage Access

Used for:

- Showing the recent-app shortcut menu when tapping the top speed readout.
- Jumping to the last recently used app.

Permission:

- `PACKAGE_USAGE_STATS`

Android grants this from `Usage access` settings.

## Installed Apps Access

Used for:

- Building the `APPS` app drawer.
- Configuring shortcut slots.
- Launching selected apps.

Permission:

- `QUERY_ALL_PACKAGES`

This is a manifest-level Android permission. It normally does not appear as a runtime prompt.

## Startup and Foreground Services

Used for:

- Starting Pip-OS after device boot.
- Keeping the launcher active.
- Running GPS tracking while the launcher is active.

Permissions:

- `RECEIVE_BOOT_COMPLETED`
- `FOREGROUND_SERVICE`
- `FOREGROUND_SERVICE_SPECIAL_USE`

