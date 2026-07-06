# Elektro Latosinszky – UI/UX Redesign Konzept (Webseite)

**One-Pager** (Single Page) – *Neon Voltage – Light Stage*
**Helles Grundkonzept mit einem gezielten dunklen Bühnenmoment**

> Version 2 — überarbeitet nach Open-Design-Craft-Regeln (Akzent-Disziplin,
> Typografie-Tracking, Animations-Disziplin, Anti-AI-Slop).

---

## 01 · ZIEL, ZIELGRUPPE, KERNAUSSAGE

### Zweck der Seite
- Schnell verständlich machen, **wer** Elektro Latosinszky ist und **wie** die Arbeit wirkt.
- Besucher:innen in 2 Schritten führen:
  1. **Leistungen** überfliegen und den passenden Bereich finden.
  2. **Kontakt** auslösen (Formular + direkte Kontaktdaten).

### Zielgruppe
- Privatkund:innen (Haus, Garten, Küche, Licht, Wallbox)
- Betreiber:innen kleiner bis mittelgroßer Projekte (Planung, Baustrom, Veranstaltungen)
- Personen, die verlässliche, individuelle Betreuung suchen (Einzelunternehmer-Charakter)

### Kernaussage (Ton)
**Locker, super sympathisch, professionell.** Energie/Technik: Neon/Elektrik als Designmetapher – ohne unseriös zu wirken.

---

## 02 · BRAND- & DESIGN-STORY

### Stimmung (Mood)
**Heller, offener, moderner UI-Grundton.** Die Seite lebt vom Licht — passend zum
Beruf (Beleuchtung, Lichtplanung). Dunkel gibt es nur an **einer Stelle als
Bühnenmoment**: dem CTA-Banner vor dem Kontakt, plus einem kurzen dunklen Footer,
der den Kreis schließt.

Kontrast entsteht **nicht** über viele dunkle Module, sondern über:
1. **Dichte-Wechsel** — luftige Sektionen (Hero, Über mich) wechseln mit
   kompakten (Leistungs-Grid).
2. **Karten-Elevation** — weiße Karten auf `#F2F2EF`-Flächen.
3. **Akzent-Disziplin** — Gelb taucht selten auf und wirkt dadurch stärker.

### Leitmetaphern
- **Stromkreis** = eine SVG-Verbindungslinie als Signature-Divider (Übergang zum dunklen CTA-Banner)
- **Neon-Sign** = Primary CTA mit Glow (auf dunklem Banner deutlich stärker)
- **Technik-Console** = Mono-Labels, Timeline
- **Lichtplanung** = Hero-Glow hinter der Headline, Brückenmotiv mit Lichtstimmung

### Lokaler Anker (NEU)
Die **Glienicker Brücke** (Wahrzeichen Potsdam/Babelsberg, direkt vor der
Haustür in Alt Nowawes) ist das Hero-Bildmotiv — Foto mit Schloss Babelsberg
im Hintergrund, als **Duotone** behandelt (warmes Grau + dezenter gelber
Lichtakzent), damit es sich dem hellen UI unterordnet statt zu dominieren.

---

## 03 · FARB- & KONZEPTSCHEMA

### Primärpalette (aus Logo abgeleitet)
| Farbe | Hex | Verwendung |
|-------|-----|-----------|
| 🟡 Brand Yellow | `#EAB308` | Nur Füllungen: Primary CTA, Chips |
| 🟡 Yellow Light | `#FACC15` | Hover/Soft-States, Icon-Tint |
| 🟤 Accent Text | `#A16207` | Gelb als **Text** (Labels, Links-Hover) — besteht 4.5:1 auf hellem Grund |

**Akzent-Budget (verbindlich):** max. **2 sichtbare Gelb-Verwendungen pro
Screen** — typisch: 1 Section-Label + 1 Primary CTA. Links sind neutral
(`#111113` mit Unterstreichung), nicht gelb.

### UI Foundation (hell — trägt 90% der Seite)
| Farbe | Hex | Verwendung |
|-------|-----|-----------|
| ⬜ Page Background | `#F6F6F4` | Off-white Seitengrund |
| ⬜ Card Surface | `#FFFFFF` | Karten, Formular |
| ⬜ Elevated Surface | `#F2F2EF` | Sektions-Flächen, Nav |
| ⬜ Borders | `#E6E6E1` | Hairlines, Trennlinien |

