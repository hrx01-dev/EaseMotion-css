# Responsive Pastel Toggle

Issue #79701 demonstrates a responsive toggle with soft pastel styling, native checkbox semantics, and clear interaction states. The component is intended as a reusable settings control that remains understandable and accessible without JavaScript.

## Overview

The toggle uses a native checkbox as its underlying control and layers a custom visual treatment around it. This keeps the interaction model familiar while allowing the appearance to fit soft, pastel, or friendly interface designs.

## Features

- Native checkbox semantics
- Soft pastel state styling
- Clear enabled and disabled states
- Visible keyboard focus
- Responsive layout
- Touch-friendly sizing
- Reduced-motion support
- Semantic HTML structure
- Pure HTML and vanilla CSS
- No external dependencies

## Structure

- `demo.html` contains the complete toggle example and supporting content.
- `style.css` contains the visual states, layout, spacing, transitions, and responsive rules.
- `README.md` documents usage and customization.

## Usage

Open `demo.html` in a modern browser to preview the component. To integrate it, copy the native checkbox and associated label structure into a settings form and include `style.css`. Update the label text and surrounding content to match your application.

## Interaction

The underlying checkbox remains the source of truth for the toggle state. CSS selectors update the visual treatment when the control is checked, allowing the component to work without a JavaScript state-management layer.

## Responsive Behavior

The toggle remains compact while preserving a comfortable click and touch target. Supporting text and surrounding content can wrap naturally on smaller screens without forcing horizontal scrolling.

## Accessibility

Using a native checkbox preserves standard keyboard interaction and assistive-technology semantics. The component also provides a visible focus treatment so keyboard users can identify the active control. State information should remain understandable from the associated label and text, not color alone.

## Customization

Change the pastel colors, border radius, dimensions, shadow strength, typography, spacing, and transition timing in `style.css`. The semantic markup can remain unchanged when only the visual design needs to be updated.

## Reduced Motion

Transitions are decorative and should not be required to understand the control. The stylesheet includes reduced-motion-friendly behavior so users who prefer less motion can interact with the toggle comfortably.

## Browser Support

The example uses standard HTML and modern CSS features supported by current evergreen browsers. No JavaScript framework, build step, or external library is required.

## Design Notes

Soft controls benefit from restrained contrast and consistent spacing. The example keeps the visual treatment focused on the state change while avoiding unnecessary decoration around the native interaction.

## Issue

EaseMotion CSS issue #79701.
