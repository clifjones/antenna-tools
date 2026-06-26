# antenna-tools

Calculators and tools for designing antennas.

## HF Linked Dipole Designer

Interactive cut-length calculator for multi-band linked dipoles (flat-top or inverted-V), with support-height geometry and an SVG wire diagram.

Open [`src/linked_dipole_designer.html`](src/linked_dipole_designer.html) in a browser, or serve the `src/` folder over HTTPS/localhost to install it as a phone app.

---

## Install on your phone (PWA — no app store)

The designer is a **Progressive Web App**. Install it from the browser like a native app.

### 1. Serve locally (for testing)

```bash
npm install
npm run serve
```

Open `http://localhost:8080/linked_dipole_designer.html` on your phone (same Wi‑Fi network), or use [GitHub Pages](#github-pages) for a public HTTPS URL.

> PWAs require **HTTPS** (or `localhost`). Opening the HTML file directly from the filesystem will not register the service worker or show an install prompt.

### 2. Add to home screen

| Platform | Steps |
|----------|--------|
| **Android (Chrome)** | Menu → **Install app** or **Add to Home screen** |
| **iPhone (Safari)** | Share → **Add to Home Screen** |

The app runs full-screen, works offline after the first load, and keeps the dark theme in the status bar.

---

## Native app (Play Store / App Store)

For a packaged Android APK/AAB or iOS app, use [Capacitor](https://capacitorjs.com/):

```bash
npm install
npx cap add android    # and/or: npx cap add ios
npm run cap:sync
npm run cap:android    # opens Android Studio
npm run cap:ios        # opens Xcode (macOS only)
```

Build and sign in Android Studio or Xcode, then publish to the stores.

---

## GitHub Pages

This repo includes a GitHub Actions workflow (`.github/workflows/deploy-pages.yml`) that deploys the `src/` folder on every push to `main`.

**One-time setup:**

1. Push to GitHub.
2. In the repo: **Settings → Pages → Build and deployment → Source** → select **GitHub Actions**.

After the first successful workflow run, the app will be live at:

`https://<user>.github.io/antenna-tools/linked_dipole_designer.html`

Install it on your phone from that URL (Add to Home Screen / Install app).

---

## Files

| Path | Purpose |
|------|---------|
| `src/linked_dipole_designer.html` | Main app (single-file calculator + diagram) |
| `src/manifest.webmanifest` | PWA install metadata |
| `src/sw.js` | Offline cache |
| `src/icons/` | App icons |
