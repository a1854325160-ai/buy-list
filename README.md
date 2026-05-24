# Buy List Design System

## Overview

**Buy List** is a shopping list and purchase management app. The product is built around helping users track what they need to buy — organized, delightful, and fast. The brand is **professional yet lively**: warm, approachable, interactive, and built on generous rounded corners throughout.

### Brand Personality
- 溫暖 Warm — uses warm color tones throughout, never cold blues or flat grays
- 活潑 Lively — interactive elements feel bouncy and responsive; the UI rewards action
- 專業 Professional — clean hierarchy, consistent spacing, readable type
- 有互動感 Interactive — hover states, transitions, press feedback everywhere
- 圓潤 Rounded — large border-radii on nearly every element (cards, buttons, inputs, avatars)

### Sources
No external codebase or Figma was provided. This design system is authored from the brand brief:
> 暖色系副色白色 有互動感 專業又活潑 使用大量圓角
> (Warm color palette, white as secondary, interactive feel, professional yet lively, lots of rounded corners)

---

## Content Fundamentals

### Tone of Voice
- **Friendly + direct**: Talks *to* the user, not at them. "Your list is ready" not "The list has been prepared."
- **You-focused**: Uses "你" / "you" framing. Avoids passive voice.
- **Warm micro-copy**: Error messages are helpful, not alarming. Empty states have personality.
- **Action-oriented**: CTAs use verbs — "Add Item", "Start Shopping", "Mark Done" — not nominals.
- **Concise**: Headings are short. Body copy is scannable. No walls of text.
- **Bilingual-ready**: Core app is Chinese-first (Traditional Chinese) but layout accommodates English labels.

### Casing
- UI labels: Title Case in English ("Add Item"), 全小寫 avoided
- Headings: Sentence case in English ("Your shopping list")
- Buttons: Title Case ("Add to List")

### Emoji
- Emoji are used **sparingly** for decoration in empty states or celebrations only
- Not used as functional icons (dedicated icon system instead)
- Example: "🎉 All done!" on completion screen

### Examples
- Empty state: "還沒有任何項目 — 點擊 + 開始新增" / "Nothing here yet — tap + to add your first item"
- Success: "✓ Added to your list"
- Error: "Oops, that didn't save. Try again?"
- Button: "開始購物" / "Start Shopping"

---

## Visual Foundations

### Color
- **Primary**: Orange (`#F97316`) — warm, energetic, trustworthy
- **Primary scale**: 50–900 (orange/amber family)
- **Accent**: Coral/Rose (`#FB7185`) — used for badges, highlights, attention
- **Secondary**: White (`#FFFFFF`) — dominant background, clean negative space
- **Neutral**: Warm stone scale (stone-50 → stone-900) — never cold gray
- **Semantic**: success (warm green), warning (amber), error (rose-red), info (warm indigo)
- **Surfaces**: Light surface = `#FFF7ED` (primary-50); cards = `#FFFFFF` with subtle shadow

### Typography
- **Display / Headings**: **Plus Jakarta Sans** — geometric, rounded terminals, friendly authority
- **Body**: **DM Sans** — clean, neutral, highly legible at small sizes
- **Monospace**: **JetBrains Mono** — for prices, quantities, codes
- **Scale**: 10 steps from xs (12px) to 5xl (48px) with a modular scale ≈ 1.25
- **Weight range**: 400 (body), 500 (label), 600 (subheading), 700 (heading), 800 (display)
- **Line height**: 1.5 for body, 1.2–1.3 for display

### Spacing
- Base unit: **4px**
- Scale: 4, 8, 12, 16, 20, 24, 32, 40, 48, 64, 80, 96px
- Components use multiples of 4; page margins use multiples of 8

### Border Radius (大量圓角 Generous Rounding)
- **xs**: 6px — tags, chips
- **sm**: 10px — inputs, small cards
- **md**: 16px — standard cards, buttons
- **lg**: 20px — large cards, bottom sheets
- **xl**: 28px — hero cards, modal dialogs
- **full**: 9999px — pill badges, avatar circles, toggle switches

### Shadows & Elevation
- **Level 0**: No shadow (flat, in-surface)
- **Level 1**: `0 1px 3px rgba(0,0,0,.06), 0 1px 2px rgba(0,0,0,.04)` — cards, dropdowns
- **Level 2**: `0 4px 12px rgba(249,115,22,.10), 0 2px 6px rgba(0,0,0,.06)` — floating action buttons, active cards (tinted orange)
- **Level 3**: `0 12px 32px rgba(249,115,22,.15), 0 4px 12px rgba(0,0,0,.08)` — modals, sheets (warm shadow)

