<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-02-17 | Updated: 2026-02-17 -->

# css

## Purpose

Contains theme stylesheets for the AdminKit template. Two complete theme variations are provided for light and dark modes.

## Key Files

| File | Description |
|------|-------------|
| `light.css` | Light theme stylesheet - default bright color scheme |
| `dark.css` | Dark theme stylesheet - alternative dark color scheme |

## For AI Agents

### Working In This Directory

- **Only one CSS file should be linked at a time** in the HTML
- Both files contain **complete, independent styles** - they are not modular
- When adding new styles, **add to both files** to maintain theme consistency
- CSS variables are likely used for theme colors and can be modified

### Testing Requirements

- After modifying styles, verify in browser with both themes
- Check responsive breakpoints (mobile, tablet, desktop)
- Ensure no visual regressions in existing components

### Common Patterns

- Bootstrap 5 class names and component styles
- Custom CSS variables (likely `--primary`, `--secondary`, etc.)
- Sidebar-specific styles for navigation
- Card, table, and form component styling

## Dependencies

### External

- **Bootstrap 5** - Base framework styles (likely included or compiled in)

### Internal

- Referenced by `index.html` via `<link>` tag
- Theme switching handled by `js/settings.js`

<!-- MANUAL: -->
