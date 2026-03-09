# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Promotional landing page for a documentary about Mike Smith (legendary jockey). Pure static HTML/CSS/JS — no build tools, no dependencies, no package manager.

## Development

Open `index.html` directly in a browser, or use any static file server:

```bash
python3 -m http.server 8000
# or
npx serve .
```

No build step, no compilation.

## Architecture

Everything lives in a single file: **`index.html`** (~1065 lines). CSS and JavaScript are inline. Images are in `bmm-images/`.

### Page Sections (anchor navigation)
- `#trailer` — video placeholder
- `#story` — documentary narrative
- `#gallery` — image grid with lightbox modal
- `#updates` — Mailchimp email signup

### CSS Design System
Custom properties defined at `:root`:
- `--deep-teal: #003A40`, `--hot-pink: #FF2D8D`, `--soft-teal: #7FE9F2`
- `--near-black: #0B0F12`, `--off-white: #F5F7FA`, `--gradient-teal: #00B7C6`

Fonts: Bebas Neue (headings), Playfair Display (accents), Archivo (body) — loaded from Google Fonts.

### JavaScript Features
- Random tagline rotation on page load
- Hamburger menu toggle for mobile (<768px breakpoint)
- Image lightbox with keyboard navigation (arrow keys, Escape)
- Smooth scroll for anchor links
- Mailchimp form submission with success state
