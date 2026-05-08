---
version: alpha
name: Camposja Paper
description: Warm parchment portfolio — Lora serif over a textured paper background, with engineer-notebook restraint and a few quirky marks of personality.

colors:
  primary: "#2a1a08"
  secondary: "#6b5540"
  tertiary: "#7a3f1c"
  neutral: "#f5ede0"
  on-tertiary: "#f5ede0"
  text-faint: "#9c836a"
  accent-hover: "#5c2d10"
  bg-section: "#efe5d4"
  bg-card: "#f9f3e8"
  tag-bg: "#d4c3a0"
  tag-text: "#4a3320"
  border: "#c8b596"
  border-light: "#d8c9aa"
  ink-bg: "#2a1a08"
  ink-text: "#e8dcc8"
  ink-accent: "#c8956a"

typography:
  display:
    fontFamily: Lora
    fontSize: 3.2rem
    fontWeight: 600
    lineHeight: 1.15
    letterSpacing: -0.01em
  h2:
    fontFamily: Lora
    fontSize: 1.7rem
    fontWeight: 600
    lineHeight: 1.3
  h3:
    fontFamily: Lora
    fontSize: 1.1rem
    fontWeight: 600
    lineHeight: 1.3
  body:
    fontFamily: Inter
    fontSize: 1rem
    lineHeight: 1.75
  body-lg:
    fontFamily: Inter
    fontSize: 1.05rem
    lineHeight: 1.8
  body-sm:
    fontFamily: Inter
    fontSize: 0.93rem
    lineHeight: 1.7
  meta:
    fontFamily: Inter
    fontSize: 0.78rem
    lineHeight: 1.5
  label-caps:
    fontFamily: Inter
    fontSize: 0.72rem
    fontWeight: 600
    letterSpacing: 0.08em
  marginalia:
    fontFamily: Lora
    fontSize: 0.92rem
    fontWeight: 400
    lineHeight: 1.5

rounded:
  none: 0px
  xs: 2px
  sm: 3px
  md: 4px

spacing:
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 40px
  xxl: 64px
  xxxl: 96px

components:
  signal-pill:
    backgroundColor: "{colors.bg-card}"
    textColor: "{colors.secondary}"
    rounded: "{rounded.sm}"
    padding: "4px 10px"
    typography: "{typography.meta}"
  signal-pill-accent:
    backgroundColor: "{colors.tag-bg}"
    textColor: "{colors.tag-text}"
    rounded: "{rounded.sm}"
    padding: "4px 10px"
  button-primary:
    backgroundColor: "{colors.tertiary}"
    textColor: "{colors.on-tertiary}"
    rounded: "{rounded.sm}"
    padding: "8px 18px"
    typography: "{typography.body-sm}"
  button-primary-hover:
    backgroundColor: "{colors.accent-hover}"
  button-secondary:
    backgroundColor: "transparent"
    textColor: "{colors.tertiary}"
    rounded: "{rounded.sm}"
    padding: "8px 18px"
  button-secondary-hover:
    backgroundColor: "{colors.tag-bg}"
    textColor: "{colors.accent-hover}"
  card:
    backgroundColor: "{colors.bg-card}"
    rounded: "{rounded.md}"
    padding: "22px 24px"
  card-feature:
    backgroundColor: "{colors.bg-card}"
    rounded: "{rounded.md}"
    padding: "28px 30px"
  card-compact:
    backgroundColor: "{colors.bg-card}"
    rounded: "{rounded.sm}"
    padding: "16px 18px"
  tag:
    backgroundColor: "{colors.tag-bg}"
    textColor: "{colors.tag-text}"
    rounded: "{rounded.xs}"
    padding: "3px 10px"
    typography: "{typography.meta}"
  marginalia:
    textColor: "{colors.text-faint}"
    typography: "{typography.marginalia}"
  stamp:
    textColor: "{colors.tertiary}"
    typography: "{typography.label-caps}"
    padding: "8px 14px"
    rounded: "{rounded.xs}"
  divider-asterisks:
    textColor: "{colors.text-faint}"
    typography: "{typography.body}"
---

## Overview

A warm-paper portfolio — Lora serif over a parchment background. The visual
metaphor is a well-loved engineer's notebook: ink on slightly textured paper,
deliberate margins, and a few hand-marked traces of personality (asterisk
dividers, marginalia, a single stamp).

The system optimizes for three readers at once:

1. **Recruiters and hiring managers** scanning quickly for shipped work,
   stack, and a resume link.
2. **Engineering peers** looking for substance — repos, real systems, and
   credible architecture choices.
3. **Anyone curious** who wants to read for a minute and come away with a
   sense of the person.

Restraint over ornament. A reader should not notice the design before they
notice the writing.

## Colors

The palette is a single warm-paper family: deep espresso ink against parchment.
Burnt sienna is the only true accent and is reserved for interaction. There is
no pure white anywhere on the page and no pure black; every neutral has warmth
in it.

