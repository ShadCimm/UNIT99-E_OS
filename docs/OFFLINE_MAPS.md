# Offline Maps Setup

Pip-OS uses Mapsforge vector map files. Once a map package is downloaded or loaded, the map works without mobile data.

## Recommended Method: Download in the App

1. Open `SET`.
2. Choose `MAP`.
3. Pick a catalog tab:
   - `EUROPE`
   - `N. AMERICA`
   - `C. AMERICA`
   - `S. AMERICA`
   - `OCEANIA`
   - `FAVORITES`
4. Find your country, state, province, or region.
5. Tap `GET`.
6. Wait for the package to finish downloading.
7. Tap `SET` or `ON` to activate the region.

Map rows show:

- Region name.
- Install state.
- Download progress and speed.
- Installed package size.
- `GET`, `CANCEL`, `SET`, or `ON`.
- `LOAD` for local files.
- `DEL` for delete.
- `FAV` for favorites.

## Active Regions

You can keep multiple downloaded regions active.

Use this when you drive across borders, for example:

- Spain and Portugal.
- Multiple US states.
- A US region package plus a specific state.

In `SET > MAP`, installed regions can be toggled active with the row action. The current primary region is the main fallback area when there is no GPS fix.

## Map Widget Controls

In `DASH`, choose the `MAP` widget.

Controls:

- Tap `NEAR`, `MID`, or `FAR` to cycle zoom level.
- Double tap the map widget to expand it.
- Double tap expanded map to return to the split dashboard.
- Long press the expanded map to open the widget picker.

## Manual Loading With the File Picker

Use this if you already downloaded Mapsforge files on a computer.

1. Open `SET > MAP`.
2. Select the region row.
3. Tap `LOAD`.
4. In Android's file picker, select the required `.map` and `.poi` files together.
5. Pip-OS copies them into its private app storage.
6. Wait for `LOAD COMPLETE`.

The exact filenames needed for the selected region are listed under `PACKAGE CONTENTS` in `SET > MAP`.

## Manual Folder Placement

The current UI uses the file picker, but the app also recognizes a `PipCarMaps` import folder pattern. This is useful on devices where file picking is awkward or for troubleshooting builds that expose direct disk import.

Common internal storage paths:

```text
Internal Storage/
  PipCarMaps/
    spain.map
    spain.poi
```

Region subfolder by region id:

```text
Internal Storage/
  PipCarMaps/
    spain/
      spain.map
      spain.poi
```

Region subfolder by Mapsforge slug:

```text
Internal Storage/
  PipCarMaps/
    great-britain/
      great-britain.map
      great-britain.poi
```

Removable storage patterns may also work:

```text
USB or SD Root/
  PipCarMaps/
```

```text
USB or SD Root/
  Android/
    data/
      com.pipcar.launcher/
        files/
          PipCarMaps/
```

Always match the exact filenames shown in `SET > MAP > PACKAGE CONTENTS`.

## Map Package Storage

After download or load, Pip-OS stores map data privately under the app's internal files area. You normally do not need to manage that folder manually.

Use `DEL` in `SET > MAP` to remove a package safely.

## Supported Map Content

The catalog covers:

- Most European countries.
- US regional packages and individual US states.
- Canadian provinces and territories.
- Mexico, Central America, and Caribbean regions.
- South American countries.
- Australia, New Zealand, and Oceania/Pacific regions.

Map POI categories include settlements, towns, fuel, police, medical, farms, industry, parks, airports, ports, churches, museums, and rail stations.

## POI Labels Explained

Pip-OS uses Fallout-style names for some real-world map markers. Here is what each label means:

| Pip-OS map label | Real-world place type |
|---|---|
| `SETTLEMENT` | City |
| `TOWN` | Town or village |
| `RED ROCKET` | Gas station / fuel stop |
| `LAW` | Police station or police-related location |
| `MEDICAL` | Pharmacy, hospital, or clinic |
| `FARM` | Farm, farmland, or farmyard |
| `FACTORY` | Industrial area or factory-type zone |
| `GREEN ZONE` | Park, garden, or nature reserve |
| `AIRFIELD` | Airport or airfield |
| `PORT` | Port or ferry terminal |
| `CHURCH` | Place of worship / church marker |
| `MUSEUM` | Museum or tourism museum POI |
| `RAIL` | Train station or rail stop |

## Notes About POIs

- `MEDICAL` can come from more than one source type in the map data. In practice it may represent a pharmacy, hospital, or clinic.
- `SETTLEMENT` and `TOWN` are the most prominent labels when zoomed farther out.
- The exact POIs available depend on the downloaded map package and its POI database.
- If a region has no installed POI package, the map may still render roads and position, but nearby place markers can be limited.
