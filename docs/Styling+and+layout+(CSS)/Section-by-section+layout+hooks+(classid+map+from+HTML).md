# Styling and Layout (CSS) – Section-By-Section Layout Hooks

## Overview

This section maps out the primary CSS selectors—classes and IDs—used across the HTML markup of the Cursor clone. Treat these as your “layout hooks”: targets for adjusting spacing, typography, alignment, grid behavior, and responsive breakpoints. By modifying rules on these selectors, you can fine-tune each section of the page without disturbing other areas.

---

## Selector Map by Section

### 1. Root Wrapper

Selector: `.container`

Type: Class

Role:

- Constrains content to a max-width and centers it on large viewports.
- Applies global horizontal padding.

### 2. Header Navigation

Selectors and IDs:

- `header` (element)
- `#logo`
- `#menu-item`
- `.nav-btn`
- `#sign-in`
- `#download`

Purpose:

- `header` establishes the top bar and often receives `display: flex; justify-content: space-between; align-items: center; padding`.
- `#logo` wraps the SVG logo image—use to size or add margin to the branding element.
- `#menu-item` contains the main links; target it to switch from horizontal `display: flex` to a vertical mobile menu, adjust `gap` between links, or change text styles on all `<h3>` children.
- `.nav-btn` holds the two action buttons; control button spacing and alignment here.
- `#sign-in` and `#download` are individual button hooks for typography, padding, border-radius, background-color, and hover states.

### 3. Hero Section

Selectors and IDs:

- `.hero`
- `#hero-text`
- `#cta-btn`
- `.down-arrow`

Layout Hooks:

- `.hero` typically sets vertical padding, text alignment (`text-align: center`), and background image/color overlays.
- `#hero-text` targets the main heading for font-size, line-height, and responsive adjustments (e.g., breakpoints to reduce font-size on narrow screens).
- `#cta-btn` is the primary call-to-action button—style its block-level width, padding, and interactive states.
- `.down-arrow` sits inside `#cta-btn`; adjust its margin (e.g., `margin-left: .5em`) or apply transforms (e.g., `transition` for a bounce effect).

### 4. Hero Image

Selectors and IDs:

- `.hero-sec`
- `#hero-img`

Details:

- `.hero-sec` is a wrapper `<div>` for the hero graphic. Use it to control overall height (e.g., `min-height`), centering via flex or grid, and responsive overflow.
- `#hero-img` sets the image’s max-width (e.g., `width: 100%; height: auto`) and may include breakpoint-specific sizing.

### 5. Trusted-By Logo Gallery

Selectors:

- `.trusted-by`
- `.logo-grid`
- `.logo-card`
- `#img1` (first logo)

Responsibilities:

- `.trusted-by` defines section padding and text alignment for the “Trusted every day…” line.
- `.logo-grid` is a grid container (e.g., `display: grid; grid-template-columns: repeat(auto-fit, minmax(120px, 1fr)); gap: 1.5rem;`). Adjust `gap` or column minima here.
- `.logo-card` wraps each logo image—use for uniform padding or background adjustments.
- `#img1` can be used to override styling for the first logo only (rarely needed).

### 6. Feature Card Sections

There are three similar sections:

- `.Feature-sections`
- `.Feature-sections-2`
- `.Feature-sections-3`

Each contains:

- `.card-layout`
- `.card-one`
- `.card-img-one`

Usage:

- `.Feature-sections*` (each variant) often sets alternating background colors or section padding.
- `.card-layout` arranges text and image side by side—commonly via `display: grid; grid-template-columns: 1fr 1fr; align-items: center; gap: 2rem;`. Tweak `grid-template-columns` or switch to `flex` as needed.
- `.card-one` holds the heading and link—target for text width, padding, and responsive line-break control.
- `.card-img-one` contains the accompanying image—use for max-width and object-fit adjustments.

### 7. Blog/News Grid

Selectors:

- Multiple `<div id="inner-text-grid-content">`

Notes:

- Although `inner-text-grid-content` is an ID, it’s repeated on each card. In CSS, consider overriding by using the parent container’s class (if present) plus a descendant selector.
- Targets for each news card: adjust border, padding, font-sizes for `<h3>` and `<p>`, and grid gaps on the parent wrapper.

### 8. Final Call-To-Action

Selector: `.final-CTA`

Scope:

- Wraps a bottom-of-page section with heading and button.
- Style with centered text, generous vertical padding, and a prominent background or border.
- Inside, target `.final-CTA h3` for heading styles and `.final-CTA button` for button overrides distinct from the hero CTA.

### 9. Footer

Selectors and Classes:

- `footer.footer`
- `.footer .container`
- `.footer-grid`
- `.footer-col`
- `.footer-col h4`
- `.footer-col a`

Structure:

- `footer.footer` applies global footer styling: background-color, text-color, padding-top/bottom.
- `.footer .container` reuses the main container constraints.
- `.footer-grid` is a grid or flex container distributing columns—adjust `grid-template-columns: repeat(auto-fit, minmax(120px, 1fr)); gap`.
- `.footer-col` is each column wrapper; use to set link spacing (`margin-bottom`) and vertical rhythm.
- Heading hooks (`.footer-col h4`) and link hooks (`.footer-col a`) let you change typography and hover effects in isolation.

---

## Quick Reference: Core Selectors

Selector                 | Type   | Role

-------------------------|--------|------------------------------------------------

`.container`             | Class  | Page max-width and centering wrapper

`header`                 | Element| Top bar flex container

`#logo`                  | ID     | Logo image wrapper

`#menu-item`             | ID     | Main nav links container

`.nav-btn`                | Class  | Sign-in/Download buttons wrapper

`#sign-in`, `#download`   | IDs    | Individual button styling hooks

`.hero`, `#hero-text`     | Class/ID | Hero text section and heading typography

`#cta-btn`, `.down-arrow` | ID/Class | Hero CTA button and icon spacing

`.hero-sec`, `#hero-img`  | Class/ID | Hero image wrapper and sizing

`.trusted-by`             | Class  | Logos section padding and text alignment

`.logo-grid`              | Class  | Logo gallery grid container

`.logo-card`              | Class  | Individual logo wrapper

`.Feature-sections*`      | Classes | Alternating feature sections

`.card-layout`            | Class  | Feature text/image grid

`.card-one`               | Class  | Feature text block

`.card-img-one`           | Class  | Feature image block

`#inner-text-grid-content`| ID     | Blog/news card (repeated)

`.final-CTA`              | Class  | Bottom CTA section

`footer.footer`           | Class  | Footer background and padding

`.footer-grid`            | Class  | Footer columns grid

`.footer-col`             | Class  | Footer column wrapper

`.footer-col h4`, `a`     | Element| Footer headings and links styling

Use this map as the starting point for any layout or style adjustments. By targeting these selectors directly, you’ll ensure consistent, section-scoped updates without unintended side effects elsewhere on the page.