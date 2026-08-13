# 3D Sidebar with Gradient Styling

## Overview

Issue #78585 demonstrates a responsive navigation sidebar using perspective depth, layered gradients, and restrained motion.

## Features

- 3D perspective treatment
- Gradient surface layers
- Responsive navigation
- Visible keyboard focus
- Reduced-motion support
- Pure HTML and vanilla CSS

## Implementation

The sidebar uses a small Y-axis transform and layered shadows to establish depth without affecting document flow. At smaller widths the perspective treatment is removed and the navigation becomes a normal stacked panel.

## Accessibility

Navigation remains semantic, links are keyboard reachable, and focus states are visible. Decorative transforms are disabled for users who prefer reduced motion.

## Files

- `demo.html` — complete responsive example
- `style.css` — layout, depth, gradients, responsive rules, and motion handling
- `README.md` — implementation notes

## Issue

EaseMotion CSS issue #78585.
