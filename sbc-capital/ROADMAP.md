# SBC Capital roadmap

Rough order. Dates are targets to agree with SBC, not commitments.

## Now: finish the prototype

1. **Investor view** in `sbc-portal-preview` on the shared demo data (phase 4 of the 4 Nov plan). Reference study first.
2. **Relink the guided tour** (`/tour`) to the rebuilt views (phase 5).
3. Walk SBC through all four views end to end; collect changes.

## Next: rules-first architecture

4. Map the rules-first architecture before any production code (agreed 3 Nov): the five checks as written rules, the three outcomes, the four match stages, approvals and the audit log. `portal/store.js` already holds a first version of the rules and match stages; treat it as the spec draft.
5. Pick the production stack and data model with Ian and Khaled. Auth, document storage, sanctions screening source, audit trail.
6. Build stage 1 of the AI ladder: **rules only**. AI comes in at stage 2 (suggests), then 3 (acts by threshold), then 4 (agent network), each gated by confidence thresholds.

## Brand and site

7. G3 sign-off on the brand kit, then release assets from draft.
8. Arabic right-to-left versions of the public site.
9. Replace every `[bracketed]` placeholder as SBC supplies facts.
10. Domain, DNS and production hosting under SBC's ownership.

## Waiting on SBC

| Item | Working answer in place |
|---|---|
| Confirm referral to checked local agents (not acting as agent) | Yes |
| Confirm sanctions re-screened monthly | Yes |
| Founders' intake answers (18 questions) | Assumed answers, signed off |
| Facts shown as `[brackets]` on the site (figures, legal entity details, contact) | Placeholders |
| Who tests the prototype | Undecided |
| Whether SBC's current brand stays alongside the new identity | Undecided |
| Team role names (engagement lead, discovery lead, brand strategist, coordinator) | Not named |

## Known gotchas

- Public site pages share head, header and footer through the Python builders in `_build/`. Editing one page's header by hand will drift; rerun the builders.
- Portal demo state lives in the viewer's browser. If a demo looks wrong, press "Reset demo data" first.
- Officer, company and buyer views share one data copy per browser, so a change in one shows in the others. This is intended for demos.
