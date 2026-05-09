# Forest Focus

A focus timer that grows trees as you stay focused. Single-page web app
that installs to your phone's home screen as a real-feeling app (PWA),
works offline, and stores all your data locally.

## Files

- `index.html` — the entire app (HTML, CSS, JS in one file)
- `manifest.webmanifest` — PWA metadata so it installs as an app
- `sw.js` — service worker so it works offline
- `icon.svg` / `icon-maskable.svg` — home-screen icons

## Install on your phone

A PWA needs a hosted URL with HTTPS. Pick one:

### Option 1: GitHub Pages (free, takes 2 minutes)

1. Push this repo to GitHub.
2. In your repo, go to **Settings → Pages**.
3. Under **Source**, choose **Deploy from a branch**, pick the branch
   (e.g. `claude/forest-focus-timer-imEer` or `main`), and **`/ (root)`**.
4. Save. Wait ~1 minute. GitHub gives you a URL like
   `https://<you>.github.io/<repo>/`.
5. Open that URL on your phone in the steps below.

### Option 2: Netlify Drop (no account needed)

1. Go to <https://app.netlify.com/drop>.
2. Drag the whole project folder onto the page.
3. You get a URL — open it on your phone.

### Add to home screen

**iPhone (Safari)**

1. Open the URL in Safari.
2. Tap the **Share** button (square with up arrow).
3. Scroll down, tap **Add to Home Screen**.
4. Tap **Add**. The app icon appears on your home screen.
5. Tap the icon — it opens full-screen with no browser chrome.

**Android (Chrome)**

1. Open the URL in Chrome.
2. Tap the **⋮** menu → **Add to Home screen** (or **Install app**).
3. Confirm. The icon installs like any app and shows up in your launcher.

After installing, the service worker caches everything, so the app works
without an internet connection.

## Development

No build step. Just open `index.html` in a browser. To test the PWA
behavior locally over HTTPS, you can use any static server with a TLS
proxy, or use `python3 -m http.server` and add the URL to Chrome's
`chrome://flags/#unsafely-treat-insecure-origin-as-secure` allowlist.
