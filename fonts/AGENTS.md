<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-02-17 | Updated: 2026-02-17 -->

# fonts

## Purpose

Contains Font Awesome icon font files in multiple formats for cross-browser compatibility. Provides brands, regular, and solid icon weights.

## Key Files

| File | Description |
|------|-------------|
| `fa-brands-400.*` | Font Awesome Brands icons (eot, svg, ttf, woff, woff2) |
| `fa-regular-400.*` | Font Awesome Regular icons (eot, svg, ttf, woff, woff2) |
| `fa-solid-900.*` | Font Awesome Solid icons (eot, svg, ttf, woff, woff2) |
| `.gitkeep` | Placeholder to maintain directory in git |

## For AI Agents

### Working In This Directory

- **Do not modify these files** - they are binary font assets
- Multiple formats ensure **cross-browser compatibility**:
  - `.woff2` / `.woff` - Modern browsers (preferred)
  - `.ttf` - Fallback for older browsers
  - `.eot` - Internet Explorer support
  - `.svg` - Legacy iOS/Safari support
- All three weights (400: regular/brands, 900: solid) are loaded

### Testing Requirements

- Icons should display correctly across browsers
- Check icon rendering at different sizes
- Verify no console errors related to font loading

### Common Patterns

- Font icons are referenced via CSS classes (e.g., `fa-solid fa-user`)
- Font loading is handled by CSS `@font-face` rules (likely in css files)
- Icons scale with `font-size` CSS property

## Dependencies

### External

- **Font Awesome Free** - Open source icon font

### Internal

- Loaded by CSS in `css/` directory
- Used throughout `index.html` for UI icons

<!-- MANUAL: -->
