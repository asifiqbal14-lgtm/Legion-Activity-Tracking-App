# Legion Tracker B13 — GitHub Pages PWA package

This package includes the updated Legion Tracker app, existing game-style icons, PWA manifest, service worker, and setup instructions.

## What's updated in B13

- Added a Pilot Focus box immediately after the player filter.
- Added a category-grouped pilot dropdown in SSR, SR, R, N order, with alphabetical pilot names in each category.
- Pilot Focus shows each pilot's current Stars and Upgrade status, editable dropdowns, basic attributes, and passive skill highlighted in purple.
- Added a Hide/Show control for Pilot Badges, Pieces, and Training Guides inventory cards; the preference is remembered on that device.
- Added the supplied SSR unlock, evolution, and upgrade criteria. Unknown SSR 4-star and 9th/10th upgrade requirements remain explicitly marked as not provided and are not guessed.
- Added the supplied N Pilot evolution and upgrade criteria. N Pilot Awakening cost remains marked as not provided.
- Changed completed Done checklist buttons to a dark tone with white text; Not Done cross buttons are unchanged.
- Existing B11 shop tile, keyboard navigation, install support, themes, and app data model are retained.

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
8. Open the published HTTPS website once while connected to the internet, then close and reopen the installed app.

## Data safety

B13 retains the existing `legionTrackerV1` local-storage key and does not intentionally reset existing player or PMS records. Export a JSON backup before replacing the deployed app.

## PWA installation

Use the published HTTPS GitHub Pages URL in Chrome on Android. The in-app Install App button or Chrome menu can be used to install it. On iPhone, open the URL in Safari and use Share → Add to Home Screen.
