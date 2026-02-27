# Hero Section (Headline + Download CTA) – User Guide

## Overview

The Hero section sits at the very top of the landing page, immediately conveying Cursor’s key value proposition and guiding visitors toward the primary action: downloading the app. It consists of a bold headline, a prominent “Download for macOS” button with a downward arrow, and a supporting product image.

---

## HTML Structure

The markup for the Hero section is contained in `index.html` under two main elements:

```html
<section class="hero">
  <h1 id="hero-text">
    Built to make you extraordinarily productive,<br />
    Cursor is the best way to code with AI.
  </h1>
  <button id="cta-btn">
    Download for macOS <span class="down-arrow">↓</span>
  </button>
</section>

<div class="hero-sec">
  <img id="hero-img" src="./assest/hero-img.png" alt="Cursor app interface" />
</div>
```

- `<section class="hero">`

Wraps the headline and primary call-to-action (CTA) button.

- `<h1 id="hero-text">`

Contains the hero headline text, including an HTML line break (`<br />`).

- `<button id="cta-btn">`

Renders the main “Download for macOS” button and arrow.

- `<div class="hero-sec">`

Holds the hero image in an `<img>` element.

- Assets are stored (note the folder name) in `./assest/`.

---

## Editing the Hero Headline

The headline lives in the `<h1>` with `id="hero-text"`. To change it:

1. Open **index.html**.
2. Locate the element:

```html
   <h1 id="hero-text">
     Built to make you extraordinarily productive,<br />
     Cursor is the best way to code with AI.
   </h1>
```

1. Replace the text inside `<h1>` (preserving or adjusting `<br />` as needed).

Example – updating to a Windows download variant:

```html
   <h1 id="hero-text">
     Unleash your productivity on Windows,<br />
     Cursor brings AI right to your IDE.
   </h1>
```

---

## Editing the Download CTA Button

The download button is defined by `<button id="cta-btn">`. You can change both its label and arrow symbol:

```html
<button id="cta-btn">
  Download for macOS <span class="down-arrow">↓</span>
</button>
```

- **Button label**: Modify the text before the `<span>`.
- **Arrow icon**: The downward arrow is a plain text character (`↓`). To use a different arrow or icon, replace the content of `<span class="down-arrow">`.
- **Platform update**: To target Windows, for instance:

```html
  <button id="cta-btn">
    Download for Windows <span class="down-arrow">↓</span>
  </button>
```

---

## Hero Image Configuration

The product image appears in the following block:

```html
<div class="hero-sec">
  <img id="hero-img" src="./assest/hero-img.png" alt="Cursor app interface" />
</div>
```

- **Image source** (`src`): Points to `./assest/hero-img.png`.
- **Alt text** (`alt`): Important for accessibility; update it to describe your new image.
- **To replace the image**:
- Place your new image file in the `./assest/` directory.
- Update the `src` attribute to match the new filename, e.g. `src="./assest/hero-windows.png"`.
- Adjust the `alt` text accordingly:

```html
     <img id="hero-img"
          src="./assest/hero-windows.png"
          alt="Cursor running on Windows terminal" />
```

---

## Styling and Interactions

All styling for the Hero section lives in **style.css**. Key selectors you may customize:

- `.hero`
- `#hero-text`
- `#cta-btn` and `.down-arrow`
- `.hero-sec` and `#hero-img`

Common adjustments include font sizes, colors, spacing, and hover effects on the CTA button. Since there is no JavaScript tied to the Hero section, interactions such as hover states are purely CSS-driven. Simply locate the matching selectors in **style.css** and tweak properties like `background-color`, `color`, `box-shadow`, or `transform` to refine the look and feel.