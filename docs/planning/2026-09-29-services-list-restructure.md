# Services List Restructure

Summary — The site currently advertises 8 services (Land Clearing & Demolition, Residential & Commercial Excavation, Site Preparation, Debris Removal, Land Grading, Leveling, Roadbeds, Forestry Mulching) across the homepage, the services page, the footer, and 8 individual detail pages. The owner wants the site trimmed to advertise only 10 specific approved services, because anything outside that list creates liability/licensing exposure for the business right now. This plan covers renaming services that map cleanly, deleting services that aren't approved, splitting/replacing services that don't map cleanly, and writing new pages for approved services that don't exist on the site yet — kept consistent across every page, link, and mention.

Out of scope
- No 301/302 redirects for deleted pages' old URLs (`/service-land-clearing-demolition`, `/service-leveling`, `/service-residential-commercial-excavation`, `/service-forestry-mulching`) — they will 404. Any Google-indexed old URLs will show broken until re-crawled; adding redirects is a separate technical change beyond this content trim.
- No SEO resubmission or sitemap ping after the change.
- No legal/licensing review of which 10 services are safe to advertise — the owner has already determined the approved list; this plan only implements it.
- Final published wording for the brand-new pages (Waterline install and repair, Building pads, Footers, Bushhogging) is placeholder copy for the owner's review, not guaranteed-final text.
- The URL slug used for the renamed "Driveway installation/repair" page (keep `/service-roadbeds` vs. a new slug) is left to the implementer — cosmetic naming, not a liability decision.

