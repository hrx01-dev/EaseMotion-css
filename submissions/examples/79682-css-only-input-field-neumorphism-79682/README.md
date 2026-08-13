# CSS-only Input Field — Neumorphism

## Overview

Issue #79682 demonstrates a soft neumorphic input field using only HTML and CSS.

## Features

- Neumorphic inset field depth
- Native text and email inputs
- Visible focus treatment
- Pressed button state
- Responsive layout
- Reduced-motion support
- No JavaScript dependency

## Implementation

The fields use paired inset shadows to create the pressed neumorphic surface. The submit button uses the same surface language with an elevated resting state and a pressed interaction.

## Accessibility

Every input has a visible label and native input semantics. Keyboard focus is represented with an additional outline so the visual style does not hide the interaction state.

## Usage

Open `demo.html` directly and reuse the labelled form controls in an existing page. The CSS variables at the top of `style.css` can be adjusted to match another surface color.

## Files

- `demo.html` — self-contained form example
- `style.css` — neumorphic surface, controls, responsive rules, and motion handling
- `README.md` — implementation notes

## Issue

EaseMotion CSS issue #79682.