- **primary (#2a1a08):** Deep espresso — body text, headlines, the dark ink panel.
- **secondary (#6b5540):** Warm mid-brown — secondary copy, captions inside cards.
- **tertiary (#7a3f1c):** Burnt sienna — links, primary button, the only call-to-action color. Use sparingly.
- **neutral (#f5ede0):** Parchment — the main background. Pair with the SVG paper-grain noise overlay for the textured feel.
- **bg-section (#efe5d4):** Slightly deeper parchment for alternating section bands.
- **bg-card (#f9f3e8):** A touch lighter than the page — surfaces a card without needing a hard border.
- **ink-bg / ink-text / ink-accent:** The inverted palette used in the nav and footer. The dark ink panels are visual brackets for the parchment body.

## Typography

Two families. **Lora** (serif) for headlines, marginalia, and anything
emphatically "set in print." **Inter** (sans) for everything functional —
body, navigation, buttons, tags, meta. The pairing carries the
"newspaper / notebook" metaphor without leaning hard on it.

- **display:** Hero name only. Clamps responsively from 2.4rem to 3.6rem in CSS.
- **h2 (section):** 1.7rem. Each section heading sits over a hand-drawn-style
  SVG underline rather than a plain border.
- **h3:** Project and capability titles. Paired with sans `label-caps` eyebrows.
- **body / body-lg:** Default reading copy. body-lg is for hero bio and About prose.
- **body-sm:** Project descriptions, capability cards.
- **meta:** Dates, tags, inline metadata. 0.78rem.
- **label-caps:** Uppercase eyebrow labels above titles.
- **marginalia:** Italic-leaning Lora for pull-quote asides. Reserved for personality lines.

## Layout

A single 860px content column. Wide outer margins on desktop are intentional —
they hold space for marginalia asides on the left of the main column.

- **max-width:** 860px content column, 24px gutter.
- **section-gap:** 96px (`spacing.xxxl`) desktop / 60px mobile.
- **rhythm:** Sections alternate between `neutral` and `bg-section` to create
  vertical rhythm. Asterisk dividers (`* * *`) sit *inside* sections to break
  long content; section transitions use the alternating background instead.
- **marginalia placement:** On screens ≥ 1024px, a marginalia note absolutely
  positions itself in the left margin of the main column. On narrower screens
  it inlines into the flow as an italic block-quote.

## Shapes

Corners are nearly square. Real paper doesn't have rounded corners; cards use
`rounded.md` (4px) at most, and tags use `rounded.xs` (2px).

- **rounded.none (0):** Section bands, full-bleed elements.
- **rounded.xs (2px):** Tags, stamp.
- **rounded.sm (3px):** Buttons, signal pills.
- **rounded.md (4px):** Cards.

No drop shadows. Depth is communicated through background color contrast
(card sits a touch lighter than the section) and an optional 1px border in
`border-light`. Shadows would break the paper feel.

## Components

- **signal-pill:** Small horizontal chip used in the hero to surface identity
  signals (e.g., "Indie shipper", "AI agents", "Tampa"). Three to five max.
  Variants: default and `signal-pill-accent` (tan fill) for emphasis.
- **button-primary:** Burnt sienna fill. Used for the resume CTA only.
- **button-secondary:** Transparent with tan border. LinkedIn, GitHub, Email.
- **card / card-feature / card-compact:** Three project tiers. `card-feature`
  is for the headline projects (OpenClaw / QR Doorbell). `card-compact` is
  for the secondary row (Empanadas / Energy / Code Wars).
- **tag:** Stack/tooling chip inside a project card. Tan fill, dark brown text.
- **marginalia:** Italic Lora set in `text-faint`. Pulled into the left margin
  on desktop, inlined as an italic block-quote on mobile.
- **stamp:** A small, slightly-rotated decorative mark (e.g., "MADE IN TAMPA")
  near the hero. Dashed double border, uppercase label-caps,
  faintly desaturated. Use exactly one per page.
- **divider-asterisks:** `* * *` centered, in `text-faint`. Used as an
  in-section break — at most twice on the whole page.

## Do's and Don'ts

**Do**

- Treat asterisk dividers and the stamp as one-off marks of personality.
  One stamp on the page; asterisk dividers at most twice.
- Keep the burnt sienna for interaction — links and the resume button. Don't
  use it for decoration.
- Let copy breathe. The 860px column is a deliberate constraint, not a budget
  to fill.
- Use marginalia for personality lines that interrupt the technical voice
  ("Pickleballer who loves dogs and the environment.").

**Don't**

- Don't add drop shadows. Paper is flat; depth comes from color, not light.
- Don't introduce a third type family. Lora and Inter cover the system.
- Don't use pure white (`#fff`) or pure black (`#000`). Every neutral is warm.
- Don't litter quirky marks. The page can hold one stamp, two asterisk
  dividers, and one or two marginalia notes — beyond that it's costume.
- Don't justify body text. Left-align always. Justified text on parchment
  reads as "fake-old," not "lived-in."
