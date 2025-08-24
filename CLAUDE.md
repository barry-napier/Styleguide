# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Tailwind CSS 4 styleguide project that provides a comprehensive component library with semantic naming conventions. The project uses Vite as the build tool and includes custom fonts (Proxima Nova) with various pre-built UI components.

## Development Commands

```bash
# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview

# Format code with Prettier
npx prettier --write .
```

## Architecture

### File Structure
- **app.css**: Main entry point that imports all stylesheets
- **theme.css**: Custom color palette and theme variables
- **base.css**: Base HTML element styles (typography, headings, etc.)
- **components.css**: Component class definitions using semantic naming
- **fonts.css**: Custom Proxima Nova font definitions
- **layouts/**: Example application layouts (dashboard, forms, kanban, landing)

### Component Naming Convention

The project follows a semantic naming pattern:

1. **Base Components**: `.component` (e.g., `.btn`, `.card`, `.badge`)
2. **Modifiers**: `.component-modifier`
   - Intent: `.btn-primary`, `.alert-success`
   - Size: `.btn-sm`, `.btn-lg`
   - State: `.btn-disabled`, `.input-error`
3. **Sub-components**: `.component-subpart` (e.g., `.card-header`, `.modal-content`)
4. **Combinations**: `.component-subpart-modifier`

### Technology Stack
- **Tailwind CSS 4**: Using `@tailwindcss/vite` plugin with the new CSS-first config approach
- **Vite**: Build tool and dev server
- **Prettier**: Code formatting with Tailwind CSS plugin for class sorting

### Key Design Patterns

1. **Custom Color Palette**: Defined in `theme.css` using CSS custom properties within `@theme` directive
2. **Component Layers**: Components defined in `@layer components` for proper Tailwind integration
3. **Responsive Design**: Mobile-first approach with responsive utilities
4. **Interactive States**: Hover, focus, active, and disabled states for all interactive components

### Component Categories

The styleguide includes these component types:
- Typography (headings, body text, code blocks)
- Buttons (primary, secondary, tertiary, destructive)
- Cards (with header, content, footer sections)
- Forms (inputs, selects, checkboxes, radios, switches)
- Feedback (alerts, badges, progress bars)
- Navigation (tabs, breadcrumbs, dropdowns)
- Overlays (modals, dialogs, tooltips)
- Layout (accordions, collapsibles, separators)
- Loading (spinners, skeleton loaders)
- Data Display (tables, chips/tags)