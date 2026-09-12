# NESTRE — "The App" page (review build)

A rebuild of the `/the-app` page for **nestre-os-cms**, built to the reverse-engineered
NESTRE brand guidelines. This repo is for **review by UXOKDC** before the page is merged
into the main site.

**Live preview:** https://nestre-mindset.vercel.app/the-app.html
**Brand guidelines:** open `nestre-brand-guidelines.html` (or the hosted Artifact link shared separately)

---

## For UXOKDC — integrating into `nestre-os-cms` (after approval)

The page is a single self-contained file (`the-app.html`) with inline CSS/JS. To port it,
copy the page section markup + its `<style>`/`<script>`, and bring these asset folders:

| Copy this | Used for |
|---|---|
| `the-app.html` | the page — hero, sections, inline styles + GSAP scripts |
| `assets/appshots/*.png` | app screenshots (hero, section 2 cycle, feature/step tiles) |
| `assets/personas/*.jpg` | Mindset Profile persona photos + the "new lens" cards |
| `assets/img/water.jpg` | "Room to reset" media |
| `assets/img/sunrise.jpg` | closing CTA background |
| `assets/video/app-hero.mp4` | hero background video (poster: `assets/img/water.jpg`) |

GSAP + ScrollTrigger load from cdnjs via two `<script>` tags — no build step, no npm.

---

## What changed vs. the original `the-app` design

1. **Hero** — same layout; now uses `app-hero.mp4` as a background video.
2. **Section 2 "On every screen"** — rebuilt as **side-by-side + sticky**: eyebrow, headline
   and the 3 category pills (**Everyday Life · Performance · Health & Wellness**) on the left;
   one large phone on the right that cycles through every app screen (slide + fade, one-by-one)
   while pinned, until all screens are seen.
3. **Removed** the "What's on your mind?" section entirely.
4. **In its place** — the **full-viewport Mindset Profile** (side-by-side "V2"): a sticky ring
   that reshapes across 4 personas as you scroll.
5. **Everything else** recreated to match the brand system (paper/navy band rhythm, aqua
   accent, Instrument Sans, pill buttons).

> Body copy in the recreated sections is on-brand placeholder text (the source CMS was
> unavailable at build time); swap in final copy as needed.

---

## Repo contents

- `the-app.html` — **main deliverable**
- `nestre-brand-guidelines.html` — reverse-engineered design system (tokens, type, components)
- `mindset-v1.html` / `mindset-v2.html` — Mindset Profile section, A/B (V2 is the one used in the page)
- `index.html` — A/B chooser landing
- `assets/` — all images, screenshots, and video

---

*Design tokens: Paper `#F4F3EE` · Navy `#081C26` · Ink `#10212A` · Aqua `#98D6D3` · Instrument Sans.*
