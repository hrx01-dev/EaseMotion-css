# Hover Footer

Usage documentation for the Hover Footer component from issue #78626. The example shows how to structure a footer that reveals supporting navigation and actions on hover or keyboard focus.

## Usage

Use a semantic `<footer>` with grouped links. The hidden content should remain available to keyboard users through `:focus-within`, while the layout adapts to narrow screens.

## Files

- `demo.html` — complete component example.
- `style.css` — responsive, properly spaced styles.

## Accessibility

Use visible focus states, descriptive link text, and `:focus-within` so the interaction is not limited to pointer users.

## Customization

Adjust spacing, reveal distance, typography, and transition timing in `style.css`.
