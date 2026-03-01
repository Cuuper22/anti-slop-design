# anti-slop-design

Claude Code skill that makes AI stop generating the same looking website every time.

You know the look — purple gradient hero, Inter font, three equal columns, rounded everything, a testimonial carousel nobody asked for. Every AI tool generates the same design because they all trained on the same data.

This skill gives Claude actual design opinions instead of the default "make it look modern" autopilot.

## What it does

Intercepts design requests and applies **domain-aware tokens** instead of generic defaults:

| Domain | You get | Instead of |
|--------|---------|------------|
| **Fintech** | Navy/institutional, Plus Jakarta Sans, 8px radius, subtle shadows | Purple gradient, Inter, "modern" look |
| **Healthcare** | Calming teal, Outfit headings, 12-16px radius, breathing space | Same purple gradient, dense layout |
| **Devtools** | Dark-first, Geist Mono, 1px borders, dot-grid texture | ...still that purple gradient |
| **Ecommerce** | Warm cream, Cormorant Garamond, 0px radius, editorial whitespace | You get the pattern |
| **Education** | Vibrant green, Nunito, bouncy animations, reward gold | |
| **Media** | Warm off-white, Playfair Display, 65ch body width, pull quotes | |
| **Government** | Pure white, Noto Sans, 0px radius, zero decorative animation | |
| **Creative** | Vermillion + purple, Clash Display, asymmetric layouts, grain textures | |

## 67 files across 7 platforms

```
references/       17 docs — platform guides, anti-patterns, accessibility
templates/         18 starters — React, HTML, SwiftUI, Compose, Electron, Tauri, CLI, PDF, email
assets/            23 files — CSS tokens, SVG textures, font stacks, domain token JSONs
scripts/            3 — validation (178 checks), domain-map generator, eval generator
evals/              1 — 12 test prompts covering all domains × platforms
```

Platforms: web-react, web-landing, web-artifacts, mobile-native, CLI/TUI, PDF/print, email.

## Install

Copy the skill folder to your Claude Code skills directory:

```bash
# Clone
git clone https://github.com/Cuuper22/anti-slop-design.git

# Copy to Claude Code skills
cp -r anti-slop-design ~/.claude/skills/anti-slop-design
```

Claude reads `SKILL.md` as the entry point, then routes to the right references and templates based on your prompt.

## How it works

1. **SKILL.md** — Hub document with the Design Thinking Protocol and 15-rule Anti-Slop Checklist
2. **domain-map.json** — 8 structured domain profiles with full color palettes (OKLCH), typography, shape, motion tokens
3. **references/** — Platform-specific field manuals (React, landing pages, mobile native, CLI, email, etc.)
4. **templates/** — Starter code with `/* THEME */` injection points for domain tokens
5. **assets/** — CSS foundations (fluid type scale, spacing scale, motion tokens), SVG textures, font stacks

The `/* THEME */` markers in templates are where domain tokens get applied — same template, different domain = fundamentally different output.

## Validation

```bash
bash scripts/validate-skill.sh
# 178/178 checks passing
```

Checks file existence, JSON validity, minimum line counts, section headers, CSS custom properties, SVG validity, theme markers, and domain token schema compliance.

## The anti-pattern bible

`references/anti-patterns.md` catalogs every convergence pattern in AI-generated design. If you're curious why everything looks the same, start there.

## License

MIT
