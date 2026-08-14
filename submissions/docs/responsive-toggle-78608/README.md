# Responsive Toggle

Documentation for the Responsive Toggle component referenced by issue #78608.

## Overview

This example demonstrates a compact toggle control that remains usable across desktop and narrow layouts. The demo shows the component structure, accessible labeling, checked state, focus treatment, and responsive sizing.

## Usage

1. Add the toggle markup to your page.
2. Keep the visible label associated with the control.
3. Use the checked state to represent the active option.
4. Adjust the CSS custom properties in `style.css` to match your interface.

## Accessibility

The control uses a native checkbox so keyboard interaction and focus behavior are preserved. The visible text provides a clear label and the demo exposes the current state to assistive technology.

## Files

- `demo.html` — complete usage example.
- `style.css` — component styling with responsive spacing.

## Customization

Change the component dimensions, track color, thumb size, transition timing, and surrounding layout without changing the HTML structure.

## Reduced Motion

The component reduces transition effects when the user has enabled `prefers-reduced-motion`.
