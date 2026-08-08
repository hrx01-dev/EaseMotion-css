# Ripple-Wave Hero

A polished, responsive hero section that uses concentric CSS ripples, ambient orbs, glassmorphism, and a compact motion-sequence panel to create a technology-focused landing-page introduction.

## Overview

The component is designed as a complete hero showcase rather than a single animation snippet. It combines a readable content hierarchy with a decorative motion field placed behind the interface. The ripple layers remain decorative, while all important content and controls remain normal HTML.

The implementation has no JavaScript, no framework dependency, no external images, and no web-font dependency.

## What is included

- Six staggered ripple layers created with one reusable `@keyframes` animation.
- A glass navigation bar with accessible anchor links.
- A large responsive headline and supporting product copy.
- Primary and secondary CTA buttons.
- A three-column component highlight panel.
- A motion-sequence indicator explaining the visual rhythm.
- Three ambient gradient orbs for depth.
- A subtle technical grid and texture layer.
- Fluid typography using `clamp()`.
- Responsive breakpoints for tablet and mobile layouts.
- Keyboard-visible focus states.
- `prefers-reduced-motion` support.

## File structure

```text
ripple-wave-hero/
├── demo.html
├── style.css
└── README.md
```

## Running the example

1. Download or clone the repository.
2. Open `demo.html` in a modern browser.
3. No build step is necessary.
4. Resize the browser to test the responsive layout.
5. Use keyboard navigation to test the focus states.
6. Enable a reduced-motion operating-system preference to test the accessibility fallback.

## HTML architecture

The page is divided into a few intentional layers.

### Hero shell

`.hero-shell` centers the component on the page and gives the example a controlled maximum width.

### Hero surface

`.hero` is the glass container. It owns the decorative layers so the animation never affects document flow.

### Navigation

The navigation contains a branded home link and three same-page links. Real anchors are used instead of clickable generic elements.

### Content

The main content uses a single `h1`, an eyebrow, supporting paragraph, and two CTA links. This keeps the document hierarchy useful to screen readers.

### Decorative motion

`.hero__waves` contains six empty spans. They are explicitly `aria-hidden` because they communicate atmosphere rather than information.

### Highlight panel

The panel summarizes three properties of the component: pure CSS, responsive behavior, and accessibility support.

### Motion sequence

The process indicator describes the three visual stages: origin, expansion, and fade. It is intentionally static so users who disable motion can still understand the concept.

## Motion design

The primary animation is attached to `.hero__waves span`.

```css
@keyframes ripple {
  0% {
    transform: scale(0.2);
    opacity: 0;
  }

  14% {
    opacity: 0.78;
  }

  70% {
    opacity: 0.28;
  }

  100% {
    transform: scale(3.35);
    opacity: 0;
  }
}
```

Every ring uses the same keyframes but a different negative delay. This creates a continuous stream without requiring separate animations for each ring.

Only `transform` and `opacity` are animated for the ripple itself. These properties are preferable for a lightweight motion effect because they avoid repeatedly changing layout dimensions.

The ambient orbs use slower transforms. They are deliberately less noticeable than the ripple field so the primary motion remains visually clear.

## Customization

The main visual tokens live in `:root`.

| Token | Purpose |
| --- | --- |
| `--bg` | Page background |
| `--surface` | Main translucent surface |
| `--surface-strong` | Stronger glass surface |
| `--border` | Primary border color |
| `--border-soft` | Secondary border color |
| `--text` | Primary text |
| `--muted` | Supporting text |
| `--subtle` | Metadata text |
| `--violet` | Primary accent |
| `--violet-light` | Light accent |
| `--cyan` | Secondary accent |
| `--ease` | Shared interaction timing |

### Changing the wave rhythm

Adjust the negative animation delays on the individual spans to make the sequence faster or slower.

### Changing wave size

The final `scale()` value controls how far the rings travel before disappearing. A smaller value produces a tighter visual field, while a larger value produces a wider broadcast effect.

### Changing the density

Add or remove wave spans in `demo.html`. If additional spans are added, give each one a progressively different negative delay.

## Responsive behavior

On wide screens the ripple field occupies the right side of the hero while the content remains left aligned. The feature panel sits over the lower portion of the decorative field.

At tablet widths, the feature panel returns to normal document flow. The motion-sequence indicator also moves below the primary content.

On small screens the navigation links are hidden to preserve space, the CTA buttons become full-width, and the highlight panel becomes a vertical list.

## Accessibility

Decorative motion elements use `aria-hidden="true"`. Interactive controls are native anchors with visible focus indicators.

The component also includes a reduced-motion media query:

```css
@media (prefers-reduced-motion: reduce) {
  .hero__waves span,
  .hero__orb {
    animation: none;
  }
}
```

The layout, hierarchy, text, and controls remain intact when animation is disabled.

## Browser considerations

The design uses standard CSS features such as grid, flexbox, gradients, `clamp()`, custom properties, and `@keyframes`. The glass effect uses `backdrop-filter` with the prefixed fallback property for browsers that expose the prefixed implementation.

The visual result is intentionally graceful if backdrop blur is unavailable: the translucent background and border still provide enough separation.

## Design principles

1. Keep the main message readable above the animation.
2. Treat decorative motion as background, not content.
3. Use transform and opacity for repeated motion.
4. Keep interaction transitions short and predictable.
5. Respect reduced-motion preferences.
6. Preserve the component's hierarchy at every breakpoint.

## License

This example is intended as a self-contained EaseMotion CSS showcase and follows the repository's contribution guidelines.
