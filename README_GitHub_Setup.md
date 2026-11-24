# Legion Tracker B7 — GitHub Pages Upload

This folder contains the complete website package. Upload **all files in this folder** to the root of one GitHub repository (not just the HTML file).

## Included files

- `index.html` — Legion Tracker B7 application.
- `legion-manifest.json` — installable web-app manifest.
- `legion-sw.js` — offline app-shell service worker; the HTML already registers this exact filename.
- `legion-icon-192.png` and `legion-icon-512.png` — app icons.
- `legion-icon-maskable-512.png` — Android maskable app icon.
- `legion-icon-180.png` — Apple touch icon asset.
- `favicon-32.png` — browser tab icon.

## Publish with GitHub Pages

1. Extract this ZIP on your computer.
2. Open your GitHub repository, or create a new repository.
3. Choose **Add file → Upload files**.
4. Upload every file from this folder, keeping the filenames unchanged and placing them in the repository root.
5. Commit the upload to the `main` branch.
6. Open **Settings → Pages** in the repository.
7. Under **Build and deployment**, select **Deploy from a branch**.
8. Select branch `main` and folder `/ (root)`, then save.
9. Wait for GitHub Pages to publish, then open the Pages URL over HTTPS.

## If replacing your existing tracker

- First export a JSON backup from the current tracker.
- Replace the site's existing `index.html` and upload/replace the manifest, service worker and icon files with the files in this package.
- Keep the exact same GitHub Pages site URL (same origin and path) if you want the browser's existing localStorage data to remain available.
- After publishing, open the site and refresh. If the old version remains visible, close the installed app/browser tab and reopen it; a service-worker update may take one reload.
- Do not delete browser site data if you need to retain player records.

## Important notes

- The app stores its tracker data in the browser on the device. A GitHub upload does not automatically synchronize player data between different devices or browsers.
- The service worker provides an offline app shell after the first successful online load. Features that require internet access (such as calendar-image OCR if used by the app) may still need a connection.
- GitHub Pages must be served over HTTPS for PWA installation and service workers.
