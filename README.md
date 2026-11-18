# Handover: SBC Capital and Gusto Caffè

Handover from Luis Madrid (texxen Project Manager) for two texxen client projects. Start here, then open the project folder you are picking up.

| Project | Client | What it is | Stage (18 Nov 2026) |
|---|---|---|---|
| [SBC Capital](sbc-capital/README.md) | SBC Capital, Dubai | Brand, public site and the SBC Strategic Portal (a vetting and matching platform for Gulf buyers, suppliers and investors) | Identity locked, public site live, portal at interactive-prototype stage |
| [Gusto Caffè](gusto-caffe/README.md) | Gusto Caffè, Egypt (Aida Gasmi) | Logo redesign plus a bilingual, scroll-animated B2B lead-generation website | Logo in cursive round with client, site v3 built on placeholders |

## What is in this repo

```
README.md            this file
CLAUDE.md            context your Claude loads automatically
ACCESS.md            accounts, repos, canvases and who still has to grant each one
HOW-WE-WORK.md       the working method and house rules both projects follow
.claude/skills/      skills to install in your Claude (two project briefs + the method skills)
sbc-capital/
  README.md          status, links, how to run and ship
  DECISIONS.md       every locked decision, with date and reason, and what was rejected
  ROADMAP.md         rough roadmap, open items, placeholders waiting on SBC
  DESIGN.md          identity, tokens, type, motion rules, links to every canvas and study
  code/              the two repos as git submodules
gusto-caffe/
  README.md, DECISIONS.md, ROADMAP.md, DESIGN.md   same layout
  site/              the current site (v3) source
```

## First hour

1. Read `HOW-WE-WORK.md`. Both clients have been shaped by it and will notice if it changes.
2. Work through `ACCESS.md` until every row says granted.
3. Pull the code: `git submodule update --init --recursive`.
4. Install the skills: copy `.claude/skills/*` into your own `~/.claude/skills/` (or keep this repo open in Claude Code, which reads `.claude/skills` from the project).
5. Open the project README, then its `DECISIONS.md` before touching any design.
