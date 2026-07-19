# Shimmer Sweep Tabs - E-Commerce Checkout

A pure CSS animated tab component creatively structured as a multi-step checkout flow. It features a continuous, trust-building shimmer sweep animation on the progress indicator, perfectly tailored for high-conversion E-Commerce interface aesthetics.

## Features

- **Pure CSS State Management:** Functions entirely without JavaScript using the `:checked` radio button hack, gracefully handling multi-step form navigation through CSS sibling combinators.
- **Shimmer Sweep Interaction:** 
  1. The active progress bar indicator (`.stepper-progress-fill`) features a continuous, sweeping light reflection animation (`shimmerSweep`).
  2. The primary CTA buttons feature an intricate CSS pseudo-element hover effect (`.shimmer-hover`), sweeping a glossy highlight across the button to draw attention and encourage clicks.
- **E-Commerce Checkout Aesthetics:** Designed to instill trust. It uses a clean white background with soft borders, a "Trust Green" primary color (`#059669`), clear typography (`Inter`), and fully styled mock checkout forms (Shipping, Payment selection, Order Summary).
- **Responsive & Accessible:** The layout uses fluid grids that collapse to single columns on mobile devices (the stepper text hides on mobile to save space, keeping just the circles). Fully keyboard operable, with focus states clearly outlined. (Includes a minimal inline script strictly to map Space/Enter keys to radio triggers on the labels/buttons).

## Customization

The component exposes several CSS variables on the `:root` pseudo-class for seamless customization:

```css
:root {
    /* Shimmer Sweep Parameters */
    --shimmer-speed: 2.5s;
    --transition-time: 0.5s;
    
    /* E-Commerce Checkout Palette */
    --primary-color: #059669; /* Trust Green */
    --bg-main: #f9fafb;
    /* ... see style.css for all properties */
}
```

## How to Use

1. Copy the HTML structure from `demo.html`. Ensure you keep the hidden `<input type="radio">` tags.
2. Include the styles from `style.css`.
3. The checkout navigation is powered by `<label>` elements acting as buttons. By setting the `for="tab-id"` attribute on a button, clicking it will trigger the CSS state change to move to the next tab.

```html
<!-- Core Structure Example -->
<div class="tabs-container">
    <input type="radio" id="step1" name="tabs" checked>
    <input type="radio" id="step2" name="tabs">
    
    <nav class="stepper-header">
        <div class="stepper-progress-bg">
            <div class="stepper-progress-fill shimmer-sweep"></div>
        </div>
        <label for="step1">1</label>
        <label for="step2">2</label>
    </nav>
    
    <div class="tabs-content">
        <div class="tab-panel panel-1">
            <!-- Navigate to next step using a label -->
            <label for="step2" class="btn-primary shimmer-hover">Next</label>
        </div>
        <div class="tab-panel panel-2">...</div>
    </div>
</div>
```
