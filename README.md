# Minja's Day

A calm day planner with a to-do list, meal plan and recipe book. It is one HTML page that installs as an app on a phone (PWA) and works offline.

**Open it:** https://rubenz21.github.io/m-app/

## What it does

- **Day** – to-do list for any day, with a week strip to jump between days. Tasks can have a time, an area (Home, Studio, Family, Errands, For me), a note, a priority star, and can repeat (daily, weekdays, weekly, monthly). Typing "Dentist at 14:30" sets the time for you. Unfinished tasks from earlier days can be brought to today in one tap. Also has breakfast / lunch / dinner and a "note to self" per day.
- **Week** – the whole week at a glance: tasks, progress, meals and notes.
- **Recipes** – the Minja's Kitchen recipe book (gluten free, dairy free): search, categories, tick off ingredients and steps, plan a recipe for a day, send its ingredients to the shopping list. New recipes come from Claude as CSV (Settings has the prompt).
- **Shopping** – shopping list with tick-off, "clear ticked" and share.
- **Settings** – name, recipe import/remove, backup and restore (JSON file).

## Install on a phone

Open the link in Chrome, tap ⋮ → **Add to Home screen** / **Install app**. On iPhone: Safari → Share → **Add to Home Screen**.

## Data

Everything is stored in the browser on the phone (localStorage). Nothing is sent anywhere. Use **Settings → Save backup** now and then.

## Files

| File | Purpose |
|---|---|
| `index.html` | The whole app (HTML, CSS, JS) |
| `manifest.webmanifest` | App name, colours, icons for installing |
| `sw.js` | Service worker for offline use; bump `CACHE` when releasing |
| `icons/` | App icons |
