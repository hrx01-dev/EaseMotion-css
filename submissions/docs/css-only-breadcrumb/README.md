# CSS-only Breadcrumb

A documentation example of a breadcrumb trail built with semantic navigation and CSS-generated separators. No JavaScript is required for the layout or visual states.

## What this example demonstrates

- Semantic `<nav>` and ordered breadcrumb items.
- CSS-generated separators instead of extra markup.
- Current-page indication with `aria-current`.
- Responsive wrapping for smaller screens.
- Keyboard-visible link states.

## Usage

Place the breadcrumb inside a `<nav aria-label="Breadcrumb">` and keep the current location marked with `aria-current="page"`. Include `style.css` for the visual treatment.

## Customization

Change separator glyphs, spacing, typography, border treatment, and colors in `style.css`. The component works with any number of breadcrumb levels.

## Accessibility

The navigation receives an accessible label, links remain real links, and the current page is explicitly identified. The CSS separator is decorative and hidden from assistive technology.

## Files

- `demo.html` — complete breadcrumb markup.
- `style.css` — responsive CSS-only presentation.
- `README.md` — usage and customization guide.
