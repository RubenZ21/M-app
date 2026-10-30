# Minja's Kitchen

A gluten-free and dairy-free recipe book. It is one HTML page that installs as an app on a phone (PWA) and works offline.

**Open it:** https://rubenz21.github.io/M-app/

## What it does

- **Recipe book**: search, filter by category, tick off ingredients and steps while cooking, notes, share a recipe as text.
- **Write or edit recipes** in the app (+ button, or the pencil on a recipe).
- **Export**: all recipes as one CSV file (download, share or copy).
- **Import**: the same CSV format comes back in, from a file or pasted text. Recipes with the same title are updated and the rest are kept. You can also replace the whole cookbook.
- **Claude prompts**: one asks for a single new recipe. The other ("More like mine") goes with the exported CSV so Claude suggests new recipes that aren't in the cookbook yet.

## CSV format

```
title,category,time,serves,tags,ingredients,steps,notes
```

One recipe per row, every field in double quotes. `ingredients` and `steps` are lists separated by ` | `, and `tags` are comma separated. Export and import use exactly this format, so an exported file can be imported again unchanged.

## Install on a phone

Open the link in Chrome, tap ⋮ → **Add to Home screen** / **Install app**. On iPhone: Safari → Share → **Add to Home Screen**.

## Data

Recipes are stored in the browser on the phone (localStorage). Nothing is sent anywhere. The exported CSV is also the backup.

## Files

| File | Purpose |
|---|---|
| `index.html` | The whole app (HTML, CSS, JS) |
| `manifest.webmanifest` | App name, colours, icons for installing |
| `sw.js` | Service worker for offline use; bump `CACHE` when releasing |
| `icons/` | App icons |
