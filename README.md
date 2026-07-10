# Spark Estimator

Mobile-first repair cost estimator built for the Spark Homes take-home challenge.

**Live demo:** https://rishabhagrawal287.github.io/spark-estimator/

## What it does

Spark Homes acquisition agents walk distressed properties and need to estimate repair costs on the spot. This app replaces a paper spreadsheet workflow with a single-file web app that works on any phone, with or without a signal.

- 75+ repair line items pulled directly from the official Spark Homes price list
- 21 collapsible groups across 7 sections (Interior, Kitchen, Bathrooms, Systems, Exterior, Bedrooms, Living Areas)
- Bathroom, Bedroom, and Living Area instances can be added or removed per property
- Swipe right to mark an item needed, swipe left to clear it
- Camera photo capture per line item, with automatic compression
- Inline price editing per item, plus bulk CSV price updates
- One-tap export to a branded Excel report, bundled with photos in a ZIP
- **Deal Analyzer** — enter ARV and purchase price to get an instant Max Offer (70% rule) and color-coded deal score
- Installs to the home screen and works fully offline after first load

## Running it

Open `index.html` in any browser. No build step, no server, no installation.

## Tech

Vanilla HTML/CSS/JavaScript. No framework. Libraries loaded via CDN:
- [Tailwind CSS](https://tailwindcss.com) — styling
- [xlsx-js-style](https://github.com/gitbrent/xlsx-js-style) — branded Excel export
- [JSZip](https://stuk.github.io/jszip/) — bundling Excel + photos into one download

All project data, photos, and price overrides are stored in the browser via `localStorage`. No backend, no database, no cost to host.

## Notes

- Built and tested on Chrome (Android) and Chrome DevTools device emulation (iPhone 14 Pro, Galaxy S20)
- `localStorage` has a 5MB ceiling; very photo-heavy projects could approach this limit. IndexedDB would be the next step for unlimited photo storage.

## AI tools disclosure

Claude (Anthropic) assisted with code generation. Architecture decisions, feature prioritization, and the Deal Analyzer concept are my own.
