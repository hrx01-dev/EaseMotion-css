# Ripple-Wave Hero

A polished, responsive hero section that uses concentric CSS ripples, soft ambient orbs, and glassmorphism to create a technology-focused landing-page introduction.

## What is included

- Five staggered ripple layers created with a single `@keyframes` animation.
- Glass navigation, CTA buttons, metrics panel, and footer metadata.
- Ambient gradient orbs for additional depth without JavaScript.
- Fluid typography using `clamp()` and responsive breakpoints.
- Keyboard-visible focus states for navigation and CTA links.
- `prefers-reduced-motion` support for users who request less animation.

## File structure

```text
ripple-wave-hero/
├── demo.html
├── style.css
└── README.md
```

## Usage

Open `demo.html` directly in a modern browser. There are no build tools, JavaScript dependencies, web fonts, or external assets required.

The main structure is intentionally semantic:

```html
<section class="hero" aria-labelledby="hero-title">
  <nav class="hero__nav" aria-label="Primary">...</nav>
  <div class="hero__content">...</div>
  <aside class="hero__panel">...</aside>
</section>
```

## Motion design

`.hero__waves span` receives the `ripple` keyframes. Each layer uses a negative animation delay so the rings appear to emit continuously from a shared origin. The animation changes only `transform` and `opacity`, keeping the effect lightweight.

The ambient orbs use separate, slow transforms to avoid competing with the primary ripple motion. CTA hover motion is intentionally short and restrained.

## Customization

The primary visual tokens live in `:root`:

| Token | Purpose |
| --- | --- |
| `--bg` | page background |
| `--surface` | translucent UI surface |
| `--border` | glass border |
| `--text` | primary text |
| `--muted` | secondary text |
| `--violet` | primary accent |
| `--cyan` | secondary accent |
| `--ease` | interaction timing |

Adjust the five ripple spans' animation delays to change the rhythm, or change the scale endpoint to make the waves tighter or wider.

## Accessibility

Decorative motion elements are marked `aria-hidden`. Interactive controls are real links, have visible focus indicators, and remain usable without hover. Reduced-motion preferences disable the ripple and ambient movement while preserving the layout and content.
