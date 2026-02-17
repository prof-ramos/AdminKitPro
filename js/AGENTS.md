<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-02-17 | Updated: 2026-02-17 -->

# js

## Purpose

Contains JavaScript modules for interactivity, UI components, and third-party library integrations. Includes main application logic, data tables, calendar functionality, and theme settings.

## Key Files

| File | Description |
|------|-------------|
| `app.js` | Main application JavaScript - core functionality and initialization |
| `settings.js` | Theme switcher and settings panel functionality |
| `datatables.js` | DataTables library for enhanced table features |
| `fullcalendar.js` | FullCalendar library for calendar views |
| `*.map` | Source maps for debugging (auto-generated) |
| `*.LICENSE.txt` | License files for bundled libraries |

## For AI Agents

### Working In This Directory

- These are **bundled/minified files** - source code is not included
- When modifying functionality:
  - Edit the original source files if available
  - Or create new separate JS files and link them in HTML
- Source maps (`.map` files) enable browser debugging
- **Do not manually edit** minified files unless necessary

### Testing Requirements

- Test all interactive features after modifications
- Check browser console for JavaScript errors
- Verify third-party integrations (tables, calendar) work correctly
- Test across different browsers if possible

### Common Patterns

- Vanilla JavaScript (no framework)
- DOM manipulation for UI updates
- Event listeners for user interactions
- localStorage likely used for theme persistence

## Dependencies

### External Libraries Bundled

- **DataTables** - jQuery plugin for advanced table features
- **FullCalendar** - Calendar/event display component

### Internal

- `css/` - Styles that JavaScript may toggle or modify
- `index.html` - HTML elements that scripts interact with

### Browser APIs

- localStorage - For saving user preferences
- DOM API - Element manipulation and event handling

<!-- MANUAL: -->
