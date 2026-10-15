# Arcade Hub — Cloudflare Pages

A static HTML-game dashboard with the supplied Raft game bundled in `games/raft/index.html`.

## Deploy to Cloudflare Pages
1. Extract this ZIP.
2. In Cloudflare, open **Workers & Pages** → **Create** → **Pages** → **Upload assets** (direct upload).
3. Upload the extracted `cloudflare-games-dashboard` folder's contents (the folder containing `index.html`, `_headers`, and `games/`).
4. Deploy. No build command is needed; the build output directory is the project root.

You can also connect this folder to a Git repository and use Pages with no framework/build command and `.` as the output directory.

## Features
- Bundled Raft HTML game.
- Search and sort the library.
- Favorites saved in browser localStorage.
- Import multiple `.html` games into browser IndexedDB.
- Play in an overlay, restart, and request fullscreen.
- Responsive layout for desktop and mobile.

## Important notes
- Imported games are stored in the browser that imported them. They do **not** upload to Cloudflare or sync between devices.
- For games with separate asset files (images, audio, JS, CSS), upload the whole game folder to your site and link its `index.html`; a single-file import is best for self-contained HTML games.
- If a game needs external network access, that game's own dependencies still need to be reachable.
- This is a static Pages dashboard; no secrets or server-side API are required.
