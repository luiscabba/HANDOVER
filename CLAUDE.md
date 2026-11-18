# Context for Claude

This repo hands over two texxen client projects: **SBC Capital** (`sbc-capital/`) and **Gusto Caffè** (`gusto-caffe/`).

Before any work on a project, load its brief skill (`sbc-capital-brief` or `gusto-caffe-brief`), then read that project's `DECISIONS.md`. Do not reopen a decision listed there, or bring back anything under "Rejected", unless the user asks.

Follow `HOW-WE-WORK.md`:
- Reference study before designing or redesigning any screen, section or brand piece (`reference-study` skill), then mockups in real use, then build.
- Design options must be genuinely different styles (`divergent-variations`).
- Headers and token names say plainly what they are (`no-ai-slop-systems`). No slogans.
- No em dashes in any copy. Client copy uses `texxen-voice`.
- Facts the client has not supplied go in as `[bracketed]` placeholders. Never invent them.
- Never reveal texxen's methods or name competitors in public material.

When you lock a new decision, add it to the project's `DECISIONS.md` with the date. When a placeholder is filled, remove it from `ROADMAP.md`.

Code: both projects are static HTML, CSS and JS with no build step. SBC code is in `sbc-capital/code/` as submodules; Gusto code is in `gusto-caffe/site/`. Push to `main` and Vercel redeploys.
