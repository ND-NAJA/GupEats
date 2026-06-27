# Food Log

A simple personal food tracker. One HTML file, no build step, runs from any static host.

## Features

- 4 meal slots: breakfast, lunch, dinner, other
- Three ways to log: barcode scan, manual entry, or one-tap from recents
- Daily / weekly / monthly views with calendar heatmap
- **Daily calorie goal** with progress bar, "remaining / over by" indicator, and per-day on-goal tracking across the week and month
- Calories optional per item — log just food names if you don't care about numbers for a given entry
- Barcode lookup via [Open Food Facts](https://world.openfoodfacts.org) (no API key, good coverage of Albert Heijn and other Belgian/Dutch products)
- Dutch product names preferred for Belgian/AH products, with French and English fallbacks
- Export / import as JSON
- All data stays in your browser — nothing leaves your phone

## Deploy to GitHub Pages

1. Sign in at [github.com](https://github.com).
2. Click the **+** top right → **New repository**. Name it `food-log` (lowercase, no spaces). Public is fine. Don't tick anything else. Click **Create repository**.
3. On the empty repo page, click the **"uploading an existing file"** link in the quick-setup text.
4. Drag `index.html` into the upload box. Scroll down and click **Commit changes**.
5. Click **Settings** (top of the repo, on the right of the menu bar — not your account settings).
6. In the left sidebar, click **Pages**.
7. Under "Source", select **Deploy from a branch**. Under "Branch", select **main** and **/ (root)**. Click **Save**.
8. Wait ~30–60 seconds, then refresh. The URL appears at the top: `https://<your-username>.github.io/food-log/`.

## Add to iPhone home screen

1. Open the URL in **Safari** (this is required — "Add to Home Screen" doesn't behave the same in Chrome).
2. Tap the share button → **Add to Home Screen** → **Add**.
3. Launch from the home screen icon — it opens fullscreen, no Safari chrome.
4. The first time you scan, Safari will ask for camera permission. Allow it. If you accidentally deny it, fix in **iPhone Settings → Safari → Camera**.

## Set a daily goal

- Open the app → **Settings** tab.
- Type a number in "Calorie target per day". Leave blank to turn goal tracking off.
- The Today screen now shows progress vs goal. Week and Month views show on-goal vs over-goal days.

## Backup

Your data lives in Safari's local storage. If you clear Safari site data or switch phones without exporting, it's gone.

- **Settings → Export data** saves a JSON file. Email it to yourself or save it to iCloud Drive every few weeks.
- **Settings → Import data** restores from a JSON file on a new device or after a wipe.
- **Clear all data** wipes entries but keeps your goal.

## Updating the app

If you change `index.html` and want the new version on your phone:

1. Go to the repo on GitHub, click `index.html`, click the pencil icon (Edit) or delete the file and re-upload the new one.
2. Commit changes. Pages redeploys automatically in about a minute.
3. On your phone, swipe up to close the app fully, then reopen — iOS will fetch the new version.

## Notes

- Open Food Facts is community-maintained. A scanned product may be missing or have incomplete nutrition info. When that happens, the manual form opens prefilled with whatever data was found — fill in the rest.
- Calorie values from barcodes are **per 100g** of product. For the actual amount you ate, adjust the number before saving.
- HTTPS is required for the camera API to work. GitHub Pages gives you HTTPS automatically.
- No analytics, no accounts, no servers. Just you and your data.
