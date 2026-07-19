# Skew-Active Glassmorphism Carousel

A pure CSS animated horizontal carousel featuring a unique Skew-Active interaction transition, exquisitely styled to complement modern Glassmorphism UI layouts.

## Features

- **Pure CSS Scrolling:** Uses native CSS Scroll Snap (`scroll-snap-type: x mandatory`) for an optimized, accessible, and native-feeling horizontal scroll experience across all devices without relying on JavaScript libraries.
- **Skew-Active Transition:** By default, cards rest at a dynamic skewed angle (`-8deg`). Upon hover or focus, the card smoothly "stands up" (unskews to `0deg`) and scales forward. This creates a very engaging, domino-like interactive feel.
- **Glassmorphism Aesthetics:** The cards utilize `backdrop-filter: blur()`, semi-transparent backgrounds, subtle white borders, and soft shadows. A vibrant fixed animated gradient background is included in the demo to allow the frosted glass effect to truly shine through.
- **Responsive:** Adapts from a multi-column desktop layout to a single-card peek layout on mobile, giving users a clear visual cue that they can scroll for more content.
- **Keyboard Accessible:** Fully operable via keyboard. The `:focus-visible` state triggers the exact same beautiful skew-and-scale interaction as a mouse hover, complete with an accessibility-friendly border highlight.

## Customization

The component exposes several CSS variables on the `:root` pseudo-class for seamless customization:

```css
:root {
    /* Skew-Active Parameters */
    --carousel-skew-idle: -8deg;
    --carousel-skew-active: 0deg;
    --carousel-scale-idle: 0.92;
    --carousel-scale-active: 1.05;
    --carousel-transition-time: 0.5s;
    --carousel-easing: cubic-bezier(0.34, 1.56, 0.64, 1);
    
    /* Glassmorphism Theme Palette */
    --glass-bg: rgba(255, 255, 255, 0.05);
    --glass-bg-hover: rgba(255, 255, 255, 0.15);
    --glass-blur: 16px;
    /* ... see style.css for all properties */
}
```

## How to Use

1. Copy the HTML structure from `demo.html`.
2. Include the styles from `style.css`.
3. Add your content inside the `.glass-card` elements. Ensure your track remains an unordered list `<ul>` and items are `<li>` for standard structural semantics.
4. *Important Note for Glassmorphism:* The glass effect (`backdrop-filter`) is only visible if there is something colorful or textured behind it. Make sure your parent container or body background has gradients, images, or abstract shapes (like the blobs provided in the demo).

```html
<!-- Core Structure -->
<div class="carousel-container">
    <ul class="carousel-track" tabindex="0">
        <li class="carousel-item">
            <article class="glass-card" tabindex="0">
                <div class="card-image" style="background-image: url('...');"></div>
                <div class="card-content">
                    <!-- Text Content -->
                </div>
            </article>
        </li>
    </ul>
</div>
```
