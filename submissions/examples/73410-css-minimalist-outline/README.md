# CSS Minimalist Outline Text

## Overview

Issue #73410 presents a minimal outlined text treatment using native CSS text stroke and transitions. The effect keeps the typography as ordinary HTML text so the visual treatment does not become a separate content layer.

## Features

- Lightweight outlined typography
- Smooth hover and focus transition
- Dark-mode compatible presentation
- Responsive sizing with `clamp()`
- Higher-contrast presentation support
- Reduced-motion support
- Text selection styling
- Pure HTML and vanilla CSS

## Implementation

The outline is created with `-webkit-text-stroke` while the fill remains transparent. Hover and keyboard focus progressively restore the text fill and add a restrained glow. The transition also includes a very small vertical lift to make the state change easier to perceive without moving the layout.

The stylesheet uses custom properties for the background, text, muted copy, outline, and focus colors. This keeps the visual system easy to tune without duplicating color values across selectors.

## Responsive Behavior

The heading uses a fluid `clamp()` size so the large display treatment scales between desktop and mobile widths. The page container also reduces its horizontal width and padding on smaller screens.

## Accessibility

The heading remains readable as normal document text even when animation is disabled. Keyboard focus receives a visible outline, and `prefers-contrast: more` increases the visual separation of the outline and supporting copy. Reduced-motion preferences remove the transition rather than hiding the content.

## Usage

Open `demo.html` in a modern browser and hover or focus the heading to reveal the filled state.

## Files

- `demo.html` — semantic example markup
- `style.css` — outline effect, responsive behavior, and accessibility states
- `README.md` — implementation documentation

## Issue

EaseMotion CSS issue #73410.
