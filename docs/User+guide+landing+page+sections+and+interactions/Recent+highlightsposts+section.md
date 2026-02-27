# User Guide: Recent Highlights Section

## Overview

The Recent Highlights section surfaces the latest posts and announcements on your landing page, helping visitors quickly discover new content. It presents a heading, a series of highlight cards—each with a title, description, and date—and a “View more posts →” link that takes users to the full blog or news archive.

## HTML Structure

All markup for this feature lives in **index.html** inside the `<section class="highlight">` block. The high-level structure is as follows:

```html
<section class="highlight">
  <div class="grid-cards">
    <!-- Section heading -->
    <div>
      <h3 id="inner-text-grid">Recent highlights</h3>
    </div>

    <!-- Cards container -->
    <div id="inner-bg-col">
      <!-- Highlight item -->
      <div id="inner-text-grid-content">
        <h3>
          Towards self-driving codebases<br />
          <span>We’re making a part of our multi-agent research harness available to try today in preview.</span>
        </h3>
        <p>Feb 5, 2026</p>
      </div>

      <!-- Additional items... -->
      <div id="inner-text-grid-content">…</div>
      <div id="inner-text-grid-content">…</div>

      <!-- View more posts link -->
      <a href="#"><p>View more posts →</p></a>
    </div>
  </div>
</section>
```

This markup comes directly from your clone of *index.html* .

### Key Elements

- `<section class="highlight">`

The outer wrapper for the Recent Highlights feature.

- `<div class="grid-cards">`

Defines a CSS grid layout to align the heading and the cards.

- `<h3 id="inner-text-grid">`

The section title (“Recent highlights”).

- `<div id="inner-bg-col">`

Background container holding all highlight cards and the “View more” link.

- `<div id="inner-text-grid-content">`

Each card, containing:

- A `<h3>` with the post title and a `<span>` for the description.
- A `<p>` element for the publication date.
- `<a href="#"><p>View more posts →</p></a>`

Navigates to the full posts archive. Update the `href` to point at your actual blog or news page.

## CSS Classes & IDs

All styling lives in **style.css**, linked in **index.html** with:

```html
<link rel="stylesheet" href="style.css" />
```

While the exact CSS rules may vary, these selectors control the Recent Highlights layout and appearance:

- `.highlight`

Section-level padding, background color, and typography.

- `.grid-cards`

A grid container, typically defining columns (e.g., `display: grid; grid-template-columns: 1fr 3fr; gap: …;`).

- `#inner-text-grid`

Styles the “Recent highlights” heading (font-size, weight, margins).

- `#inner-bg-col`

Styling for the card background block (e.g., background-color, border-radius, padding).

- `#inner-text-grid-content`

Individual card styling (background, hover effects, inner spacing, shadow).

- `a > p` within `.highlight`

Link styling for the “View more posts” call-to-action.

## Editing & Adding Entries

To update or extend the highlight list:

1. Open **index.html** and locate:

```html
   <section class="highlight"> … </section>
```

1. Within `<div id="inner-bg-col">`, find the existing card blocks:

```html
   <div id="inner-text-grid-content">…</div>
```

1. **Duplicate** one `<div id="inner-text-grid-content">…</div>` block for each new post.
2. **Update** inside each new block:
3. The `<h3>` text for the **title**.
4. The `<span>` text for the **description**.
5. The `<p>` content for the **date**.
6. **Adjust** the order of the cards by cutting and pasting blocks—newest first is typical.
7. If needed, **modify** the `<a href="#">` URL on the “View more posts →” link to point at your blog index.

### Example: Adding a Fourth Highlight

```html
<div id="inner-text-grid-content">
  <h3>
    Introducing multi-agent orchestration<br />
    <span>Coordinate multiple AI agents seamlessly in your workflow.</span>
  </h3>
  <p>Mar 15, 2026</p>
</div>
```

## Interaction & Behavior

- This section is **static HTML/CSS only**, with no JavaScript dependencies.
- The “View more posts →” link should navigate users to your full posts page. Ensure the `href` attribute is set correctly.
- Cards do not animate by default; any hover or focus styles must be defined in **style.css** under `#inner-text-grid-content:hover` or similar selectors.

With this guide, you can confidently maintain and expand the Recent Highlights section, keeping your landing page content fresh and engaging.