# References — Table of Contents

> The field manual index. Every reference doc, what it covers, when to reach for it.
> If you're Claude and you're reading this: start here, then go deep.

---

## Core System

| File | What It Covers | When to Use |
|------|---------------|-------------|
| [`anti-patterns.md`](anti-patterns.md) | The AI Slop Bible — convergence patterns, detection heuristics, counter-techniques | Every single time. Read first, design second |
| [`color-systems.md`](color-systems.md) | OKLCH primer, 3-tier token architecture, palette generation, dark mode | Picking colors, building palettes, theming |
| [`typography.md`](typography.md) | Font selection per domain, fluid scales, vertical rhythm, pairing rules | Any text styling, font choices, type scale work |

## Web Platform

| File | What It Covers | When to Use |
|------|---------------|-------------|
| [`web-react.md`](web-react.md) | React/Next.js stack, component libraries, code patterns, View Transitions | React apps, SaaS dashboards, Next.js projects |
| [`web-landing.md`](web-landing.md) | Section anatomy, hero patterns, social proof, CTA strategy | Marketing pages, landing pages, product sites |
| [`web-artifacts.md`](web-artifacts.md) | Claude.ai artifact constraints, single-file patterns, domain adaptation | Artifact mode specifically — different rules apply |

## Data & Motion (Phase 3)

| File | What It Covers | When to Use |
|------|---------------|-------------|
| `dataviz.md` | Chart defaults, color-blind palettes, grid/axis styling | Any data visualization, charts, graphs |
| `animation-motion.md` | Duration scales, easing tokens, reduced-motion, meaningful motion | Animations, transitions, micro-interactions |
| `layout-spacing.md` | Fluid spacing scale, grid systems, container queries, density tokens | Page layout, spacing, responsive patterns |

## Native Platforms (Phase 4)

| File | What It Covers | When to Use |
|------|---------------|-------------|
| `mobile-native.md` | iOS/Android HIG mapping, platform tokens, safe areas | Native mobile apps (Swift/Kotlin) |
| `mobile-crossplatform.md` | React Native/Flutter token bridging, platform-aware components | Cross-platform mobile (RN, Flutter) |
| `desktop.md` | Electron/Tauri patterns, system tray, native menu integration | Desktop apps |

## Documents & CLI (Phase 5)

| File | What It Covers | When to Use |
|------|---------------|-------------|
| `cli-terminal.md` | ANSI color mapping, TUI layout, progress patterns, domain-aware prompts | Terminal UIs, CLI tools |
| `pdf-print.md` | CMYK considerations, print stylesheets, PDF generation tokens | Print, PDF, physical output |
| `email.md` | Email client constraints, inline styles, dark mode in email | HTML emails, newsletters |

---

## Reading Order

**New to the system?** Go: `anti-patterns.md` → `color-systems.md` → `typography.md` → platform-specific ref

**Building a React app?** Go: `web-react.md` → check domain in `../domain-map.json` → grab template from `../templates/web/`

**Making an artifact?** Go: `web-artifacts.md` → `../templates/web/artifact-react.jsx` → adapt

**Quick domain lookup?** Skip all this, go straight to `../domain-map.json`

---

*Phase 3-5 files listed above are placeholders — they'll exist when those phases ship.*
