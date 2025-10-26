# Painter's Studio — Landing + Gallery

A lightweight, CSS-driven painter blog landing page with a 3D featured gallery, posts preview, artist about section, newsletter form, and an artwork detail page.

## Features
- Pure CSS 3D rotating gallery (hidden on small screens for UX)
- Responsive layout for gallery and posts (3 → 2 → 1 columns)
- Artist About section with portrait, slogan note, and social links
- Detail page (`detail.html`) showing an artwork via URL params
- Accessible motion preference: stops auto-rotation when `prefers-reduced-motion: reduce` is set

## Project structure
- `index.html` — Main landing page
- `detail.html` — Artwork detail (reads `img`, `title`, optional `desc`, `meta` from URL)
- `style.css` — All styles and responsive rules
- `images/` — Artwork, background, and model images

## Quick start
1. Open `index.html` directly in a browser.
2. Replace example images under `images/` with your own assets.
3. Click any image in the 3D slider or Gallery grid to open `detail.html`.

## Customization
- Title/brand: Edit in `index.html` header.
- Artist name and bio: In the hero author block and About section.
- Slogan label text: Edit `.about .slogan::before` content in `style.css`.
- Social links: Update `href` and labels in the About section.
- Gallery items: Add/remove `<figure class="gallery-item">` in the Gallery section.
- Posts: Update cards in the Latest Posts section.

## Detail page links
Link format:
```
detail.html?img=images/dragon_4.jpg&title=Autumn%20Study&desc=Oil%20on%20canvas&meta=Oil%20on%20canvas%20·%2040x60cm
```
Params:
- `img` (required) — image path
- `title` (optional)
- `desc` (optional)
- `meta` (optional)

## Assets
Expected images (replace with your own):
- Background: `images/bg.png`
- Model: `images/model.png` (also used in About as portrait by default)
- Slider/Gallery: `images/dragon_1.jpg` … `images/dragon_10.jpg`

## Responsive behavior
- Header nav hidden ≤ 640px (add a hamburger if needed)
- 3D slider hidden ≤ 640px to reduce clutter; hero text shown first, model below
- Grids adapt to screen width; forms stack on small screens

## Accessibility
- Honours `prefers-reduced-motion`
- Add meaningful `alt` text to your images for better screen reader support

## Notes
- No build step required. Pure HTML/CSS with a tiny inline script for year and detail params.
- If using version control on Windows, Git may normalize line endings (CRLF/LF) — this is expected.

## License
MIT. Replace or include your own license if needed.
