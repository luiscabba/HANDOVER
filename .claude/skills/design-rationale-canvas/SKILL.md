---
name: "design-rationale-canvas"
description: "Work back from a finished website to a Claude Design canvas that walks the client through the journey: diagnostic, findings, real alternatives per decision with the chosen one highlighted, system, then the site."
---

# Design rationale canvas

Texxen builds and iterates websites fast. Dropping a finished site on day three makes the work look cheap, however much method sat behind it. This skill takes a completed (or near-complete) site and builds the presentation that takes the client through the journey to it, so the effort and methodology are visible before the result is.

The model is the PITX Brand System canvas: rationale reverse-engineered from a built site, presented as diagnostic, decisions, system, applied result.

No em dashes anywhere in the output.

## The one rule: present an argument, never a fake history

Everything on the canvas must be true. The canvas shows **why** the site is built this way, not a diary of how it happened.

- Every step the canvas presents is actually done, after the build if need be: the audit is a real audit, the references are real captures, the alternatives are real artboards built for this deck, the contrast ratios are computed.
- Never write dates, rounds or sequence words that imply a timeline that did not happen: no "first we tried", "Round 1", "after testing", "weeks of exploration", no fake version numbers. Use "Considered" and "Chosen".
- Never claim research that was not run (user interviews, testing, analytics) unless it was. If a decision rests on judgement plus references, say that.
- If working back reveals a decision on the site that cannot be honestly justified, do not invent a rationale. Log it in the internal notes as a candidate fix and ask Luis whether to change the site or present the decision on what it does have.

## 0. Frame the job

Establish, from the conversation, memory files and the repo before asking:

- **The site:** live URL, preview URL or repo path. It is frozen: this skill does not redesign it.
- **The client:** who they are, what they asked for, what they currently have (live site, brand assets, nothing).
- **Tier:**
  - **Light** (default for a normal website job): 10 to 14 artboards. Diagnostic, findings, principles, 3 to 5 decisions, system, site.
  - **Full** (pitches and engagements meant to grow, like PITX): adds sitemap and journeys, business model, evolution frames, applied surfaces beyond the site, and hands off to the brand-system plugin for framework depth.
- **Reveal:** one meeting, or staged across two (see section 6). Default to one unless Luis says otherwise.
- **Design system on the canvas chrome:** client-facing texxen documents use the texxen system for the canvas furniture; the client's own system appears inside the artboards that show their work.

Ask only what changes what gets built, one question per line. Otherwise state the inferred answer and go.

Set up a task list: extract, ground, decisions, system, site capture, assemble, verify, internal notes.

## 1. Extract: measure the built site

Measure, never eyeball. Use Playwright (Chromium is pre-installed; do not run `playwright install`) or the repo's CSS/tokens:

- Colour tokens with hex and role, type families, scale steps with px and weight, spacing base, radii, container widths, breakpoints.
- Component inventory: nav, hero, buttons and states, cards, forms, footer, anything bespoke.
- Page inventory and nav structure.
- Full-page captures of every key page at 1440 and 390 wide. These become the reveal.

Recompute every contrast ratio in code as it is written (WCAG relative luminance). Record any failures; they go in the internal notes as fixes to make on the site before the meeting, not on the canvas as defects of texxen's own work.

## 2. Ground: the evidence the decisions rest on

**Diagnostic (if the client has a current site or assets).** Audit it for real: capture it, measure its tokens, list concrete defects. Follow the PITX register: observations, not characterisations, and every defect paired with the fix the new site makes. Re-verify each defect against the live site before any meeting. If greenfield, this page becomes "The brief": what they asked for, who it serves, what it has to do.

**Reference study.** Run the `reference-study` skill (6 to 8 references across its tiers, live captures). Keep only what feeds a decision.

**Audience and job.** One artboard naming the primary visitor types and the one job each comes to do. If the site serves several, a simple journey per type.

**Principles.** Derive 3 to 4 design principles from the findings, each in one line with the finding that produced it. Every decision later must trace to at least one principle. A principle no decision uses gets cut.

## 3. Decisions: real alternatives, the chosen one highlighted

Pick the decisions that carry the site, usually 3 to 5 for Light, up to 8 for Full. Typical set: first impression (hero), navigation and structure, typography, colour, the signature component or feature, imagery. Choose the ones with the most real reasoning behind them, not a full checklist.

