# Vandelay Industries — Quarterly Advisory Board Briefing

## Purpose

This is a **template deck**. It's an example presentation that small business owners can adapt to brief their own advisory boards. The fictional stand-in is Vandelay Industries (the deliberately vague company from Seinfeld). Every slide should be plausible-but-generic — concrete enough to be illustrative, neutral enough that any small business owner can map their own context onto it.

## Audience

Advisory board members of a small/medium business. Typical profile: 3–5 outside experts/mentors, meet quarterly, time-poor but engaged, signed up to help. They want clarity over theater, honest problems over polished updates, and they want to feel useful — which means specific asks, not vague "any thoughts?"

## Narrative mode

Informational with a dialogic spine. The deck should feel like a working document the founder is walking through — not a sales pitch. Tone: confident, honest, grounded. The board should leave feeling they know what's happening, where the founder is stuck, and what specifically they can do to help.

## Reading context

Live 60–90 minute quarterly board meeting. In-person or video. Slides should also work as a read-ahead document — board members who skim it beforehand should arrive prepared, which makes the live meeting faster.

## Design system

This deck uses an **alternate, deck-local design system** (Option A from setup discussion). DESIGN.md and deck.css live inside this deck's folder, separate from the Stella Decks shared system at `decks/styles/deck.css`. Slides in this deck link to `../styles/deck.css` (one level up), not the project-shared CSS.

## Slide arc (13 main + 6 appendix = 19 slides)

### Main deck — Quarterly Briefing (slides 1–13)

| # | Slide | File | Purpose |
|---|---|---|---|
| 1 | Cover (dark) | `slide-cover.html` | Vandelay Industries · Q3 2026 Advisory Board Briefing · [Date] |
| 2 | Agenda | `slide-agenda.html` | What we'll cover, with time markers |
| 3 | Vision / North Star (dark) | `slide-north-star.html` | Why we exist — brief reminder |
| 4 | Business Model Canvas | `slide-canvas.html` | Full Osterwalder 9-block. Cells unchanged since last quarter are grayed out; new/changed cells are highlighted. Demonstrates the canvas as a living artifact. |
| 5 | Highlights since last meeting | `slide-highlights.html` | Specific wins — what shipped, what worked |
| 6 | What's hard right now | `slide-whats-hard.html` | Honest friction — the credibility moment |
| 7 | Financial KPIs | `slide-financial-kpis.html` | 3–4 key metrics, vs target / vs prior period |
| 8 | Strategic Objectives — Now | `slide-objectives-now.html` | Review of last quarter's objectives |
| 9 | Strategic Objectives — Next | `slide-objectives-next.html` | Current/next quarter's objectives |
| 10 | Strategic Objectives — Later | `slide-objectives-later.html` | Long-term planning |
| 11 | Team / Org chart updates | `slide-team.html` | Hires, departures, structural changes |
| 12 | Focused Topic **OR** Asks | `slide-focused-topic.html` / `slide-asks.html` | Presenter chooses per quarter (see below) |
| 13 | Discussion / Q&A | `slide-discussion.html` | Close |

### Appendix — Emergency Board Meeting Template (slides 14–23)

A self-contained mini-deck demonstrating how to brief the board when something urgent comes up. Mirrors the main deck's opening (cover, agenda, vision, canvas) so the board re-anchors before the emergency content begins. Then the emergency-specific arc: situation → impact → options → recommendation → ask. Tight, decision-forward, no fluff.

| # | Slide | File | Purpose |
|---|---|---|---|
| 14 | Appendix divider (dark) | `slide-emergency-divider.html` | Marks the section break + sets emergency gravity |
| 15 | Emergency cover (dark) | `slide-emergency-cover.html` | Cover for the emergency mini-deck. Adapt date and meeting label per use. |
| 16 | Emergency agenda | `slide-emergency-agenda.html` | Time markers and structure for the emergency meeting. Adapt to fit. |
| 17 | Vision / North Star (dark) | `slide-emergency-north-star.html` | Same vision as main deck — re-anchors why this matters before facts begin |
| 18 | Business Model Canvas | `slide-emergency-canvas.html` | Same canvas as main deck — re-anchors what the business is before the emergency lands |
| 19 | The situation | `slide-situation.html` | What happened, factually — no spin |
| 20 | What's at stake | `slide-impact.html` | Financial, operational, reputational impact |
| 21 | Options considered | `slide-options.html` | What we weighed and why we ruled options out |
| 22 | Our recommendation | `slide-recommendation.html` | What we propose, with rationale |
| 23 | What we need from you | `slide-emergency-ask.html` | The decision/vote/sign-off — concrete and time-bound |

### Stand-in scenario for the appendix

The fictional emergency for Vandelay is an **unsolicited acquisition offer**: a larger competitor has sent an LOI with a 14-day response window. This is a high-stakes "positive" emergency — not every advisory board scenario is bad news, and demonstrating this case teaches founders how to use the template for opportunity-driven emergencies as well as crisis-driven ones.

## The optional slide 12

Each quarter, the presenter picks one or the other — never both:

- **Focused Topic** (`slide-focused-topic.html`) — deep-dive on a single strategic question, with the board's input solicited live
- **Asks** (`slide-asks.html`) — a bulleted list of specific board asks (intros, expertise, decisions needed)

Both files exist in the slides/ folder; only one is referenced in the manifest at any time. Switch by editing manifest.json.

## Stand-in content guidance

Vandelay Industries is deliberately vague (officially: importer/exporter, latex specifically). That ambiguity is useful — content can lean toward whatever's most adaptable for real users.

- **KPIs**: revenue, gross margin, customer count, retention rate (the universal four)
- **Wins**: shipped a feature/launched a campaign/closed a deal
- **What's hard**: hiring, a stalled customer segment, cash runway pressure (pick something universal)
- **Strategic objectives**: 2–3 per quarter, written as outcomes not activities

Mark editable placeholders with italic notes at the bottom of each slide where helpful (e.g., *"Replace with your top 3 KPIs."*).

## Status

- Folder structure: ✓ created
- BRIEF.md: ✓ written
- manifest.json: ✓ stubbed (slides referenced but not yet built)
- DESIGN.md: placeholder — to be filled in via `/design-setup`
- styles/deck.css: not yet created — `/design-setup` will produce it
- Slides: not yet built — design system first
