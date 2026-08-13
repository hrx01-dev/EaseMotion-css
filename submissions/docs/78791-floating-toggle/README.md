# Floating Toggle Usage

## Issue

EaseMotion CSS issue #78791.

## Overview

This guide documents a floating toggle pattern for compact settings and preference controls.

## Basic structure

Use a native checkbox so keyboard, touch, and assistive technology behavior remain familiar:

```html
<label class="floating-toggle">
  <input type="checkbox">
  <span aria-hidden="true"></span>
  <span>Notifications</span>
</label>
```

The visible text should describe the setting being changed.

## Positioning

Place the toggle inside a positioned container or use `position: fixed` only when it should remain attached to the viewport. Provide sufficient spacing from edges and other controls.

## Accessibility

Do not hide the checkbox in a way that removes keyboard access. The checked state should have a clear visual difference and the label should remain associated with the input.

## Responsive behavior

On narrow screens, reduce decorative padding while preserving the control's touch target. Avoid placing the floating control over important content.

## Reduced motion

If the toggle uses a sliding transition, disable the transition with `prefers-reduced-motion: reduce`.
