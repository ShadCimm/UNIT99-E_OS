# Radio Station Setup

Pip-OS can play your own local audio files as named radio stations. Each station is a folder.

## Where to Put Radio Files

Primary location:

```text
Internal Storage/
  Music/
    PipCarRadio/
```

Fallback location:

```text
Internal Storage/
  Downloads/
    PipCarRadio/
```

Use `Music/PipCarRadio/` unless your device makes that difficult.

## Folder Structure

Each folder inside `PipCarRadio` becomes a station.

```text
Internal Storage/
  Music/
    PipCarRadio/
      Diamond_City_Radio/
        song_01.mp3
        song_02.ogg
        station.ini
      Nuka_World_Radio/
        track_01.flac
        track_02.mp3
      My_Custom_Station/
        intro.wav
        mix_01.m4a
```

Folder rules:

- The root folder must be named exactly `PipCarRadio`.
- Station folders may be up to 3 levels deep inside `PipCarRadio`.
- Folder names become station names.
- Underscores in folder names are shown as spaces.
- Duplicate station names from the fallback folder are ignored if already found in the primary folder.

## Supported Audio Files

Supported extensions:

- `.mp3`
- `.ogg`
- `.wav`
- `.flac`
- `.m4a`
- `.aac`

Other file types are ignored.

## Optional `station.ini`

Place a text file named exactly `station.ini` inside a station folder.

Example:

```ini
station_name=Diamond City Radio
ordered=false
```

Supported keys:

| Key | Purpose |
|---|---|
| `station_name` | Overrides the display name shown in Pip-OS |
| `ordered` | `true` plays alphabetically; `false` shuffles |

Notes:

- `[metadata]` style section headers are ignored, so they are optional.
- Lines starting with `;` are ignored as comments.
- If `ordered` is not set, the station shuffles.

## Refreshing Stations

Open the `RADIO` tab after adding stations. The app scans the folder the first time the Radio screen opens in a session.

If new files do not appear:

1. Confirm storage/media permissions are granted.
2. Confirm the folder is named `PipCarRadio`.
3. Fully close/reopen Pip-OS or reboot the head unit if the Radio screen has already cached the station list.

## External Music Player

The top station is always `EXTERNAL MUSIC PLAYER`. It controls the last external Android media app that had an active media session.

For best results:

1. Start playback once in your music app.
2. Return to Pip-OS.
3. Open `RADIO`.
4. Choose `EXTERNAL MUSIC PLAYER`.

Notification access is recommended so Pip-OS can read metadata and control the external session reliably.
