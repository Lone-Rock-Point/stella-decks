# Design System — Vandelay Industries Advisory Board Briefing

This is a deck-local design system, intentionally distinct from the shared Stella Decks editorial style. Slides in this deck link to `../styles/deck.css` (deck-local), not `../../styles/deck.css` (project-shared).

## Brand

**Operator Energy. A working document, not a pitch deck.**

Positioning: A board briefing template that reads like a thoughtful founder talking through their quarter — not a vendor selling. Headlines feel like essay titles, body copy feels like working prose. The deck is one continuous cream-toned document held together by warm restraint.

## Voice

**Three adjectives:** honest, grounded, working.

The reader should feel: *"This founder is telling me the truth. They know what's hard. They know what they need from me. I'm here to help, not to be impressed."*

Avoid: pitch-deck polish, marketing language, exclamation points, hype words ("game-changing," "revolutionary"), corporate hedging ("we believe," "going forward").

Lean into: specifics, numbers in context, plain admission of what's hard, direct asks.

## Color Palette

Warm cream foundation. Single sage accent used sparingly. Deep ink for content. No pure black, no pure white except where cards need to lift.

| Token | Hex | Usage |
|-------|-----|-------|
| `--ink` | `#1C1C1C` | Headlines, primary content text on cream slides |
| `--ink-light` | `#3A3A3A` | Secondary headline weight, sub-headers |
| `--warm-dark` | `#1C1810` | Dark slide background (cover, vision/north star). Warm undertone to pair with cream as a tonal sibling. |
| `--sage` | `#6B7F5C` | THE accent — section labels, key numbers, single italic emphasis per slide, hairline rules under labels |
| `--sage-soft` | `#A8B69A` | Lighter sage — used for accents on dark slides where mid-value sage loses legibility |
| `--cream` | `#F5F1E8` | Main slide background on cream slides; primary text color on dark slides |
| `--cream-alt` | `#EDE7DA` | Emphasis cards, "highlighted" canvas cells, callout backgrounds |
| `--cream-dim` | `rgba(245,241,232,0.65)` | Secondary text on dark slides |
| `--slate` | `#5A5A5A` | Body text on cream |
| `--slate-light` | `#8A8580` | Secondary text, captions, slide numbers, "grayed out" canvas cells |
| `--white` | `#FFFFFF` | Cards that need to lift visually — sparingly |
| `--rule` | `rgba(28,28,28,0.10)` | Hairline borders on cream slides |
| `--rule-dark` | `rgba(245,241,232,0.15)` | Hairline borders on dark slides |

**The accent rule:** Sage appears **once per slide** as a deliberate moment. Section label, or one key number, or one italic phrase — never all three. If two things on a slide are sage, one of them is wrong.

## Typography

**Headlines:** Source Serif 4 — a contemporary serif with a warmer, less stuffy feel than Tiempos. Available on Google Fonts.

**Body:** Inter — neutral, friendly, reads cleanly at small sizes.

```
@import url('https://fonts.googleapis.com/css2?family=Source+Serif+4:ital,opsz,wght@0,8..60,400;0,8..60,600;0,8..60,700;1,8..60,400;1,8..60,600&family=Inter:wght@400;500;600;700&display=swap');
```

### Size scale

| Element | Size | Weight | Notes |
|---------|------|--------|-------|
| Argument headline | 38px | 600 | Most slides. Source Serif. Tight letter-spacing (-0.4px). Line-height 1.2. |
| Data headline | 30px | 600 | KPI / canvas / table-heavy slides. |
| Cover headline | 64px | 600 | Cover only. Stand-alone moment. |
| Section label | 11px | 600 | Sage, uppercase, letter-spacing 1.6px. |
| Body large | 18px | 400 | Vision/north star, "what's hard" prose. Line-height 1.55. |
| Body | 15px | 400 | Default body. Line-height 1.6. |
| Body small | 13px | 400 | Card captions, sub-text. |
| Editor note (italic) | 12px | 400 italic | The "*Replace with your top 3 KPIs*" placeholder hints. Slate-light color. |
| Slide number | 11px | 500 | Slate-light. Lowercase "03 / 13" format. |

### Headline rules

- Headlines end with a period. They're complete thoughts, like essay titles.
- Lowercase headlines are allowed and encouraged on emotional/honest slides ("what's hard right now."). Use sentence case for structural slides ("Strategic objectives — Now.").
- `<em>` inside headlines renders italic + sage. Use it once per slide max for emphasis.

## Slide Rhythm

**Dark slides are section openers. That's the only thing they do.**

This is the system's most distinctive choice. Dark slides exist only to mark a transition and establish gravity — never as decoration, never mid-flow.

The example deck has five dark slides, all following this rule:

