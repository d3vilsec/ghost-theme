# d3vilsec Ghost theme

Custom retro-purple Ghost theme for the d3vilsec.com blog (served at `/blog`).

## Deployment

Pushing to `main` auto-deploys to Ghost via the
[`TryGhost/action-deploy-theme`](https://github.com/TryGhost/action-deploy-theme)
GitHub Action (`.github/workflows/deploy-theme.yml`). No manual zip uploads.

### One-time setup

1. In **Ghost admin → Settings → Advanced → Integrations → + Add custom integration**
   (name it e.g. `GitHub Deploy`). Copy the **Admin API Key** and **API URL**.
2. In this repo: **Settings → Secrets and variables → Actions → New repository secret**:
   - `GHOST_ADMIN_API_URL` → `https://d3vilsec.com/blog`
   - `GHOST_ADMIN_API_KEY` → the Admin API key from step 1
3. Push to `main`. The action lints with `gscan` and uploads + activates the theme.

## Brand

- Background `#0a0a0f`, accent `#bd00ff` (neon purple), secondary `#ff00aa` / `#00ffff`
- Fonts: Press Start 2P (headings), IBM Plex Mono / Sans
- Matches the Hugo site CSS in the main repo (`assets/css/extended/retro.css`)