Answered questions (2026-09-29, owner accepted all recommended defaults via "fix it")
1. Rename "Site Preparation"→"Construction site prep," "Debris Removal"→"Construction debris removal," "Land Grading"→"Grading" everywhere. — Accepted.
2. Delete "Land Clearing & Demolition" entirely (page, cards, footer link, sidebar mentions, About/FAQ prose). — Accepted.
3. Delete "Leveling" entirely (no fold-in). — Accepted.
4. Split "Residential & Commercial Excavation" into two new, narrower pages — "Utility excavation" and "Light excavation" — dropping foundation/basement/pool/commercial-site-work content. — Accepted.
5. Rename/narrow "Roadbeds" in place to "Driveway installation/repair," dropping access-road and general roadbed bullets. — Accepted.
6. Delete "Forestry Mulching" content and write a new, distinct "Bushhogging" page rather than relabel mismatched copy. — Accepted.
7. Write full detail pages (hero/description/bullets/CTA/sidebar, matching the site's existing pattern) for services with no existing content — Waterline install and repair, Building pads, Footers — with placeholder copy for owner review. — Accepted.
8. Show all 10 approved services on the homepage grid (no curated subset + "See More"). — Accepted.
9. Rewrite the About-section prose and FAQ answer to name only the approved services. — Accepted.
10. Rebuild the footer "Services" column to list exactly the final 10 pages. — Accepted.
11. Use the owner's given order everywhere: Construction site prep, Building pads, Waterline install and repair, Utility excavation, Driveway installation/repair, Bushhogging, Construction debris removal, Footers, Grading, Light excavation. — Accepted.
12. Rebuild every page's "Other Services" sidebar to reference exactly the other 9 approved services, in that order. — Accepted.
13. Fix the pre-existing bug where homepage "Learn More" links point to `/services/<slug>` (404) instead of the real `/service-<slug>` pages, since this section is being rewritten anyway. — Accepted.
14. Let deleted pages' old URLs simply 404 (no redirect mechanism exists today). — Accepted.

## Services List

Synopsis — Reduce the site's advertised services from 8 to exactly the 10 owner-approved services, consistently named and ordered across the homepage (hero grid, About prose, FAQ answer), the full services page, the footer, and each service's own detail page and sidebar, replacing or removing any content that isn't on the approved list.

Stories
- S1: As the business owner, I want the site to list only the 10 approved services (Construction site prep, Building pads, Waterline install and repair, Utility excavation, Driveway installation/repair, Bushhogging, Construction debris removal, Footers, Grading, Light excavation), because listing anything beyond that creates liability/licensing exposure for the business right now.
- S2: As a prospective customer browsing the homepage, I want the services grid, About-section prose, and FAQ answer to all name the same 10 approved services in the same order, because inconsistent lists on one page erode trust.
- S3: As a prospective customer, I want every "Learn More" link, footer service link, and sidebar "Other Services" link to lead to a working page for one of the 10 approved services, because a dead link is a dead end for someone trying to get a quote.
- S4: As the business owner, I want "Land Clearing & Demolition" and "Leveling" removed entirely — page, homepage/services cards, footer link, sidebar mentions, and About/FAQ prose — because neither is on the approved list.
- S5: As the business owner, I want "Residential & Commercial Excavation" replaced by two distinct pages, "Utility excavation" and "Light excavation," with foundation/basement/pool/commercial-site-work content dropped, because that content is exactly the liability-driving material.
- S6: As the business owner, I want the "Roadbeds" page renamed and narrowed to "Driveway installation/repair," dropping access-road and general roadbed bullets, because only driveway work is approved.
- S7: As the business owner, I want "Forestry Mulching" replaced by a new, distinct "Bushhogging" page rather than relabeled mulching copy, because the two services are technically different and mislabeling misdescribes the work.
- S8: As the business owner, I want full detail pages (hero, description, bullet list, CTA, sidebar) written for the services with no existing content — Waterline install and repair, Building pads, Footers — matching the site's existing page pattern, with placeholder copy I can review and edit.
- S9: As a prospective customer, I want the homepage services grid to show all 10 approved services rather than a curated subset, because 10 is few enough to show in full.
- S10: As the business owner, I want the About-section paragraph and FAQ answer on the homepage rewritten to name only the approved 10 services, because leftover prose would keep advertising excluded work in running text even after the cards are fixed.
- S11: As the business owner, I want the footer's "Services" column rebuilt to link to exactly the 10 final service pages, in the same order as the homepage grid, because a stale footer list undercuts the fix everywhere else.
- S12: As a prospective customer, I want the homepage's existing "Learn More" links fixed so they resolve to the real page instead of 404ing, because that bug exists today independent of this trim and would undermine the rebuilt section if left in place.
- S13: As the business owner, I'm accepting that old URLs for removed services (e.g. `/service-land-clearing-demolition`, `/service-leveling`, `/service-residential-commercial-excavation`, `/service-forestry-mulching`) will simply 404 rather than redirect, because no redirect mechanism exists today and adding one is outside a content trim.

Edge cases
- S-E1: When two approved services (Utility excavation, Light excavation) both derive from one prior page (Residential & Commercial Excavation), each must get its own distinct bullet list — neither can silently disappear into the other.
- S-E2: When a new page (Waterline install and repair / Building pads / Footers / Bushhogging) has no existing bullet content to draw from, its placeholder copy must still follow the site's existing per-page pattern (hero heading, one paragraph description, 4 bullets, CTA) so it doesn't look unfinished next to the other 9.
- S-E3: When a page is deleted (Land Clearing & Demolition, Leveling, the old combined Excavation page, Forestry Mulching), every other surviving page's "Other Services" sidebar must drop that reference rather than link to a now-missing page.
- S-E4: When a page is renamed or re-slugged, every internal link to its old identity (nav, footer, homepage card, sidebar, FAQ prose) must be updated in the same pass — a rename that only touches the page's own heading but leaves a stale link elsewhere reintroduces a broken or mismatched link.
- S-E5: Visiting a deleted service's old URL directly (not via a link on the site) should return the site's normal 404, not a leftover cached page — confirm the build actually removes the old output file rather than orphaning it in `_site/`.
- S-E6: Where two kept services already had overlapping bullets under old names (e.g. "Foundation preparation" appeared on both Site Preparation and Leveling before Leveling is deleted), the surviving page's bullet list must stand on its own without depending on content that lived on the deleted page.
- S-E7: The homepage's About-section prose and FAQ sentence must be checked separately from the services grid — fixing the grid does not automatically fix prose elsewhere on the same page.
- S-E8: All 10 services must appear in the same order (the owner's original list order) across the homepage grid, the services page, and the footer column — no page should end up with a different order than another.

Dependencies — None; single subject, static Eleventy/Nunjucks content site, no other subsystem involved.

Reference (illustrative only — never copied verbatim into the codebase)

Final service → status → source mapping:

| # | Approved service | Status | Was |
|---|---|---|---|
| 1 | Construction site prep | Rename in place | Site Preparation |
| 2 | Building pads | New page | — |
| 3 | Waterline install and repair | New page | — |
| 4 | Utility excavation | New page (split) | part of Residential & Commercial Excavation |
| 5 | Driveway installation/repair | Rename + narrow in place | Roadbeds |
| 6 | Bushhogging | New page, old copy discarded | Forestry Mulching |
| 7 | Construction debris removal | Rename in place | Debris Removal |
| 8 | Footers | New page | — |
| 9 | Grading | Rename in place | Land Grading |
| 10 | Light excavation | New page (split) | part of Residential & Commercial Excavation |

Deleted entirely (page, cards, footer link, sidebar mentions, prose): Land Clearing & Demolition, Leveling, Residential & Commercial Excavation (combined page), Forestry Mulching (old copy).
