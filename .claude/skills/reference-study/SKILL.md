---
name: "reference-study"
description: "Run a reference study before designing or redesigning any screen, feature, site or brand piece: pull 6-8 real references across five source tiers, capture live screenshots, compare, and end in mockups. Use for /reference-study."
---

# Reference study

Luis expects a reference study (how comparable products handle it) before any design or redesign, then mockups. A study is only as good as what it pulls, so this skill fixes the sourcing first and the analysis second. The keep / change / do-not-copy discipline is adapted from OpenDesign's reference-design-contract skill (github.com/nexu-io/open-design, Apache 2.0).

No em dashes anywhere in the output.

## 0. Frame the job (before pulling anything)

**If a screen-purpose-pass has run for this work** (in this conversation, or its artifact exists), take the framing from it instead of re-deriving: artifact, primary audience and job, market, platform, and the study questions it handed over. Also apply its extra lens: for each reference, record who that screen serves, what its core purpose appears to be, and what it deliberately leaves out. When running inside that pass, stop after step 3 (Analyze) and return to it; skip mockups unless Luis asks.

Otherwise, write one short block, inferred from the conversation and the project's memory files where possible:

- **Artifact:** the exact screen, feature, page, flow or brand piece ("B2B order form on desktop", not "the website").
- **User and job:** who uses it and what they are trying to get done there.
- **Market:** where the users are (PH, UAE, Egypt, global). This decides which local players count as direct comps.
- **Platform:** desktop web, mobile web, iOS, Android, print, social.
- **Constraints:** an existing brand system, settled decisions, a stack.
- **Study questions:** 2 to 4 specific questions the study must answer ("How do supplier sites handle minimum order quantities?"). Every reference is chosen to answer one of these.

If the screen's purpose or audience is unclear, suggest running screen-purpose-pass first.

Ask at most one question, only if a missing answer would change what gets pulled. Otherwise label the guess as inferred and go.

## 1. Pull plan: 6 to 8 references across the tiers

Default quota (adjust to the job, but every tier is considered every time):

| Tier | What it is | Quota |
|---|---|---|
| A. Incumbent | The client's current version: live site or app, existing brand assets, what they use today. Skip only for a true greenfield. | 1 (always first, if it exists) |
| B. Direct comps | Same category, same job, including at least one local player in the target market and one category leader. | 2 to 3 |
| C. Same problem, other categories | Best-in-class answers to the same interaction or communication problem from outside the category. | 2 to 3 |
| D. Pattern sources | Real shipped screens from free galleries, and design-system guidance for the pattern. | 1 to 2 |
| E. Evidence | UX research on the pattern, so choices rest on more than taste. | cited, not counted |

Write the pull plan as a short table (tier, candidate, why it answers which study question) before capturing. Over-pull candidates by about 50%, then cut to the strongest.

### Where each tier comes from

**A. Incumbent.** The URL or app the user names, files they attached, the project's memory file, existing canvases or design systems among their artifacts.

**B. Direct comps.** Web search for the category plus the market ("espresso supplier horeca Egypt", "pickleball club Manila booking"), competitors the client named, category leaders. Prefer companies a real customer would actually compare against.

**C. Cross-category.** Name the underlying problem in plain words ("trust before a first B2B order", "choosing a time slot", "explaining a price tier"), then find who solves it best anywhere. Products known for craft in that problem: e.g. Linear, Stripe, Notion, Airbnb, Wise, Revolut, Superhuman, Apple, Arc, Cal.com, Shopify, Duolingo for product UI; strong editorial and brand sites for marketing work.

**D. Pattern sources (no paid accounts; Luis has none).**
- Marketing sites: Godly (godly.website), Land-book, Lapa Ninja, One Page Love, SaaS Landing Page, Awwwards (winners and honorable mentions, real sites only), SiteInspire.
- Product UI without Mobbin/Refero/Page Flows: capture the live product itself where it is public (sign-up, pricing, settings, empty states reachable without an account), the company's own product pages, help-center articles and changelogs (they show real current screens), and App Store / Play Store screenshots.
- Design-system guidance: official docs for the pattern (Material, Apple HIG, Polaris, Carbon, Atlassian, GOV.UK for forms and trust).
- Design-system write-ups: OpenDesign's library of 154 `DESIGN.md` files (tokens, type, color, components for brands like stripe, linear-app, airbnb, apple, notion, wise, revolut, shopify, spotify, vercel, plus style presets like editorial, brutalism, minimal). Fetch once per session:
  ```bash
  OD="${TMPDIR:-/tmp}/open-design"
  [ -d "$OD/.git" ] || git clone --depth 1 --filter=blob:none --sparse https://github.com/nexu-io/open-design "$OD" && git -C "$OD" sparse-checkout set design-systems
  ls "$OD/design-systems"
  ```
  Read `design-systems/<name>/DESIGN.md`. These are reverse-engineered, so label anything taken from them as inferred, never as the brand's official spec.

