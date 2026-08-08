# Scale-Hover Pricing Table

## Overview

This showcase demonstrates a glassmorphism pricing table where the active card gently scales above the surrounding cards. The interaction is deliberately restrained: the content does not move in normal document flow, so users can compare every plan before and during interaction.

## Goals

- Create a polished pricing surface using only HTML and CSS.
- Use `transform: scale()` as the primary motion primitive.
- Preserve layout stability while a card is emphasized.
- Give pointer and keyboard users equivalent feedback.
- Reduce the motion on smaller screens.
- Respect `prefers-reduced-motion`.

## File structure

```text
scale-hover-pricing-table/
├── demo.html
├── style.css
└── README.md
```

## Features

- Three complete pricing tiers.
- Glassmorphism surfaces with translucent layers.
- Radial lighting that appears on interaction.
- Scale interaction using a custom easing curve.
- Stronger border and shadow on the active card.
- Keyboard-friendly `:focus-within` interaction.
- Responsive grid and mobile layout.
- Reduced-motion fallback.
- No JavaScript and no external assets.

## How the motion works

The resting card uses the normal transform state. When the pointer enters the card, or when an interactive child receives keyboard focus, the card receives `transform: scale(1.055)` on larger screens.

The scale is intentionally small. A pricing card should gain emphasis without becoming so large that it obscures neighboring choices.

The shadow also becomes deeper and the border becomes brighter. These changes reinforce the same state without introducing a second animation language.

## Interaction states

### Rest

All cards use the same translucent surface and spacing.

### Hover

The hovered card scales, gains a brighter border, and reveals a soft radial highlight.

### Keyboard focus

`:focus-within` mirrors the hover treatment. A user can tab to a plan action and receive the same visual hierarchy.

### Reduced motion

The media query for `prefers-reduced-motion: reduce` removes the transform transition and prevents the card from scaling.

## Markup anatomy

The page is organized into a masthead, an interaction guide, a pricing grid, supporting notes, and a compact footer.

Each pricing card contains a plan identifier, title, description, price, feature list, and action link. This keeps the component useful as a real interface example rather than a purely decorative animation.

## CSS architecture

### Design tokens

The `:root` block contains colors, surfaces, borders, easing, and accent values. This makes it easy to adapt the component to another visual system.

### Page shell

`.page` controls the readable maximum width and overall vertical rhythm.

### Hero

`.hero`, `.hero__copy`, and `.hero__meta` establish the introduction and explain the interaction before the user reaches the cards.

### Pricing grid

`.plans` provides the desktop three-column layout. The grid changes to a single column at the tablet breakpoint.

### Card

`.plan` owns the glass surface, depth, motion, and spacing. Pseudo-elements provide lighting without extra markup.

### Action

The action link has its own hover and focus treatment. It is intentionally lightweight so the scale animation remains the main feature.

## Customization

The primary variables are:

| Variable | Role |
| --- | --- |
| `--bg` | Page background |
| `--surface` | Base glass surface |
| `--surface-strong` | Card gradient surface |
| `--border` | Card border |
| `--text` | Primary text |
| `--muted` | Supporting text |
| `--subtle` | Metadata text |
| `--accent` | Accent color |
| `--accent-light` | Highlighted accent |
| `--cyan` | Secondary glow |
| `--ease` | Scale easing curve |

### Changing scale

The default desktop value is `1.055`.

A calmer interface can use `1.03`. A more expressive showcase can use `1.07`, although large values should be avoided in dense pricing layouts.

### Changing timing

The default motion duration is `300ms`. Around `200ms` feels more immediate, while values around `400ms` feel more cinematic.

### Changing the glow

The `.plan::before` gradient controls the internal highlight. Lower its alpha for a quieter interface or increase it for a stronger glass effect.

## Responsive behavior

At desktop widths, all three plans sit side by side. At widths below 920px, the cards stack vertically and the scale is reduced to `1.025`.

The supporting detail cards become two columns and then one column on very narrow screens. The interaction guide also collapses so labels remain readable.

## Accessibility

The component does not rely on color alone. Plan names, prices, and features remain visible in every state.

Actions are semantic links with visible focus outlines. The same scale hierarchy is exposed through `:focus-within` so keyboard users are not excluded from the interaction.

Reduced-motion support removes scaling while preserving all content and focus behavior.

## Performance

The effect uses `transform`, `opacity`, and `box-shadow`. It does not animate width, height, padding, or margins, which helps avoid unnecessary layout recalculation.

There is no JavaScript loop, observer, timer, or event listener. Motion happens only during user interaction.

The glass effect uses `backdrop-filter` with a prefixed fallback. Browsers without blur support still receive a translucent card and border.

## Testing checklist

1. Open `demo.html` in a current desktop browser.
2. Hover each pricing card.
3. Confirm only the active card gains scale.
4. Tab through the action links.
5. Confirm keyboard focus receives the same emphasis.
6. Resize below the tablet breakpoint.
7. Confirm the scale becomes more restrained.
8. Resize to a narrow mobile viewport.
9. Enable reduced motion in the operating system.
10. Confirm the scale animation is disabled.
11. Confirm content remains fully readable.

## Design principles

1. Motion should establish hierarchy, not distract from content.
2. A pricing comparison should remain stable while a card is emphasized.
3. Keyboard interaction must receive the same visual treatment as pointer interaction.
4. Mobile motion should be restrained.
5. Reduced-motion preferences should be honored.
6. Decorative effects should never replace semantic information.
7. A showcase should remain dependency-free when the feature itself is CSS motion.

## Browser notes

The example uses standard CSS grid, flexbox, custom properties, gradients, transitions, transforms, pseudo-elements, media queries, and `backdrop-filter`.

No JavaScript is required. The layout gracefully degrades to a translucent surface when backdrop blur is unavailable.

## Contribution notes

The example is self-contained under the feature-named submission directory. It does not modify shared repository styles or dependencies.
