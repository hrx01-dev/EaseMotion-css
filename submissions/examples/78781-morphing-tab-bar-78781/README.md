# Morphing Tab Bar

## Overview

Issue #78781 demonstrates a minimalist responsive tab bar with a distinct active surface and restrained motion.

## Features

- Minimalist tab styling
- Responsive wrapping
- Native anchor navigation
- Visible keyboard focus
- Reduced-motion support
- Pure HTML and vanilla CSS

## Implementation

The active tab is represented with a contrasting rounded surface while inactive tabs remain lightweight. Transforms are limited to small hover changes so the navigation does not cause layout shifts.

## Accessibility

Navigation uses semantic links and an `aria-current` marker for the active destination. Focus-visible outlines remain independent from the visual active state.

## Usage

Open `demo.html` in a modern browser and reuse the `.tabs` and `.tab` classes for a compact navigation control.

## Files

- `demo.html` — expanded component demonstration
- `style.css` — responsive layout and tab styling
- `README.md` — implementation documentation

## Issue

EaseMotion CSS issue #78781.
