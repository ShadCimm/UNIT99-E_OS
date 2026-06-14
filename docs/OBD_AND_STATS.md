# OBD-II and Vehicle Stats

Pip-OS can show live vehicle information from a Bluetooth ELM327 OBD-II adapter.

## What You Need

- A vehicle with an OBD-II port.
- A Bluetooth ELM327-compatible adapter.
- Android Bluetooth enabled.
- The adapter paired in Android settings before using Pip-OS.

Pip-OS does not pair the adapter for you. Pair it in Android first.

## Pair the Adapter

1. Plug the ELM327 adapter into the car's OBD-II port.
2. Turn the ignition/accessory power on.
3. Open Android Bluetooth settings.
4. Pair with the adapter.
5. Common pairing PINs are `0000` or `1234`, depending on the adapter.

## Select the Adapter in Pip-OS

1. Open `SET`.
2. Choose `OBD-II`.
3. Under `SELECT PREFERRED DEVICE`, tap your paired ELM327 device.
4. Optional: enable `AUTOCONNECT ON LAUNCH`.
5. Optional: adjust retry interval from 5 to 300 seconds.
6. Tap `CONNECT`, or go to `STATS` and use `QUICK CONNECT`.

## Live Data Shown

Pip-OS polls:

| Value | Source |
|---|---|
| RPM | OBD PID `010C` |
| Coolant temperature | OBD PID `0105` |
| Voltage | ELM command `ATRV` |
| Intake temperature | OBD PID `010F` |
| Mass air flow | OBD PID `0110` |
| Engine load | OBD PID `0104` |
| Vehicle speed | OBD PID `010D` |
| DTC codes | OBD mode `03`, read on demand |

The app updates quickly while connected. Some low-cost adapters or vehicles may not support every value.

## STATS Screen

The `STATS` screen shows:

- `S SPEED`: OBD speed in KPH.
- `P POWER`: RPM.
- `E ENGINE`: coolant temperature.
- `C CHARGE`: voltage.
- `I INTAKE`: intake temperature.
- `A AIRFLOW`: MAF.
- `L LOAD`: engine load percentage.
- DTC trouble-code area.

Warning colors:

- RPM turns red at or above the configured RPM warning.
- Coolant is blue when cold and red when hot.
- Voltage turns red when outside the configured safe range.

## Reading Trouble Codes

1. Connect OBD-II.
2. Open `SET > OBD-II`.
3. Tap `READ DTCs`.
4. Trouble codes appear in the settings panel and on `STATS`.

## Demo Mode

For testing without a car:

1. Open `SET > DEV`.
2. Enable `DEMO OBD DATA`.

Demo mode simulates RPM, coolant, voltage, load, speed, and example DTC codes. It is unavailable while a real OBD connection is active.

## Troubleshooting

- If no devices appear, pair the adapter in Android Bluetooth settings first.
- If connect fails, confirm Bluetooth permission is granted.
- If the adapter connects but values stay blank, the adapter or vehicle may not support the queried PID.
- If auto-connect loops too quickly, increase retry interval in `SET > OBD-II`.
- If demo mode will not start, disconnect the real OBD adapter first.
