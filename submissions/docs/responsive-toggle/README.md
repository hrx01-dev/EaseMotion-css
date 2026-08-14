# Responsive Toggle

A responsive toggle control documented for reuse in EaseMotion CSS projects. The example demonstrates a compact switch that adapts to narrow and wide layouts while preserving a clear focus state and accessible labeling.

## What this example demonstrates

- Responsive sizing with CSS media queries.
- A semantic checkbox as the interaction model.
- Visible checked, hover, and keyboard-focus states.
- A smooth thumb transition without JavaScript.
- A layout that remains usable on touch and desktop screens.

## Usage

Include `style.css` and place the markup from `demo.html` in the page where the toggle is required. The hidden checkbox remains the source of truth, while CSS renders the visual switch.

```html
<label class="responsive-toggle">
  <input type="checkbox" />
  <span class="responsive-toggle__track" aria-hidden="true"></span>
  <span>Enable responsive mode</span>
</label>
```

## Customization

Adjust the track dimensions, transition duration, typography, and spacing in `style.css`. Keep the input associated with a visible label so the control remains keyboard and screen-reader friendly.

## Accessibility

The demo uses a real checkbox instead of a click-only element. The focus-visible treatment makes keyboard navigation apparent, and the label gives the control an accessible name.

## Files

- `demo.html` — complete usage example and preview.
- `style.css` — responsive component styling.
- `README.md` — implementation and customization notes.
