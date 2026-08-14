# Brutalism Segmented Switch Control — Theming Configuration

## Overview
This guide documents the theming configuration for the Brutalism Segmented Switch Control.

The component uses semantic buttons grouped inside a single control.

The visual treatment is intentionally bold, high-contrast, and geometric.

The guide focuses on modifier classes and custom CSS property overrides.

The markup can be copied directly into a documentation page or application.

## Markup

```html
<div class="segmented-switch" role="group" aria-label="Display mode">
  <button class="segmented-switch__option segmented-switch__option--active" type="button" aria-pressed="true">Grid</button>
  <button class="segmented-switch__option" type="button" aria-pressed="false">List</button>
</div>
```

Keep each option as a native button.

Use `aria-pressed` when the control represents a toggleable selection.

Provide a descriptive group label when the purpose is not obvious from nearby content.

## Class Structure

`segmented-switch` is the component block.

`segmented-switch__option` is the reusable option element.

`segmented-switch__option--active` represents the selected visual state.

Additional modifiers can define compact or large presentations.

Keep modifier names consistent when extending the component.

## Custom Properties

Theme values are exposed through CSS custom properties.

```css
.segmented-switch {
  --switch-border: 3px solid #111111;
  --switch-surface: #f6e95f;
  --switch-active: #111111;
  --switch-active-text: #ffffff;
  --switch-shadow: 5px 5px 0 #111111;
}
```

Override variables on the component or an appropriate theme scope.

Avoid duplicating selectors only to change a color or spacing value.

## Modifiers

Use a modifier for intentional size variants.

A compact modifier can reduce padding while preserving the same interaction model.

A high-contrast modifier can increase border weight without changing markup.

Keep modifiers optional so the base component remains useful.

## Keyboard Navigation

Native buttons participate in the normal tab order.

Users can move focus with Tab and Shift+Tab.

Activation should work with Enter and Space through native button behavior.

If arrow-key navigation is introduced, document the roving-focus model clearly.

Do not trap keyboard focus inside the component.

## Accessibility

Maintain visible focus styles for keyboard users.

Do not rely only on color to identify the active option.

Keep text contrast strong against both selected and unselected surfaces.

Use `aria-pressed` only when it accurately describes the state.

Avoid unnecessary ARIA roles when native semantics already provide the behavior.

## Responsive Behavior

The control should fit within narrow containers.

Allow options to shrink without clipping their labels.

Use a stacked layout only when the available width requires it.

Test the control at mobile, tablet, and desktop widths.

## Reduced Motion

The theme does not require motion to communicate state.

Optional transitions should be disabled or shortened under `prefers-reduced-motion`.

The selected state must remain clear without animation.

## Usage

Place the component where users need to switch between related views.

Keep option labels short and mutually understandable.

Update `aria-pressed` when application state changes.

Use the active modifier to mirror the current visual state.

## Testing Checklist

- Test mouse and touch interaction.
- Test keyboard focus and activation.
- Test visible focus indicators.
- Test selected-state contrast.
- Test narrow layouts.
- Test browser zoom.
- Test reduced-motion preferences.

## Files

`README.md` contains this theming guide.

`demo.html` provides the standalone example.

`style.css` contains the presentation and theme variables.

## Summary

The Brutalism Segmented Switch Control can be themed without changing its semantic structure.

Custom properties keep design tokens centralized.

Native buttons provide a reliable accessibility foundation.

The result remains reusable, responsive, and easy to adapt.