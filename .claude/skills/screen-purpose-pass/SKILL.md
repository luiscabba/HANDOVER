---
name: "screen-purpose-pass"
description: "Design thinking pass that defines the core purpose and audience of every screen before design work, then hands its questions to reference-study and folds the findings back in."
---

# Screen Purpose Pass

A thinking exercise, not a design exercise. Output: why each screen exists and who it is for, checked against how comparable products serve the same audience. No mockups, no visual critique, no layout suggestions.

Runs as a pair with **reference-study**:
1. This skill defines audiences and purposes (Steps 1 to 5).
2. reference-study runs with its framing filled from this skill (Step 6).
3. This skill folds the study back in and locks the purposes (Steps 7 to 9).

## Writing rules
- No em dashes.
- Short. Tables and one-line statements over prose.
- Decisions needed from Luis go at the end, one question per line (or AskUserQuestion), never inside text.
- Never invent an audience or purpose the material does not support. Mark anything assumed as (assumed) and ask.
- Every claim carries a label: observed, provided, inferred (same labels as reference-study).

## Step 1: Context
Gather what the product is, the business goal behind it, and who it is sold to versus who actually uses it. Read the brief, files, memory and any existing screens. List the screens or pages in scope.

## Step 2: Audiences (Empathize)

| Audience | Role / situation | What they are trying to get done | What they already know | What worries or blocks them | How often they come |

Separate buyers, users, approvers and onlookers (e.g. a manager who only reads reports). Note where audiences conflict.

## Step 3: Screen to audience map
Per screen:
- Primary audience (the screen is built for them)
- Secondary audiences (served, never at the primary's expense)
- Who should NOT need this screen

One primary audience per screen. If two compete, flag it.

## Step 4: Core purpose (Define), draft
Per screen:
- Arrival: where they came from, state of mind
- Job: the question they need answered or task they need done
- Core purpose: "This screen exists so that [audience] can [outcome] because [need]."
- Supporting purposes: at most two
- Exit: where they go next, what done looks like
- Success signal: an observable sign the purpose was met

Mark this as DRAFT until Step 7.

## Step 5: Point of view and How Might We
Per screen, one POV: "[Audience] needs a way to [need] because [insight]." Then 1 to 3 How Might We questions that frame the problem without solving it.

## Step 6: Hand to reference-study
Load the reference-study skill and pre-fill its Step 0 from this pass, so it does not re-derive them:
- Artifact: the screens in scope
- User and job: the primary audience and job from Steps 3 and 4
- Market and platform: from Step 1
- Study questions: pick the 2 to 4 HMW questions where the answer is least obvious or audiences conflict. Each becomes a study question.
- Extra study lens: for each reference, also record who that screen serves, what its core purpose appears to be, and what it deliberately leaves out.

The study's own rules (tiers, live capture, selection) apply unchanged. Stop at the study's analysis output; skip its mockup step while running inside this pass unless Luis asks.

## Step 7: Fold the study back in
Per screen, compare the draft purpose to the references:
- Convergence: the purpose most comparable screens share. This is the baseline users expect; keep it unless there is a reason not to.
- Divergence: where references serve a different audience or job on the same screen, and which fits this product.
- The opening: an audience need no reference serves well. Promote it to a supporting purpose, or the core one if the evidence is strong.
- Evidence: tier E findings that confirm or overturn a purpose.

Then rewrite the core purpose as FINAL, with one line citing which references or findings shaped it.

## Step 8: Stress test
Across the whole set:
- Screens with no clear purpose (merge or cut)
- Two screens with the same purpose (consolidate)
- Audience needs no screen serves (gaps)
- Screens serving too many audiences (split or prioritise)
- Purpose that conflicts with the business goal
- Flow breaks: a screen's exit does not match the next screen's arrival
- Purposes that drifted far from convergence with no stated reason

## Step 9: Design implications
Per screen, 2 to 4 short principles that follow from its final purpose, audience and the study (e.g. "answer the status question in one glance, as every comp does", "assume first-time user, no jargon"). These guide later design. Still no visuals.

## Output
One artifact (load artifact-design first), linking the reference-study artifact:
1. Audience table
2. Screen purpose sheet: per screen, audience ranking, draft vs final purpose, job, exit, success signal, POV, HMW, what the study changed, principles
3. Stress test findings
4. Questions for Luis, one per line

## Quality gate
- One primary audience and one core purpose per screen.
- Every study question traces to a HMW from Step 5.
- Every final purpose cites the references or evidence behind it, or says it holds against convergence and why.
- No mockups, no layout talk.
- No em dashes.