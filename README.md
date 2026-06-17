<div align="center">
  <h1>UNIT 99-E OS</h1>
  <p><strong>Vault Maintenance Unit</strong></p>
</div>

Welcome to **Unit 99-E OS**, a custom, Fallout-inspired Android car launcher explicitly designed for tablets and aftermarket Android head units.

This launcher was designed and developed as the digital heart of the real-world [**Vault-Tec Hyundai Accent (Vault Maintenance Unit 99-E)**](https://www.reddit.com/r/Fallout/comments/1tp90gw/finally_took_my_custom_vaulttec_hyundai_accent/) project.

Optimized to run smoothly on low-end and budget dashboard hardware, this launcher brings the wasteland aesthetic directly to your vehicle without sacrificing system performance.

This repository is intended for APK releases and user documentation only.

## Quick Start

1. Download the latest APK from this repository's release page, or place release APKs in the `releases/` folder if you mirror them in git.
2. Install the APK on your Android device.
3. Set `Pip-OS` as your default Home app when Android asks.
4. If your head unit does not open the Home launcher at boot, install `PipBooter.apk` and select it as the unit's startup/navigation app. See [PipBooter Setup](docs/PIPBOOTER.md).
5. Grant the permissions needed for the features you plan to use. Important for media controls: open `SET > APPS` and grant notification access.
6. Optional: add local radio stations in `Music/PipCarRadio/`.
7. Optional: download or load offline maps from `SET > MAP`.
8. Optional: pair an ELM327 Bluetooth OBD-II adapter and select it in `SET > OBD-II`.

Pip-OS is designed for Android 10 or newer head units and tablets. It runs in landscape orientation.

## Main Features

- Pip-Boy style boot animation, CRT scanlines, color themes, sound effects, and terminal UI.
- Five main sections: `DASH`, `RADIO`, `STATS`, `APPS`, and `SET`.
- Optional `PipBooter` helper APK for head units that can auto-launch a navigation app but do not boot directly into the Home launcher.
- Custom two-panel dashboard with selectable widgets.
- GPS speedometer, GPS info, offline map widget, media widget, clock, tachometer, coolant widget, OBD gauges, and Vault Boy display widgets.
- Local folder-based radio stations with optional `station.ini` metadata.
- External music player bridge for apps like Spotify, YouTube Music, Poweramp, and other Android media apps.
- Offline Mapsforge map packages with POI markers and multiple active regions.
- OBD-II telemetry for RPM, coolant, voltage, intake temp, MAF, engine load, speed, and DTC trouble codes.
- Full app drawer with configurable dashboard and top-bar shortcuts.
- Configurable HUD, effects, themes, watermarks, shortcuts, OBD behavior, and gauge thresholds.
- Geiger counter SFX when coolant, voltage, and RPM are over configurable warning levels.

## Documentation

- [Installation Guide](docs/INSTALLATION.md)
- [PipBooter Setup](docs/PIPBOOTER.md)
- [Feature Guide](docs/FEATURES.md)
- [Permissions Explained](docs/PERMISSIONS.md)
- [UI Sections and Gestures](docs/UI_AND_GESTURES.md)
- [Radio Station Setup](docs/RADIO_STATIONS.md)
- [Offline Maps Setup](docs/OFFLINE_MAPS.md)
- [OBD-II and Vehicle Stats](docs/OBD_AND_STATS.md)
- [Configurable Settings](docs/CONFIGURATION.md)

## About

### Project

Vault Maintenance Unit 99-E is a fan-made project by Shadc.

Pip-OS / PipCar is a personal fan launcher inspired by retrofuturistic terminal interfaces and the Fallout series.

### Support Development

Optional support helps keep the project moving, from UI polish to maps, testing, and new car-unit features.

- [🥤 Buy me a Nuka Cola](https://ko-fi.com/shadc)

### Social

- [Reddit: u/ShadowCimmer](https://www.reddit.com/user/ShadowCimmer/)
- [Instagram: @unit99e](https://instagram.com/unit99e)
- [TikTok: @unit99e](https://tiktok.com/@unit99e)

### Thanks

Special thanks to [ZapWizard's PypBoy](https://github.com/zapwizard/pypboy) project on GitHub for helping start this project, including reference material, assets, sounds, and ideas that shaped the early build.

### Safety and Warranty

This launcher is intended for parked, passenger, or safe hands-free use. Do not operate or configure the app in a way that distracts you while driving.

Always pay attention to the road, traffic conditions, vehicle controls, and local laws. The driver is responsible for safe and legal use of any dashboard or head unit software.

This fan-made project is provided as-is, without warranties of any kind. No guarantee is made that features, data, maps, media controls, OBD-II readings, or system integrations will work perfectly or be error-free.


## Legal Disclaimer & Fair Use Notice

This software is an entirely non-commercial, hobbyist fan project distributed completely free of charge. It generates zero revenue, contains no corporate advertisements, and features no paid or premium content gating. 

Any integrated user interface configurations, parody text structures, or contextual ambient sound effects are included strictly under **Fair Use** guidelines for the sole purpose of non-profit thematic parody, transformative artistic customization, and personal fan enjoyment.

*Fallout, Vault Boy, Vault-Tec, Pip-Boy*, and related names, artwork, logos, and fictional assets are trademarks or copyrights of Bethesda Softworks LLC, Bethesda Game Studios, ZeniMax Media Inc., Microsoft, and/or their respective parent organizations. This project is entirely independent and is **not** affiliated with, endorsed by, sponsored by, or approved by Bethesda, ZeniMax, Microsoft, or any associated intellectual property rights holder. No ownership over corporate assets is claimed or implied.