### Dunkler Bühnenmoment (nur CTA-Banner + Footer)
| Farbe | Hex | Verwendung |
|-------|-----|-----------|
| ⬛ Dark Stage BG | `#18181B` | CTA-Banner, Footer |
| ⬛ Dark Stage Card | `#1E1E22` | Flächen im dunklen Modul |
| ⬛ Dark Stage Border | `rgba(255,255,255,0.08)` | Semi-transparente Hairlines statt solider dunkler Borders |
| ⬜ Dark Stage Text | `#FAFAFA` | Primärtext auf dunklem Grund |
| 🔘 Dark Stage Muted | `#A1A1AA` | Sekundärtext auf dunklem Grund |

### Textsystem
| Farbe | Hex | Verwendung |
|-------|-----|-----------|
| ⬛ Primary Text | `#111113` | Headlines, wichtiger Content |
| 🔘 Secondary Text | `#4A4A52` | Body, Beschreibungen |
| 🔘 Muted Text | `#6B6B76` | Labels, Meta-Info |

### Gestrichen (Craft-Korrektur)
Electric Cyan und Hot Magenta entfallen. **Ein Akzent** (Gelb) reicht —
mehrere Akzentfarben verwässern die Wiedererkennung und brechen die
Akzent-Disziplin.

### Glow-Logik
- Heller Hero: ein einziger warmer Glow `rgba(234,179,8,0.18)` hinter der Headline
- Dunkler CTA-Banner: Neon-Glow am Primary CTA `rgba(234,179,8,0.40)`
- Sonst: keine Glows

---

## 04 · TYPOGRAFIE & HIERARCHIE

### Fonts
- **Headlines / Retro Bold:** `Bebas Neue`
- **Body / Lesbarkeit:** `Inter`
- **Labels / Tech-Details:** `JetBrains Mono`

### Typo-Skala (Richtwerte)
- **H1:** `clamp(44px, 6vw, 72px)`
- **H2:** `clamp(30px, 3.2vw, 44px)`
- **Section Title:** `clamp(28px, 2.8vw, 38px)`
- **Card Titles:** 18–20px
- **Body:** 16–18px, max. Zeilenlänge `65ch`
- **Small Labels / Meta:** 12–14px

### Tracking-Regeln (verbindlich, aus craft/typography.md)
| Kontext | Letter-Spacing |
|---------|---------------|
| Display/H1 (Bebas Neue) | `-0.01em` bis `-0.02em` |
| ALL-CAPS-Labels (Mono) | `0.08em` — **nie ohne Tracking** |
| Button-Text | `0.02em` |
| Body | `0` |

### Gewichte (3-Gewichte-System)
- **400** Body · **550** Labels/Nav · **600** Buttons/Card-Titles
- Kein 700+; Bebas Neue trägt die Headline-Wirkung über Größe, nicht Gewicht.

### Semantische Regeln
All-Caps nur für: Section-Labels (Mono), Eyebrow, H1-Headline (Bebas Neue ist
inhärent caps). Nirgendwo sonst.

---

## 05 · LAYOUT & INFORMATIONSARCHITEKTUR (One-Pager)

### Navigation (Sticky Header, hell)
- Links: **Logo** (EL-Monogramm, `assets/images/logo.png`) + Sektionen (Leistungen, Über mich, Kontakt)
- Rechts: CTA-Button **«Jetzt anfragen»**

### Content Flow (Sections) — NEU: Light Stage

| Nr. | Sektion | Modus | Charakter |
|-----|---------|-------|-----------|
| 1 | Hero (Intro + Brückenmotiv) | ☀️ HELL | Luftig, Glow-Akzent, Duotone-Bild |
| 2 | Leistungen (6 Cards) | ☀️ HELL | Kompakt, weiße Karten auf `#F2F2EF` |
| 3 | Über mich (Story + Timeline + Foto) | ☀️ HELL | Luftig, editorial |
| 4 | CTA-Banner (Zwischenruf) | 🌑 DUNKEL | **Der eine Bühnenmoment** |
| 5 | Kontakt (Formular + Kontaktdaten) | ☀️ HELL | Weiße Formular-Karte, einladend |
| 6 | Footer | 🌑 DUNKEL | Kurz, erdend, schließt den Kreis |

