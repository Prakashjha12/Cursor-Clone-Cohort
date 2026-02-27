# User Guide: Join-Us Section

## Overview

The Join-Us section is a dedicated call-to-action near the end of the landing page that highlights Cursor’s mission and invites users to explore career opportunities. Visually, it consists of a two-column “card” layout: on one side, a brief heading with a “Join us →” link; on the other side, a wide illustrative image. This section reinforces Cursor’s identity as an applied research team and provides a clear next step for interested visitors.

## Structure and Markup

### HTML Structure

The section is defined in `index.html` as follows:

```html
<section class="join-now">
  <div class="card-layout">
    <div class="card-one">
      <h3>
        Cursor is an applied research team focused on building the future
        of software development. <br />
      </h3>
      <a href=""><p>Join us →</p></a>
    </div>
    <div class="card-img-one">
      <img
        style="width: 1000px; object-fit: cover"
        src="./assest/join-now-img.png"
        alt=""
      />
    </div>
  </div>
</section>
```

The above markup shows:

- A `<section>` wrapper with class `join-now`.
- A `div.card-layout` container, typically styled as a two-column flex or grid layout.
- Left column (`div.card-one`) containing:
- An `<h3>` with the descriptive text.
- An `<a>` wrapping a `<p>` that displays the “Join us →” link text.
- Right column (`div.card-img-one`) containing the illustrative `<img>` asset.

## Styling

### CSS Classes & Selectors

- `.join-now`

• Section-level container.

- `.card-layout`

• Layout container that arranges child `.card-one` and `.card-img-one` side by side.

- `.card-one`

• Text content wrapper for heading and link.

- `.card-img-one`

• Image wrapper for the wide illustration.

### Image Asset

- File path: `./assest/join-now-img.png`
- Note that the project’s assets directory is spelled `assest` (not `assets`), so the path must match exactly.

### Inline Image Sizing

Currently, the `<img>` tag uses inline styles:

```html
<img
  style="width: 1000px; object-fit: cover"
  src="./assest/join-now-img.png"
  alt=""
/>
```

- `width: 1000px;` fixes the image width.
- `object-fit: cover;` ensures the image fills its box, cropping if necessary.

#### Moving Inline Styles into CSS

To improve maintainability, you can remove the `style` attribute and add the following rules to `style.css`:

```css
.join-now .card-img-one img {
  width: 1000px;
  object-fit: cover;
}
```

If you prefer a responsive approach (so the image scales with the viewport), you might use:

```css
.join-now .card-img-one img {
  width: 100%;
  height: auto;
  object-fit: cover;
}
```

## Interaction

### Join us Link

- Element: `<a href=""><p>Join us →</p></a>`
- Current behavior: Clicking navigates to the URL specified in `href`. As it stands, `href` is empty, so it reloads the current page.
- To activate this CTA, replace `href=""` with the desired careers or signup page URL.

### Accessibility & Semantics

- Consider removing the `<p>` inside the `<a>` and placing the link text directly in the anchor for cleaner semantics:

```html
  <a href="/careers" class="join-link">Join us →</a>
```

- Ensure `alt` text on the `<img>` conveys the image’s meaning if decorative; if purely decorative, consider `alt=""` as is.

---

*End of Join-Us Section documentation.*