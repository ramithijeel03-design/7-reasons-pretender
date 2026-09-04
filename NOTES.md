# LymphDrop — 7 Reasons Pre-Lander — Deployment Notes (v4)

**File:** `7-reasonsv1.html` — single self-contained block for a Shopify page.
Built to the v2 rebuild brief: Javvy 1:1 layout, image-left/text-right
reasons, inline 👉 CTA links, cream dashed final offer block. Launch-ready —
**every image loads live from your store CDN, nothing to upload.**

## How to deploy

1. Shopify Admin → **Online Store → Pages → Add page**.
2. Title: `7 Reasons Why LymphDrop Uses 11 Herbs Instead of 4`.
3. Click the **`<>` (Show HTML)** button in the content editor toolbar.
4. Paste the ENTIRE contents of `7-reasonsv1.html`.
5. Set **Search engine listing → URL handle** to `7-reasonsv1`.
6. Save → set visibility → done.

> ⚠️ **Only ever edit this page via the `<>` HTML view.** Saving from the
> visual (rich text) editor can strip the styles and the countdown script.

## Page structure (per brief v2)

- Sticky teal announcement bar: 🔥 50% off + SALE ENDS IN countdown
- Left-aligned headline → avatar byline (Research Team, Sep 2026) → quote hook
- Comparison table: LymphDrop column card with teal header, 5 rows, ✅/❌
- TLDR line
- Reasons 1–7: square image left (40%) / number + headline + body right;
  stacked image-top on mobile; herbs as bullets in reasons 5 & 6
- Inline 👉 teal underlined CTA links after reasons 3, 4, 5, 6, 7 only
  (unique anchor text each, all carrying the UTM string)
- Centred escalation block with ✨ subtext
- Final CTA: cream `#FFFBF0` dashed box — product image left; 🎁 FREE BOTTLE
  badge, 50% OFF headline, demand line, synced timer, dark-teal pill button,
  risk line right
- Compliance footer

Removed from previous build: testimonials band, herb cards, SVG diagrams,
logo header.

## Images (all live)

Reasons 1–7: `Reason_1.png` … `Reason_7.png` · Author avatar:
`untitled_Gemini_3_Nano_Banana_Pro__2026-09-04_03-27-33.png` · Final offer:
`L2.png` — all on cdn.shopify.com, URLs exactly as briefed.

## Countdown timer

Counts down to **2:00 PM Australia/Sydney daily** (DST-safe; UTC+10 fallback
on ancient browsers). Top bar and final block always in sync; rolls over at
2pm automatically.

## QA before traffic

- [ ] Phone: sticky bar + timer visible on load; reason images stack on top.
- [ ] All 9 images load (Reason_1–7, avatar, L2).
- [ ] All 5 👉 links + final button land on the PDP with UTM intact and
      $39.95 / $79.95 compare-at pricing.
- [ ] Table swipes horizontally on mobile.
- [ ] Timer shows time to 2pm Sydney, not a fixed 24h.
- [ ] Clarity records the page (store-wide install, nothing to add).
