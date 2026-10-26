# MG MAPS

Explore, navigate and discover. A free, installable map web app by MGCowbell / MGTECH, built with plain HTML, CSS and JavaScript (no build step).

## Features

- Interactive vector map that stays sharp when zoomed, with Standard, Satellite, Terrain, Dark and Business styles
- Your location, address, and named places around you
- Nearby Places by category (restaurants, hotels, hospitals, pharmacies, gas stations, ATMs, banks and more)
- Route planner for driving, walking and cycling, with the shortest route selected first and alternatives
- Turn-by-turn navigation with voice guidance
- Saved places, share and copy location, distance measuring, dark mode
- Installable as an app (PWA) with an offline app shell

## Data sources

Map data © OpenStreetMap contributors (ODbL). Maps: OpenFreeMap, OpenMapTiles, CARTO, Esri, OpenTopoMap. Search and address lookup: Nominatim. Places: Overpass API. Routing: OSRM (routing.openstreetmap.de). These are free public services with fair-use limits and no live traffic, photos, ratings or Street View.

## Run locally

Geolocation and the service worker need HTTPS or localhost:

```bash
python3 -m http.server 8080
# open http://localhost:8080
```

## Deploy on GitHub Pages

1. Create a new repository on GitHub and upload all files in this folder (keep `index.html` in the root).
2. Go to **Settings > Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, then **Save**.
4. After a minute your site is live at `https://YOUR-USERNAME.github.io/YOUR-REPO/`.

## Android APK download

Put your APK at `downloads/MG-MAPS.apk` (rename it to match). The app's download button links to that path. For files over 25 MB, attach the APK to a GitHub Release and update `APK_URL` in `index.html`.

## Updating the live site

After you change `index.html`, raise the cache version in `service-worker.js` (for example `mgmaps-v7` to `mgmaps-v8`) so phones load the new files.

## Project files

| File | Purpose |
|---|---|
| `index.html` | The whole app (UI, map, search, routing) |
| `service-worker.js` | Offline app shell cache |
| `manifest.json`, `icon.svg` | Install-as-app settings and icon |
| `downloads/` | Place the Android APK here |
