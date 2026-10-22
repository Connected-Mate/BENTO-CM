# CLAUDE.md — BENTO-CM (Connected Mate)

<!-- agentation:rules:begin -->
## Règles & équipe du projet — maintenu par Agentation
_Partagé via GitHub pour que **tout agent** (Claude Code, Codex, OpenCode, Antigravity, Cursor, Gemini…) travaille de la même façon. Bloc géré automatiquement — ne pas éditer à la main ; source complète : `docs/agentation/rules.md`._

### Équipe
_Personne renseigné pour l'instant._

### Comment ce projet fonctionne
# Règles du projet

_Comment ce projet fonctionne — vos agents s'y réfèrent pour travailler de la même façon._
<!-- agentation:rules:end -->

## Project purpose
Static GitHub Pages website for Connected Mate — Alexandre Cormeraie's ecosystem:
AI conferences/keynotes, tech podcast (100+ episodes), privacy-first iOS/macOS apps.
Live at: https://alex-connected-mate.github.io/BENTO-CM/

## Stack
- **Pure static HTML/CSS/JS** — no build system, no npm, no framework
- Fonts: IBM Plex Mono (monospace branding) + system sans-serif (-apple-system stack)
- Deployed to GitHub Pages; `docs/` is the web root

## Entry points
- `docs/index.html` — homepage (FR, default)
- `docs/en/` — English mirror
- `docs/style.css` — single global stylesheet (design tokens at top `:root {}`)
- `docs/ascii-canvas.js` — ASCII animated background on hero

## Key pages
| File | Purpose |
|---|---|
| `docs/index.html` | Homepage |
| `docs/apps.html` | Apps catalogue |
| `docs/blog.html` | Blog index |
| `docs/about.html` | About page |
| `docs/services.html` | Services |
| `docs/keynotes.html` | Conferences/keynotes |
| `docs/pock.html` | Pock app page |
| `docs/dys-keyboard.html` | Dys Keyboard app page |
| `docs/notetaker-ai.html` | Notetaker AI app page |
| `docs/better-dictate.html` | Better Dictate app page |

## Build & test
- **No build step** — edit files directly under `docs/`
- **Preview**: open `docs/index.html` in a browser, or serve with `python3 -m http.server 8080 --directory docs`
- **No automated tests** — visual QA only

## Naming conventions
- CSS classes: BEM-ish kebab-case (`.hero-section`, `.cs-card`, `.trust-band`)
- IDs: kebab-case (`#primary-nav`, `#ascii-canvas`)
- Files: lowercase kebab-case (`dys-keyboard.html`, `notetaker-ai.html`)

## Forbidden / don't touch
- `docs/en/` — English translations, keep in sync with FR changes
- `.git/` — never edit manually
- No npm/package.json — do not add build tooling without explicit request

## Git branch convention
- Main branch: `claude/bento-connected-mate-gVqqK`
- Worker task branches: `agentation/task-<first-8-chars-of-taskId>`

## Languages
- Primary: French (`lang="fr"`)
- Secondary: English (`docs/en/`)
- Copy must be consistent across both when changed
