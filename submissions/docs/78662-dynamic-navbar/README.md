# Dynamic Navbar

Documentation and standalone usage guide for issue #78662.

## Overview

The Dynamic Navbar is a responsive navigation pattern that changes presentation by width.
The desktop layout provides direct access to the main navigation links.
A compact menu control is introduced when the viewport becomes narrow.
The component keeps navigation semantic while adapting its visual arrangement.
It is suitable for landing pages, dashboards, documentation, and application shells.

## Features

- Responsive desktop and compact layouts.
- Native navigation links.
- Compact menu button for narrow screens.
- `aria-expanded` state communication.
- Visible keyboard focus styling.
- Reduced-motion support.
- No external navigation framework required.

## Demo

Open `demo.html` in a modern browser to preview the navigation.
Resize the viewport to observe the transition between navigation layouts.
Use the compact menu control on smaller screens to reveal the links.
Press Tab to test keyboard navigation and visible focus states.
The example includes branding, navigation links, and a clear menu state.

## Usage

Use a semantic `<nav>` element for the main navigation.
Keep the navigation links grouped inside the navigation landmark.
Use a native button for the compact menu control.
Update `aria-expanded` whenever the compact navigation opens or closes.
Keep the menu state synchronized with its visual presentation.
Link `style.css` through the host project's normal stylesheet pipeline.

## Accessibility

Native links and buttons provide expected keyboard interaction.
The compact menu button exposes its state with `aria-expanded`.
Focus indicators remain visible when navigating without a pointer.
Navigation remains understandable without decorative transitions.
Reduced-motion preferences simplify or remove animated state changes.
Labels should remain descriptive and distinguish navigation from other controls.

## Responsive Behavior

The desktop layout displays navigation links in a horizontal arrangement.
A breakpoint changes the presentation when available width becomes limited.
The compact menu avoids forcing links into an overcrowded row.
The mobile navigation can stack links vertically for easier touch access.
Spacing adapts so the header remains usable on narrow screens.

## Customization

Adjust the responsive breakpoint to match the host navigation width.
Change navigation gaps to control desktop density.
Modify menu panel padding for different mobile layouts.
Update transition timing to match the site's motion language.
Change typography, borders, and surface treatments to match the design system.
Keep the menu control visually distinct from ordinary navigation links.

## Implementation Notes

The HTML keeps navigation semantics independent from presentation.
The interaction logic only controls the compact menu state.
CSS handles layout changes, spacing, transitions, and responsive behavior.
The demo can be opened directly without a build process.
The pattern can be integrated into application shells with minimal changes.

## File Structure

- `demo.html` — expanded responsive navbar demonstration.
- `style.css` — navigation layout and responsive styling.
- `README.md` — usage and accessibility documentation.

## Browser Support

The component targets current evergreen browsers.
It uses standard HTML, CSS media queries, transitions, and browser events.
Navigation remains functional when decorative transitions are unavailable.

## Testing Checklist

- Verify all navigation links are reachable by keyboard.
- Confirm the compact button exposes its expanded state.
- Test opening and closing the mobile navigation.
- Resize the viewport around the responsive breakpoint.
- Enable reduced-motion and inspect transition behavior.
- Check that the navigation does not cause horizontal page scrolling.

## Reuse

Replace the example links and branding with project-specific content.
Adjust the breakpoint based on the real navigation content rather than a device label.
Follow repository contribution and licensing conventions when reusing the example.
