# Dimas Adi Darmawan — Digital Marketing & Creative Communication Portfolio

Static site built from `PRD_Website_Portofolio_Marketing_Creative_v2.docx` and
`Content-Inventory_v2.xlsx`, using `PRPortfolioDimasAdiDarmawan.zip` as the
authoritative structural + asset reference. Plain HTML/CSS/JS, no build step,
no framework — same as the reference codebase. Deploy by uploading this
folder as-is to any static host (GitHub Pages, Netlify, Vercel, Canva Sites,
etc.) with `index.html` at the root.

## Design direction: reverted to match the reference codebase exactly

**This build no longer applies the PRD's Section 4 (Deep Teal + Amber) and
Section 5 (UI/UX enhancement) proposals.** Per Dimas's explicit instruction,
the Selected Work layout and every color token were changed back to match
`PRPortfolioDimasAdiDarmawan.zip` exactly:

- **Colors**: `:root` tokens, the 5 contrast "companion fixes," `favicon.svg`,
  and every hardcoded `rgba()` glow/overlay are back to the reference's
  original teal (`#2F6F5E` accent, `#14231F` deep bookend) + terracotta
  (`#C97B4A` secondary accent) palette. Nothing here still runs Amber.
- **Selected Work**: removed the category filter row, `.project-card--wide`
  usage, the coursework tag color variant, and the view-count badges. All 9
  project cards are now plain, uniform `.project-card` entries in a 3-column
  grid — visually identical treatment to the reference's own 6-card section,
  just with 9 cards instead of 6. `main.js` no longer carries the filter
  click handler (it's byte-for-byte identical to the reference's `main.js`
  again).

The `.exp-media--gallery` Committee Visit gallery and the 2-column education
timeline are unaffected — those already matched the reference's own markup
before this change and still do.

If a future revision wants the Deep Teal + Amber identity or the Section 5
enhancements back, they're described in full in `PRD_Website_Portofolio_Marketing_Creative_v2.docx`
Sections 4–5; this repo just isn't running them right now.

## Asset status: 34 real photos, 0 placeholders

An initial build (before `PRPortfolioDimasAdiDarmawan.zip` was supplied) used
whatever photos existed in this git repo, which turned out to be an older,
thinner snapshot than the PRD's own asset inventory assumed. Once the actual
reference `.zip` was provided, **every one of those real photos/certificates
was swapped in**, plus the gallery and timeline components were corrected to
match the reference codebase's real markup (`.exp-media--gallery` /
`.gallery-item`, and a 2-column education timeline) instead of the
approximated versions used in the first pass.

### Real photos in place (34 files)
Hero and About portraits, both Disnaker (internship) and KPID (event) photos
and certificates, all 7 Committee Visit company photos (Mandom,
Faber-Castell, Sari Roti, Metro TV, Ajinomoto ×3), all 9 Selected Work
project photos, all 9 certificate scans, and both Leadership org photos +
the BEM certificate — all pulled directly from the reference `.zip`, byte for
byte, at their authentic dimensions.

Three photos were supplied directly by Dimas afterward, all now linked to
their real sources:
- The Sariwangi Tea short film's project photo (`projects/sariwangi-film.jpg`)
  — a still frame from the film — linked to its real YouTube upload and Canva
  research doc.
- The Disnaker Infographics/Reels/Coverage project photo
  (`projects/disnaker-content.jpg`) — a cropped montage of six real
  Instagram posts from the department's official account — linked to a real
  infographic post, a Reels video, and a field-coverage Reels video.
- The Cimory Squeeze Yogurt TVC project photo (`projects/cimory-tvc.jpg`) —
  a product close-up — linked to its real YouTube upload and Canva research
  doc.

`assets/img/org/english-2.jpg` is also included as a spare (the reference
site's own HTML only ever displays `english-1.jpg`, since its org-card layout
shows one photo per card — this build matches that behavior).

No placeholders remain. Every image and every outbound link on the site
resolves to real content.

## Decisions defaulted (PRD Section 9) — confirm with Dimas before launch

The build had to pick an answer for each of the PRD's 9 open decisions so the
site would actually ship. None of these are hard to change — flagging them
here so nothing gets mistaken for a verified fact.

1. **Two-site strategy** — proceeded as a fully separate site, per the PRD's own scope.
2. **Visual direction** — reverted to the reference codebase's original teal + terracotta palette per Dimas's explicit instruction (see "Design direction" above) — the PRD's Deep Teal + Amber proposal is not currently applied.
3. **Degree on Hero** — used "Communication Science Graduate" (not "S.I.Kom"), since the program runs through 2026 and the degree isn't conferred yet.
4. **Current city** — used "Karawang, West Java, Indonesia" per the PRD's own note.
5. **Instagram handle** — kept the reference site's existing split: `@gulagin__` on the Alluvia project link, `@dimasdarmawan2` on the general Contact link. **Still needs Dimas's confirmation** — pick one if a single handle is preferred.
6. **Writing-sample section** — not added; video/design work carries the "Selected Work" section for now.
7. **"Fluoxetine" poster** — kept, described neutrally (typography/poster-design skill only, no plot detail) given the sensitive subject matter. **Confirm keep/remove** — it's a single card, trivial to remove from `index.html` (`#work` section) if Dimas prefers.
8. **"Sole liaison" wording** — softened to "served as field liaison" (dropped "sole") since it's an unverified superlative — the reference site's own copy says "sole." Restore the original wording if Dimas confirms it's accurate.
9. **New assets/links** — see placeholder list above.

## What still follows the PRD
- Content: all 9 Selected Work projects, 9 certificates, 3 experience entries, 2 leadership entries, 4 competency groups — copy and structure per PRD Section 6.
- Hero stat swap to "Content pieces produced: 80+" (PRD 5.5) and the new marquee keyword set (PRD 5.6) — content-level changes, kept since the layout/color revert didn't touch these.
- Nav now includes **Leadership**, which was missing from the reference site's own nav/scrollspy even though the section exists in its HTML — fixed here per the PRD's sitemap (Section 3).
- Typo/consistency fixes carried over: no "RESEACRH" typo, all CTAs in English, "Content Strategy" capitalized consistently.
- Gallery and timeline components structurally match the reference codebase's own markup and CSS classes exactly (`.exp-media--gallery`, `.gallery-item`, `.gallery-caption`, 2-column `.timeline`).

## Not currently applied from the PRD
- Section 4 (Deep Teal + Amber palette, including the 5 WCAG companion fixes) — reverted, see "Design direction" above.
- Section 5.1–5.4 (wide project cards, coursework tag color variant, view-count badges, category filter chips) — reverted; Selected Work is a plain uniform grid again, matching the reference.

## Verified before delivery
- Every `src`/`href`/`data-lightbox` path resolves to a real file — zero broken images or links.
- No orphaned/unused image files besides the intentional `english-2.jpg` spare.
- `assets/css/style.css` and `assets/js/main.js` diffed line-by-line against the reference codebase — only intentional content differences remain (site title/description, 9 vs. 6 project cards, the cert-footnote disclaimer).
- Mobile viewport (390px) has no horizontal scroll.
- No console/page errors on load.
