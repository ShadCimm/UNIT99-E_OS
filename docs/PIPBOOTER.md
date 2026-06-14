# PipBooter: Launcher Boot Helper

`PipBooter` is an optional helper APK for Android head units that do not automatically open the selected Home launcher after boot.

Some generic Android car units wake or boot into the last-used app instead of the configured Home app. PipBooter works around that behavior by acting like a tiny launcher trigger: when PipBooter is opened, it performs the same kind of action as pressing the Android Home button. If `Pip-OS` is set as the default Home app, Android then opens Pip-OS and the normal Pip-OS boot animation runs.

In short:

```text
Head unit boot action -> PipBooter opens -> Home is triggered -> Pip-OS opens
```

It is basically a launcher for the launcher.

## When You Need PipBooter

Use PipBooter if your head unit:

- Does not open Pip-OS automatically after boot.
- Always restores the last-used app after boot.
- Has a setting such as `Launch navigation app on boot`, `Startup navigation`, `Boot app`, or similar.
- Lets you choose one app to auto-launch, but that app cannot be the Home launcher directly.

You do not need PipBooter if your head unit already opens Pip-OS normally when it boots or wakes.

## Setup

1. Install the main `pipOS_*.apk`.
2. Set `Pip-OS` as the default Android Home app.
3. Install `PipBooter.apk`.
4. Open your head unit's system settings.
5. Find the setting that launches a navigation/startup app on boot.
6. Select `PipBooter` as that startup/navigation app.
7. Reboot the unit to test.

Expected result:

1. The head unit boots.
2. The head unit launches PipBooter.
3. PipBooter triggers Home.
4. Android opens Pip-OS because Pip-OS is the default Home app.
5. Pip-OS plays its boot animation and opens the dashboard.

## Important Notes

- PipBooter is optional.
- PipBooter does not replace Pip-OS.
- PipBooter must not be set as the default Home app.
- Pip-OS should be the default Home app.
- PipBooter should only be selected in the head unit's startup/navigation-app setting.
- The exact setting name depends on the head unit firmware.

## Troubleshooting

If PipBooter opens but Pip-OS does not:

1. Press the Android Home button manually.
2. If Android asks which launcher to use, choose `Pip-OS` and tap `Always`.
3. Reboot and test again.

If the unit still opens the last-used app:

1. Confirm the head unit startup/navigation setting points to `PipBooter`.
2. Confirm PipBooter is installed and not blocked by battery/startup restrictions.
3. Confirm Pip-OS is still the default Home app.

