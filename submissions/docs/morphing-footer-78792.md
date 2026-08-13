# Morphing Footer

## Overview

Issue #78792 documents the usage of the Morphing Footer component.

## Basic usage

Structure the footer as a semantic `<footer>` element with grouped navigation and a visual surface that can transition between its resting and expanded shapes.

```html
<footer class="morph-footer">
  <nav aria-label="Footer navigation">
    <a href="#about">About</a>
    <a href="#work">Work</a>
    <a href="#contact">Contact</a>
  </nav>
</footer>
```

## Motion

Use transform, border-radius, opacity, and other compositor-friendly properties for the morphing treatment. Keep the content position stable while the decorative surface changes shape.

## Accessibility

Use a semantic footer and native links. Keep focus-visible indicators distinct from the morphing background so keyboard users can track their position.

## Responsive behavior

Allow the navigation to wrap or stack at smaller widths rather than forcing the footer into a fixed desktop shape.

## Reduced motion

Provide a stable footer state when `prefers-reduced-motion: reduce` is enabled. The component should remain fully usable without animation.

## Issue

EaseMotion CSS issue #78792.