**Rhythmus:** Hell → Hell → Hell → **Dunkel** → Hell → **Dunkel**.
Der dunkle CTA-Banner ist der einzige Kontrastbruch im Content-Flow und wirkt
dadurch stärker als vorher. Der Übergang Hell→Dunkel wird vom
Stromkreis-Signature-Moment inszeniert (siehe 10).

---

## 06 · KOMPONENTEN-SPEZIFIKATION

### 6.1 Buttons

**Primary Button (Neon CTA)**
- Hintergrund: `#EAB308` · Text: `#111113` · Radius: 12px · Padding: 14px 24px
- Hover (150ms): `translateY(-2px)` + `box-shadow: 0 0 0 4px rgba(234,179,8,0.18), 0 12px 30px rgba(234,179,8,0.18)`
- Press: `translateY(0)` bei 100ms
- Auf dunklem CTA-Banner: Glow `rgba(234,179,8,0.40)` → Neon-Effekt

**Secondary / Ghost Button**
- Transparent, Border `1px solid #E6E6E1` (hell) / `rgba(255,255,255,0.15)` (dunkel)
- Hover: Border `#A16207`, Text `#A16207`

### 6.2 Service Cards (Leistungen)
- BG `#FFFFFF` · Border `1px solid #E6E6E1` · Radius 14px · Padding 24px
- Icon: **monoline SVG, 1.6px Stroke, `currentColor`** — keine Emojis
- Icon-Container: `#FACC15` Soft-Tint (zählt nicht ins Akzent-Budget, da Flächen-Tint < 15% Sättigung)
- Hover (200ms): Border-Shift zu `#EAB308`, sanftes Shadow-Pop, kein Left-Border-Accent (AI-Tell)
- Card-Text: Title 18–20px/600, Description 15–16px, line-height 1.6

### 6.3 Section-Labels (Console-Style)
- Mono: `01` + Wort (z.B. «LEISTUNGEN»), Tracking `0.08em`
- Dünne Hairline daneben, Farbe `#A16207`

### 6.4 Hero (Signature — HELL)

**Design-Elemente**
- Hintergrund: `#F6F6F4` mit sehr subtilem Stromkreis-Grid (Hairlines, Opacity ≤ 0.05)
- Ein warmer Glow `rgba(234,179,8,0.18)` hinter der Headline
- **Brückenmotiv rechts:** Glienicker Brücke mit Schloss Babelsberg
  (`assets/images/hero-glienicker-bruecke.jpg`), als Karte (Radius 14px),
  **Duotone-Behandlung** (Grayscale + warmer Gradient-Overlay), Mono-Caption
  «GLIENICKER BRÜCKE · POTSDAM-BABELSBERG»

**Hero Copy**
- Eyebrow: Monoline-SVG-Blitz (1.6px Stroke) + `ELEKTRO LATOSINSZKY` (Mono, Tracking 0.08em) — **kein Emoji**
- H1: **STROM MIT STIL.** (Bebas Neue, Tracking -0.02em)
- Subtext: «Dein Elektriker in Potsdam-Babelsberg. Von der Steckdose bis zum Lichtkonzept – zuverlässig, kreativ, persönlich.»

**Hero CTAs**
- Primary: «Jetzt anfragen»
- Secondary Link: «Leistungen ansehen» (neutral, mit Pfeil-Micro)

### 6.5 Logo-Einbindung
- Nav: `logo.png` klein (Monogramm-Bereich), `mix-blend-mode: multiply` (weißer PNG-Grund verschwindet auf hellem BG)
- Dunkler Footer: `filter: invert(1)` + `mix-blend-mode: screen` (Marke erscheint weiß)

---

## 07 · INHALTE (WEB-OPTIMIERT)

### Leistungen (6)

