# SELENE — Lunar Mission Lab

Vite + React + Cesium front end; Vercel serverless Groq endpoint.

## Local development
```bash
npm install
npm run dev
```

## Deploy to Vercel
Import this GitHub repository. Build command: `npm run build`; output directory: `dist`. Add environment variable `GROQ_API_KEY` (and optionally `GROQ_MODEL`) in Vercel Project Settings, then redeploy.

## Scientific status (important)
- Cesium renders the Moon globe; this scaffold does NOT yet configure an authenticated/verified LROC WMS endpoint. No satellite tile layer is claimed as loaded.
- The descent is a simplified 1D vertical point-mass integration with constant thrust and lunar gravity. It is not a complete guidance/6-DOF/terrain collision model.
- LOLA elevation and Diviner temperature are linked as sources but are not sampled into the simulator.
- Do not use for real flight operations.

NASA sources: https://trek.nasa.gov/moon/ ; https://pds-geosciences.wustl.edu/missions/lro/
