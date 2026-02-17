<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-02-17 | Updated: 2026-02-17 -->

# avatars

## Purpose

Contains user avatar images for profile displays, user lists, and chat interfaces. These placeholder images demonstrate the user avatar functionality in the AdminKit template.

## Key Files

| File | Description |
|------|-------------|
| `avatar.jpg` | Default user avatar image |
| `avatar-2.jpg` through `avatar-5.jpg` | Additional user avatar images for demos |

## For AI Agents

### Working In This Directory

- Images are **JPG format** for web optimization
- Used for **demo purposes** - replace with real user avatars in production
- Consistent sizing likely applied via CSS classes
- When adding new avatars, follow the naming pattern: `avatar-{n}.jpg`

### Testing Requirements

- Verify avatars display correctly in user profile sections
- Check avatar rendering in table rows and cards
- Ensure consistent sizing across the UI

### Common Patterns

- Referenced as: `img/avatars/avatar.jpg`
- May be used with CSS classes for circular cropping
- Multiple avatars shown in user lists and team sections

## Dependencies

### Internal

- Referenced by `index.html` for demo content
- Styled by CSS in `css/` directory

<!-- MANUAL: -->
