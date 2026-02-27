# Changelog Cards

## Overview

The **Changelog** section on the landing page surfaces the most recent product updates and enhancements. It consists of a vertically stacked list of dated entries—each highlighting a headline change—and concludes with a prominent “See what’s new in Cursor →” link. This guide explains the HTML structure, how to update existing entries, and how to add new cards within the `#Changelog-card` container.

## HTML Structure

### Section Wrapper

The entire changelog lives inside:

```html
<section class="Changelog">
  <h2>Changelog</h2>
  <div id="Changelog-card">
    <!-- individual cards -->
  </div>
  <a id="btn-cards" href="">
    <p>See what's new in Cursor →</p>
  </a>
</section>
```

– The outer `<section>` has class `Changelog`.

– The `<h2>` labels the section.

– The `<div id="Changelog-card">` is the container for all entry cards.

– The `<a id="btn-cards">` link/button appears immediately after the cards list .

### Entry Card Markup

Each changelog entry is a `<div>` with `id="cards-log"`, containing:

- A `<p>` element for the date (optionally prefixed by a `<span>` for a version number).
- An `<h3>` element for the entry title.

Example of one card:

```html
<div id="cards-log">
  <p>Feb 26 , 2026</p>
  <h3>Bugbot Autofixs</h3>
</div>
```

Four of these cards are rendered by default in `index.html`:

```html
<div id="Changelog-card">
  <div id="cards-log">
    <p>Feb 26 , 2026</p>
    <h3>Bugbot Autofixs</h3>
  </div>
  <div id="cards-log">
    <p>Feb 24, 2026</p>
    <h3>Cloud Agents with Computer Use</h3>
  </div>
  <div id="cards-log">
    <p>Feb 18, 2026</p>
    <h3>CLI Improvements and Mermaid ASCII Diagrams</h3>
  </div>
  <div id="cards-log">
    <p><span>2.5</span>Feb 17, 2026</p>
    <h3>Plugins, Sandbox Access Controls, and Async Subagents</h3>
  </div>
</div>
```

## Updating Existing Entries

1. Open `index.html`.
2. Locate the `<div id="Changelog-card">` block.
3. For each `<div id="cards-log">` you wish to update:
4. Change the date inside `<p>…</p>`.
5. Change the title inside `<h3>…</h3>`.

Example:

```diff
<div id="cards-log">
- <p>Feb 18, 2026</p>
- <h3>CLI Improvements and Mermaid ASCII Diagrams</h3>
+ <p>Mar 3, 2026</p>
+ <h3>Enhanced Multi-Agent Logging</h3>
</div>
```

## Adding a New Changelog Card

To introduce a new entry:

1. Copy one of the existing `<div id="cards-log">…</div>` blocks.
2. Paste it immediately before the closing `</div>` of `#Changelog-card`.
3. Update its `<p>` and `<h3>` contents.

```html
<div id="Changelog-card">
  <!-- existing cards -->
  <div id="cards-log">
    <p>Mar 10, 2026</p>
    <h3>Real-Time Collaboration Agents</h3>
  </div>
</div>
```

## “See what’s new in Cursor →” Link/Button

The link at the bottom of the section uses:

```html
<a id="btn-cards" href="path/to/full-changelog.html">
  <p>See what's new in Cursor →</p>
</a>
```

- **`id="btn-cards"`** lets you target this element in CSS (or JavaScript if interactivity is added).
- Update the `href` attribute to point to your full changelog or release-notes page.

## Styling Notes

- CSS selectors in `style.css` target:
- `.Changelog` for section spacing and typography
- `#Changelog-card` for grid or flex layout of cards
- `#cards-log` to style each card (margin, border, background)
- `#btn-cards` to style the link/button (padding, hover state)

Review and adjust these rules in `style.css` to match your design.

## Accessibility Considerations

- Ensure the `<h2>` and `<h3>` hierarchy is preserved for screen readers.
- Use clear, consistent date formats.
- If you add version badges via `<span>`, include an `aria-label` on the `<p>` or the `<span>` to clarify its purpose (e.g., `<span aria-label="Version 2.5">2.5</span>`).

---

With this guide, you can keep your landing page’s changelog up-to-date, add new entries easily, and ensure consistent styling and accessibility.