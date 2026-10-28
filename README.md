# Haze Report 2026

Single-page haze and weather monitor.

- **Singapore tab:** PSI by area (north, south, east, west, central) with PM2.5, PM10 and main pollutant, plus Singapore weather and a 9-hour outlook.
- **ASEAN weather tab:** current weather, today's range, rain chance, UV and sunrise/sunset for 16 cities, with an illustration for each condition.

## Data

The page is static and shows a snapshot taken on 28 Oct 2026. It does not fetch anything at runtime.

- Haze (Singapore only): National Environment Agency via data.gov.sg, `https://api-open.data.gov.sg/v2/real-time/api/psi`. Reading for 10:00 SGT, updated 10:15 SGT.
- Weather: [Open-Meteo](https://open-meteo.com), observed around 10:30 SGT.

To refresh, update the `AREAS`, `CITIES` and `HOURLY` arrays near the top of the `<script>` in `index.html`.

## Deploy on Vercel

No build step. Import the repo in Vercel with the **Other** framework preset, leave the build command and output directory empty, and deploy. `vercel.json` only adds clean URLs and basic security headers.

Local preview: `npx serve .` or open `index.html` in a browser.
