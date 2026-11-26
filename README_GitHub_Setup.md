# Legion Tracker B11 — GitHub Pages PWA package

This package includes the updated Legion Tracker app, existing game-style icons, PWA manifest, service worker, and setup instructions.

## What's updated in B11

- Improved readability of item names in Shop & Resources tiles.
- Shop names wrap inside their tiles instead of overflowing.
- Removed the Last Purchase history strip and Undo button.
- Shop & Resources table entry: Enter moves down within the same column and wraps to the first entry in that column at the end.
- Players & Power entry: Enter moves right across the current player's editable fields, then to the first field of the next player.
- Existing local-storage key and tracker data model are retained.

## Upload the extracted files

**Upload the files inside this ZIP to the root of your existing GitHub repository. Do not upload the ZIP itself and do not create a nested folder.**

The repository root should contain:

```text
index.html
legion-manifest.json
legion-sw.js
legion-icon-192.png
legion-icon-512.png
legion-icon-maskable-512.png
legion-icon-180.png
favicon-32.png
.nojekyll
README_GitHub_Setup.md
```

1. Download and extract this ZIP.
2. Open the extracted folder.
3. Select all files inside it, including `.nojekyll`.
4. Upload them to the root of your existing GitHub repository.
5. Replace matching files when prompted and add new files.
6. Commit the changes to the branch used by GitHub Pages, normally `main`.
7. Wait for GitHub Pages deployment to complete.
8. Open the published HTTPS website and refresh it.

## Refresh an installed app

The service-worker cache name has been changed to B11. After deployment, open the website once while connected to the internet, refresh, then close and reopen the installed app. If the previous interface remains visible, clear the site's cached data in Chrome and reopen the published HTTPS URL.

## Data safety

B11 keeps the existing tracker storage key and data structure. Nevertheless, export a JSON backup before replacing the deployed app.

## PWA installation

Use the published HTTPS GitHub Pages URL in Chrome on Android. The in-app Install App button or Chrome menu can be used to install it. On iPhone, open the URL in Safari and use Share → Add to Home Screen.
