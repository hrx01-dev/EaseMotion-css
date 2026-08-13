# CSS-only Neumorphic Input

Issue #79682 demonstrates a responsive, CSS-only form input built around a soft neumorphic surface. The component focuses on clear hierarchy, tactile depth, accessible focus treatment, and a layout that remains usable across screen sizes.

## Overview

The input is designed as a reusable form-field pattern for landing pages, dashboards, settings panels, checkout forms, and other interfaces that benefit from a soft raised or inset visual language. It uses native HTML controls so the component does not depend on JavaScript or a framework.

## Features

- Native label and input semantics
- Soft neumorphic surface treatment
- Inset depth styling for the field
- Responsive spacing and sizing
- Visible keyboard focus states
- Mobile-friendly layout
- Touch-friendly control dimensions
- Clean placeholder and helper-text presentation
- Pure HTML and vanilla CSS
- No external dependencies
- Reduced-motion friendly transitions

## Structure

The demonstration is intentionally small and easy to reuse:

- `demo.html` contains the semantic form markup and complete example.
- `style.css` contains the surface, spacing, typography, responsive, and state styles.
- `README.md` documents the component, behavior, and integration guidance.

## Usage

Open `demo.html` in a modern browser to preview the component. To integrate it into another page, copy the input markup into the desired form and link `style.css`. Replace the label, placeholder, helper text, and surrounding form content with application-specific information.

## Styling

The visual depth is created with CSS shadows rather than images or JavaScript. The surrounding surface and field shadows can be adjusted to match a project's existing background, border radius, spacing scale, and typography system.

## Responsive Behavior

The layout uses flexible widths and spacing so the field remains comfortable on smaller screens. Desktop layouts can provide more horizontal breathing room, while mobile layouts keep the control within the viewport and preserve readable text.

## Accessibility

Native form controls remain in use, which preserves expected browser and assistive-technology behavior. The label is associated with the input, and a clear focus treatment helps keyboard users identify the active field. Visual depth is decorative and does not carry essential information.

## Customization

Adjust the colors, border radius, shadows, font sizes, spacing, and focus treatment in `style.css`. The markup can remain unchanged when only the visual theme needs to be updated.

## Browser Support

The example uses standard HTML and modern CSS features supported by current evergreen browsers. No build step, JavaScript runtime, or external library is required.

## Design Notes

Neumorphic effects work best when the contrast between the component and its surrounding surface remains controlled. The example therefore uses layered shadows and spacing rather than excessive borders or decorative imagery.

## Issue

EaseMotion CSS issue #79682.
