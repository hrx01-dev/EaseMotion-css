# Parallax SaaS Footer

Issue #79687 demonstrates a responsive SaaS-style footer with layered depth and a lightweight parallax-inspired visual treatment.

## Overview

The footer is designed for SaaS landing pages, product sites, portfolios, and dashboards. CSS creates the visual depth while semantic HTML keeps the navigation simple and reusable.

## Features

- Responsive footer columns
- Layered visual depth
- Parallax-inspired decoration
- Clear navigation hierarchy
- Keyboard-visible links
- Small-screen stacking
- Touch-friendly spacing
- Native HTML links
- Pure HTML and vanilla CSS
- No external dependencies
- Reduced-motion friendly styling

## Structure

- `demo.html` — complete footer markup and demonstration content
- `style.css` — layout, depth effects, spacing, responsive rules, and states
- `README.md` — implementation and customization documentation

## Usage

Open `demo.html` in a modern browser to preview the component. Copy the footer markup into the required page and link `style.css`. Replace the product name, navigation destinations, labels, and supporting content with project-specific information.

## Responsive Behavior

Footer columns remain distributed on wider screens and collapse into a readable stack on smaller screens. The layout avoids fixed widths that could cause horizontal scrolling.

## Accessibility

Navigation uses native links and visible keyboard focus. Headings provide a clear information hierarchy, while decorative depth is not required to understand the content.

## Styling

The depth effect uses CSS layers, shadows, gradients, and spacing. Colors, typography, border radius, shadow strength, and breakpoints can be customized directly in `style.css`.

## Performance

No JavaScript animation loop or external library is required. The component relies on standard CSS rendering and can be opened directly without a build step.

## Browser Support

The example uses standard HTML and modern CSS features supported by current evergreen browsers.

## Issue

EaseMotion CSS issue #79687.
