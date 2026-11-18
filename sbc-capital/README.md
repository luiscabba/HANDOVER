# SBC Capital

## In one paragraph

SBC Capital (Dubai) qualifies international companies and introduces them to Gulf buyers. texxen is doing the whole stack: the brand framework, the identity, the public website, and the SBC Strategic Portal, a platform where SBC officers review companies against five checks and award the **SBC-Qualified** mark, buyers post needs and tenders and browse qualified companies, and investors follow along. The brand must always be written "SBC Capital", never "SBC" alone.

## Status (18 Nov 2026)

| Workstream | State |
|---|---|
| Brand framework (stages 1 to 3) | Signed off 8 Oct 2026, kept open to changes. SBC let texxen assume answers the founders could not give |
| Identity | Locked 13 Oct 2026 (palette B2 "The Gate", two marks) |
| Brand kit | Built as a G3 presentation kit; assets stay draft until SBC signs G3 |
| Public site | Live on Vercel. Aligned to the founders' briefing on 15 Oct. Arabic (RTL) screens not built yet |
| Portal | Interactive prototype with demo data. Officer console, company portal and buyer portal rebuilt; investor view not started |
| Production platform | Not started. Architecture direction agreed (rules first, AI in stages) |

## Code

Both are plain static HTML, CSS and JavaScript. No framework, no build step for deploy.

| Repo | What | Run locally |
|---|---|---|
| `code/sbc-capital-site` | Public site. Home, For companies (+ Apply), For buyers, How the review works, Contact, Privacy, Mark terms | `npx serve .` or any static server. Page builders in `_build/` are Python scripts that regenerate shared head, header and footer; rerun them after header or footer changes (see that repo's README) |
| `code/sbc-portal-preview` | Client-facing portal prototype. `/officer` (demo login autofills), `/company`, `/buyer`, `/tour` | `npx serve .` All views share `portal/data.js` and `portal/store.js`; changes persist per browser, "Reset demo data" restores |

Shipping: push to `main`, Vercel redeploys. `vercel.json` sets clean URLs.

## People

| Who | Role |
|---|---|
| SBC founders | Approve brand and scope; answer the foundation intake |
| Khaled (SBC) | Proposed the AI-agent ecosystem direction; the platform conversation goes through him |
| Ian Madrid (texxen) | Principal. Set the rules-first platform direction that SBC approved |
| Luis Madrid (texxen) | Outgoing project manager and designer |

## Read next

- [DECISIONS.md](DECISIONS.md) before changing anything
- [DESIGN.md](DESIGN.md) for tokens, marks and every canvas link
- [ROADMAP.md](ROADMAP.md) for what is next and what SBC still owes us
