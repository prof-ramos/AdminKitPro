<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-02-17 | Updated: 2026-02-17 -->

# icons

## Purpose

Contains brand icons and application icons for the AdminKit template. Includes both SVG brand logos and the main application favicon/icon.

## Key Files

| File | Description |
|------|-------------|
| `icon-48x48.png` | Main application icon (favicon, 48x48 pixels) |
| `brand-1.svg` through `brand-5.svg` | Brand/partner logo placeholders for demo content |

## For AI Agents

### Working In This Directory

- **icon-48x48.png** is the main favicon - referenced in `index.html`
- **brand-*.svg** files are **SVG format** for scalability
- Brand icons are demo placeholders - replace with actual partner/client logos
- SVG files can be edited directly as text if needed

### Testing Requirements

- Verify favicon displays in browser tab
- Check brand icons render correctly in footer/partner sections
- Ensure SVG icons scale properly at different sizes

### Common Patterns

- Favicon linked in HTML `<head>`: `<link rel="shortcut icon" href="img/icons/icon-48x48.png" />`
- Brand icons displayed in footer or "trusted by" sections
- SVG icons allow for easy color customization via CSS

## Dependencies

### Internal

- `icon-48x48.png` referenced in `index.html` `<head>`
- Brand icons used in layout footer or demo sections

<!-- MANUAL: -->
