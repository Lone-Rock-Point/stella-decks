# Design System

## Brand

**Stella Decks — Editorial display on a modern sans infrastructure.**

Positioning: Slides that read like paper, not software. Serif headlines carry weight and authority; geometric sans body keeps everything else modern and exact. A single warm terracotta accent directs the reader's attention where it matters.

## Voice

**Confident. Quiet. Contemporary.**

The reader should feel like they're being addressed by someone who knows exactly what they want to say and trusts the ideas enough not to dress them up. No ornament. No decoration. Just structure, type, and one spot of color where it counts.

## Color Palette

Warm minimalism — paper-warm backgrounds, soft-black ink, one restrained terracotta accent. Nothing is pure black or pure white; everything has a trace of warmth.

| Token | Hex | Usage |
|-------|-----|-------|
| `--ink` | `#1A1A1A` | Soft-black. Dark slide backgrounds, headline text on light slides |
| `--ink-light` | `#2E2E2E` | Secondary dark for supporting emphasis |
| `--coral` | `#B6470E` | **Brand terracotta.** The single accent — key stats, emphasized words, highlights |
| `--coral-soft` | `#E8A79B` | Lighter terracotta tint — section labels on dark backgrounds |
| `--warm-bg` | `#FAF8F3` | Paper-warm off-white. Primary light slide background |
| `--warm-bg-alt` | `#F2EDE5` | Slightly deeper warm — zone backgrounds, subtle cards |
| `--slate` | `#5A5A5A` | Body text on light slides |
| `--slate-light` | `#B8B2A8` | Body text on dark slides, secondary metadata |
| `--white` | `#FFFFFF` | Card surfaces on light slides, text on dark |

### Accent rule

**One editorial spot of terracotta per slide, maximum.** It marks the single most important word, stat, or signal. If you can't decide what deserves it, the slide has too much happening. Never use it as a large background fill.

Section labels (`.section-label`) are structural chrome — they use `--coral` by default and don't count against the one-spot rule. The rule applies to editorial choices: the `<em>` in a headline, a key stat, a highlighted number.

## Typography

Two families, each with one job. **DM Serif Display** carries every headline — high-contrast, bracketed serifs, strong editorial presence. **Inter** handles everything else — body, labels, UI, data. The tension between the two is the design.

```
@import url('https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=Inter:wght@400;500;600;700&display=swap');
```

| Token | Family | Usage |
|-------|--------|-------|
| `--serif` | `'DM Serif Display', Georgia, serif` | All display headlines, large stat numbers, pull quotes |
| `--sans` | `'Inter', sans-serif` | Body, UI, captions, data, labels |

### Size scale

| Size | Use |
|------|-----|
| 72px | Cover tagline |
| 64px | Section divider title |
| 56px | Hero company name, close logo |
| 48px | Summary / section headlines |
| 42px | Argument-tier headline (default for narrative slides) |
| 36px | Data-tier headline (dense slides) |
| 26–32px | Subheadlines, large quote text |
| 16–18px | Body copy |
| 13–14px | Card labels, secondary text |
| 11–12px | Section labels, small metadata (uppercase, tracked) |

### Weight rules

**DM Serif Display** ships in a single weight (400) with italic. No bold, no light — the typeface's high stroke contrast does the work. Never apply `font-weight: bold` to serif headlines.

**Inter** (sans):
- `400` Regular — body, long-form
- `500` Medium — subtle emphasis, labels, bios
- `600` Semibold — uppercase section labels, card titles
- `700` Bold — rare; reserved for data-table emphasis or specific UI moments

### Tracking

- Serif headlines: `-0.5px` to `-2px` (tighter as sizes grow — DM Serif Display is naturally open, needs tightening at display sizes)
- Body (Inter): default
- Uppercase sans labels: `+1px` to `+2.5px` (open them up for legibility)

### Italic

DM Serif Display's italic is a real italic (not an oblique) with distinct letterforms. Use it as an editorial gesture: the emphasized word inside a headline (with terracotta color), or a pull quote. Inter italic is avoided — if you need emphasis in body text, use color or weight.

