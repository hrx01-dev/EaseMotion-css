# SaaS Modern Header Navbar — Theming

## Overview
This guide documents theming configuration for the SaaS Modern Header Navbar.
The component uses semantic navigation markup and CSS custom properties.
The goal is visual flexibility without changing the HTML structure.

## Scope
- Theme-level custom properties.
- Navbar modifier classes.
- Responsive navigation layout.
- Keyboard navigation guidance.
- Accessible landmark structure.
- Standalone demo usage.

## Markup
Use a `header` containing a `nav` landmark.
Keep navigation links inside a logical list.
Use descriptive link text and preserve source order.

## Modifiers
Use modifiers for meaningful presentation variants.
Keep modifier names attached to the component block.
Avoid creating duplicate selectors for simple color changes.

## Theme Tokens
Expose surface, text, accent, border, spacing, radius, and shadow variables.
Override tokens from a theme scope instead of editing individual selectors.

## Surface
Choose a surface that separates the header from page content.
Keep the surface readable in both light and dark contexts.

## Text
Use a primary text token for navigation labels.
Use a muted token only for secondary information.

## Accent
Use the accent token for links and active states.
Check contrast after changing the accent color.
Do not make active state meaning depend on color alone.

## Spacing
Keep consistent gaps between navigation items.
Use a smaller gap only in compact variants.
Avoid spacing that causes overflow on narrow screens.

## Accessibility
The `nav` element provides a native navigation landmark.
Give it an accessible label when multiple navigation landmarks exist.
Use real links for destinations.
Provide visible focus states.
Do not rely on hover alone.

## Keyboard Navigation
Links must remain reachable with Tab.
Focus order should match visual order.
If a mobile menu exists, its trigger should be a real button.
Expose expanded state when a collapsible menu is used.

## Responsive Behavior
Allow navigation to wrap or collapse at an intentional breakpoint.
Keep tap targets comfortable on narrow screens.
Avoid fixed widths that create horizontal overflow.
Test intermediate widths.

## Reduced Motion
Respect `prefers-reduced-motion` for optional menu transitions.
The navigation remains usable without animation.

## Customization
Change theme variables at component or page scope.
Use the accent token for active and interactive states.
Keep contrast suitable for every supported theme.

## Demo
Open `demo.html` directly to inspect the themed header.
Resize the viewport to verify responsive behavior.
Use keyboard navigation to verify focus order.

## Testing Checklist
- Validate navigation landmarks.
- Test every link with the keyboard.
- Test visible focus indicators.
- Test narrow viewport widths.
- Test wide viewport widths.
- Test custom property overrides.
- Test contrast after theme changes.
- Test reduced-motion preferences.

## File Structure
`README.md` documents theming and usage.
`demo.html` provides the standalone example.
`style.css` contains presentation and theme variables.

## Implementation Notes
Keep structure in HTML and presentation in CSS.
Prefer custom properties for reusable design tokens.
Use modifiers only for meaningful variants.
The component can be embedded without framework dependencies.

## Summary
The themed navbar keeps visual customization predictable.
Preserve semantic navigation and keyboard behavior while changing appearance.
Use the CSS variables as the primary design-system integration point.