### Backgrounds & Surfaces
- App background: `#FFF7ED` (warm orange-50) or `#FAFAF9` (stone-50)
- Cards: `#FFFFFF` with Level 1 shadow
- Header/Nav: White with bottom border `#F5F5F4`
- Accent surface: `#FFEDD5` (primary-100) for highlighted sections
- **No heavy gradients** — subtle linear gradients only as decorative accents on hero banners

### Animation & Motion
- Easing: `cubic-bezier(0.34, 1.56, 0.64, 1)` — slight overshoot/bounce for interactive feedback
- Standard: `cubic-bezier(0.4, 0, 0.2, 1)` — smooth ease-in-out for transitions
- Duration: 120ms (micro), 200ms (standard), 300ms (enter/exit), 400ms (layout shifts)
- Hover: scale(1.02) + shadow lift on cards; background tint on list items
- Press: scale(0.96) with slight shadow reduction
- Checkmark: Animated SVG stroke on completion
- Entry: Fade + slide-up (8px) for new list items

### Hover & Press States
- **Buttons**: darken 8%, slight scale(1.02)
- **Cards**: shadow lift to Level 2, translateY(-2px)
- **List rows**: background → primary-50
- **Icon buttons**: circular background fill (primary-100)
- **Press/Active**: scale(0.96), shadow reduce

### Imagery & Icons
- **Icon style**: Lucide Icons — 24px, 1.5px stroke, rounded caps/joins
- **Illustration**: Simple, minimal line-art with warm orange fills — not used heavily
- **Photography**: Not part of core UI; product images use rounded corners (radius-md)
- **Color vibe**: Warm — imagery should have warm tones when used

### Corner Radii in Practice
- Inputs: `border-radius: var(--radius-md)` (16px)
- Buttons: `border-radius: var(--radius-full)` (pill) or `var(--radius-md)`
- Cards: `border-radius: var(--radius-lg)` (20px)
- Avatars: `border-radius: var(--radius-full)` (circle)
- Chips/Tags: `border-radius: var(--radius-full)` (pill)
- Modals: `border-radius: var(--radius-xl)` (28px) top corners

---

## Iconography

- **System**: [Lucide Icons](https://lucide.dev/) via CDN — `https://unpkg.com/lucide@latest`
- **Style**: Outline/stroke icons, 1.5px stroke weight, rounded line caps and joins
- **Size**: 16px (small/inline), 20px (default UI), 24px (primary actions), 32px (hero/feature)
- **Color**: Inherits text color; accent icons use `--color-primary-500`
- **Emoji**: Used only in celebratory/empty state moments, not as functional icons
- **No custom SVG icon font** — Lucide covers all shopping/list UI needs

Key icons used in Buy List:
- `shopping-cart`, `shopping-bag` — primary app metaphor
- `check`, `check-circle-2` — completion states
- `plus`, `plus-circle` — add actions
- `trash-2` — delete
- `tag`, `tags` — categories
- `search` — search bar
- `user`, `users` — account/sharing
- `star`, `heart` — favorites
- `bell` — notifications
- `share-2` — sharing lists
- `package` — items/products
- `receipt` — purchase history

---

## App Concept (Updated)

Buy List is a **personal purchase wishlist** — not a grocery app. Users track items they want to buy (laptops, drones, gadgets) across three priority sections:

1. **優先購入** — Priority: buy soon
2. **延後購入** — Deferred: buy later
3. **觀望** — Watching: still deciding

**Updated color direction**: Primary black `#111`, secondary white `#fff`. Clean, minimal, reminder-like feel.

---

## File Index

```
README.md                          ← You are here
SKILL.md                           ← Skill definition for Claude Code
colors_and_type.css                ← All CSS custom properties (tokens)
assets/
  logo.svg                         ← Buy List logo (wordmark, dark text)
  logo-icon.svg                    ← Icon-only logomark
  logo-dark.svg                    ← Wordmark on dark backgrounds
preview/
  colors-primary.html              ← Primary orange scale (warm accent)
  colors-neutral.html              ← Neutral warm stone scale
  colors-accent.html               ← Coral/rose + amber secondaries
  colors-semantic.html             ← Success/warning/error/info + surfaces
  type-scale.html                  ← Full 9-step type scale
  type-specimens.html              ← Display/body/mono/weight specimens
  spacing-tokens.html              ← 4px-base spacing scale, 12 steps
  radius-shadow.html               ← 7-step radius + 4-level elevation
  components-buttons.html          ← Button variants, sizes, states
  components-inputs.html           ← Inputs, search, checkbox, toggle
  components-cards.html            ← Card variants (list, summary, compact)
  components-badges.html           ← Badges, category chips, status dots
  components-list-items.html       ← Shopping row states
ui_kits/
  app/
    README.md                      ← App UI kit guide
    index.html                     ← Interactive prototype (black/white)
    ios-frame.jsx                  ← iOS bezel starter component
```
