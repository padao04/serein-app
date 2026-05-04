# Smart Bookmark Dashboard

A Progressive Web App (PWA) for the Smart Bookmark reading tracker.

## Files
- `index.html` — the app
- `manifest.json` — PWA manifest (enables "Add to Home Screen")
- `sw.js` — service worker (offline caching)
- `icon-192.png` / `icon-512.png` — app icons (create these, see below)

---

## Deploying to GitHub Pages (free HTTPS — required for BLE)

Web Bluetooth requires HTTPS. GitHub Pages is free and gives you HTTPS automatically.

1. Create a free GitHub account at github.com if you don't have one
2. Click **New repository** → name it `bookmark-app` (or anything)
3. Set it to **Public**
4. Upload all files in this folder to the repo
5. Go to **Settings → Pages → Source → Deploy from branch → main → / (root)**
6. Save — within ~60 seconds your app is live at:
   `https://YOUR_USERNAME.github.io/bookmark-app/`

That URL works in Chrome on Android and opens via BLE.

---

## Adding to Home Screen (makes it feel like a native app)

### Android (Chrome)
- Visit your GitHub Pages URL in Chrome
- Tap the three-dot menu → "Add to Home screen"
- OR: a banner will appear automatically asking to install

### iPhone (Safari)
- Visit the URL in Safari (Chrome on iOS does NOT support Web Bluetooth)
- Tap the Share button → "Add to Home Screen"
- Note: Web Bluetooth is NOT supported on iOS at all currently.
  iPhone users cannot connect via BLE — this is an Apple restriction.

---

## Creating App Icons

You need two PNG icons: 192×192 and 512×512 pixels.
Name them `icon-192.png` and `icon-512.png` and add them to the same folder.

Quick option: use https://favicon.io or https://realfavicongenerator.net
to generate icons from text or an image, then download the PNGs.

---

## Notes

- BLE works on **Android Chrome** and **desktop Chrome/Edge**
- BLE does NOT work on iOS/Safari (Apple limitation, not fixable)
- BLE requires HTTPS — local `file://` won't work, but localhost does
- If testing locally: `npx serve .` gives you http://localhost:3000
