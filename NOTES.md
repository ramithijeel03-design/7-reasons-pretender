# LymphDrop — 7 Reasons Pre-Lander — Deployment Notes

**File:** `7-reasonsv1.html` — a single self-contained HTML/CSS/JS block for a Shopify page. No PageFly, no external assets, no dependencies.

## How to deploy

1. Shopify Admin → **Online Store → Pages → Add page** (or open the draft page if one was already created for you).
2. Title: `7 Reasons Why LymphDrop Uses 11 Herbs Instead of 4`.
3. In the content editor toolbar click the **`<>` (Show HTML)** button.
4. Paste the ENTIRE contents of `7-reasonsv1.html`.
5. Set **Search engine listing → URL handle** to `7-reasonsv1`.
6. Save. Set visibility when ready to go live.

> ⚠️ **Never re-save the page from the visual (rich text) mode.** Always edit
> via the `<>` HTML view. The visual editor can strip the `<style>` and
> `<script>` tags that power the design and countdown timer.

## Swapping in real images

Search the file for `IMG-SLOT` — there are 11 slots, each a labelled placeholder
box. Upload each image via **Shopify Admin → Content → Files**, copy its CDN
URL, then replace the whole `<div class="ld7-ph" ...>...</div>` block with:

```html
<img class="ld7-img" src="CDN-URL-HERE" alt="Description" loading="lazy" width="800" height="500">
```

For testimonial avatars replace the `<div class="ld7-avatar">...</div>` with:

```html
<img class="ld7-avatar" src="CDN-URL-HERE" alt="David K." loading="lazy" width="80" height="80" style="object-fit:cover;border:none;">
```

Logo: search `LOGO-SLOT` (header is on white — use the black logo version).

## Countdown timer behaviour

- 24-hour countdown, stored in `sessionStorage` — resets on every new visit
  (new tab/session), persists across refreshes within the same visit.
- Top bar and final offer block are synced (same storage key `ld7TimerEnd`).
- Rolls back to 24:00:00 if it ever hits zero mid-session.

## Optional: hide theme header/footer

The page works inside your normal theme layout. For a cleaner pre-lander
(recommended for paid traffic), create a stripped page template:

1. Online Store → Themes → ⋯ → **Edit code**.
2. Under **Templates**, add a new template: type `page`, name `prelander`.
3. In the new template remove/keep sections as desired (remove header/footer
   section references in a JSON template, keep only the main page content).
4. Assign it to the page under **Theme template** on the page editor sidebar.

## QA checklist before sending traffic

- [ ] Open on a phone: countdown visible without scrolling.
- [ ] All 4 CTA buttons land on the PDP with `?utm_source=meta&utm_medium=paid&utm_campaign=prelander&utm_content=7reasons` intact and 50% compare-at pricing showing.
- [ ] Comparison table swipes horizontally on mobile.
- [ ] Timer resets in a fresh incognito tab.
- [ ] Real images swapped in, no placeholder boxes left.
- [ ] Microsoft Clarity session shows up for the page (installed store-wide, nothing extra needed).