1. **Beleuchtung** – Individuelles und exklusives Lichtkonzept nach persönlichem Geschmack – Garten, Küche oder Party.
2. **E-Mobilität** – Beratung zu Lademöglichkeiten: Wallbox-Auswahl, Anschluss und Anmeldung beim Netzbetreiber.
3. **Installation** – Elektroinstallationen aller Art in Alt- und Neubau – vom Hausanschlusskasten bis zur Steckdose.
4. **Baustrom** – Maßgeschneiderte Lösungen: Berechnung, Anmeldung und Inbetriebnahme von Baustromverteilern.
5. **Prüfung / Wartung** – Prüfung nach VDE 0100-600 / VDE 0105-100. Reparaturen und Fehlerbeseitigungen.
6. **Veranstaltungen** – Professionelle Beleuchtungsplanung für Events – basierend auf Erfahrung als Oberbeleuchter bei Film und Fernsehen.

### Über mich (Werdegang)

**Inhaber:** Andreas Latosinszky – Ihr Elektriker in Potsdam und Umgebung
**Foto:** `assets/images/andreas-latosinszky.png`

**Timeline:**
- `1990` – Ausbildung als Elektroinstallateur (Mainz)
- `1992` – Staatlich geprüfter Techniker (Mainz)
- Festanstellungen als Elektrotechniker beim ZDF und den Schott Glaswerken
- Tätigkeit als Oberbeleuchter bei Film und Fernsehen
- Erwerb des TREI-Zertifikats und Gründung des eigenen Elektrobetriebs

> «Als Einzelunternehmer steht zeitnahe, individuelle Betreuung im Vordergrund – von der einzelnen Steckdose bis zum Großprojekt. Breites Dienstleistungsspektrum mit zuverlässigem, verbindlichem, freundlichem und professionellem Service.»

---

## 08 · KONTAKT (HELLES MODUL — NEU)

Der Kontaktbereich ist **hell**: Das Formular liegt als weiße Karte auf
`#F2F2EF` — offen und einladend statt dramatisch. Das Drama hat der
CTA-Banner davor bereits geliefert.

### Formular-Felder
- Name (Pflicht)
- E-Mail (Pflicht)
- Nachricht (Pflicht)
- Optional: Telefonnummer (empfohlen für Rückruf)
- Datenschutz-Checkbox (Pflicht)

### Formular UX
- Klassische Labels (barrierearm)
- Focus State: Ring `#A16207`
- Input-BG: `#FFFFFF` · Border: `#E6E6E1`
- Success: Inline Toast «Danke! Wir melden uns zeitnah.»
- Fehler: pro Feld, klar benannt

### Kontaktinfos
- Telefon: `0331-70427910`
- E-Mail: `info@e-lato.de`
- Adresse: `Alt Nowawes 85, 14482 Potsdam-Babelsberg`

### Map
- Google Maps Embed (Light Mode), Radius 14px, nur nach Consent laden

---

## 09 · SOCIAL PROOF

