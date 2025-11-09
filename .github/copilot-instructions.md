## Quick context

- This repository currently contains only `README.md` and a Git history. The project is a small static "Landing Page" (see `README.md`) and does not include HTML/CSS/JS sources yet.
- Primary goal for an AI agent: make productive, low-risk contributions (scaffold site, add CI or GitHub Pages config, or improve README) and explain assumptions in PRs.

## What I should know before editing

- Treat this as a static site / frontend-only project unless new server files appear. There are no build scripts, package manifests, or tests in the repo root.
- When adding files, prefer minimal, self-contained changes (e.g., add `index.html`, `assets/`, or `package.json`) and include a short README update that documents run/build steps.

## Useful patterns and examples for this repo

- README usage: `README.md` contains project description. If you add scaffolding, update `README.md` to show how to serve the site locally:

  - Example (PowerShell):

    ```powershell
    python -m http.server 8000
    # or, if node tooling is added:
    npm install && npm run start
    ```

- GitHub Pages: If you add `index.html` at the repository root or `docs/`, prefer GitHub Pages publishing (branch `main` or `gh-pages`) and document the choice in the PR.

## Editing and PR guidance (what to include in your changes)

1. Keep changes minimal and reversible. If you add scaffolding, include one small example page (`index.html`) and an `assets/` folder with a placeholder image or CSS.
2. Update `README.md` with run instructions and a short explanation of what you added and why.
3. In PR description, include:
   - Files added/changed and their purpose.
   - How to run locally (PowerShell commands for Windows).
   - Any assumptions made (for example: "I added a simple CSS reset and placeholder content because the repo had no UI files").
4. Regla de commits: cada cambio que haga un agente se debe commitear y subir a GitHub con un mensaje de commit en español. Puede usar prefijos tipo Conventional Commits (`feat:`, `fix:`, `chore:`) pero la descripción debe estar en español.

  Ejemplos de mensajes de commit (en español):

  - `feat: agregar index.html y assets iniciales`
  - `docs: actualizar README con instrucciones de despliegue en PowerShell`
  - `chore: añadir .github/copilot-instructions.md`

  Subir (push) al repositorio después de commitear y abrir un PR si el cambio es más que trivial.

## When to ask for human review

- Major changes: adding a build system (npm, webpack, Vite), changing site structure, or introducing external APIs. Leave a clear migration plan and roll-back steps.
- Styling/UI decisions that affect branding or copy—ask the repository owner.

## Small checklist to follow on trivial PRs

- [ ] Files are descriptive and minimal (`index.html`, `assets/`, optional `package.json`).
- [ ] `README.md` updated with run steps and a one-line summary of changes.
- [ ] PR description documents assumptions and local test steps (PowerShell examples preferred).

## Example commit/PR titles (use these formats)

- feat: add initial `index.html` scaffold and local serve notes
- chore: add `.github/copilot-instructions.md` with repo guidance
- docs: update `README.md` with run instructions

## If you can't find expected files

- Stop making large design changes. Instead, open a draft PR or create a small scaffold and explicitly mention missing artifacts (e.g., "no `package.json` found — added minimal `package.json` to enable local dev; revert if not desired").

---
If anything in this guidance is unclear or you'd like me to prefer Spanish for all edits and messages, tell me and I'll iterate on this file.
