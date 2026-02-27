# Styling and Layout (CSS)

## Global Stylesheet Inclusion

All CSS for the Cursor-Clone landing page is defined in a single global stylesheet named **style.css**, which is linked once in the `<head>` of **index.html**. Any visual or layout change across the entire site should be made within this file:

```html
<head>
  …
  <link rel="stylesheet" href="style.css" />
</head>
```

## Centralized Styling in style.css

- **Location**

The file `style.css` sits at the project root alongside `index.html`.

- **Structure**

While the exact content may vary, a typical organization inside **style.css** is:

1. **CSS Reset / Normalize** – overrides browser defaults.
2. **Root Variables & Base Typography** – custom properties, font-family, line-height.
3. **Layout Utility Rules** – flex/grid helpers, spacing utilities.
4. **Component Sections** – grouped by page areas (e.g., Header, Hero, Features, Testimonials, Footer).
5. **Media Queries** – breakpoint-specific overrides at the bottom.

By keeping every selector and declaration centralized here, you ensure consistent styling and simplify future maintenance.

## Locating and Modifying CSS Rules

To update spacing, colors, typography, or layout for any part of the page, open **style.css** in your editor and search for the corresponding class or ID from **index.html**. Below is a mapping of major HTML selectors to their page sections:

- **Header & Navigation**

Selectors:

• `.container` (wrapper for page content)

• `header`

• `nav#logo` (logo area)

• `nav#menu-item` (main menu links)

• `.nav-btn` (Sign in / Download buttons)

• `#sign-in`, `#download` (button specifics)

- **Hero Section**

Selectors:

• `.hero` (hero background and centering)

• `#hero-text` (main headline)

• `#cta-btn` (call-to-action button)

• `.down-arrow` (icon inside CTA)

- **Hero Image**

Selectors:

• `.hero-sec` (wrapper for image)

• `#hero-img` (hero graphic)

- **Trusted-By Logo Grid**

Selectors:

• `.trusted-by` (section container)

• `.logo-grid` (grid layout for logos)

• `.logo-card` (individual logo cell)

- **Feature Cards**

Selectors (repeatable variations):

• `.Feature-sections`, `.Feature-sections-2`, `.Feature-sections-3`, `.Feature-sections-4`

• `.card-layout` (flex/grid wrapper)

• `.card-one` (text block)

• `.card-img-one` (image block)

- **Testimonials**

Selectors:

• `.testomonials` (section heading + card container)

• `.testo-cards`, `.testo` (individual testimonial card)

• `#testo-img` (avatar + citation block)

- **Use Cases**

Selectors:

• `.usecases` (grid section)

• `#grid-card-layout`, `#cardwith-img` (grid items)

- **Changelog**

Selectors:

• `.Changelog` (title + list wrapper)

• `#Changelog-card`, `#cards-log`, `#btn-cards` (entry cards + link)

- **Join-Now & Highlights**

Selectors:

• `.join-now` (team intro card)

• `.highlight` (recent highlights grid)

• `.grid-cards`, `#inner-text-grid`, `#inner-bg-col`, `#inner-text-grid-content`

- **Final Call-to-Action**

Selectors:

• `.final-CTA` (last download prompt)

- **Footer**

Selectors:

• `.footer`

• `.footer-grid` (multi-column layout)

• `.footer-col` (each column of links)

## Tips for Centralized Changes

- **Search by Selector**

Use your editor’s “Find in File” to jump directly to declarations—e.g. search for `.hero`, `#cta-btn`, or `.footer-col`.

- **Group with Comments**

Organize **style.css** with comment headers like `/* Hero Section */` to visually separate each page area.

- **Maintain Naming Consistency**

Keep class and ID names in sync with the markup in **index.html**. If you rename a section class in HTML, update the corresponding rule in **style.css** immediately.

- **Leverage Variables (Optional)**

If you introduce CSS custom properties (e.g., `--primary-color`), define them at the top of **style.css** under `:root` to ensure global theming.

By following these guidelines, all styling concerns remain consolidated in a single file, making global theming, responsive tweaks, and visual maintenance straightforward.