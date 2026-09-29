# Base44 Dev Environment

## Project type
Static HTML/CSS/JS marketing site (Bootstrap 3 template). No build step, no backend, no package manager.

## Running
```
docker compose -f docker-compose.base44.yml up -d
```
Serves the repo root via nginx:alpine on host port 3000. The CSS is pre-compiled (`css/style.css`); edits to HTML/CSS/JS are live on refresh — no recompilation needed.

## Notes
- `sass/` contains SCSS sources but the compiled `css/style.css` is committed and used directly. To restyle, edit SCSS and recompile locally, or edit `css/style.css` directly.
- `js/google_map.js` exists but is NOT referenced in `index.html`, so no Google Maps API key is needed.
- No external credentials required.
