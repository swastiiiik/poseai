# PoseAI 📸

> A PWA that overlays location-aware pose suggestions over your camera feed.

---

## What it does

| Feature | Details |
|---|---|
| 📍 Location detection | Uses GPS + OpenStreetMap (free, no API key) to detect Beach, Urban, Nature, Mountain, Café, Cultural, Shopping |
| 🎭 35 curated poses | 5 poses per category, all with detailed photographer tips |
| 📐 Rule-of-thirds grid | Toggle on/off with the ⊞ button |
| 🔄 Front / rear camera | Flip with one tap |
| 📸 Photo capture | Captures from the live camera feed with a flash effect |
| 📱 PWA | Install to iPhone Home Screen via Safari |

---

## How to deploy (Windows laptop → iPhone 17)

### Step 1 — Create a GitHub repository (free)

1. Go to [github.com](https://github.com) and sign up / log in
2. Click **New repository**
3. Name it `poseai` (or anything you like)
4. Set it to **Public**
5. Click **Create repository**

### Step 2 — Upload the files

In the repository page, click **Add file → Upload files**, then drag and drop all four files:
```
index.html
manifest.json
sw.js
icon.svg
```
Click **Commit changes**.

### Step 3 — Enable GitHub Pages

1. In the repo, go to **Settings → Pages**
2. Under **Branch**, select `main` and folder `/root`
3. Click **Save**
4. GitHub will show a URL like:
   ```
   https://YOUR-USERNAME.github.io/poseai/
   ```
   (It takes ~60 seconds to go live)

---

## How to use on iPhone 17

### First time — Install as an app

1. Open **Safari** (⚠️ must be Safari, not Chrome or Firefox)
2. Go to your GitHub Pages URL:
   ```
   https://YOUR-USERNAME.github.io/poseai/
   ```
3. Tap the **Share button** (box with arrow pointing up)
4. Scroll down and tap **"Add to Home Screen"**
5. Tap **Add** — the PoseAI icon appears on your home screen
6. Open it from the home screen — it runs full-screen like a native app

### Every time you use it

1. Open PoseAI from your Home Screen
2. **Allow camera** when Safari asks
3. **Allow location** when Safari asks (tap "Allow Once" or "Allow While Using")
4. The app detects your location and loads the right poses automatically
5. **Swipe the pose card** left/right (or tap ‹ ›) to browse all poses
6. Tap **⊞** to toggle the rule-of-thirds composition grid
7. Tap **🔄** to switch front/rear camera
8. Tap the **white shutter button** to capture
9. In the preview, tap **"Open Full Size"** — a new tab opens with just the photo
10. **Long-press that photo → "Add to Photos"** to save to your camera roll

### Tips

- For best results, use the **rear camera** (someone else frames the shot while you pose)
- The pose card stays visible as a reference; only the clean camera image is captured (no UI overlay)
- **Location updates automatically** each time you open the app
- Works offline after first load (service worker caches the app shell)

---

## Location categories & pose counts

| Category | Detected when near | Poses |
|---|---|---|
| 🏖️ Beach | Coastline, bay, shore, sea | 5 |
| 🏙️ Urban | City streets, roads (default) | 5 |
| 🌿 Nature | Park, garden, forest, reserve | 5 |
| ⛰️ Mountain | Peak, ridge, hill, trail | 5 |
| 🏛️ Cultural | Museum, gallery, monument, temple | 5 |
| ☕ Café | Restaurant, cafe, bar, pub | 5 |
| 🛍️ Shopping | Mall, market, retail, bazaar | 3 |
| 📍 General | Fallback for unrecognised places | 5 |

---

## Privacy

- Location is used **only** to call OpenStreetMap's free reverse-geocoding API
- No data is stored, sent to any server, or logged anywhere
- Photos are captured entirely on-device and never uploaded
