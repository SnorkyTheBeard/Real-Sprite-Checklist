SPRITE CHECKLIST — PERMANENT HEADER CACHE FIX

Upload these four files to the ROOT of your GitHub repository and choose Replace:
- art-config.js
- service-worker.js
- index.html
- app.js

WHAT THIS FIX DOES
- Changes the current header URL to main-header.webp?v=3 so the latest image loads now.
- Bumps the service-worker cache from v45 to v46, deleting the stale image cache.
- Registers service-worker.js?v=46 so browsers detect the update promptly.
- Makes everything inside assets/header/ and assets/page-backgrounds/ network-first.
- Uses cache:no-cache when checking those folders, while keeping cached copies for offline fallback.

FUTURE HEADER UPDATES
Keep replacing:
assets/header/main-header.webp

You will not need to rename the image or edit art-config.js each time. The updated service worker will check GitHub for the newest file before using its cached fallback.

After uploading, wait for GitHub Pages to finish, then fully close and reopen the site once so service worker v46 activates.
