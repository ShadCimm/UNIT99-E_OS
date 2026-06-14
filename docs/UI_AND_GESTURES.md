# UI Sections and Gestures

Pip-OS has one persistent outer frame and five main sections: `DASH`, `RADIO`, `STATS`, `APPS`, and `SET`.


## Persistent UI

Top status bar:

- Vault-Tec logo at the left.
- Current time.
- Centered speed readout (GPS based).
- Optional CPU usage.
- Optional memory usage.
- Optional GPS indicator.
- Optional Bluetooth indicator.

Bottom navigation bar:

- `DASH`
- `RADIO`
- `STATS`
- `APPS`
- `SET`

Global background:

- Configurable Vault Boy watermark.
- Configurable Vault-Tec logo watermark.
- Configurable Vault-Tec name watermark.
- Optional scanlines and CRT effects.

## Global Gestures

| Gesture | Where | Result |
|---|---|---|
| Tap a bottom tab | Bottom navigation bar | Opens that section |
| Swipe left | Anywhere in main UI | Moves one section to the right |
| Swipe right | Anywhere in main UI | Moves one section to the left |
| Swipe left/right | Bottom navigation bar | Loops to previous/next tab |
| Press Android Home while already in Pip-OS | System Home button | Returns to `DASH` |
| Tap during boot | Boot screen | Skips boot animation |

## Top Status Bar Controls

| Element | Action | Result |
|---|---|---|
| Vault-Tec logo | Tap | Opens top-bar app shortcut menu |
| App shortcut in logo menu | Tap | Launches that configured app |
| Speed readout | Tap | Runs the configured speed tap action |

Speed tap actions:

- Show recent-app menu.
- Jump to last recent app.
- Open Android system Recents.
- Open Android Auto through `com.imotor.phoneconnect`.
- Open CarPlay through `com.imotor.phoneconnect`.

## DASH

UI elements:

- Left widget slot.
- Right widget slot.
- Center divider.
- Optional expanded map view.
- Widget picker overlay.

Gestures and controls:

| Gesture | Where | Result |
|---|---|---|
| Long press | Left widget slot | Opens picker for left slot |
| Long press | Right widget slot | Opens picker for right slot |
| Swipe up/down | A dashboard widget slot | Changes that slot to another widget |
| Double tap | A `MAP` widget slot | Expands the map to full dashboard area |
| Double tap | Expanded map | Returns map to normal split layout |
| Long press | Expanded map | Opens the widget picker for that map slot |
| Tap `NEAR/MID/FAR` | Map widget | Cycles map zoom preset |
| Tap media controls | Media widget | Previous, play/pause, next |
| Tap app shortcuts | Speedometer/media widget | Launches configured app |

## RADIO

UI elements:

- Station list on the left.
- `EXTERNAL MUSIC PLAYER` station.
- Waveform display on the right.
- Track title and artist.
- Previous, play/pause, and next controls.

Controls:

| Action | Result |
|---|---|
| Tap a station | Selects it and starts playback if it is a local station |
| Tap `EXTERNAL MUSIC PLAYER` | Stops local radio and resumes/controls the last external media app if available |
| Tap previous | Previous track, or restart current local track if more than 3 seconds in |
| Tap play/pause | Toggles playback |
| Tap next | Skips to next track |

## STATS

UI elements:

- Vehicle status header.
- Quick connect / linked / demo status control.
- Disconnect control when connected.
- OBD status indicator.
- Seven S.P.E.C.I.A.L.-style stat bars.
- Vehicle image.
- DTC trouble-code area.

Controls:

| Action | Result |
|---|---|
| Tap `QUICK CONNECT` | Connects to the saved OBD-II device |
| Tap `DISCONNECT` | Disconnects the OBD-II adapter |

## APPS

UI elements:

- Application count.
- Scrollable six-column app grid.
- App icons and labels.

Controls:

| Action | Result |
|---|---|
| Tap an app icon | Launches that app |
| Install/remove/update an app | Grid refreshes automatically |

## SET

UI elements:

- Category list on the left.
- Settings panel on the right.
- Toggles, sliders, buttons, region rows, and app pickers.

Controls:

| Action | Result |
|---|---|
| Tap a category | Opens that settings category |
| Tap a toggle | Enables/disables the feature |
| Drag a slider | Changes a numeric value |
| Tap a shortcut slot | Opens an app picker |
| Tap a map row | Makes that map region primary |
| Tap `GET` | Downloads a map package |
| Tap `LOAD` | Opens file picker for local map files |
| Tap `DEL` | Deletes an installed map package |
| Tap `FAV` | Adds/removes a map favorite |
