# Neumorphic Progress Bar Usage

## Issue

EaseMotion CSS issue #78789.

## Overview

This guide documents how to use a neumorphic progress bar while keeping the value readable and the component responsive.

## Basic structure

Use a semantic progress element when the browser semantics match the product requirement:

```html
<progress class="neo-progress" value="68" max="100">68%</progress>
```

The fallback text between the opening and closing tags provides a useful textual value.

## Styling approach

The visual treatment can combine a soft background with inset and outer shadows. Keep the contrast between the filled and unfilled portions strong enough to communicate progress without relying on shadow depth alone.

## Responsive behavior

Use a fluid width such as `width: min(100%, 520px)` and avoid fixed heights that become uncomfortable on small screens.

## Accessibility

Keep the numeric value available through the progress element. If the progress is indeterminate, omit the value rather than exposing a misleading percentage.

## Reduced motion

If the fill uses a decorative transition, disable or shorten it under `prefers-reduced-motion: reduce`.

## Example CSS

```css
.neo-progress {
  width: min(100%, 520px);
  height: 18px;
  border: 0;
  border-radius: 999px;
  box-shadow: inset 4px 4px 8px rgba(0, 0, 0, .12);
}
```
