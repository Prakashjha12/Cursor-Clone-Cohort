# Testimonials Section (Static Cards)

## Overview

The **Testimonials** section presents social proof by displaying static testimonial cards in a responsive grid. It lives in `index.html` under the `<section class="testomonials">` wrapper and is styled via **style.css**. No JavaScript carousel or slider logic is included—cards are laid out purely with HTML and CSS.

## Markup Structure

Each testimonial card follows the same HTML pattern. Here’s the core structure from `index.html`:

```html
<section class="testomonials">
  <h2>The new way to build software.</h2>
  <div class="all-cards">
    <div class="testo-cards">
      <!-- Single testimonial card -->
      <div class="testo">
        <p>
          “It was night and day from one batch to another, adoption went
          from single digits to over 80%. It just spread like wildfire,
          all the best builders were using Cursor.”
        </p>
        <div id="testo-img">
          <img src="./assest/testo-dummy.jpg" alt="Diana Hu" />
          <p>
            Diana Hu <br />
            <span>General Partner, Y Combinator</span>
          </p>
        </div>
      </div>
      <!-- Repeat .testo for each additional card -->
    </div>
  </div>
</section>
```

This markup snippet   shows:

- A section heading wrapped in `<h2>`.
- An outer container `.all-cards`.
- A grid/flex container `.testo-cards`.
- Individual `.testo` cards, each containing:
- A `<p>` block for the quote.
- A `#testo-img` block for avatar and author details.

## CSS Classes & IDs

- `.testomonials`: Section wrapper.
- `.all-cards`: Outer padding/background container.
- `.testo-cards`: Flex/grid container for cards.
- `.testo`: Single testimonial card.
- `#testo-img`: Avatar + author info container.
- Element tags:
- `<p>` for quote text and author name.
- `<span>` for author title.
- `<img>` for avatar.

All styles are defined in **style.css**, so maintain these exact class and ID names when editing.

## Assets

- Avatar placeholder: `./assest/testo-dummy.jpg`.
- All image assets (SVGs, PNGs, JPGs) reside in the `./assest/` folder (note the spelling).
- To use a custom avatar, replace the `src` attribute:

```html
  <img src="./assest/your-avatar.jpg" alt="Author Name" />
```

## Current Testimonials

The static cards in the markup feature endorsements from:

- Diana Hu — General Partner, Y Combinator
- Jensen Huang — President & CEO, NVIDIA
- Andrej Karpathy — CEO, Eureka Labs
- Patrick Collison — Co-Founder & CEO, Stripe
- shadcn — Creator of shadcn/ui
- Greg Brockman — President, OpenAI

## Adding or Removing Testimonial Cards

**To add a new card**:

1. Copy an existing `<div class="testo">…</div>` block.
2. Paste it inside the `<div class="testo-cards">` container.
3. Update:
4. The quote text inside the first `<p>`.
5. The `<img src="…">` path and its `alt`.
6. The author name and title in the second `<p>` and `<span>`.

Example:

```html
<div class="testo">
  <p>“Your new testimonial quote goes here.”</p>
  <div id="testo-img">
    <img src="./assest/new-avatar.jpg" alt="Author Name" />
    <p>
      Author Name <br />
      <span>Author Title</span>
    </p>
  </div>
</div>
```

**To remove a card**, simply delete its `<div class="testo">…</div>` block.

## Editing Section Heading

> Keep class names and the `#testo-img` ID consistent to ensure styling remains intact.

The main heading is in:

```html
<section class="testomonials">
  <h2>The new way to build software.</h2>
  …
</section>
```

Modify the `<h2>` text directly to change the section title.

## Responsive Behavior

The `.testo-cards` container uses CSS rules in **style.css** (e.g., `display: flex; flex-wrap: wrap; justify-content: center;`) to ensure cards wrap on narrower viewports. No changes are needed to maintain responsiveness—just preserve the markup structure.

## Accessibility Considerations

- **Alt Text**: Each `<img>` tag includes an `alt` attribute. Update it to the author’s name for screen readers.
- **Semantic Tags**: Quotes use `<p>` tags; author titles use `<span>`.

By following this guide, you can confidently maintain, extend, and localize the Testimonials section on the Cursor landing page clone.