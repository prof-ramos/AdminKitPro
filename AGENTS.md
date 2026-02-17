<!-- Generated: 2026-02-17 | Updated: 2026-02-17 -->

# AdminKitPro

## Purpose

AdminKitPro is a responsive Admin & Dashboard Template based on Bootstrap 5. It provides a complete front-end foundation for building admin panels, dashboards, and management interfaces with support for multiple themes (light/dark), sidebar configurations, and various UI components.

## Key Files

| File | Description |
|------|-------------|
| `index.html` | Main dashboard entry point with sidebar navigation and content layout |
| `index.html` | Core HTML structure demonstrating the template layout and components |

## Subdirectories

| Directory | Purpose |
|-----------|---------|
| `css/` | Stylesheets for theme variations (see `css/AGENTS.md`) |
| `js/` | JavaScript modules for interactivity and components (see `js/AGENTS.md`) |
| `fonts/` | Font Awesome icon fonts (see `fonts/AGENTS.md`) |
| `img/` | Static image assets organized by type (see `img/AGENTS.md`) |
| `.claude/` | Claude Code configuration |
| `.omc/` | Oh-my-claudecode state and configuration |

## For AI Agents

### Working In This Directory

- This is a **static HTML/CSS/JS template** - no build process required
- The template uses **Bootstrap 5** as the primary CSS framework
- **Theme switching** is handled via CSS file selection (light.css/dark.css)
- The project includes a **settings.js** script for demo theme switching

### Testing Requirements

- Open `index.html` directly in a browser for visual verification
- Test theme switching functionality if modifying settings-related code
- Verify responsive behavior at different viewport sizes

### Common Patterns

- HTML uses **data attributes** for configuration: `data-theme`, `data-layout`, `data-sidebar-position`, `data-sidebar-layout`
- CSS theme files are mutually exclusive - only one should be linked at a time
- Font Awesome icons are used throughout the UI
- Google Fonts (Inter) are loaded for typography

## Dependencies

### External

- **Bootstrap 5** - Front-end framework for components and layout
- **Font Awesome** - Icon library (brands, regular, solid weights)
- **Google Fonts (Inter)** - Primary typeface
- **SimpleBar** - Custom scrollbar for sidebar
- **Datatables** - Table enhancement plugin (via js/datatables.js)
- **FullCalendar** - Calendar component (via js/fullcalendar.js)

### Internal Dependencies

- `css/light.css` or `css/dark.css` → Required by `index.html`
- `js/app.js` → Main application JavaScript
- `js/settings.js` → Theme switcher functionality
- `img/` → Static assets referenced in HTML

## Technology Stack

- **HTML5** - Markup structure
- **CSS3** - Styling with custom themes
- **Vanilla JavaScript** - No framework dependencies
- **Bootstrap 5** - UI component framework

<!-- MANUAL: Custom project notes can be added below -->
