<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-02-17 | Updated: 2026-02-17 -->

# flags

## Purpose

Contains country flag images (PNG format) for displaying user locations, language selection, or region-specific content. Flags use ISO 3166-1 alpha-2 country codes for file naming.

## Key Files

| File | Description |
|------|-------------|
| `*.png` | Country flag images named by ISO code (e.g., `us.png`, `br.png`, `gb.png`) |

## For AI Agents

### Working In This Directory

- **Do not modify** flag images - they are standardized assets
- File naming follows **ISO 3166-1 alpha-2** country codes
- Contains flags for most UN member countries
- Images are **PNG format** with transparency support
- Total: 200+ country flag files

### Testing Requirements

- Verify flags display correctly when referenced
- Check flag rendering at different sizes
- Ensure proper aspect ratios are maintained

### Common Patterns

- Referenced by country code: `img/flags/us.png` for United States
- Often used in dropdowns or user profile cards
- May be combined with country name display

## Dependencies

### Internal

- Referenced by `index.html` for demo language/region selectors
- Styled by CSS in `css/` directory

### External

- ISO 3166-1 alpha-2 country code standard

<!-- MANUAL: -->