## Slide Rhythm

Light is default. Dark is punctuation. Not strict alternation.

| Slide type | Background | Why |
|------------|-----------|-----|
| Opening cover | `--ink` | Sets the tone. Dark = weight |
| Section dividers | `--ink` | Chapter breaks. Let the reader breathe |
| Body slides (most) | `--warm-bg` | Where the argument lives |
| Data / stats | `--warm-bg` | Tables need contrast and calm |
| Hero / case study | `--ink` | Dramatic proof moments |
| Split-quote slides | Half dark, half light | Two voices in dialogue |
| Closing slide | `--ink` | Echo the cover. Bookend |

If you find yourself placing two dark body slides in a row, ask whether one should be light.

## Spacing

Whitespace is structural. It creates hierarchy without ornament.

| Tier | Y padding | X padding | Use |
|------|-----------|-----------|-----|
| Argument (default) | `56px` | `80px` | Narrative, hero, section slides |
| Data | `48px` | `64px` | Dense tables, multi-column data |
| Cover / Close | `72px` | `80px` | Maximum breathing room |

**Card gaps:** 24–32px between cards in a grid. Never less than 20px.

**Density philosophy:** Density flexes with subject. A hero slide should feel spacious (one idea, massive type). A stat slide should feel measured (4 cards, breathing room). A data table should feel exacting (every row matters). Never force uniformity — let each slide be as sparse or as packed as its content demands.

## Design Principles

1. **Typography carries the design.** Size, weight, and tracking do the work. When something looks weak, make the headline bigger before adding decoration.

2. **One spot of color per slide.** The terracotta marks the single most important thing. If you can't pick one, you have too many.

3. **Whitespace is structural, not decorative.** Let slides breathe. A slide with room to breathe communicates confidence; a crowded slide communicates anxiety.

4. **Density flexes with subject.** Don't make the data slide sparse to match the hero. Make the hero sparse and the data slide exact.

5. **Borders are 1px and structural.** They divide zones — they don't decorate. Shadows, heavy rules, and ornamental borders have no place here.

## What NOT to Do

- **Never** use terracotta as a large background fill. It's an accent.
- **Never** use more than one display size per slide. One headline, not two competing.
- **Never** add drop shadows for "depth." This design is flat. Depth comes from contrast and type.
- **Never** use gradients on primary elements. Gradients live only in hero image overlays.
- **Never** mix multiple accent colors. Terracotta is the only accent — no green for positive, no red for negative. Use weight or position for semantic difference.
- **Never** use ornamental borders (double lines, dashed, curly brackets). A 1px horizontal rule and whitespace do the job.
- **Never** cram to fit. If content doesn't fit, split the slide or edit the content. Don't shrink the type.

## Component Aesthetics

**Cards**
- Background: `--white` on light slides, `rgba(255,255,255,0.03)` on dark
- Border: `1px solid rgba(0,0,0,0.04)` on light, `0.5px solid rgba(255,255,255,0.06)` on dark
- Border-radius: `8px` — just enough to feel modern, not soft
- No shadows. Flat or nothing.

**Tables**
- Horizontal rules only. No vertical lines, no cell backgrounds.
- Header: uppercase, tracked, `--slate` color, 2px bottom border in `--ink`
- Rows: 7–8px vertical padding minimum, subtle `rgba(0,0,0,0.06)` separators
- Key numbers use `--coral` with `tabular-nums`

**Emphasis**
- Inside headlines: wrap the key word in `<em>` — terracotta color + italic
- In body: `<strong>` for weight-based emphasis
- Never use background highlights, underlines, or boxes for emphasis

**Section labels**
- Uppercase, 11–12px, letter-spacing 2–2.5px, weight 600
- `--coral` on light slides, `--coral-soft` on dark
- Always above the headline, 2–4 words max

**Numbers and stats**
- Display stats use `--serif` (Inter Tight) at 40–56px
- Key numbers take `--coral`
- Labels: 13px, `--slate`, weight 500
