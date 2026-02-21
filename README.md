# SafeComment

A dark glass-style multilingual comment wall built as a single-file app (`index.html`) using Tailwind CDN + vanilla JavaScript.

## Features

- 1→4 column responsive wall layout (up to 4 columns at full width)
- Inline comment editing (same comment text becomes editable)
- Instant delete from 3-dot menu
- Like/Dislike with single-vote-per-user-per-comment logic
- Translate per comment via context menu with Indian-language priority + search
- Latest-comment glow and smooth post animation
- Local persistence with `localStorage`
- Virtualized rendering for large comment sets (performance)

## Tech

- HTML + Tailwind CSS (CDN)
- Vanilla JavaScript
- Browser `localStorage`
- Translation pipeline:
  1) Google public translate endpoint
  2) MyMemory fallback
  3) Lingva fallback

## Run locally

Just open `index.html` in your browser.

For best behavior, use a local server (optional):

```bash
# Python
python -m http.server 5500
```

Then open `http://localhost:5500`.

## Deploy with GitHub Pages (live link)

1. Push this repo to GitHub (branch `main`).
2. On GitHub: **Repo → Settings → Pages**.
3. Under **Build and deployment**:
   - Source: **Deploy from a branch**
   - Branch: **main**
   - Folder: **/(root)**
4. Save.
5. Wait 1-2 minutes. Your live URL will look like:

`https://<your-username>.github.io/<repo-name>/`

## Notes

- Comments are stored in browser localStorage (per device/browser).
- This app is static; no backend DB is used.
- If translation provider rate-limits temporarily, fallback providers are used.

## File structure

- `index.html` — full app UI + logic
- `README.md` — project docs
