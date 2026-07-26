# LymphDrop — 7 Reasons Pre-Lander — Deployment Notes (v2)

**File:** `7-reasonsv1.html` — a single self-contained block for a Shopify page.
Javvy-style layout, brand teal, launch-ready: every image is live (product
photos load from your store CDN, diagrams and avatars are built-in vector
graphics). Nothing to fill in.

## How to deploy

1. Shopify Admin → **Online Store → Pages → Add page**.
2. Title: `7 Reasons Why LymphDrop Uses 11 Herbs Instead of 4`.
3. In the content editor toolbar click the **`<>` (Show HTML)** button.
4. Paste the ENTIRE contents of `7-reasonsv1.html`.
5. Set **Search engine listing → URL handle** to `7-reasonsv1`.
6. Save → set visibility → done.

> ⚠️ **Only ever edit this page via the `<>` HTML view.** Saving from the
> visual (rich text) editor can strip the styles and the countdown script.

## Images

| Where | Source |
|---|---|
| Reason 3 | Herbs infographic `L3.png` from your CDN — CSS-cropped to hide the bottom "6 Traditional Herbs" text row, which contradicts the 11-herb story (it also names red clover, which isn't on your label) |
| Reason 5 | Supplement Facts panel `L6.png` (all 11 herbs on the label) |
| Reason 7 | Bottle photo `L1.png` |
| Final offer | Box + bottle photo `L2.png` |
| Reasons 1, 2, 4, 6 | Built-in vector diagrams (4 stages, dissolve, pump, liposome vs stomach acid) in brand colours |
| Testimonials | Built-in monogram avatars (DK / MT / JR) |

To swap any photo later: find its `<img ... src="https://cdn.shopify.com/...">`
tag and replace the URL between the `src="..."` quotes.
Logo: search `LOGO-SLOT` to swap the text wordmark for your black logo image.

> Note: if you ever fix the infographic's "6 Traditional Herbs" row to say 11,
> you can remove the crop by deleting the `<div class="ld7-crop">` wrapper
> around that image.

## Countdown timer

- Counts down to **2:00 PM Australia/Sydney, every day** (DST-safe via the
  browser's timezone database; falls back to UTC+10 on very old browsers).
- Top bar and final offer block always show the same time.
- At 2pm it rolls over to the next day automatically.

## QA checklist before sending traffic

- [ ] Open on a phone: teal SALE ENDS IN bar + timer visible without scrolling.
- [ ] Timer shows time remaining until 2pm Sydney (not a fixed 24h).
- [ ] All 4 product photos load (they come from cdn.shopify.com).
- [ ] Reason 3 image is cropped — no "6 Traditional Herbs" text visible.
- [ ] All 5 CTA buttons land on the PDP with the UTM string intact and
      $39.95 / $79.95 compare-at pricing showing.
- [ ] Comparison table swipes horizontally on mobile.
- [ ] Microsoft Clarity records the page (installed store-wide, nothing to add).
