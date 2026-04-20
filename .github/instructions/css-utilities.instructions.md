---
description: CSS utility classes and styling practices for this Python/Jinja2 project. Cozy coffee shop theme.
---

# CSS Styling Practices — Cozy Coffee Shop Theme

## Overview
This project uses a **"Cozy Coffee Shop"** design theme with custom CSS in `app/static/css/app.css`. Fonts (Gaegu + Nunito) are vendored in `app/static/fonts/`. All styling is self-contained — no external CDN.

## Design Tokens (CSS Variables)
```css
/* Warm palette — defined in :root */
--cream, --linen, --cork, --cork-dark
--espresso, --espresso-mid, --espresso-light
--terracotta, --terracotta-light
--sage, --sage-dark, --sage-light
--mustard, --mustard-light, --mustard-dark
--paper, --paper-shadow, --overlay
--coffee-brown, --coffee-light, --latte-cream
```

## Fonts
- **Gaegu** (handwritten) — headings, use `.cozy-heading` class
- **Nunito** — body text (default via `body` rule)

## Key Component Classes
```css
.cozy-heading    /* Gaegu handwritten font for headings */
.btn-cozy        /* Terracotta gradient button with hover lift */
.btn-back        /* Subtle back button */
.cozy-header     /* Paper-style page header */
.cozy-card       /* Cork-bordered card */
.bg-cork         /* Cork board texture background */
.bingo-square    /* Board square with paper card feel + staggered reveal */
.bingo-square.marked   /* Sage green marked state */
.bingo-square.winning  /* Mustard gold winning state */
.bingo-square.free-space /* Dashed linen free space */
.stamp-check     /* Check mark with stamp animation */
.bingo-banner    /* Mustard gradient BINGO indicator */
.modal-overlay   /* Overlay with blur */
.modal-card      /* Warm glow modal */
.coffee-scene    /* CSS coffee cup illustration (BINGO win) */
.spill-scene     /* Coffee spill animation (game reset) */
```

## Layout Utilities (unchanged names)
```css
.flex, .flex-col, .flex-1, .grid, .grid-cols-5
.items-center, .justify-center, .justify-between
.h-full, .w-full, .w-16, .min-h-full
.max-w-xs, .max-w-sm, .max-w-md, .aspect-square
```

## Spacing (unchanged names)
```css
.p-1, .p-3, .p-4, .p-6, .px-3, .px-4, .px-6, .px-8
.py-1\.5, .py-2, .py-3, .py-4
.mb-2, .mb-3, .mb-4, .mb-6, .mb-8, .mx-auto
.gap-1, .space-y-2
```

## Colors (mapped to cozy palette)
```css
/* Backgrounds — same class names, warm values */
.bg-white → paper    .bg-gray-50 → cream    .bg-gray-100 → linen
.bg-accent → terracotta gradient    .bg-marked → sage-light
/* Text — same class names, espresso/sage/mustard values */
.text-gray-500..900 → espresso shades
.text-green-600..800 → sage    .text-amber-500..900 → mustard/espresso
```

## Animations
```css
.animate-fade-in     /* Page entrance fade + slide up */
.animate-stamp       /* Check mark stamp pop */
.bingo-square        /* Auto staggered card-reveal (nth-child delays) */
/* Coffee cup: steam-rise, cup-appear */
/* Spill: cup-tilt, liquid-pour, drop-splash */
/* Modal: modal-pop */
```

## Best Practices
1. Use `.cozy-heading` for any heading text (activates Gaegu font)
2. Use `.btn-cozy` for primary actions, `.btn-back` for navigation
3. Use `.bg-cork` to wrap the bingo board for texture
4. Use `.bingo-square` with `.marked` / `.winning` / `.free-space` modifiers
5. Use CSS variables (`var(--espresso)`, etc.) for any new colors
6. Add new utilities to `app.css` following existing patterns

## Example
```html
<div class="flex flex-col items-center justify-center min-h-full bg-gray-50">
    <h1 class="text-4xl font-bold cozy-heading">Soc Ops</h1>
    <button class="btn-cozy py-4 px-8 text-lg cozy-heading">
        Start Game
    </button>
</div>
```