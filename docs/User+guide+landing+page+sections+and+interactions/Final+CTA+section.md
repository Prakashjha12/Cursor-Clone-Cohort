## Final CTA Section

### Overview

The Final CTA section serves as the closing call-to-action on the landing page, prompting users to begin their Cursor experience. Positioned immediately before the footer, it reiterates the primary download action introduced in the hero and maintains consistency in messaging and styling as users reach the end of the page.

### Section Structure

```html
<section class="final-CTA">
  <h3>Try Cursor now</h3>
  <button>Download for macOS</button>
</section>
```

- **`<section class="final-CTA">`**

Acts as a full-width wrapper for this final prompt.

- **`<h3>`**

Presents the concise, imperative invitation: “Try Cursor now.”

- **`<button>`**

Triggers the primary action, labeled “Download for macOS.”

### Styling & Layout

- The `.final-CTA` container is horizontally centered and separated from surrounding content by consistent vertical padding.
- Text within the section is center-aligned to draw focus.
- The button inherits the same base styles as the hero’s download button (font size, padding, border radius), ensuring a unified look and feel.

### Interaction

- **Click Behavior**

The `<button>` is a native HTML button element, making it focusable and activatable via mouse, touch, and keyboard. In a fully wired implementation, its click event should initiate the macOS download flow (same URL or installer asset used in the hero CTA).

- **Visual States**

Hover, focus, and active states match those defined for the hero download button—e.g., background-color transition, outline or shadow on focus—to reinforce consistency.

### Copy Consistency

- **Heading vs. Hero**

The hero section introduces Cursor’s value proposition with an H1 and its own download button. The final CTA’s H3 “Try Cursor now” echoes that invitation, guiding users toward the same goal.

- **Button Label**

Using **exactly** “Download for macOS” in both hero and final CTA ensures users recognize the action and avoid confusion. Any variation in phrasing or casing could dilute the call-to-action’s impact.

### Accessibility

- The use of a semantic `<button>` guarantees built-in keyboard support and correct role announcement by screen readers.
- Heading hierarchy is maintained: H1 in hero → H3 here.
- Ensure focus outlines are visible and color contrast between text/button and background meets WCAG AA standards.

### Responsive Behavior

- On narrow viewports, the heading and button stack vertically with consistent spacing, preserving tappable target size.
- Padding adapts to maintain breathing room without excessive scroll.

### Testing Considerations

- Verify the `.final-CTA` section appears immediately above the footer on all breakpoints.
- Confirm the heading text exactly reads “Try Cursor now” and the button text “Download for macOS.”
- Test keyboard navigation: tab focus lands on the button and Enter/Space triggers the click event.
- Hover and focus styles should mirror those in the hero’s download button.