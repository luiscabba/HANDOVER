# Gusto Caffè

## In one paragraph

Gusto Caffè is a family business (since 2008) in Egypt: a factory and distributor of Italian café beverages, coffee beans, machines and PAUL-style pre-prepared sandwiches, selling B2B only to cafés, hotels and shops, local orders only. texxen is doing a logo redesign and a bilingual (Arabic and English) scroll-animated website whose only job is to turn a visiting buyer into an inquiry on WhatsApp or email. No cart, no payments, no CRM. Orders are handled by hand by Aida Gasmi, who is also the sole design approver.

## Status (18 Nov 2026)

| Workstream | State |
|---|---|
| Logo | Client rejected the seal, crest and wordmark shortlist (4 Nov) as feeling dated; they want cursive. Presented 12 Nov: four new cursive logos (A Firma brush signature, B Neon monoline, C Grasso bold script, D Pennello gold brush and cup) plus their own logo with the steam redrawn (5a two wisps outlined, 5b one tricolore ribbon). **Awaiting Aida's pick** |
| Site v3 | Built and working, 10 scroll scenes, in the O2.2 skin with placeholder content. Source in `site/` |
| Next site version | One continuous walk through a Gusto shop (door, shelf, bar, vitrine, machine, back door, counter), drink by drink at the bar. Storyboard done 3 Nov, not built |
| Arabic | Supported in v3 (`dir="rtl"`, mirrored motion); copy not final. texxen writes the Arabic |
| Hosting | Not on a production domain yet |

## Code

`site/` is a single `index.html` plus `img/`. Plain HTML, CSS and JS; no build step.

- Run: `npx serve site`
- The hero, coffee and bar scenes are canvas frame sequences (Blender renders, 48 webp frames each) scrubbed by scroll, in `site/seq/hero/`, `site/seq/coffee/`, `site/seq/bar/` as `f_00.webp` to `f_47.webp`. The Blender scene files that made them are not in this repo yet (see `ACCESS.md`).
- Fonts load from Google Fonts: Bodoni Moda, Figtree, Noto Naskh Arabic, IBM Plex Sans Arabic.
- Placeholders are `[bracketed]` in the HTML (client logos, counts, quote, delivery time, map, contact details).

## Read next

- [DECISIONS.md](DECISIONS.md) before changing anything
- [DESIGN.md](DESIGN.md) for tokens and every canvas link
- [ROADMAP.md](ROADMAP.md) for what is next and what Gusto still owes us
