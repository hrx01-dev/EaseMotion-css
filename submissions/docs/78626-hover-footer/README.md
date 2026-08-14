# Hover Footer

Documentation and standalone usage guide for issue #78626.

## Overview

The Hover Footer is a responsive footer component with clear interaction feedback.
It gives navigation links a refined visual response when hovered or focused.
The design is suitable for landing pages, product sites, portfolios, and documentation.
The footer keeps navigation grouped so related destinations remain easy to scan.
The implementation uses semantic HTML and CSS without a UI framework.

## Features

- Responsive footer layout for different viewport sizes.
- Clear hover and keyboard focus treatment.
- Semantic navigation and native links.
- Flexible link groups for reusable footer content.
- Reduced-motion support for animated states.
- Clean spacing that can be adapted to existing layouts.
- No dependency on external animation libraries.

## Demo

Open `demo.html` in a modern browser to view the complete footer.
The example includes branding, grouped navigation, and supporting information.
Move the pointer across links to see the hover treatment.
Use Tab to verify that keyboard focus receives equivalent feedback.
Resize the browser to check the responsive stacking behavior.

## Usage

Place the footer after the main page content.
Use a semantic `<footer>` element for the page-level container.
Group navigation links inside appropriately labelled navigation sections.
Keep link text descriptive so destinations are understandable without visual context.
Link `style.css` using the normal stylesheet mechanism of the host project.
Reuse the same structure when adding or removing navigation groups.

## Accessibility

Navigation items use native anchor elements and normal browser behavior.
Keyboard users can reach every link without relying on pointer interaction.
`:focus-visible` styling keeps the active keyboard location easy to identify.
Hover effects are not used to communicate essential information.
The footer remains readable when animation is reduced or disabled.
Color changes should maintain sufficient contrast in custom themes.

## Responsive Behavior

The footer uses flexible columns for larger screens.
Navigation groups can stack when the available width becomes limited.
Spacing is reduced carefully at smaller breakpoints.
Long link labels are allowed to wrap rather than forcing horizontal scrolling.
The footer remains visually separated from the page content on mobile screens.

## Customization

Adjust footer padding to change the overall visual density.
Change the maximum width to align the footer with the main page container.
Modify link transitions to match the project's interaction language.
Update border, shadow, and background values for different themes.
Change column gaps without altering the semantic markup.
Keep focus styling visible when customizing hover effects.

## Implementation Notes

The demo keeps the footer structure readable and easy to reuse.
Presentation is contained in `style.css` rather than inline attributes.
The hover interaction is paired with keyboard focus behavior.
Responsive rules are organized around layout needs instead of device names.
The component can be integrated into static sites or application layouts.

## File Structure

- `demo.html` — expanded footer demonstration.
- `style.css` — responsive footer styling.
- `README.md` — usage and accessibility documentation.

## Browser Support

The component targets current evergreen browsers.
It relies on standard semantic HTML, CSS layout, and CSS transitions.
The navigation remains useful even when decorative effects are unavailable.

## Testing Checklist

- Verify every footer link is reachable with the keyboard.
- Confirm focus styling is visible without using the mouse.
- Resize the viewport and inspect navigation wrapping.
- Check link contrast against the footer background.
- Test the footer with reduced-motion enabled.
- Confirm long labels do not create unwanted horizontal scrolling.

## Reuse

Copy the component structure into a page and replace the example content.
Keep semantic grouping intact when adapting the navigation categories.
Follow repository contribution and licensing conventions when reusing the example.
