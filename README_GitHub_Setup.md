# Legion Tracker B9 — GitHub Pages PWA package

This package contains the tracker website, modern game-style app icons, PWA manifest, service worker, and installation guidance.

## IMPORTANT: Upload the FILES inside this extracted folder

Do not upload the enclosing folder as one nested directory. Open this folder, select every file inside it, and upload those files to the **root** of your GitHub repository. Your repository root should look like:

```
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

## Publish

1. Extract the ZIP on your computer.
2. Open the extracted `Legion_Tracker_B9_GitHub_Upload` folder.
3. Select all files INSIDE it and upload them to the repository root (not inside another folder).
4. Commit the changes to the branch selected by GitHub Pages, normally `main`.
5. In GitHub, open **Settings → Pages**. Choose **Deploy from a branch**, select `main` and `/(root)`, then save.
6. Wait for the deployment to finish.
7. Open the actual published GitHub Pages address, which starts with `https://` and usually looks like `https://USERNAME.github.io/REPOSITORY/`. Do not use the `github.com/...` repository page as the app link.

## Install on Android

1. Open the published HTTPS Pages URL directly in **Google Chrome**. Do not open it inside WhatsApp, Facebook, Gmail, or the GitHub app's built-in browser.
2. Wait for the page to finish loading while online. The app registers its service worker in the background.
3. Tap the green **Install App** button in the tracker header.
4. If Chrome provides its native install prompt, confirm it. If no native prompt is available yet, the button opens step-by-step instructions: Chrome menu `⋮` → **Install app** or **Add to Home screen**.

Chrome controls when it offers the native prompt. The app cannot force a prompt to appear if Chrome does not consider the site installable, if it is already installed, or if it is opened in an unsupported in-app browser. The manual Chrome menu option is the fallback.

## iPhone

Open the HTTPS Pages URL in Safari → Share → Add to Home Screen → Add.

## If Install App is still unavailable

- Confirm that the URL is the published `https://USERNAME.github.io/...` Pages site, not the GitHub repository page.
- Confirm `index.html`, `legion-manifest.json`, `legion-sw.js`, and all icon PNGs are in the repository root (or all in the exact same published subfolder if Pages is configured to publish that folder).
- Open the page in Chrome, not an in-app browser.
- Check GitHub **Actions** or **Settings → Pages** and wait until deployment succeeds.
- In Chrome, open the Pages URL again, refresh, and allow it to load online once.
- If an old version is cached, close the site and reopen it. The B9 service worker uses a new cache name.

## Replacing an existing tracker

1. Export a JSON backup from the current tracker first.
2. Replace the existing website files with the files from this package.
3. Keep the same GitHub Pages origin/path if you want the browser's existing localStorage records to remain available.
4. Do not clear browser site data if you need to preserve player records.

## Data note

Tracker records are stored locally in the browser on each device. GitHub Pages does not synchronize those records between users or devices automatically.


B9 visual update: Daily Tasks buttons now use bold black labels and the Daily Tasks columns use more vibrant colors. These styles are scoped to the Daily Tasks tab only; other tabs are unchanged.
