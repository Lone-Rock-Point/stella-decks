# BrightRidge Broadband — Website Redesign Finalist Pitch

## Purpose

Final-round pitch deck. Lone Rock Point is a finalist for BrightRidge Broadband's website redesign. The job of this deck is to make BrightRidge walk out feeling that Lone Rock Point is the obvious choice and that they can't wait to start working with us.

## Critical directive from BrightRidge

> *"Please keep in mind that we do not want a presentation of the RFQ submitted; but we will be going through each of the talking points based off of the RFQ that was submitted, with a chance for our team to ask additional questions, as well as your team to ask additional questions."*

**This shapes everything.** The deck is not a proposal recital. Every slide is a speaker-supporting visual that invites discussion. Keep slides sparse, typographic, and provocation-led. Leave room for conversation.

## Audience

BrightRidge Broadband leadership team, expected in the room:
- **Stacy Conzet** — Marketing Supervisor
- **Bonnie Donnolly** — Chief Development & Market Strategy Officer
- **Carrie Boeve** — (role TBC)
- **PJ Witt** — Digital Media Specialist

They have already shortlisted LRP based on capability. The question is chemistry, specificity, and conviction.

## Narrative mode

**Persuasive / narrative, but dialogic.** Not a capabilities overview and not a monologue. Every slide should build conviction by surfacing a specific observation, POV, or plan — then invite BrightRidge to react.

## Reading context

Live 90-minute finalist interview. In-person or video. Slides support the speakers; they do not stand alone as a leave-behind. No walls of text.

## BrightRidge context

- Not-for-profit, public power provider serving electricity and broadband in Washington, Sullivan, Carter, and Greene counties in Northeast Tennessee
- Broadband division formed July 2018
- Current site: mybrightridge.com
- ~45–60 pages; bilingual (English/Spanish) is a core requirement
- Serves residential and business customers
- Target contract start: July 1, 2026. Target launch: ~October 2026

## What BrightRidge said they want (from the RFQ)

- New, responsive WordPress site, hosted on their WP Engine account
- Modernized look, streamlined UX, key info above the fold
- Staff independence — internal team edits content without vendor reliance
- Integrations: SmartHub, JotForms, TranslatePress (must keep)
- ADA compliant (currently using accessiBe — LRP will challenge this)
- Modern pricing boxes + nutrition labels (non-negotiable, currently painful to edit)
- Emergency notifications (pop-up + scroll-across, easy to activate)
- Fast load times, Core Web Vitals, GA4 cross-domain to SmartHub
- Pre-launch training + post-launch support

## LRP's POV going into this meeting

From LRP's internal observations:
- **accessiBe overlay is actively hurting them** — performance and accessibility both. LRP will recommend discontinuing it and going deeper: theme-layer compliance + Equalize Digital Accessibility Checker Pro.
- **TranslatePress approach is impacting performance.** Worth discussing configuration and alternatives within it.
- **Chatbot is impacting performance.** Worth questioning its value to BrightRidge.
- **Hypothesis:** Technical bloat on MyBrightRidge.com stems from poor foundations at the application layer — not just surface-level issues.

Questions LRP wants to surface during the meeting:
- What's the content situation — big changes coming, or using what's there?
- What's the value of the animations from BrightRidge's perspective?
- Is BrightRidge staff genuinely ready for the level of independence we're proposing?
- "Build tools users can use" includes the internal user — how do they feel about their current CMS experience?

## The LRP team on this engagement

- **JJ Toothman** — Product Manager. 20-year digital veteran. Built NASA's first WordPress-powered public blog. Founded LRP in 2016. Government-sector web modernization, accessibility, UX.
- **Gary Kovar** — Principal Software Engineer. WordPress.org Training Team contributor, WordCamp organizer/speaker, Learn WordPress SME.
- **Michelle Hunt** — UX Engineer. Minneapolis. Visual Communications + Psychology + Sociology background; strategy-led design and frontend development.

## Proof points available to reference

- **NASA.gov** — large-scale migration, 100% accessibility scores, public-sector scale. Primary analog.
- **Groundhogg CRM** — content-rich WordPress, SEO and IA strength.
- **WordPress VIP Gold Partner** — 2023 VIP Partner of the Year. Select group.
- **Small Business (SAM.GOV UEI: HBMJNLR5CKN7, CAGE: 87L38)** — relevant for public-sector procurement credibility.

