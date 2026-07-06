# Elektro Latosinszky — Neon Voltage · Light Stage

> Design system for the Elektro Latosinszky one-page landing site.
> Source: `01_Konzept/Elektro_Latosinszky_UI_Konzept_Hell.md` (v2, Light Stage)
> Open Design baseline: `open-design-v0.13.0`

## Visual Theme & Atmosphere

Hell, offen, modern — die Seite lebt vom Licht (passend zum Beruf: Beleuchtung, Lichtplanung). Retro-Neon-Charakter nur in Akzent-Details. Dunkel existiert an genau einer Stelle als Bühnenmoment (CTA-Banner) plus kurzem dunklen Footer. Kontrast über Dichte-Wechsel und Karten-Elevation, nicht über dunkle Flächen. Stimmung: locker, sympathisch, professionell.

Lokaler Anker: Glienicker Brücke (Potsdam-Babelsberg) als Duotone-Hero-Motiv.

## Color Palette & Roles

### Tokens
- `--bg: #F6F6F4` — Seitengrund (off-white, nie `#fff`)
- `--surface: #FFFFFF` — Karten, Formular
- `--surface-alt: #F2F2EF` — Sektions-Flächen, Nav
- `--border: #E6E6E1` — Hairlines
- `--fg: #111113` — Headlines, Primärtext
- `--fg-secondary: #4A4A52` — Body
- `--muted: #6B6B76` — Labels, Meta
- `--accent: #EAB308` — NUR Füllungen (Primary CTA, Chips)
- `--accent-soft: #FACC15` — Hover, Icon-Tints
- `--accent-text: #A16207` — Gelb als Text/Labels (besteht 4.5:1 auf hell)

### Dark stage (nur CTA-Banner + Footer)
- `--dark-bg: #18181B`
- `--dark-card: #1E1E22`
- `--dark-border: rgba(255,255,255,0.08)` — semi-transparente Hairlines
- `--dark-fg: #FAFAFA`
- `--dark-muted: #A1A1AA`

### Accent-Budget (verbindlich)
Max. **2 sichtbare Akzent-Verwendungen pro Screen** (typisch: 1 Section-Label + 1 Primary CTA). Links sind neutral (`--fg` + Underline). Keine zweite Akzentfarbe — Cyan/Magenta sind gestrichen.

### Glow
- Hero (hell): ein Glow `rgba(234,179,8,0.18)` hinter der Headline
- CTA-Banner (dunkel): Neon-Glow `rgba(234,179,8,0.40)` am Primary CTA
- Sonst keine Glows

## Typography Rules

- **Display:** `'Bebas Neue', 'Arial Narrow', sans-serif` — Tracking `-0.02em`
- **Body:** `'Inter', -apple-system, system-ui, sans-serif`
- **Mono:** `'JetBrains Mono', ui-monospace, monospace` — Labels, Timeline, Captions

Scale: H1 `clamp(44px,6vw,72px)` · H2 `clamp(30px,3.2vw,44px)` · Section Title `clamp(28px,2.8vw,38px)` · Card Title 18–20px · Body 16–18px (max `65ch`) · Small 12–14px

Tracking (verbindlich): ALL-CAPS-Labels `0.08em` · Buttons `0.02em` · Display `-0.02em` · Body `0`.
Gewichte: 400 (Body) / 550 (Labels, Nav) / 600 (Buttons, Card-Titles). Kein 700+.
All-Caps nur: Section-Labels, Eyebrow, H1.

## Component Stylings

### Primary Button (Neon CTA)
BG `--accent`, Text `--fg`, Radius 12px, Padding 14px 24px, Tracking 0.02em.
Hover (150ms): `translateY(-2px)` + `box-shadow: 0 0 0 4px rgba(234,179,8,.18), 0 12px 30px rgba(234,179,8,.18)`. Auf dunklem Banner: Glow 0.40.

### Ghost Button
Transparent, Border `1px solid var(--border)` (dunkel: `rgba(255,255,255,0.15)`). Hover: Border+Text `--accent-text`.

### Service Card
BG `--surface`, Border `1px solid var(--border)`, Radius 14px, Padding 24px.
Icon: monoline SVG 1.6px Stroke `currentColor` in `--accent-soft`-Tint-Container. Keine Emojis, kein Left-Border-Accent.
Hover (≤200ms): Border → `--accent`, sanftes Shadow-Pop.

### Section Label
Mono `01 LEISTUNGEN`, Tracking 0.08em, Farbe `--accent-text`, Hairline daneben.

### Form Inputs (hell)
BG `--surface`, Border `--border`, Focus-Ring `--accent-text`, klassische Labels.

