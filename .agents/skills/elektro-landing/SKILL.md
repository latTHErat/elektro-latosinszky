---
name: elektro-landing
description: |
  Build the Elektro Latosinszky one-page landing site (Neon Voltage – Light Stage design).
  Uses DESIGN.md tokens, light-first layout with one dark stage module, and content from 01_Konzept/.
  Use when building, prototyping, or implementing the Elektro Latosinszky website,
  landing page, or Next.js components for this project.
triggers:
  - "elektro latosinszky"
  - "elektro landing"
  - "strom mit stil"
  - "neon voltage"
od:
  mode: prototype
  platform: desktop
  scenario: marketing
  preview:
    type: html
    entry: index.html
  design_system:
    requires: true
    sections: [color, typography, layout, components]
  craft:
    requires: [typography, color, anti-ai-slop, animation-discipline, accessibility-baseline]
  outputs:
    primary: index.html
  capabilities_required:
    - file_write
---

# Elektro Latosinszky Landing (Light Stage)

Build the one-page site for Elektro Latosinszky following Open Design v0.13.0 craft and this project's `DESIGN.md`.

## Before writing code

1. Read `DESIGN.md` in the project root — color, typography, motion, and component tokens are binding.
2. Read `01_Konzept/Elektro_Latosinszky_UI_Konzept_Hell.md` for full copy, section structure, and UX details.
3. For HTML prototypes, read `../web-prototype/assets/template.html` and `../web-prototype/references/layouts.md`.
4. Apply craft references from `craft/` when relevant: typography, color, anti-ai-slop, animation-discipline, accessibility-baseline.

## Section order (one-pager, light-first)

| # | Section | Mode |
|---|---------|------|
| 1 | Hero (copy + duotone bridge image) | light |
| 2 | Leistungen (6 service cards) | light |
| 3 | Über mich (story + timeline + photo) | light |
| 4 | CTA-Banner | **dark — the only stage moment** |
| 5 | Kontakt (white form card + details) | light |
| 6 | Footer | dark, short |

## Assets

- Logo: `assets/images/logo.png` — nav via `mix-blend-mode: multiply`; dark footer via `filter: invert(1)` + `mix-blend-mode: screen`
- Hero image: `assets/images/hero-glienicker-bruecke.jpg` (Glienicker Brücke + Schloss Babelsberg) — duotone treatment (grayscale + warm overlay), rounded card, mono caption. **CC BY-SA 3.0 — attribution required in footer.**
- Portrait: `assets/images/andreas-latosinszky.png` for Über mich

## Implementation modes

**HTML prototype (fast preview):** Self-contained `index.html`, inline CSS, `data-od-id` on editable elements.

**Next.js production (target stack):** Next.js + Tailwind + Framer Motion. Components: `Navbar`, `Hero`, `Services`, `ServiceCard`, `About`, `TimelineItem`, `Contact`, `ContactForm`, `Footer`, `SectionLabel`, `NeonButton`, `CircuitDivider`, `DarkStage`. Content as data arrays in `src/data/`.

## Hard rules

- All colors from DESIGN.md — no invented hex values. Accent budget: max 2 visible yellow uses per screen (section label + primary CTA).
- Yellow `#EAB308` only as fill; yellow text uses `#A16207`.
- Only sections 4 and 6 are dark (`#18181B`); everything else light.
- Hero: eyebrow = monoline SVG bolt (1.6px stroke) + `ELEKTRO LATOSINSZKY` (mono, 0.08em tracking) — no emoji. H1 `STROM MIT STIL.` (Bebas Neue, -0.02em).
- Primary CTA everywhere: `Jetzt anfragen`
- 6 Leistungen exactly as in the Konzept (Beleuchtung, E-Mobilität, Installation, Baustrom, Prüfung/Wartung, Veranstaltungen) with monoline SVG icons.
- Motion per DESIGN.md timing table; one signature moment (circuit line stroke-draw at the light→dark transition); respect `prefers-reduced-motion`.
- WCAG AA contrast gates.

## Self-check

- [ ] Light/dark rhythm matches section table (only 4 + 6 dark)
- [ ] Accent budget respected per screen
- [ ] ALL-CAPS labels have ≥0.06em tracking
- [ ] Contact data correct (phone, email, address)
- [ ] Social links: Instagram, TikTok, LinkedIn, Xing
- [ ] CC BY-SA attribution for bridge photo in footer
- [ ] Responsive at 375px, 768px, 1440px
- [ ] No lorem ipsum, no emoji icons, no AI-tell aesthetics
