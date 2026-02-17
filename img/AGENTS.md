<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-02-17 | Updated: 2026-02-17 -->

# img

## Purpose

Contains all static image assets organized by type: avatars for user profiles, flags for country indicators, icons for branding, and photos for content/demos.

## Key Files

No files directly in this directory - all assets are in subdirectories.

## Subdirectories

| Directory | Purpose |
|-----------|---------|
| `avatars/` | User avatar images for profile displays (see `avatars/AGENTS.md`) |
| `flags/` | Country flag images for localization/region display (see `flags/AGENTS.md`) |
| `icons/` | Brand icons and app icons (see `icons/AGENTS.md`) |
| `photos/` | Stock photos for demo content (see `photos/AGENTS.md`) |

## For AI Agents

### Working In This Directory

- **Only reference images that exist** - check subdirectories before adding image paths
- When adding new images, organize them into the appropriate subdirectory
- Image formats: primarily JPG (avatars, photos), PNG (icons), PNG (flags)
- Keep image sizes optimized for web performance

### Testing Requirements

- Verify all images load correctly in the browser
- Check for broken image links
- Ensure images display properly at different viewport sizes

### Common Patterns

- Images referenced via relative paths: `img/avatars/avatar.jpg`
- Consistent naming convention: `avatar-{n}.jpg`, `brand-{n}.svg`
- Flag images use ISO country codes: `us.png`, `br.png`, etc.

## Dependencies

### Internal

- Referenced by `index.html` and CSS files
- May be used by JavaScript for dynamic content

<!-- MANUAL: -->