### Hero-Bild
`assets/images/hero-glienicker-bruecke.jpg` als Karte (Radius 14px), Duotone: `filter: grayscale(1)` + warmer Gradient-Overlay (multiply). Mono-Caption. CC BY-SA 3.0 Attribution im Footer.

### Logo
`assets/images/logo.png` (dunkelgrau auf weiß). Nav: `mix-blend-mode: multiply`. Dunkler Footer: `filter: invert(1)` + `mix-blend-mode: screen`.

## Layout Principles

One-Pager, Rhythmus Hell → Hell → Hell → **Dunkel** → Hell → **Dunkel**:
1. Hero — hell (Copy links, Duotone-Brückenbild rechts)
2. Leistungen (6 Cards, 3-spaltig) — hell, kompakt
3. Über mich (Story + Mono-Timeline + Foto) — hell, luftig
4. CTA-Banner — **dunkel** (der eine Bühnenmoment)
5. Kontakt (weiße Formular-Karte + Infos) — hell
6. Footer — dunkel, kurz

Sticky Nav hell: Logo + Sektionen links, CTA «Jetzt anfragen» rechts.
Max-width ~1200px. Section spacing 80px Desktop / 48px Tablet / 32px Mobile.
Dichte-Wechsel: luftig (Hero, Über mich) vs. kompakt (Leistungen).

## Depth & Elevation

Minimal. Karten flach mit Hairline-Border; Hover: leichtes Shadow-Pop. Hero: subtiles Stromkreis-Grid (Opacity ≤ 0.05) + ein Glow. Kein Glassmorphism, keine dekorativen Blobs/Waves, kein AI-Gradient.

## Motion

| Interaktion | Dauer | Easing |
|---|---|---|
| Button Hover/Press | 100–150ms | `cubic-bezier(0.2,0,0,1)` |
| Card Hover | ≤200ms | `cubic-bezier(0.2,0,0,1)` |
| Scroll-Reveal (fade + 12px translateY, 60ms Stagger) | 300–400ms | `cubic-bezier(0.2,0,0,1)` |
| Signature: Stromkreis-Linie (stroke-dashoffset) | ~600ms | linear |

Genau ein Signature Moment: SVG-Stromkreislinie am Übergang zu Sektion 4 (Hell→Dunkel = Strom fließt). `prefers-reduced-motion: reduce`: Transforms entfallen, nur Opacity-Crossfades, Linie statisch.

## Do's and Don'ts

- ✅ Hell als Grundton, ein dunkler Bühnenmoment
- ✅ Akzent-Budget einhalten (max. 2× Gelb pro Screen)
- ✅ Monoline-SVG-Icons (1.6px, currentColor) — nie Emojis als Icons
- ✅ ALL-CAPS immer mit ≥0.06em Tracking
- ✅ Echte Inhalte aus dem Konzept — kein Lorem Ipsum
- ❌ Kein `#6366f1`/Indigo, kein Purple-Blue-Gradient
- ❌ Keine Rounded Card mit farbigem Left-Border
- ❌ Keine erfundenen Metriken («10× schneller»)
- ❌ Keine externen Bild-CDNs (Unsplash, placehold.co)
- ❌ Gelb nie als Text auf hellem Grund (dafür `--accent-text`)

## Responsive Behavior

- Mobile < 640px: 1 Spalte, Hero-Bild unter Copy, Padding −33%
- Tablet 640–1023px: Leistungen 2-spaltig
- Desktop ≥ 1024px: Leistungen 3-spaltig, Über mich + Kontakt 2-spaltig
- Large ≥ 1280px: max-width greift

## Agent Prompt Guide

Beim Generieren von Artefakten:
- Lies zuerst `01_Konzept/Elektro_Latosinszky_UI_Konzept_Hell.md` für vollständige Inhalte (Leistungen, Timeline, Kontakt).
- Farbtokens sind verbindlich — keine neuen Hex-Werte. Akzent-Budget: max. 2× Gelb pro Screen.
- Tech-Ziel: Next.js + Tailwind + Framer Motion. HTML-Prototyp: self-contained `index.html` mit `data-od-id`.
- Hero: Eyebrow = SVG-Blitz + `ELEKTRO LATOSINSZKY` (Mono), H1 `STROM MIT STIL.`, Brückenbild als Duotone-Karte.
- Kontakt: Tel `0331-70427910`, E-Mail `info@e-lato.de`, `Alt Nowawes 85, 14482 Potsdam-Babelsberg`.
- Footer: CC BY-SA 3.0 Attribution für das Brückenfoto (Wikimedia Commons).
- Conversion-Flow: Leistungen → CTA-Banner → Kontaktformular.
