# User Guide: Footer Links

## Overview

The footer section sits at the bottom of every page and provides quick access to key areas of the Cursor site. It’s organized into five columns—Product, Resources, Company, Legal, and Connect—grouping related links together. This structure helps users find what they need with minimal effort, whether they’re exploring product features, seeking documentation, or connecting via social channels.

## HTML Structure

The markup for the footer is defined in `index.html` within a `<footer class="footer">` block. Inside, a `.container` holds a `.footer-grid`, which in turn contains multiple `.footer-col` elements—one per link group:

```html
<footer class="footer">
  <div class="container">
    <div class="footer-grid">
      <!-- .footer-col elements go here -->
    </div>
  </div>
</footer>
```

Each `.footer-col` has a heading (`<h4>`) and a list of `<a>` tags  .

## Link Groups

### Product

```html
<div class="footer-col">
  <h4>Product</h4>
  <a href="#">Agents</a>
  <a href="#">Enterprise</a>
  <a href="#">Code Review</a>
  <a href="#">Tab</a>
  <a href="#">CLI</a>
  <a href="#">Cloud Agents</a>
  <a href="#">Pricing</a>
</div>
```

These links point to core product pages. To wire up:

- Replace `href="#"` with your site’s routes:
- `/agents`
- `/enterprise`
- `/code-review`
- `/tab`
- `/cli`
- `/cloud-agents`
- `/pricing`

Ensure your router or server serves those paths appropriately .

### Resources

```html
<div class="footer-col">
  <h4>Resources</h4>
  <a href="#">Download</a>
  <a href="#">Changelog</a>
  <a href="#">Docs</a>
  <a href="#">Forum</a>
  <a href="#">Status</a>
  <a href="#">Future</a>
  <a href="#">Marketplace</a>
</div>
```

This section links to support and community resources. Update each link to:

- `/download`
- `/changelog`
- `/docs`
- `/forum`
- `/status`
- `/future`
- `/marketplace`

Confirm these pages exist or redirect as needed .

### Company

```html
<div class="footer-col">
  <h4>Company</h4>
  <a href="#">Careers</a>
  <a href="#">Blog</a>
  <a href="#">Community</a>
  <a href="#">Students</a>
  <a href="#">Brand</a>
  <a href="#">Anysphere</a>
</div>
```

Use this group for corporate and community links. Example paths:

- `/careers`
- `/blog`
- `/community`
- `/students`
- `/brand`
- `/anysphere`

Or point to external microsites as appropriate .

### Legal

```html
<div class="footer-col">
  <h4>Legal</h4>
  <a href="#">Terms of Service</a>
  <a href="#">Privacy Policy</a>
  <a href="#">Data Use</a>
  <a href="#">Security</a>
</div>
```

Legal documents typically live at absolute URLs. Common patterns:

- `https://yourdomain.com/terms`
- `https://yourdomain.com/privacy`
- `https://yourdomain.com/data-use`
- `https://yourdomain.com/security`

Make sure these pages are published before linking .

### Connect

```html
<div class="footer-col">
  <h4>Connect</h4>
  <a href="#">X</a>
  <a href="#">LinkedIn</a>
  <a href="#">YouTube</a>
</div>
```

Social links direct to external platforms. Best practices:

- Use full URLs:
- `https://twitter.com/yourhandle`
- `https://linkedin.com/company/yourcompany`
- `https://youtube.com/yourchannel`
- Open in a new tab:

```html
  <a href="https://twitter.com/yourhandle" target="_blank" rel="noopener noreferrer">X</a>
```

Ensure you include `target="_blank"` and `rel="noopener noreferrer"` for security .

## Wiring Links to Real URLs

1. Find each `<a href="#">…</a>` in the footer columns.
2. Replace `#` with the actual path or absolute URL.
3. Verify that clicking the link navigates correctly:
4. Internal routes (same domain) use relative paths.
5. External destinations use full URLs plus `target` and `rel` attributes.
6. Test keyboard navigation and ensure focus states are styled.

## Interaction States

- **Hover**: By default, links should change color or underline on hover—controlled via `style.css`.
- **Focus**: Include a visible outline (e.g., `outline: 2px solid #005fcc;`) to support keyboard users.
- **Active**: Optionally, add a pressed state (darker color or inset shadow) for feedback.

With these guidelines, your footer will be fully functional, accessible, and aligned with the design of the Cursor landing page.