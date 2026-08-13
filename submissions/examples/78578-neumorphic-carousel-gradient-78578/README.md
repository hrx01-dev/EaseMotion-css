# Neumorphic Gradient Carousel

## Overview

Issue **#78578** demonstrates a responsive carousel built around soft neumorphic depth, restrained gradients, and clear content hierarchy.

The example is intentionally self-contained so the visual treatment can be studied and reused without a framework or external component library.

## Design approach

The component combines raised surfaces, inset-style depth, rounded geometry, and a restrained accent color. The cards remain visually distinct while sharing the same spacing system and surface treatment.

## Features

- Responsive three-card carousel presentation
- Neumorphic raised and inset visual depth
- Subtle gradient card surfaces
- Native keyboard-focusable controls
- Clear active-slide indicators
- Responsive single-column layout on smaller screens
- Reduced-motion support
- Semantic HTML structure
- Pure HTML and vanilla CSS
- No external JavaScript dependency

## Accessibility

The controls use native buttons and visible `:focus-visible` outlines. Links remain keyboard reachable, and the design does not depend on hover to communicate essential information.

The `prefers-reduced-motion` media query removes decorative movement for users who request reduced motion.

## Responsive behavior

On wider screens, the component displays three cards in a grid. At smaller widths, the cards stack vertically and the controls move above the content so the layout remains comfortable on touch devices.

## Usage

Open `demo.html` in a modern browser. The example is self-contained and can be reused as a visual reference for dashboards, product collections, feature galleries, or other card-based interfaces.

## Files

- `demo.html` — semantic carousel demonstration and supporting content
- `style.css` — spaced, responsive neumorphic visual system
- `README.md` — implementation and accessibility notes

## Implementation notes

The visual depth is created with CSS shadows and gradients rather than image assets. This keeps the component lightweight and makes the spacing, surface colors, and motion behavior easy to customize.
