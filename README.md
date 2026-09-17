# MinePlan

A browser-based planner for Minecraft builds — draw floor plans block by block,
set block heights, and see the result as a 3D isometric preview.

Built by Chase and son. One self-contained HTML file: no build step, no
dependencies, no server code. It also works offline if you just open the file.

## Live site

https://igotdvds.github.io/mineplan/

Unlisted — reachable by link, told not to appear in search results
(`noindex` + `robots.txt`). Not password-protected.

## Publishing an update

1. Open `index.html` here on GitHub and click the pencil (Edit).
2. Change **one line** near the top — line 9:

   ```html
   <meta name="mineplan-build" content="2026-09-17.1">
   ```

   Bump it to today's date, e.g. `content="2026-10-04.1"`. Add `.2`, `.3` for
   more than one change in a day.
3. Paste in the new file contents, then **Commit changes**.
4. Live in about 30 seconds.

Anyone with the old version open gets a "A newer version is ready" bar at the
bottom. Clicking **Save & reload** autosaves their build first, then loads the
new version — bypassing the browser cache.

If you forget to bump that line, nothing breaks. The banner just won't appear,
and a normal refresh still picks up the change within about ten minutes
(GitHub Pages caches HTML for 600 seconds).

## Files

| File | Why it's here |
|---|---|
| `index.html` | The whole app. |
| `robots.txt` | Keeps the site out of search engines. |
| `.nojekyll` | Stops GitHub trying to process the site as a Jekyll blog. |
| `README.md` | This file. |

## Where builds are saved

- **Autosave** — every 15 seconds into the browser's local storage, and again
  when the tab is hidden. Per-browser, per-device; not synced anywhere.
- **Save / Save As** — writes a real `.mineplan.json` file you can back up,
  email, or keep in a folder.
- **Share Link** — packs the whole build into the URL itself (compressed).
  No server involved. Long builds can exceed what a URL holds; the app says so
  and tells you to send the file instead.

Browser storage is not a backup. For anything you'd be sad to lose, hit Save.

## Version history

See the commit list on this repo — every upload is a restore point. To go back,
open the file, click **History**, pick a version, and copy it forward.
