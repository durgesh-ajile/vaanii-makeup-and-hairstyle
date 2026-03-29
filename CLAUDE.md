# Vaanii Makeup and Hairstyle — Claude Guide

## Project Overview
Single-page React portfolio website for Shivani (Vaanii Makeup and Hairstyle), a bridal makeup artist in Jabalpur, India. Deployed on Vercel at `vaanii-makeup-and-hairstyle.vercel.app`.

## Tech Stack
- React 19, Create React App (react-scripts 5)
- No external UI libraries
- Google Fonts: Cormorant Garamond + Montserrat

## Structure
- `src/App.js` — entire app in one large component; all sections, data, and styles are here
- `src/App.css` — minimal CSS (only the `#about` grid layout and its mobile override)
- `public/` — all portfolio images as `.jpeg` files, plus `index.html` and `robots.txt`

## Design System
- Background: `#0a0806` (near-black)
- Gold accent: `#c9a84c`
- Text: `#f5ede0` (cream)
- CSS classes are defined in an inline `<style>` block inside `App.js` (not in a separate stylesheet)
- Breakpoint: 768px (mobile vs desktop)

## Image Naming Conventions
Images live in `public/` and are referenced as `./filename.jpeg`:
- `bride1.jpeg` – `bride12.jpeg` — bridal makeup
- `hair 1.jpeg`, `hair2.jpeg` – `hair10.jpeg` — hairstyling (note the space in `hair 1.jpeg`)
- `eng1.jpeg` – `eng7.jpeg` — engagement
- `sider1.jpeg` – `sider19.jpeg` — party/sangeet/reception (sider17 is missing)
- `pre1.jpeg` – `pre5.jpeg` — pre-wedding shoots
- `mehendi.jpeg`, `mehendi2.jpeg` – `mehendi5.jpeg` — mehendi looks

## Key Data Arrays (in App.js)
- `NAV_LINKS` — navigation items
- `SERVICES` — 6 service cards
- `TESTIMONIALS` — 5 client reviews
- `BRANDS` — brand names displayed as tags
- `GALLERY_ITEMS` — all gallery entries with `src`, `label`, and `tag` fields

## Commands
```bash
npm start    # dev server
npm run build  # production build
```

## Notes
- Gallery is filterable by tag: All, Bridal, Hairstyling, Party, Engagement, Shoots, Mehendi
- Scroll animations use IntersectionObserver to add `visible` class to `.fade-up` elements
- Nav highlights active section on scroll
