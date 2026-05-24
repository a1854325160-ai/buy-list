---
name: buylist-design
description: Use this skill to generate well-branded interfaces and assets for Buy List — a personal purchase wishlist app. Contains essential design guidelines, colors, type, fonts, assets, and UI kit components for prototyping.
user-invocable: true
---

Read the README.md file within this skill, and explore the other available files.

If creating visual artifacts (slides, mocks, throwaway prototypes, etc), copy assets out and create static HTML files for the user to view. If working on production code, you can copy assets and read the rules here to become an expert in designing with this brand.

If the user invokes this skill without any other guidance, ask them what they want to build or design, ask some questions, and act as an expert designer who outputs HTML artifacts _or_ production code, depending on the need.

## Quick Reference

**Brand**: Buy List — personal purchase wishlist / reminder app for bigger items (electronics, gadgets, etc.)

**Color**: Primary #111 (near-black), Secondary #fff (white). Warm orange (#f97316) available as tertiary accent if needed.

**Type**: Plus Jakarta Sans (display/headings, 800 weight for titles), DM Sans (body), JetBrains Mono (prices/quantities)

**Rounding**: Generous — 13–20px on cards, 9999px on pills/FAB/checkboxes

**3 Core Sections**:
1. 優先購入 (Priority) — dot #111
2. 延後購入 (Deferred) — dot #888  
3. 觀望 (Watching) — dot #ccc

**Tone**: Minimal, clean, reminder-like. NOT a grocery app. Items = electronics, gadgets, big purchases.

**Key Files**:
- `colors_and_type.css` — all CSS custom properties
- `ui_kits/app/index.html` — interactive prototype
- `assets/` — logo SVGs
- `preview/` — component cards
