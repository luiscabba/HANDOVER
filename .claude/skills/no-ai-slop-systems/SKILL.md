---
name: "no-ai-slop-systems"
description: "Strip corny, slogan-style or invented wording from design systems: token, color and component names, board and page headers, principles, usage notes. Use instead of no-ai-slop when the text is a system, not prose."
---

# No AI slop: design systems

A design system is a reference people look things up in. Every name and label has one job: tell the reader what the thing is, fast. Clever wording makes them decode it first. Write like a spec sheet, not a brand campaign.

This skill covers the words in a system: token names, color names, component names, board and page headers, section labels, principles, usage notes and rationale lines. For visual cliches (gradients, glass, generic layouts) use design-taste-frontend. For prose drafts use no-ai-slop.

## Two jobs

**Edit (default).** Rewrite the system's wording with the rules below. Return the changes as a before and after table (Old, New, Why in a few words), then the full updated text or files if they were given.

**Detect.** When asked to audit or flag without rewriting: list each offending item, quote it, name the pattern, give the fix in a few words. Do not rewrite.

## The core test

For every name or header ask: if someone saw only this label, would they know what is under it? If they would have to guess, rename it to what it literally is.

Second test: does it sound like a tagline, a poem or a product launch? If yes, it is slop.

## Rules

**Headers name the contents.** "SBC Capital Marks", "Usage Guidelines", "Color Palette", "Type Scale", "Button States". Never "Where Clarity Meets Craft", "The Language of Trust", "Our Visual DNA", "Building Blocks of Belief".

**Section labels are plain nouns.** "Spacing", "Icons", "Do and don't", "Logo clear space". Not "Room to Breathe", "Little Signals", "The Rules of the Road", "Vibe Check".

**Colors get a role or a plain hue name.** Semantic tokens by role: `text/primary`, `surface/raised`, `border/subtle`, `status/error`. Palette swatches by hue and step: "Blue 600", "Gray 100", or one plain word ("Navy", "Off-white", "Orange"). Never "Midnight Whisper", "Ember Glow", "Trust Blue", "Ocean of Possibility", "Velvet Dusk". Only keep a brand color name the client already uses, and still give its hex next to it.

**Components use the standard names.** Button, Card, Data table, Tabs, Modal, Toast, Badge. Do not brand ordinary parts ("Signal Card", "Pulse Bar", "Insight Tile", "Hero Moment"). A custom component gets a descriptive compound name: "KPI card", "Collection status chip".

**Type and spacing use scales, not moods.** "Display / H1 / H2 / Body / Caption" or "Text 14 / 16 / 20". "Space 4 / 8 / 16". Not "Whisper", "Statement", "Breath", "Pause".

**No metaphor system names.** Don't name the system or its parts after concepts ("The Compass System", "Pillars", "Foundations of Light"). "texxen Design System" or "Kalend Brand Manual" is the name.

**Principles are checkable rules, not virtues.** Cut one-word value stacks ("Bold. Human. Honest.") and adjective lists. Write the rule a designer can check work against: "Every chart labels its units on the axis", "Orange is for one action per screen", "Body text stays at 16px or larger".

**Usage notes say when and how.** "Use for the main action on a page. One per screen." Not "A versatile button for every moment" or "Designed to inspire confident action".

**Rationale states the reason, not the feeling.** "Navy because the client's existing signage is navy and it passes AA on white" beats "Navy evokes trust, depth and stability". If the only reason is a mood word (evokes, conveys, embodies, speaks to, feels), ask for or find the real reason, or cut it.

**No decoration in labels.** No emoji, no taglines under headers, no numbered pseudo-chapters ("01 / The Origin") unless the board really is a sequence.

**Same thing, same word.** Pick one term per concept across tokens, headers and notes. Don't call it "surface" on one board and "canvas" on the next.

## Words that flag slop in a system

whisper, glow, breath, pulse, essence, DNA, soul, heartbeat, moment, journey, story (as a label), signal (for a non-signal), pillar, foundation (as decoration), language of, meets, unlock, elevate, crafted, curated, harmony, symphony, canvas (for a non-canvas), magic, delight, vibe.

These are allowed only when they are the literal name of something.

## Copy rules carried over

No em dashes. Sentence case for labels unless the brand guide says otherwise. Keep client and product names exactly as given.

## Workflow

1. Read the whole system or board list first.
2. List every name, header, label, principle and note.
3. Run the core test and the rules on each. Mark plain items as fine and leave them.
4. For edits, return the Old / New / Why table, then the updated text or files.
5. Check: every header names its contents, no poetic color or token names, no branded ordinary components, every principle is checkable, no em dashes, one term per concept.