# SherryBlossoms
# Sherry Blossoms — Website Project

**Sherry Blossoms** — responsive static website for fragrances, keychains and lifestyle gifts.  
This repository contains a production‑ready static site (HTML, CSS, JavaScript) with a responsive Collections grid, multi‑image product quick view, accessible markup, and performance best practices.

---

## Table of contents

- [Overview](#overview)  
- [Features](#features)  
- [File structure](#file-structure)  
- [Quick start](#quick-start)  
- [Development workflow](#development-workflow)  
- [Adding images & products](#adding-images--products)  
- [Performance recommendations](#performance-recommendations)  
- [Accessibility & SEO](#accessibility--seo)  
- [Deployment](#deployment)  
- [Troubleshooting](#troubleshooting)  
- [Credits & license](#credits--license)  
- [Contact](#contact)

---

## Overview

This project is a clean, brand‑forward static website template for **Sherry Blossoms**. It uses:

- Semantic HTML and ARIA attributes for accessibility  
- Responsive CSS grid and breakpoints for phones, tablets, and desktops  
- Vanilla JavaScript to render product data, filters, search, and a quick‑view modal with thumbnails  
- Lazy loading and `srcset` support for faster image delivery  
- A small, maintainable codebase (three main files: `index.html`, `style.css`, `script.js`)

---

## Features

- **Collections grid** with product cards and price badges  
- **Multiple images per product** (thumbnail strip + main image in modal)  
- **Filters** (category, price) and **search**  
- **Responsive layout**: 3 columns desktop → 2 columns tablet → 1 column mobile  
- **Accessible modal**: keyboard focus trap, Escape to close, ARIA attributes  
- **Footer credit** with animated glow and hover effects linking to GKroon (Pty) Ltd  
- **Performance**: lazy loading, optional `srcset` for responsive images

---

## File structure

project-root/ ├─ index.html          # Main site (Home, Collections, About, Contact) ├─ style.css           # All styles and responsive rules ├─ script.js           # Product data, rendering, filters, modal logic ├─ README.md           # This file └─ assets/ ├─ logo.png ├─ about-studio-800.jpg ├─ fragrances/ │  ├─ fragrance-1-400.jpg │  ├─ fragrance-1-800.jpg │  ├─ fragrance-1-1200.jpg │  └─ ... (fragrance images) └─ keychains/ ├─ kc01-400.jpg ├─ kc01-800.jpg ├─ kc01-1200.jpg ├─ kc02-800.jpg └─ ... (all keychain images)


> **Note:** Filenames above are examples. Keep a consistent naming convention (e.g., `name-400.jpg`, `name-800.jpg`, `name-1200.jpg`) to enable `srcset` generation and optimal image selection by browsers.

---

## Quick start

1. **Copy files** into a project folder (or clone the repo if available).

2. **Open locally (quick)**  
   Open `index.html` directly in your browser for a quick preview.

3. **Run a local static server (recommended)**  
   Use a simple static server to enable proper `fetch` behavior and consistent paths:

   ```bash
   # using npx http-server (no install required)
   npx http-server . -p 5500
   # open http://localhost:5500  

4. Optional Node static server
If you have `server.js` and `package.json` (provided earlier), install dependencies and run:
`npm install`
`npm start`

## Development workflow
- Edit products: update the PRODUCTS array in script.js. Each product object should include:
- id (unique string)
- title (string)
- price (string, e.g., "R50")
- priceValue (number, e.g., 50) — used for filtering/sorting
- category (string, e.g., "keychains")
- short (short description)
- long (detailed description)
- images (array of image paths, ordered: thumbnail/medium/large)
- Add images: place images in assets/keychains/ and assets/fragrances/. Use consistent naming to enable srcset.
- Style changes: edit style.css. Colors and fonts are controlled by CSS variables in :root.
- Test responsiveness: use Chrome DevTools device toolbar and test on real devices.  

1. Adding images & products (13 keychains + 3 fragrances example)
- Organize images:
assets/keychains/
  kc01-400.jpg
  kc01-800.jpg
  kc01-1200.jpg
  kc02-400.jpg
  kc02-800.jpg
  ...
assets/fragrances/
  fragrance-1-400.jpg
  fragrance-1-800.jpg
  fragrance-1-1200.jpg
  fragrance-2-800.jpg
  ...

Responsive images: provide -400, -800, -1200 variants for each product image.

Style changes: edit style.css (colors, fonts, layout).

Test responsiveness: use Chrome DevTools device toolbar and real devices.  

## 📸 Adding Products
Each product entry in script.js should include:  
```
{
  id: 'kc01',
  title: 'Name Keychain — Rose',
  price: 'R50',
  priceValue: 50,
  category: 'keychains',
  short: 'Custom name keychain with glitter edge.',
  long: 'Handmade acrylic name keychain with rose-gold clasp.',
  images: [
    'assets/keychains/kc01-400.jpg',
    'assets/keychains/kc01-800.jpg',
    'assets/keychains/kc01-1200.jpg'
  ]
}
```

## ⚡ Performance Recommendations
Generate resized images (400px, 800px, 1200px) for each product.

Compress images (JPEG/WebP) for faster load times.

Use lazy loading (loading="lazy") — already enabled.

Serve assets via CDN for production.

Enable gzip/Brotli compression on your server.


## ♿ Accessibility & SEO
Semantic HTML (header, main, section, footer)

ARIA attributes for navigation, modal, and dynamic content

Keyboard support: Escape closes modal, Tab focus trap

Meaningful alt text for all images

Meta tags (description, keywords, author) included

## 🌍 Deployment
Static hosting: GitHub Pages, Netlify, Vercel, or any static host.

Recommended: push to GitHub and connect to Netlify/Vercel for CI/CD.

Configure caching headers and compression for performance.  

## 🐞 Troubleshooting
Logo not showing: confirm assets/logo.png exists and path is correct.

Image 404s: check filenames in script.js match actual files.

Server errors: run node server.js directly; install dependencies with npm install.

Port in use: change port or kill the process using it.  

## 👨‍💻 Credits & License
Design & Development: GKroon (Pty) Ltd  
Author/Developer: Jonathan Peters
License: MIT (recommended). Add a LICENSE file if publishing.  

## 📬 Contact
Sherry Blossoms — update contact details in footer (index.html)

Developer: GKroon (Pty) Ltd — link in footer credit







