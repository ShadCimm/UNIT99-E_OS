# Feature Guide

## System and Launcher

- Replaces the Android Home launcher.
- Runs full-screen in landscape mode.
- Keeps the screen on while active.
- Starts a small foreground service so Android is less likely to kill the launcher.
- Can auto-open after device boot.
- Can return to the dashboard when Home is pressed while Pip-OS is already open.
- Can reappear on screen wake or supported ACC power-on broadcasts from some Rockchip head units.
- Optional `PipBooter` helper APK can be selected as a head-unit startup/navigation app to trigger Home and open Pip-OS on units that restore the last-used app instead of launching Home.

## Boot Experience

- Three-phase boot sequence: memory dump, PIP-OS system log, and Vault Boy/logo reveal.
- Boot sounds are synchronized with the animation.
- Tap anywhere during boot to skip to the main UI.
- `SET > DEV` includes a boot preloading toggle for slower devices (NOT RECOMMENDED EVEN ON SLOW DEVICES).

## DASH

The dashboard is split into left and right widget slots. Each slot can show a different widget.

Available widgets:

- `SPEEDOMETER`: GPS speed gauge with optional app shortcuts.
- `MEDIA PLAYER`: current track, album art, and media controls.
- `GPS INFO`: GPS fix, heading, coordinates, and radar-style visual.
- `MAP`: offline map and POI view.
- `TACHOMETER`: OBD-II RPM gauge.
- `COOLANT TEMP`: focused coolant temperature display.
- `OBD-II GAUGES`: compact RPM, coolant, voltage, and load gauges.
- `VAULT-TEC CLOCK`: branded live clock.
- `GEAR VAULT BOY`: speed-reactive Vault Boy display.
- `VAULT BOY PIP`: rotating Pip-Boy image slideshow.
- `BLANK`: empty slot.

## RADIO

- Plays local radio stations from folders on device storage.
- Adds an `EXTERNAL MUSIC PLAYER` station for controlling another Android media app.
- Shows track title, artist, station, waveform display, and playback buttons.
- Supports optional live waveform capture when enabled.
- Automatically stops local radio if an external app starts playing.
- Publishes Pip-OS radio playback as an Android media session.

## STATS

- S.P.E.C.I.A.L.-style vehicle status display.
- Shows live OBD-II values when connected:
- `S`: speed in KPH.
- `P`: power/RPM.
- `E`: engine coolant temperature.
- `C`: charge/voltage.
- `I`: intake air temperature.
- `A`: airflow/MAF.
- `L`: engine load.
-Global Geiger counter SFX for values exceeding thresholds set in `SET > STATS` 
- Shows diagnostic trouble codes after a DTC read.
- Includes quick connect and disconnect controls.
- Includes demo data mode under `SET > DEV`.

## APPS

- Full app drawer for installed launchable apps.
- Six-column grid layout.
- Tapping an app launches it.
- The app list refreshes when apps are installed, removed, changed, or updated.

## SET

Two-panel settings interface with categories:

- `DISPLAY`
- `MAP`
- `AUDIO`
- `HUD`
- `EFFECTS`
- `APPS`
- `OBD-II`
- `STATS`
- `DEV`
- `SYSTEM`
- `ABOUT`
