# Responsive Tab Bar — SaaS Modern

## Overview

Issue #79679 demonstrates a responsive tab bar designed for a clean SaaS dashboard interface.

## Features

- Responsive horizontal tab navigation
- Native accessible links
- Clear active and hover states
- Visible keyboard focus
- Compact mobile behavior
- Reduced-motion support
- Pure HTML and vanilla CSS

## Structure

The navigation uses native links inside a labelled `nav` landmark. The active tab is identified with `aria-current="page"`, while the supporting dashboard content demonstrates how the navigation can sit inside a larger product surface.

## Responsive behavior

On wide screens the tabs share the available width. On narrow screens they remain horizontally usable without forcing the page to overflow, preserving comfortable touch targets.

## Accessibility

The component does not depend on JavaScript for basic navigation. Focus-visible outlines make keyboard interaction clear, and the active page is exposed semantically.

## Motion

Small transitions provide visual feedback, while `prefers-reduced-motion: reduce` removes non-essential movement.

## Usage

Open `demo.html` directly in a browser. Copy the `.tabs` and `.tab` structure into a dashboard and replace the example links with application routes.

## Files

- `demo.html` — self-contained responsive example
- `style.css` — tab styling, layout, responsive rules, and motion handling
- `README.md` — implementation documentation

## Issue

EaseMotion CSS issue #79679.