### Social Links
- Instagram: [@elektro_lato](https://www.instagram.com/elektro_lato)
- TikTok: [@elektro_lato](https://www.tiktok.com/@elektro_lato)
- [LinkedIn](https://www.linkedin.com/in/elektrolatosinszky)
- [Xing](https://www.xing.com/profile/Andreas_Latosinszky)

---

## 10 · INTERAKTION & ANIMATION (überarbeitet nach craft/animation-discipline.md)

> Motion nur, wo sie Zustand oder Raumwechsel kommuniziert — nie als Dekoration.
> Alle Werte verbindlich.

### Timing-System
| Interaktion | Dauer | Easing |
|-------------|-------|--------|
| Button Hover/Press | 100–150ms | `cubic-bezier(0.2, 0, 0, 1)` |
| Card Hover | ≤200ms | `cubic-bezier(0.2, 0, 0, 1)` |
| Scroll-Reveal | 300–400ms | `cubic-bezier(0.2, 0, 0, 1)` |
| Signature-Linie | ~600ms | linear (stroke-dashoffset) |

### Scroll-Reveal
- Cards und Timeline Items: fade + `translateY(12px)`, staggered (60ms Versatz)
- Nur beim ersten Eintritt, kein Loop

### Micro-Interactions
- Card-Hover: Border-Shift + Shadow (Motion bestätigt Fokus)
- Links: Underline-Animation left-to-right, 150ms
- Buttons: 2px Lift + Glow

### Signature Moment (einer!)
**Stromkreis-Linie** als SVG am Übergang Sektion 3 → CTA-Banner: die Linie
«zeichnet sich» beim Scrollen (stroke-dashoffset) und «zündet» den dunklen
Banner. Ein Moment mit Bedeutung (Hell→Dunkel = Strom fließt) statt vieler
dekorativer Effekte.

### Reduced Motion
Bei `prefers-reduced-motion: reduce`: alle Transforms entfallen,
Zustandswechsel nur als Opacity-Crossfade. Signature-Linie erscheint statisch.

---

## 11 · RESPONSIVE VERHALTEN

### Breakpoints
- Mobile: < 640px
- Tablet: 640–1023px
- Desktop: 1024–1279px
- Large: ≥ 1280px

### Anpassungen
- Hero: Bild unter Copy auf Mobile
- Leistungen: 3 Spalten Desktop, 2 auf Tablet, 1 auf Mobile
- Über mich: 1 Spalte auf Mobile (Bild oben), 2 Spalten auf Desktop
- Kontakt: Form über Info auf Mobile, 2 Spalten auf Desktop

---

## 12 · ACCESSIBILITY (WCAG AA+)

- **Kontrast-Gates:** Body ≥ 4.5:1, Large Text ≥ 3:1, UI-Komponenten ≥ 3:1.
  Gelb `#EAB308` nie als Text auf hellem Grund — dafür `#A16207`.
- **Keyboard Navigation:** alle CTAs/Links erreichbar
- **Semantisches HTML:** header/nav/main/section/footer
- **Focus Styles:** sichtbar (nicht weg-rendern)
- **Reduced Motion:** siehe 10

---

## 13 · ENTWICKLUNGS-HINWEISE (CURSOR)

### Empfohlene Tech Basis
- Next.js (Vercel) + Tailwind + Framer Motion
- Formular per serverless (z.B. Resend/Formspree)
- HTML-Prototyp: self-contained `index.html`, `data-od-id` auf editierbaren Elementen

### Komponentenliste
- `Navbar`, `Hero`, `Services`, `ServiceCard`
- `About`, `TimelineItem`
- `Contact`, `ContactForm`
- `Footer`, `SocialLink`
- `SectionLabel`, `NeonButton`
- `CircuitDivider` (Signature-SVG)
- `DarkStage` (Wrapper nur für CTA-Banner + Footer)

### Content-Integration
- Leistungen als Datenarray (title/description/icon)
- Timeline als Datenarray (year/text)
- Kontakt als config object

---

## 14 · BILD- & ILLUSTRATIONS-ASSETS

| Asset | Pfad | Quelle/Lizenz |
|-------|------|---------------|
| Logo (EL-Monogramm + Wortmarke) | `assets/images/logo.png` | e-lato.de (eigene Marke) |
| Hero: Glienicker Brücke + Schloss Babelsberg | `assets/images/hero-glienicker-bruecke.jpg` | Wikimedia Commons, **CC BY-SA 3.0** — Attribution im Footer nötig |
| Portrait Andreas Latosinszky | `assets/images/andreas-latosinszky.png` | e-lato.de (eigenes Foto) |
| Altes Header-Bild (Referenz) | `assets/images/_source-alte-seite-header.jpg` | e-lato.de |

- Service-Icons: Inline SVG, monoline 1.6px Stroke, `currentColor`
- Stromkreis-Grid + Signature-Linie: Inline SVG/CSS
- Keine externen Bild-CDNs (Unsplash etc.)

---

## 15 · ZUSAMMENFASSUNG

- **Hell-dominantes Konzept** (5 von 6 Sektionen hell) mit **einem dunklen Bühnenmoment** (CTA-Banner) + dunklem Footer
- Lokaler Anker: **Glienicker Brücke** als Duotone-Hero-Motiv
- Wiedererkennung über **Section-Labels + diszipliniertes Akzentgelb** (max. 2×/Screen)
- Signature Moment: **eine Stromkreis-Linie** am Hell→Dunkel-Übergang
- Craft-fest: Tracking-Regeln, Kontrast-Gates, Animations-Timing, keine AI-Tells
- Klarer Conversion-Flow: Leistungen → CTA-Banner → Kontaktformular
