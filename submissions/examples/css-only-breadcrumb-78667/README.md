# CSS-only Breadcrumb — Issue #78667

A lightweight breadcrumb navigation showcase built with semantic HTML and CSS only.

## Files

- `demo.html` — accessible breadcrumb markup and live example.
- `style.css` — responsive styling, states, spacing, and reduced-motion support.

## Usage

Include `style.css` and copy the breadcrumb `<nav>` into a page. Replace the placeholder links with the appropriate destinations.

## Accessibility

The component uses a labelled `<nav>`, `aria-current="page"` for the current location, and visible keyboard focus through `:focus-visible`.

## Responsive behavior

The breadcrumb wraps naturally on narrow screens while preserving readable spacing between items.
