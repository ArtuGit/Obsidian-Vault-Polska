# Polska from Artu. Obsidian Vault, powered by Quartz.

Obsidian notes about learning Polish, published with [Quartz 4](https://quartz.jzhao.xyz/). Keep adding or editing Markdown files and Quartz will handle the navigation automatically.

## Structure

- `content/` — all public notes. Drop any `.md` file here and Quartz will include it.
- `quartz/`, `quartz.config.ts`, `quartz.layout.ts` — the engine and theme settings.
- `.github/workflows/deploy.yml` — GitHub Actions workflow that builds and deploys from the `main` branch.

## Local development

```bash
npm install         # once
npm run dev         # build + run local server
```

The site is served at `http://localhost:8080/` with hot reload.

## Publishing to GitHub Pages

1. Push the repo to GitHub (e.g. `artu/Polska`).
2. In **Settings → Pages** choose **GitHub Actions** as the source.
3. Every `git push` to `main` runs `.github/workflows/deploy.yml`, which:
   - executes `npm ci`,
   - builds via `npm run build` (outputs to `public/`),
   - publishes through `actions/deploy-pages`.

If you host in another repo, update `homepage`/`repository` in `package.json` and `baseUrl` in `quartz.config.ts` (currently `artu.github.io/Polska`).

## Adding new notes

1. Create a file in `content/` (e.g. `content/slownictwo.md`).
2. Use Obsidian-style wikilinks `[[note-name]]` — Quartz resolves them automatically.
3. Commit and `git push`.

Quartz will refresh the navigation, latest notes list, graph, and search index without additional configuration.

