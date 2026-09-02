# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository purpose

This is a **content repository**, not a software project. It holds finished SEO deliverables (Markdown files) written for **weboot.it**, an Italian wellness/supplements content site, and its Be Health product line. There is no build system, no tests, no linter, and no application code — every file under `articoli/` is a self-contained content deliverable ready to hand off to the client.

## Deliverable structure

Each file in `articoli/*.md` follows the same fixed template, in this order:

1. **Title line** (`# Deliverable SEO — <topic>`) followed by a one-line brief: which silo/hub the piece belongs to, the target URL on weboot.it, and (for cluster articles) which pillar article it links back to.
2. Optional **`Nota importante`/`Aggiornamento`** callout right after the brief — used when the piece is a personal landing page (first-person as "Alessandro"), preserves original CTAs/images/WhatsApp links verbatim, or resolves a cannibalization/redirect issue. Read this note before editing — it records constraints (e.g. "keep this exact phone number and pre-filled WhatsApp text") that aren't otherwise visible in the HTML.
3. **`## a) Titolo SEO`** — SEO title with character count noted.
4. **`## b) Meta description Yoast`** — ≤155 characters, with character count noted.
5. **`## c) Titolo clickbait onesto`** — an "honest clickbait" alternate headline.
6. **`## d) Testo Facebook`** — social share copy with emoji bullets and a CTA back to the article.
7. **`## e) Articolo HTML completo`** — the actual article body, as a fenced ```html block ready to paste into the CMS (uses `<p>`, `<h2>`/`<h3>`, `<ul>/<li>`, `<strong>`; no inline styles or classes).
8. **`## f) Prompt immagine Nano Banana`** — an image-generation prompt (for the "Nano Banana" tool) describing the featured/Discover image for the piece.
9. **`## Note metodologiche`** — explicitly marked as *not* part of the deliverable, for internal transparency only. Lists what was fact-checked, which myths were debunked, which internal links were used (and why), and confirms no invented testimonials/quotes were added.

When creating a new article or editing an existing one, preserve this section order and heading format exactly — the client consumes these files section-by-section.

## Content conventions to preserve

- **Language**: all deliverables are in Italian.
- **Fact-checking discipline**: claims in section (e) are expected to be backed by real evidence; section 9 (`Note metodologiche`) must reflect whatever fact-checking, myth-busting, or sourcing decisions were actually made. Don't add unverifiable claims, and don't invent testimonials, reviews, or quotes attributed to real or fictional people.
- **Internal linking**: only link to URLs that actually exist in the site's sitemap/silo structure (as referenced in the brief or prior articles) — don't fabricate URLs.
- **Personal/landing pages** (e.g. `collagene-supernova-su-amazon.md`, `integratori-stanchezza-dolori-articolari.md`) are written in first person as "Alessandro" and include product CTAs, images, and WhatsApp links with specific pre-filled text/numbers — these must be preserved exactly, not paraphrased, when revising such pages.
- **Silo/pillar relationships**: articles belong to named silos (e.g. `rimedi/collagene`, `be-health`) and reference their pillar/cluster relationships in the brief line — check sibling articles in `articoli/` for the same silo before changing internal links or claims, to keep the cluster consistent.
