# LymphDrop 7-Reasons Pre-Lander — Strategy Record

Bridge page between Meta video ads and the PDP. Replicates the Javvy Coffee
listicle format (try.javvycoffee.com/a/a61) adapted to 7 reasons, built as a
single HTML file dropped into a native Shopify page (no PageFly — decided
2026-07-22).

## Locked decisions

| Decision | Call |
|---|---|
| Build method | Single self-contained HTML file → pasted into a Shopify page via the `<>` HTML editor. No PageFly. |
| Competitor naming | Generic **"Standard 4-Herb Formula"** column — Lymphoria never named (legal + Meta disparagement risk; the ad already primes the 4-herb comparison). |
| 11 ingredients | All 11 herbs woven into the 7 reasons: each stage reason (2–5) keeps its hero herb + an "Also working Stage N" card. Stage 1: Burdock, Calendula (2) · Stage 2: Cleavers, Echinacea, Plantain (3) · Stage 3: Yarrow, Rose Hip, Blue Vervain (3) · Stage 4: Dandelion, Elderberry, Thyme (3). |
| ALT testimonial | Softened — David K. now says "my check-up came back the best it's been in two years" (no lab-marker claim). |

## Key research findings (July 2026)

**Lymphoria (competitor, unnamed on page):** exactly 4 herbs — Cleavers, Red
Clover Blossom, Stillingia Root, Prickly Ash Bark. Plain alcohol-free tincture,
no liposomal/delivery story (our biggest wedge). Guarantee is 30-day
discretionary (advertised as 60 in ads) vs our 90-day no-questions. **They
pre-emptively attack multi-herb formulas as "fillers (11–26 ingredients)"** —
so the page argues stage coverage ("11 jobs, 11 herbs, zero filler"), never
"more herbs = better". Their hero herb (Cleavers) is inside our formula.
Their audience skews women; ours is men 45+ who drink.

**Javvy reference page:** verified structure = urgency bar w/ countdown +
"Sell-Out Risk" red text → numbered benefit-led reasons (1–3 short paragraphs +
one image each) → interspersed CTAs → testimonials that echo the preceding
claims → final CTA banner recapping all USPs as a checklist → guarantee close.
The Javvy family has **no comparison table** — ours is an intentional addition
because this page's job is competitor displacement.

**Store facts (verified via Shopify Admin):**
- Active product handle `lymphdrop™-liposomal-lymphatic-drainage-drops`
  ($39.95, compare-at $79.95 = the "50% off, auto-applied" — no discount code
  exists or is needed). Variants Buy 1 / Buy 2 Get 1 / Buy 3 Get 2 live on the
  PDP (bundles intentionally not shown on pre-lander).
- Label (source of the 11 herbs): European Elder Berry, Burdock Root, Calendula
  Flower, Cleavers Herb, Dandelion Root, Echinacea Root, Rose Hip, Plantain
  Leaf, Yarrow Leaf/Flower, Blue Vervain Herb, Thyme Leaf. Liposome carrier:
  phosphatidylcholine from non-GMO sunflower oil (used in Reason 6 copy).

## Page structure (as built)

1. Sticky red announcement bar — 50% off + 24h countdown (sessionStorage, resets per visit, synced top/bottom)
2. Logo header (text wordmark, swap slot for black logo)
3. H1 + research-team byline + hook line
4. Comparison table (LymphDrop / Standard 4-Herb Formula / Capsules)
5. TLDR box
6. Reasons 1–7 (CTAs after 1, 4, 6; testimonial band after 4; herb cards on 2–5)
7. Escalation block
8. Final offer: 50% badge, countdown #2, bundle shot, 6-item ✓ checklist, red CTA, risk line
9. FTC/TGA-safe footer disclaimer

All 4 CTAs → PDP with `utm_source=meta&utm_medium=paid&utm_campaign=prelander&utm_content=7reasons`.
