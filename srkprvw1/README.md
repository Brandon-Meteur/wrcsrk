# WRC Safari Rally Kenya — Photography Portfolio

A static photography portfolio site for the WRC Safari Rally Kenya, designed for GitHub Pages hosting.

## Site Structure

```
/
├── index.html          ← Homepage with fullscreen hero
├── gallery/
│   ├── 2024.html       ← 2024 gallery (masonry + lightbox)
│   ├── 2025.html       ← 2025 gallery
│   └── 2026.html       ← 2026 gallery
└── README.md
```

## Deploying to GitHub Pages

1. Create a new GitHub repository (e.g. `wrc-safari-portfolio`)
2. Push all files to the `main` branch
3. Go to **Settings → Pages**
4. Under *Source*, select **Deploy from a branch**
5. Choose `main` branch, `/ (root)` folder → click **Save**
6. Your site will be live at: `https://yourusername.github.io/wrc-safari-portfolio/`

## Adding Your Photos

Replace the placeholder Unsplash URLs in each gallery HTML file with your own images.

### Option A — GitHub-hosted images
Upload your photos to a `/images/2024/`, `/images/2025/`, `/images/2026/` folder and update the `src` attributes:
```html
<img src="../images/2026/photo-001.jpg" alt="..." loading="lazy" />
```

### Option B — External CDN (recommended for large galleries)
Use Cloudinary, Imgix, or Bunny.net for optimised delivery. Replace `src` with your CDN URLs.

### Photo Guidelines
- **Format**: JPEG or WebP
- **Resolution**: 1200–2400px wide for gallery; 1920px+ for hero
- **Naming**: `YYYY-rally-NNN.jpg` (e.g. `2026-safari-001.jpg`)
- Each gallery page supports **any number** of photos — just add more `.masonry-item` blocks

## Customisation

| What | Where |
|------|-------|
| Logo text | `nav-logo` and `footer-logo` divs |
| Social links | `nav-social` and `footer-social` — update `href="#"` |
| Email | `mailto:hello@wrcsafarike.com` → your address |
| Hero background | `.hero-bg` background-image URL in `index.html` |
| Colour scheme | CSS variables in `:root` (`--dust`, `--black`, etc.) |

## Security Features
- `X-Content-Type-Options: nosniff`
- `X-Frame-Options: DENY`
- `Referrer-Policy: no-referrer`
- Right-click / context menu disabled on all images
- `draggable="false"` on all images
- `-webkit-user-drag: none` preventing drag-save
- No external JS dependencies (zero attack surface)
- All links use `rel="noopener noreferrer"`

## License
All photography © [Your Name]. All Rights Reserved.