**How many alternatives per decision. It depends, and the rule is:**

| Situation | Show |
|---|---|
| Genuinely open decision, several credible directions | 3 (two considered plus the chosen) |
| Constrained decision, the real choice is between two approaches | 2 (one considered plus the chosen) |
| Forced by a constraint (existing logo, mandated colour, platform limit) | No alternatives. Show the chosen with the constraint stated plainly. Never fake options around a fixed asset |

**Building the alternatives.**
- Build them as real artboards at the same dimensions as the chosen one, using the same real content (same headline, same photos, same nav items), so the only variable is the decision itself.
- No strawmen. Each alternative must be something a competent designer could ship, with one stated strength. If an alternative has no real strength it is padding: replace it or drop to two.
- Prefer alternatives grounded in the reference study ("the pattern the category leader uses") so the rejection reads as a judgement against a real option.
- Mid fidelity is enough; the chosen one is the real site capture or a faithful rebuild of it.

**The highlight treatment (consistent across every decision artboard):**
- Alternatives side by side, chosen one last (rightmost or bottom), so the eye ends on it.
- Chosen gets a solid accent outline and a "Chosen" tag; considered ones get a hairline outline, a "Considered" tag and reduced emphasis (not greyed into illegibility; they must still read as real options).
- Under each option: its strength in one line. Under each considered option: the one reason it lost, tied to a finding or principle.
- A rationale panel beside the chosen option in Challenge / Rationale / Solution form, three short blocks, citing the principle number and any measurement (contrast ratio, tap target, load weight).

Naming: `D1-Hero`, `D2-Navigation`, `D3-Type`... with options `D1-Hero-A`, `D1-Hero-B`, `D1-Hero-Chosen` on a Decisions page. Names are permanent once assigned.

## 4. The system

One to three artboards: tokens (colour with hex, role and contrast pairs; type scale with px and weight), spacing and radii, components styled and in states. It must read as applied, not as swatches. Mark which layers are new versus measured off the build only in the internal notes.

## 5. The site: the reveal comes last

The full captures from step 1, desktop and mobile, key pages, in a flow that matches the visitor journeys from step 2. Annotate sparingly: a numbered marker on the site pointing back to the decision it embodies (D1, D2...), so the client sees each argument land in the real thing.

## 6. Assemble and stage

Canvas page order, which is also presentation order:

1. **The Diagnostic** (or **The Brief**)
2. **What we learned** (references, audience, principles)
3. **Decisions**
4. **The System**
5. **The Site**
6. (Full only) **Structure & Model**, **What comes next**

Build with the `design` skill for all canvas mechanics: seeding, the `.dc.html` format, checks, publishing. If it is not available, say so and offer a written build sheet instead; do not substitute a single HTML page.

**Staged reveal (when chosen):** publish pages 1 to 3 for meeting one (diagnostic, findings, principles, decisions with directions), then add pages 4 and 5 to the same canvas URL for meeting two. Remind Luis in the internal notes that the payment milestones should match the meetings so holding a finished site does not delay cash.

## 7. Two layers, never mixed

Everything on the canvas is client-facing, sticky notes included. Deliverable rules:

1. Never "the client" or "the client's": name the organisation or the thing.
2. No process history, no corrections, no dates of internal work.
3. Lead with the claim.
4. Observations, not characterisations; never let a line get its energy from someone else's work looking bad.
5. Every defect is paired with its fix.
6. Rejected alternatives stay, framed as considered options.
7. Mark unknowns as open questions; bracket any specimen figure.
8. Never invent the intent behind someone else's existing mark or asset.
9. No pitch or presentation talk inside the deliverable.

Internal notes go in `<project>-rationale-notes-INTERNAL.md`, never published: presentation order and talking points per page, what to hold back until asked, the true build timeline, specimen versus verified figures, the re-verify list for live-site defects, contrast failures to fix on the site, and any decision flagged as weak in the rule above.

## 8. Verify before handing over

- Open the published canvas and look at every artboard.
- Every decision traces to a principle; every principle traces to a finding.
- Every considered option has a real strength; none is a strawman.
- No timeline language, no fake research claims, no em dashes, no "the client".
- Every contrast ratio on the canvas was computed in this run.
- Diagnostic defects re-checked against the live site.

Finish with the canvas link card, a one-line summary, the internal notes file sent separately, and the single most useful next step (usually: fix the flagged items on the site before the meeting).