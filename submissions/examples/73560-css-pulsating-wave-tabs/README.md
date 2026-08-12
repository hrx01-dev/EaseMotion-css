# CSS Pulsating Wave Tabs

## Overview

This example implements the EaseMotion #73560 Pulsating Wave tab variation using semantic HTML and vanilla CSS. The selected segment is highlighted by a softly breathing wave surface that slides between options.

## Features

- Pure HTML and vanilla CSS
- Native radio controls for persistent selection
- Animated active-state wave
- Dark-mode-friendly palette
- Responsive segmented control
- Visible keyboard focus styling
- Reduced-motion support
- No external dependencies

## Implementation

The tabs use radio inputs so one option is always selected. CSS sibling selectors move the decorative wave to the matching segment. Keyframe animation changes the intensity of the wave without relying on JavaScript.

## Accessibility

Each control has an associated label, and the underlying radio input remains part of the interaction model. Focus styling is preserved so keyboard users can identify the active control. Reduced-motion preferences disable decorative animation and transitions.

## Files

- `demo.html` — semantic tab structure and sample content
- `style.css` — layout, active-state positioning, animation, responsive rules, and accessibility styles
- `README.md` — implementation documentation

## Usage

Open `demo.html` directly in a modern browser. No build process or package installation is required.

## Issue

EaseMotion CSS issue #73560.
