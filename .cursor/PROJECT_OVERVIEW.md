# Project Overview

## Goal
Publish the Obsidian-based “Polska” grammar notes as a Quartz 4 site hosted through GitHub Pages. Quartz handles nav/link generation automatically, so keeping notes up to date just means committing Markdown files.

## Layout
- `content/` — Markdown sources pulled straight from the vault (`index.md`, `powitanie.md`, `czesci-mowy.md`, `przypadki.md`, etc.). Add more files here to expose new pages.
- `quartz/`, `quartz.config.ts`, `quartz.layout.ts`, `tsconfig.json` — Quartz engine and visual configuration.
- `.github/workflows/deploy.yml` — CI job that builds (`npm run build`) and deploys the `public/` folder to GitHub Pages on every push to `main`.
- `.obsidian/` — local editor metadata; ignored from the public build by `ignorePatterns` in `quartz.config.ts`.

## Local workflow
```
npm install         # first run
npm run dev         # build + serve with hot reload on http://localhost:8080
```

Quartz writes the static output to `public/` (ignored by git). When ready, commit changes and `git push` — the Pages workflow handles publication automatically. Update `<github-username>` placeholders inside `quartz.config.ts` and `package.json` once the final repo path is known.

