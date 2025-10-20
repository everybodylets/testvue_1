# Vue Leaflet Sandbox

Minimal Vite + Vue 3 + TypeScript project configured with `@vue-leaflet/vue-leaflet` and `leaflet`.

## Run locally

1. Install dependencies:
```bash
npm install
```

2. Run dev server:
```bash
npm run dev
```

Open the URL printed by Vite (usually http://localhost:5173).

## Notes / fixes included
- `src/shims-vue.d.ts` to avoid TypeScript errors for `.vue` imports.
- Marker icon fix (`L.Icon.Default.mergeOptions`) for Vite/ESM so default markers display correctly.
