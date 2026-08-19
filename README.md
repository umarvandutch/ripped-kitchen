# Ripped Kitchen

Installable mobile-first nutrition, meal-prep, training and physique progress PWA.

## What is included

- Home dashboard with daily macro progress
- Date navigation and weekday-aware meal plan
- Gym / MMA / football / rest-day context
- Tap-to-complete meals
- Steps, training minutes, water and sleep tracking
- Weight and waist check-ins
- Finalised daily snapshots stored by date
- Saved history so previous days can be reopened
- Detailed recipe macros, ingredient weights and beginner-friendly steps
- Sunday / Wednesday / Friday 5-container meal-prep workflows
- Matrix-style schematic physique progress visualisation
- Offline service worker
- Installable PWA manifest
- Automatic GitHub Pages deployment workflow

## Data storage

Version 1 stores progress in the device/browser using `localStorage`. This survives page changes and normal browser/app restarts on that device. Clearing browser/app data or uninstalling can remove local history.

A future version can add authenticated cloud sync for phone/tablet sharing and backups.

## Development workflow

Changes merged/pushed to `main` automatically run `.github/workflows/pages.yml` and deploy the current app to GitHub Pages once Pages is configured to use GitHub Actions.

The app is deliberately split into:

- `index.html` — UI shell
- `styles.css` — responsive/mobile UI
- `data.js` — recipes, meal plans and prep instructions
- `app.js` — tracking, history, navigation and PWA logic
- `manifest.webmanifest` — install metadata
- `sw.js` — offline cache
- `icons/` — app icon assets

This separation makes future recipe/UI/features changes safer than editing one large HTML file.

## Nutrition note

Meal macro values are working estimates until the exact branded product labels and ingredient database choices are reconciled. The app labels recipe macros accordingly rather than presenting generic estimates as laboratory-exact values.