## LRP's three differentiators

1. **Bringing design systems to life in WordPress.** Design systems that actually integrate with the CMS, not just static style guides.
2. **The storyteller experience.** CMS dashboard UX, backend wireframing, editor support structures — the internal user matters as much as the end user.
3. **Complete modernization.** Redesign + performance + accessibility + SEO + integration readiness + security, as one coherent engagement.

## Key design/content decisions for the deck

- **POV-led, not capabilities-led.** Every slide leads with an observation or opinion, not a service line.
- **Show the work by embedding it.** NASA.gov and Groundhogg appear as evidence within sections — no dedicated portfolio slide.
- **Name the team with faces.** Slide 2 is the LRP humans, not a logo grid.
- **Pick the accessiBe fight.** It's a credibility-establishing moment. Done well, it separates LRP from competitors reading from the RFQ.
- **Concrete first 30 days** and a week-by-week timeline de-risks the engagement.
- **Respect the 90-minute agenda.** Slides follow their exact structure so the presentation moves with them, not against them.

## What to watch for

- **Every slide should be a provocation.** If a slide could apply to any agency or any client, it's failing.
- **Tone: confident, not aggressive.** We believe we're the right fit. No shouting. No superlatives.
- **Visual restraint.** Design system is Modern Precision + DM Serif Display headlines. One spot of terracotta per slide. Let whitespace carry the confidence.
- **Don't regurgitate the RFQ.** BrightRidge said so explicitly.

## MyBrightRidge.com audit findings (April 2026)

**Technical stack confirmed:**
- Theme: **Enfold** (commercial, avia-* prefix, 2017-era). Root of the foundation bloat.
- **94 `<script>` tags** on homepage. **243KB of raw HTML** before content renders.
- **accessiBe** overlay active (`acsbapp.com` script). Confirmed.
- **Google Language Translator** plugin active &mdash; **not** TranslatePress as stated in the RFQ. The live Spanish experience is machine translation only.
- **Gravity Forms + Gravity Forms reCAPTCHA** active &mdash; **not** JotForms as stated in the RFQ. Multiple CSS/JS bundles per pageload.
- **Popup Maker + Announcer** plugins &mdash; two overlapping notification systems.
- **Live chat** is a Popup Maker modal wrapping an iframe from `chat.brightridge.com:8443` (likely on-prem Cisco ECC / UCCX contact-center system).
- **WPO365-login** for Microsoft 365 admin authentication.
- **Google Site Kit + Pixel Caffeine** for analytics / FB Pixel.

**Content & IA issues:**
- **Pricing inconsistency**: 10 Gig tier shows $159.98/mo on the homepage, $149.99/mo in the nutrition-label modal. Content drift is measurable.
- **"Video (old)"** still in main navigation &mdash; legacy deprecated product never removed.
- **Language toggle** buried in footer-bottom-right &mdash; invisible to Spanish-speaking arrivals, especially on mobile.
- **No homepage search** despite schema referencing one.
- **Nutrition labels** rendered as HTML modals (good news: editable content) but managed through Popup Maker (brittle).
- **"Middle-Mile Grant"** availability checker is a separate tool with its own map &mdash; creates brand/service-area confusion for prospects.

**The four observations we'd lead with on slide 5:**
1. The translation story doesn't match the RFQ (Google Translator, not TranslatePress).
2. accessiBe is the problem, not the solution.
3. The theme is the foundation bloat (Enfold, 94 scripts).
4. The truth lives in too many places ($159.98 vs $149.99, two notification plugins).

## Open questions (fill in as we build)

- **Photos of the LRP team** &mdash; drop into `decks/assets/team/` as `jj-toothman.jpg`, `gary-kovar.jpg`, `michelle-hunt.jpg`.
- **JotForms vs Gravity Forms** &mdash; the RFQ says JotForms, production runs Gravity Forms. Is this an error in the RFQ, a migration plan, or something to clarify with them?
- **Chatbot's value** &mdash; the ECC chat iframe works. Is BrightRidge married to it, or open to alternatives that don't require a Popup Maker wrapper?
- **The accessiBe argument** &mdash; how hard do you want to push it? Slide 5 puts it plainly. Slide 12 is the full fight.
- **The emergency notification moment** &mdash; there's a chance to show a visual mockup of how it would look on the new site. Worth doing?
