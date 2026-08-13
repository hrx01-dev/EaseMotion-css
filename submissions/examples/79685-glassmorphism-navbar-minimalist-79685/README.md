# Glassmorphism Navbar — Issue #79685

A responsive glassmorphism navigation bar built as a self-contained EaseMotion CSS example.

## ✨ Features

- Frosted-glass navigation surface using `backdrop-filter`.
- Responsive layout for desktop, tablet, and mobile screens.
- Clear active, hover, and keyboard-focus states.
- Semantic navigation markup with accessible links.
- Lightweight implementation with no JavaScript dependency.
- Reduced-motion support through `prefers-reduced-motion`.

## 📁 Files

- `style.css` — Expanded, readable component styles with consistent spacing.
- `demo.html` — Complete interactive demonstration and usage example.

## 🚀 Usage

Open `demo.html` directly in a modern browser. The page demonstrates the navigation structure, glass surface, active link treatment, CTA button, responsive behavior, and supporting content cards.

The component can also be copied into an existing EaseMotion CSS project. Keep the navigation markup and the selectors in `style.css` together so the example remains self-contained.

## 🎨 Design Details

The navigation uses a translucent surface, subtle border, blur, saturation, rounded corners, and layered shadows to create the glass effect. The layout uses CSS Grid on larger screens and collapses into a two-row navigation on smaller screens.

The stylesheet is intentionally expanded rather than minified so contributors can easily review, understand, and modify each rule.

## ♿ Accessibility

Interactive elements include visible `:focus-visible` states. The layout remains usable on narrow screens, and non-essential transitions are disabled when the user requests reduced motion through their operating-system preference.

## 🌐 Browser Notes

The example targets modern browsers supporting CSS custom properties, Grid, transitions, and `backdrop-filter`. The `-webkit-backdrop-filter` declaration is included for WebKit-based browsers.

## 🧩 Related Issue

This example implements **Issue #79685 — Glassmorphism Navbar / Minimalist Navigation**.

## 📄 License

This submission follows the licensing terms of the EaseMotion CSS repository.
