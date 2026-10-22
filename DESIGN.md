# DESIGN.md — Connected Mate Design System

## § Color palette (from `:root` in `docs/style.css`)

| Token | Value | Use |
|---|---|---|
| `--bg` | `#f6f6f8` | Page background |
| `--surface` | `rgba(255,255,255,0.84)` | Card/surface |
| `--surface-strong` | `#ffffff` | Elevated surface |
| `--surface-soft` | `#efeff3` | Subtle fill |
| `--surface-dark` | `#151516` | Dark sections |
| `--surface-dark-soft` | `#242426` | Dark cards |
| `--text` | `#0a0a0b` | Primary text |
| `--text-muted` | `#666666` | Secondary text |
| `--text-soft` | `#8e8e93` | Tertiary / meta |
| `--accent` | `#0a0a0b` | Accent (near-black) |
| `--green` | `#2ed158` | Success / live badge |
| `--blue` | `#0a84ff` | Links / info |
| `--orange` | `#ff9f0a` | Warning / beta |
| `--purple` | `#bf5af2` | Feature highlight |
| `--red` | `#ff453a` | Error / alert |

## § Typography

- **Display font**: `-apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif` (system stack — NOT Inter)
- **Mono font**: `'IBM Plex Mono', ui-monospace, monospace` — used for branding, badges, code
- Base: `0.9375rem` / `line-height: 1.55`
- Hero heading: `clamp(2.5rem, 5.5vw, 4.5rem)` `font-weight: 700` `letter-spacing: -0.04em`
- Section heading: `clamp(1.75rem, 3.5vw, 2.75rem)` `font-weight: 700` `letter-spacing: -0.03em`
- Body large: `clamp(1.1rem, 1.8vw, 1.35rem)` `font-weight: 500` `letter-spacing: -0.015em`
- Labels / badges: uppercase `0.78rem` `letter-spacing: 0.12em` `font-weight: 600–800` (IBM Plex Mono)

## § Spacing scale

- Section gap: `clamp(4rem, 8vw, 7rem)` (`--section-gap`)
- Container: `min(1440px, calc(100% - 8vw))`

## § Border radius ladder

| Token | Value |
|---|---|
| `--radius-xl` | `32px` |
| `--radius-lg` | `24px` |
| `--radius-md` | `18px` |
| `--radius-sm` | `12px` |
| Pills | `999px` |

Do NOT use arbitrary radius values outside this ladder.

## § Motion / easings

- Default transition: `0.2s ease` (color/opacity)
- Bounce/spring (CTAs, cards): `cubic-bezier(0.34, 1.56, 0.64, 1)` 0.18s
- Loader bar: `cubic-bezier(0.05, 0.7, 0.1, 1)` 400ms
- Emil Kowalski enter: `cubic-bezier(0.16, 1, 0.3, 1)`
- Emil Kowalski exit: `cubic-bezier(0.7, 0, 0.84, 0)`

## § Responsive breakpoints

| Breakpoint | Width |
|---|---|
| Desktop XL | ≥ 1440px |
| Desktop | ≥ 1201px |
| Desktop min | ≥ 1025px |
| Tablet | 768px – 1024px |
| Mobile L | ≤ 767px |
| Mobile M | ≤ 720px |
| Mobile S | ≤ 560px |
| Mobile XS | ≤ 360px |

## § Anti-patterns (hard rules)

- **NO Inter font** — system font stack or IBM Plex Mono only
- **NO violet/indigo gradient as full-surface background**
- **NO nested cards** (`.card .card`) — flat hierarchy only
- **NO gray text on saturated color background** — check contrast
- **NO arbitrary border-radius** — use the ladder above
- **NO excessive shadows** — use `--shadow` / `--shadow-strong` tokens only

## § Component conventions

- Cards: backdrop-filter blur, `--surface`, `--radius-lg/md`, subtle `--line` border
- Badges/tags: IBM Plex Mono uppercase, tight letter-spacing, pill radius
- Sections alternate: light (`--bg`) → dark (`--surface-dark`) → light
- Hover states: subtle `transform: translateY(-2px)` + shadow deepening (spring easing)

## § Changelog

| Date | Change |
|---|---|
| 2026-06-11 | Initial DESIGN.md created during project onboarding |