1. **Cover** (slide 1) — opens the main deck
2. **Vision / North Star** (slide 3) — opens the body of the quarterly briefing
3. **Appendix divider** (slide 14) — opens the emergency-briefing mini-deck
4. **Emergency cover** (slide 15) — opens the emergency mini-deck itself
5. **Emergency vision** (slide 17) — opens the body of the emergency briefing

The appendix mirrors the main deck's rhythm because it *is* a self-contained mini-deck. Same opener pattern repeats: dark cover → cream re-anchor (agenda) → dark vision → cream content. If you add another mini-deck in the future, it gets its own dark cover and vision; everything else stays cream.

Every other slide is cream. The cream slides are not a presentation; they're a document. Inflection within the cream stretch comes from content density, not contrast — some slides are sparse (what's hard), some are dense (canvas, KPIs). Both are valid.

### Dark slide rules (cover + vision only)

- Background: `--warm-dark` (#1C1810). Slightly warmer than pure black; tonal sibling of cream.
- Primary type: `--cream` (#F5F1E8). High contrast, but the warm tone preserves cohesion.
- Secondary type: `--cream-dim` (cream at 65% opacity).
- Accent: `--sage-soft` (#A8B69A) — mid-value sage loses legibility on warm-dark, so accents lift to the lighter sage tone.
- Hairline rules: `--rule-dark` (cream at 15% opacity).
- The slide number on dark slides uses `--cream-dim` and remains lowercase format (`01 / 13`).

## Spacing

```
--pad-argument-y: 64px;   /* generous vertical breathing for prose slides */
--pad-argument-x: 88px;   /* wide horizontal margin */
--pad-data-y: 48px;       /* tighter for data slides */
--pad-data-x: 64px;       /* tighter for data slides */
--gap-card: 20px;         /* gap between cards in a grid */
--gap-section: 32px;      /* gap between major sections within a slide */
```

**Density philosophy:** Asymmetry is allowed and encouraged. Not every slide needs to fill the canvas. The "what's hard right now" slide can have 60% empty cream. The Business Model Canvas slide will use every pixel. Both are valid.

## Component Aesthetics

### Cards

- Border: 1px solid `--rule`
- Border-radius: 6px (small, restrained — not pill-shaped)
- Background: `--white` for default cards, `--cream-alt` for emphasis cards
- Padding: 24px
- **No shadows.** Ever. Cards lift through border + background contrast, not drop-shadow.

### Tables

- Row dividers: 1px solid `--rule` (no zebra striping)
- Row padding: 14px vertical, 16px horizontal
- Header row: section-label styling (uppercase, sage, 11px)
- Numeric columns: tabular-nums + right-aligned

### Hairline rules

A 1px sage rule directly under section labels is the deck's recurring visual signature. Width is constrained (40–60px), not full-width. Like the underline on an essay's chapter title.

### Emphasis

- **Italic + sage** for editorial emphasis inside headlines (one per slide)
- **Bold** for data emphasis inside body copy (sparingly, ideally just numbers)
- **Sage** for ONE key number per data slide (the headline number — never multiple)

### Slide numbers

Lowercase format: `03 / 13`. Slate-light color. Bottom-right corner, 24px from edges. Quiet, document-like — not "slide 3 of 13" formality.

## Design Principles

1. **Type carries the design.** Headlines do the work. When in doubt, make the headline more confident and remove decoration.

2. **Cream over white.** White is for cards that need to lift. Everything else is cream. The warm tone holds the deck together — even the dark slides use a warm-dark that's a sibling of cream, not a contrast stranger.

3. **One sage moment per slide.** The accent appears once, intentionally, to draw the eye. If two things are sage, one of them is wrong.

4. **Honesty over polish.** If a slide reads too smooth, it doesn't sound like the founder talking. Embrace plainspoken phrasing. Asymmetry is fine where it serves the message.

5. **Dark slides are section openers, never decoration.** Cover and vision in any briefing — and the same pattern repeats inside any mini-deck (like the appendix). Inflection in the cream stretch comes from content, not contrast.

## What NOT to Do

- **Never use dark slides as decoration.** Dark is reserved for section openers — cover and vision in any briefing. Mini-decks within the deck (like the appendix) repeat the same pattern with their own cover and vision. A dark slide in the middle of a content flow reads as presentation theatre — and this isn't theatre.
- **Never use card shadows.** Borders only.
- **Never use sage as a background fill for large areas.** It's a needle, not a wall.
- **Never set headlines in all-caps.** The voice is conversational. SHOUTING isn't.
- **Never use exclamation marks in slide copy.** The deck's tone is grounded.
- **Never use bullet points without thinking.** A short paragraph or single bolded number often beats a list.
- **Never use stock-deck phrases.** No "key takeaways," "going forward," "circle back." Plain language only.
- **Never let a slide do two things.** If you're tempted to add a second idea, that's a second slide.