**E. Evidence.** Baymard Institute (forms, checkout, product pages, e-commerce), Nielsen Norman Group (general UX patterns), and the official design-system guidance above. Quote the specific finding and link it.

### Selection rules

Keep a reference only if all hold:
- **Real and shipped.** Live product or published site. No Dribbble or Behance concepts, no template-marketplace demos, no AI-generated mockups.
- **Current.** Check it still looks that way today; note the capture date.
- **Same platform** as the artifact, or the platform difference is the point.
- **Answers a study question.** If you cannot say which question it answers, cut it.
- **Not a monoculture.** No more than two references from the same aesthetic family or the same company size.

## 2. Capture: live screenshots

Capture through the built-in browser on Luis's Mac (read the built-in-browser skill before the first step). The workspace shell cannot reach most of these sites.

- Capture the **exact state the artifact is about**, not just the hero: the form, the empty state, the pricing toggle, the error, the mobile menu.
- Desktop and mobile widths whenever the artifact is responsive.
- Record for each: URL, capture date, tier, viewport.
- Never sign up with Luis's identity, submit forms or start trials to reach a screen. Use what is publicly reachable; otherwise use help-center or store screenshots and say so.
- If the browser is unavailable, say so plainly and ask Luis to attach screenshots or links; label anything not captured live as "not captured".

Upload captures as assets of the study artifact so the board shows real images.

## 3. Analyze

For every reference, one card:
- **What it does** for the study question, in one or two lines.
- **Serves / purpose / leaves out** (when screen-purpose-pass is driving): who the screen is for, its apparent core purpose, what it deliberately omits.
- **Keep:** controllable qualities worth borrowing (density, hierarchy, flow order, copy pattern, interaction, material, rhythm).
- **Change:** what must adapt to this client (content, brand, market, platform).
- **Do not copy:** logos, proprietary UI, exact layouts, claims, copy.
- **Confidence label** on each claim: `observed` (seen in the capture), `provided` (from Luis or the client), `inferred`.

Then across references:
- **Comparison matrix:** rows are the dimensions that matter for this artifact (e.g. step count, where price appears, trust signals, CTA wording, mobile pattern, and audience served / core purpose when purpose-driven); columns are references.
- **Convergence:** what most of them do. Treat it as the expected baseline users already know.
- **Divergence:** where they split, and why each choice fits its product.
- **The opening:** what none of them do well that this client could own.
- **Evidence:** the tier E findings that support or overturn the patterns.

## 4. Output: one study artifact, then mockups

Publish the study as one HTML artifact (load artifact-design first): framing block, pull plan, annotated screenshot board grouped by tier, matrix, convergence / divergence / opening, evidence with links, and sources with capture dates.

Then do not stop at prose. Luis wants every visual decision shown in real use: turn the recommended direction into mockups of the actual artifact. If the study surfaced two genuinely competing directions, mock both side by side and recommend one. Mockups go to the Design type (or the project's existing canvas) per normal output rules. Exception: when running inside screen-purpose-pass, hand the analysis back instead and skip mockups unless Luis asks.

## 5. Hand off

- **Screen purpose work:** return the analysis to screen-purpose-pass Step 7.
- **Client brand work:** feed the study into the brand-system plugin; each decision it supports becomes evidence in that decision's Challenge / Rationale / Solution block.
- **Website or UI build:** hand the chosen direction to the build workflow (impeccable, design-taste-frontend, or the project's own skills such as texxen-update or portfolio-update).
- Save nothing to memory on your own; the study artifact is the record.

## Quality gate (check before delivering)

- Every tier was considered, and the incumbent is included when one exists.
- 6 to 8 references, each tied to a study question, at least one local to the market.
- Every reference is real, shipped and captured live (or explicitly labeled otherwise) with URL and date.
- No concepts, template demos or AI mockups in the set.
- Every claim carries observed / provided / inferred.
- The matrix, convergence, divergence and opening are all present.
- The study ends in mockups, not a list of recommendations (unless it was run inside screen-purpose-pass).
- No em dashes.