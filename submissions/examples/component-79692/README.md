# Floating Gradient Sidebar

Issue #79692 demonstrates a responsive floating sidebar with gradient depth, clear navigation states, and a compact application-shell layout. The component is intended for dashboards, SaaS interfaces, documentation pages, and other layouts that need persistent navigation without a heavy framework.

## Overview

The sidebar uses layered surfaces and gradients to create a floating appearance while keeping the navigation itself simple and semantic. The visual treatment is implemented entirely with CSS so the component can be reused in static HTML or adapted to a larger application.

## Features

- Responsive floating sidebar
- Layered gradient surface
- Visual depth without images
- Clear active and hover states
- Visible `:focus-visible` navigation states
- Responsive navigation layout
- Touch-friendly spacing
- Native semantic links
- Pure HTML and vanilla CSS
- No external libraries or runtime dependencies
- Reduced-motion friendly presentation

## Structure

- `demo.html` contains the complete sidebar demonstration.
- `style.css` contains layout, gradients, depth, spacing, responsive behavior, and interaction states.
- `README.md` documents the component and integration details.

## Usage

Open `demo.html` directly in a modern browser to preview the sidebar. For integration, copy the navigation markup into the application shell and include `style.css`. Replace the labels and destinations with the routes used by your project.

## Responsive Behavior

The sidebar maintains a comfortable navigation width on larger screens and adapts into a narrower, readable layout on smaller screens. Content remains within the viewport and navigation spacing is preserved for touch interaction.

## Accessibility

Navigation uses native links so standard keyboard and browser behavior remains available. Focus-visible styling identifies the current keyboard target, and the visual gradient is not required to understand the navigation structure.

## Visual System

The floating appearance is created with gradients, shadows, borders, and controlled spacing. The component avoids excessive decoration so the navigation remains the primary focus of the interface.

## Customization

Adjust surface colors, gradient stops, shadow intensity, typography, spacing, border radius, and breakpoints in `style.css`. The HTML can be reused with different content without changing the underlying layout approach.

## Performance

The component has no JavaScript animation loop and no external assets are required for its core presentation. CSS handles the visual depth and responsive layout, keeping the implementation lightweight.

## Browser Support

The demo uses standard HTML and modern CSS features supported by current evergreen browsers. No build process is required to preview the example.

## Issue

EaseMotion CSS issue #79692.
