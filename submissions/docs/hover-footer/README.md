# Hover Footer

A documentation example for a footer that reveals secondary actions and visual emphasis when the pointer or keyboard focus reaches the footer region.

## What this example demonstrates

- A footer layout that stays usable at different viewport widths.
- Hover and focus-visible transitions for links.
- Clear grouping for navigation and supporting information.
- Responsive spacing without JavaScript.
- Reduced-motion handling for accessibility.

## Usage

Use the semantic `<footer>` element and keep navigation links inside a labeled `<nav>`. The included `style.css` provides the presentation and interaction states shown in the demo.

## Customization

Change the link spacing, reveal distance, border treatment, and transition timing in `style.css`. The footer can be placed directly below the page content or adapted into a sticky layout.

## Accessibility

Keyboard users receive the same visual emphasis as pointer users through `:focus-visible`. Link text remains readable without relying on hover alone.

## Files

- `demo.html` — complete footer usage example.
- `style.css` — responsive footer styling and interactions.
- `README.md` — usage and customization documentation.
