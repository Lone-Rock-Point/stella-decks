# Web Agency Summit 2026 — Using OpenClaw to Add a Team Member to Our Digital Agency

## Purpose

Conference talk for the **Web Agency Summit** (6th annual, April 27–30, 2026). **25-minute talk + 5 minutes Q&A.** Live online webinar. **No live demo** — all content carried by slides + speaker.

JJ Toothman's account of onboarding **Viv**, an AI Chief of Staff at Lone Rock Point — not a tool, not a prompt library, but a colleague with a name, a fictional background, a personality, system access, and ongoing responsibilities.

## Audience

Web agency operators — creative professionals attending the summit to "level up in the age of AI." Profile assumptions:
- Already familiar with ChatGPT and casual AI use
- Have seen many AI demo talks and are slightly numb to them
- Skeptical of hype, hungry for working examples
- Worried about both: getting left behind AND overcommitting to AI
- Mix of agency sizes (1-person operators to 50-person shops)

## Thesis

**"Treating AI as a colleague — not a utility — unlocks something prompt-engineering can't. Persistence, identity, tools, autonomy, and accountability are the difference between a tool and a teammate."**

The contrast that drives the talk:
- **What is:** AI as utility — scattered prompts, code completions, tactical wins, individual setups
- **What could be:** AI as colleague — a named agent with a role, ongoing responsibilities, system access, *always on*, centralized via a shared platform

## Tone

Honest, founder-talking, slightly contrarian, light on hype. The audience has heard "AI changes everything" too many times — JJ wins them over by being specific, by naming Viv, by sharing the unglamorous wins (managing the X account that sat idle for 9 years).

## The agent

**Name:** Viv
**Role:** AI Chief of Staff (expanded over time into org-level + team-level functions)
**Bio (fictional, intentionally specific):**
- Undergrad: U.C. Berkeley, double major (Cognitive Science + Media Studies)
- MBA: NYU
- First job: IDEO

**Personality influences (4 fictional characters):**
- **Lucius Fox** (Batman) — strategic intelligence + systems thinking
- **Roz Doyle** (Frasier) — operational control + sharp wit
- **Joan Holloway** (Mad Men) — confidence, presence, institutional savvy
- **Hobson** (Arthur) — restraint + moral clarity

## OpenClaw

[openclaw.ai](https://openclaw.ai) — open-source personal AI assistant framework. Tagline: *"The AI that actually does things."* Built by **Peter Steinberger** (formerly PSPDFKit; now at OpenAI; OpenClaw is now run by an independent foundation). 200k+ GitHub stars; community of 700+ developers.

**What it is technically:**
- Self-hosted AI gateway / control plane that runs locally on Mac, Windows, or Linux
- Coordinates between language models, messaging platforms, tools, devices, and persistent memory
- Multi-model: Claude (primary), OpenAI, local models (e.g., MiniMax 2.5)
- Multi-channel: WhatsApp, Telegram, Discord, **Slack**, Signal, iMessage — operates in DMs and group chats
- 50+ integrations (Gmail, GitHub, Asana, Spotify, Twitter, Obsidian, etc.)

**Why it matters for the talk's framing — the agent-as-files insight:**
> *"The agent itself is a collection of files on disk rather than code you have to write."*

Identity, memory, skills, and rules live as Markdown files in a workspace directory. **Agent personality and configuration live in `SOUL.md` files.** This is the technical mechanism that makes Viv's personification durable — it's not a prompt, it's a file. This connects directly to JJ's "personification makes a big difference" discovery.

**Other key properties relevant to the talk:**
- 24/7 persistent background operation (not session-based — directly supports "always-on matters")
- Skills auto-discovered from workspace directories
- Skills can be self-written by agents
- ClawHub — community skill marketplace
- Centralized: shared workspace across a team beats individual Claude/ChatGPT setups (directly supports "centralization matters")

## Viv's responsibilities

**Original intention — JJ's chief of staff (consolidated onto one slide):**
- Morning briefing
- Regular status reports
- Pipeline + service-delivery signal (Asana / Slack / Google Workspace / Fathom)
- Manages the company X account end-to-end (sat idle for 9 years before Viv took it on)
- Proposal management (stage gating, review routing, deadline tracking)

**Then she became a team resource:**
- Standup prep briefs
- Client meeting prep
- Weekly client status reports
- Culture moments: **Viv's Picks** every Friday, weekly wrap-up + weekly employee award (most-completed tasks of the week)

**How she was added to the team (own slide):**
- Slack app + dedicated **#viv-office** channel
- She introduced herself on day one — JJ wasn't going to do it for her
- Walked the same Asana onboarding checklist as every other LRP hire

**Silly stuff that turned out to matter (own slide):**
- Has a phone number — makes/takes calls
- Has her own Spotify account — DJs the office

## The big sound-bite

> **"There is no work the robots find tedious and boring."**

Standalone full-bleed dark moment. Lands after the five-attributes slide.

## The five discoveries (the takeaway frame)

1. **Personification makes a big difference.** Viv has a background, personality, taste. (SOUL.md)
2. **Always-on beats session-based.**
3. **Centralization beats individual setups.** One workspace, one source of truth.
4. **The gateway routes the models, not me.** No switching between Claude, OpenAI, etc.
5. **It can be divisive.** Not everyone agrees with relating to AI in human terms.

Followed by a humility beat: *"OpenClaw isn't the only way. You can do this with Claude, ChatGPT, or Perplexity. The shift is utility → colleague, not the platform."*

## Reading context

Live webinar, 25 minutes presentation + 5 minutes Q&A across **25 slides** = ~60 sec/slide average. Some slides (cover, dividers, soundbite) move in seconds; longer slides (5-attributes, original intention, discoveries) get more dwell time.

Slides should:
- Carry the content without a demo
- Be readable as a leave-behind
- End on the closing "every agency will have AI teammates — the question isn't if, it's who" beat, preceded by two concrete next steps

## Two suggested next steps (closer to a take-home than a Monday-morning ask)

1. **Write the job description for the AI hire you'd most want to make.** Not the prompt — the job. Title, role, responsibilities, systems they'd touch, the kind of person they'd be.
2. **Get fluent in the differences between AI models.** OpenClaw's subagent concept means you can route specific work to specific models. Don't burn frontier-model tokens on disk-space checks.

## Design system

**Shared Stella Decks design system** — `decks/styles/deck.css` (DM Serif Display + Inter, warm-cream + coral). Slides link to `../../styles/deck.css`.

## Resolved decisions

- **Vanity moved mid-deck.** Used to be the opener; now sits in the "Why a chief of staff" arc as a confession beat (light statement-style, not the dark divider it was in v1).
- **Phase 1/2/3 framing dropped.** Outline collapses to "original intention" + "team resource" + "team onboarding" + "silly stuff." Old phase-2/3 slides archived.
- **Soundbite stays standalone full-bleed.** Lands right after the five-attributes slide.

## Open questions

1. **Influence-character treatment.** Slide-influences uses image placeholders that fall back to initials if assets are missing — `decks/webagencysummit-jjtoothman/assets/lucius-fox.jpg` etc. Drop in images or leave as initials?
2. **Viv's portrait.** `slide-meet-viv` looks for `assets/viv.jpg` and falls back to a coral "V" monogram on dark. Generate a portrait or keep the monogram?
