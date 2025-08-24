# Tailwind CSS 4 Component Styleguide

A comprehensive, production-ready component library and design system built with Tailwind CSS 4.0, featuring semantic naming conventions, custom typography with Proxima Nova fonts, and a complete set of reusable UI components.

![License](https://img.shields.io/badge/license-ISC-blue.svg)
![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-4.0-38B2AC?logo=tailwind-css)
![Vite](https://img.shields.io/badge/Vite-6.3-646CFF?logo=vite)

## 🎯 Overview

This styleguide provides a modern, accessible, and highly customizable design system that serves as the foundation for building consistent user interfaces. Built with the latest Tailwind CSS 4 architecture, it offers improved performance, better developer experience, and a semantic component naming system that makes development intuitive and maintainable.

### Key Features

- **🎨 100+ Pre-built Components** - Comprehensive collection of UI components ready for production use
- **📱 Fully Responsive** - Mobile-first design approach with responsive utilities
- **🎭 Semantic Naming Convention** - Intuitive class names following BEM-like patterns
- **🚀 Tailwind CSS 4.0** - Latest version with CSS-first configuration approach
- **⚡ Vite-Powered** - Lightning-fast development with HMR and optimized builds
- **🔤 Custom Typography** - Professional Proxima Nova font family with 7 weights plus italic
- **🎨 Custom Color Palette** - Extended color system with light-blue accent colors
- **📦 Minimal Dependencies** - Only Tailwind CSS 4 and Vite required for production
- **♿ Accessibility First** - Components with ARIA attributes and keyboard navigation support
- **🔧 Developer Friendly** - Hot reload, Prettier integration, and comprehensive documentation

## 📋 Table of Contents

- [Installation](#-installation)
- [Quick Start](#-quick-start)
- [Project Structure](#-project-structure)
- [Component Library](#-component-library)
- [Design System](#-design-system)
- [Development Workflow](#-development-workflow)
- [Configuration](#-configuration)
- [Example Layouts](#-example-layouts)
- [Best Practices](#-best-practices)
- [Browser Support](#-browser-support)
- [Contributing](#-contributing)
- [License](#-license)

## 🚀 Installation

### Prerequisites

- Node.js 18+ and npm 9+
- Git

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/barry-napier/Styleguide.git
   cd Styleguide
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start development server**
   ```bash
   npm run dev
   ```

4. **Open in browser**
   ```
   http://localhost:5173 (port may vary if already in use)
   ```

## ⚡ Quick Start

### Basic HTML Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My App</title>
    <link rel="stylesheet" href="/app.css">
</head>
<body>
    <!-- Your content here -->
    <button class="btn btn-primary">
        <span class="btn-text">Get Started</span>
    </button>
</body>
</html>
```

### Import in React/Next.js

```javascript
// In your main App.js or _app.js
import './app.css'

function MyApp() {
  return (
    <button className="btn btn-primary">
      <span className="btn-text">Get Started</span>
    </button>
  )
}
```

### Import in Angular

```typescript
// In angular.json
"styles": [
  "src/styles.css",
  "node_modules/@your-package/styleguide/app.css"
]
```

## 📁 Project Structure

```
Styleguide/
├── app.css                 # Main entry point (currently imports theme.css only)
├── theme.css              # Unified theme with ALL styles in one file
├── base.css               # Base HTML element styles (modular approach)
├── components.css         # Component-specific styles (modular approach)
├── fonts.css              # Font-face declarations (modular approach)
├── index.html             # Complete component showcase
├── vite.config.js         # Vite configuration
├── package.json           # Project dependencies and scripts
├── CLAUDE.md              # AI assistant instructions
├── fonts/                 # Proxima Nova font files
│   ├── proxima_nova_thin-webfont.woff
│   ├── proxima_nova_light-webfont.woff
│   ├── proxima_nova_reg-webfont.woff
│   ├── proxima_nova_sbold-webfont.woff
│   ├── proxima_nova_bold-webfont.woff
│   ├── proxima_nova_bold_it-webfont.woff
│   ├── proxima_nova_xbold-webfont.woff
│   └── proxima_nova_black-webfont.woff
├── layouts/               # Example application layouts
│   ├── dashboard.html     # Admin dashboard layout
│   ├── form-layout.html   # Form-heavy application layout
│   ├── kanban.html        # Kanban board layout
│   └── landing.html       # Marketing landing page
└── dist/                  # Production build output
```

> **Note:** The project includes both modular CSS files and a unified `theme.css`. Currently, `app.css` imports only `theme.css` which contains all styles (fonts, base, components) in one file. The modular files (base.css, components.css, fonts.css) are available for a more granular approach if needed.

## 🎨 Component Library

### Component Categories

Our component library is organized into logical categories for easy discovery and use:

#### **Typography & Content**
- **Headings** - H1-H6 with consistent sizing and weight
- **Body Text** - Paragraphs with various sizes and weights
- **Links** - Standard, bold, no-underline, and external link variants
- **Lists** - Styled, numbered, disc, check, and arrow lists
- **Code Blocks** - Inline code and multi-line code blocks
- **Blockquotes** - Standard and primary styled quotes

#### **Buttons & Actions**
- **Button Variants** - Primary, Secondary, Tertiary, Destructive
- **Button Sizes** - Small (sm), Default, Large (lg)
- **Button States** - Default, Hover, Active, Focus, Disabled
- **Icon Buttons** - With leading/trailing icons or icon-only

#### **Forms & Inputs**
- **Text Inputs** - Default, error, success states with sizes
- **Select Dropdowns** - Custom styled with arrow indicator
- **Textareas** - Resizable with consistent styling
- **Checkboxes** - Custom styled with focus states
- **Radio Buttons** - Grouped with enhanced styling
- **Toggle Switches** - iOS-style toggle switches
- **Labels** - With optional required indicators
- **Form Groups** - Container patterns for form layouts

#### **Layout & Structure**
- **Cards** - Standard, compact, hover effects
- **Headers** - Application headers with navigation
- **Modals** - Dialog boxes with overlays
- **Accordions** - Collapsible content sections
- **Tabs** - Tabbed content navigation
- **Separators** - Horizontal and vertical dividers

#### **Feedback & Status**
- **Alerts** - Info, Success, Warning, Error, Destructive
- **Badges** - Various colors and sizes for status indicators
- **Progress Bars** - With color variants for different states
- **Spinners** - Loading indicators in multiple sizes
- **Skeleton Loaders** - Content placeholders while loading
- **Tooltips** - Contextual help in all directions

#### **Navigation**
- **Breadcrumbs** - Hierarchical navigation
- **Dropdowns** - Menu dropdowns with items
- **Tabs** - Content switching navigation

#### **Data Display**
- **Tables** - Responsive tables with hover states
- **Chips/Tags** - Removable tags for categorization
- **Avatars** - User avatars in various sizes with fallbacks

#### **Interactive**
- **Collapsibles** - Show/hide content sections
- **Dialogs** - Modal dialogs with checkbox hack
- **Tooltips** - Hover tooltips in all positions

### Component Naming Convention

Our semantic naming system follows these patterns:

```
Base Component:     .component
Modifiers:          .component-modifier
Sub-components:     .component-subpart
Combined:           .component-subpart-modifier
```

#### Examples:

```css
/* Base Components */
.btn                /* Button */
.card               /* Card container */
.alert              /* Alert box */

/* Modifiers (Intent) */
.btn-primary        /* Primary button */
.alert-success      /* Success alert */
.badge-warning      /* Warning badge */

/* Modifiers (Size) */
.btn-sm             /* Small button */
.input-lg           /* Large input */
.avatar-xl          /* Extra large avatar */

/* Modifiers (State) */
.btn-disabled       /* Disabled button */
.input-error        /* Error input */
.card-hover         /* Card with hover effect */

/* Sub-components */
.card-header        /* Card header section */
.card-body          /* Card body section */
.modal-content      /* Modal content area */

/* Combined */
.form-label-required /* Required form label */
.table-header-sorted /* Sorted table header */
```

## 🎨 Design System

### Color Palette

The design system includes a comprehensive color palette with custom light-blue accent colors:

#### Primary Colors
- **Light Blue** (Primary Accent)
  - `light-blue-50` to `light-blue-950`
  - Primary: `light-blue-700` (#0070a9)
  - Hover: `light-blue-800` (#075a83)

#### Semantic Colors
- **Success** - Green shades for positive feedback
- **Warning** - Orange/Yellow for cautions
- **Error/Danger** - Red shades for errors
- **Info** - Blue shades for information

#### Neutral Colors
- **Gray Scale** - Custom gray palette from 50-950
  - Background: `gray-100`
  - Text: `gray-900`
  - Borders: `gray-200`

### Typography System

#### Font Stack
```css
font-family: "Proxima Nova", system-ui, -apple-system, BlinkMacSystemFont, 
             "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
```

#### Font Weights
- **100** - Thin
- **300** - Light
- **400** - Regular
- **600** - Semibold
- **700** - Bold
- **700i** - Bold Italic
- **800** - Extra Bold
- **900** - Black

#### Type Scale
- **xs** - 0.75rem (12px)
- **sm** - 0.875rem (14px)
- **base** - 1rem (16px)
- **lg** - 1.125rem (18px)
- **xl** - 1.25rem (20px)
- **2xl** - 1.5rem (24px)
- **3xl** - 1.875rem (30px)
- **4xl** - 2.25rem (36px)

### Spacing System

Consistent spacing scale based on rem units:

- **xs** - 0.25rem (4px)
- **sm** - 0.5rem (8px)
- **md** - 1rem (16px)
- **lg** - 1.5rem (24px)
- **xl** - 2rem (32px)
- **2xl** - 3rem (48px)
- **3xl** - 4rem (64px)

### Shadow System

Custom shadow utilities with blue-tinted shadows:

```css
--shadow-sm: 0 1px 2px 0 rgba(101, 153, 202, 0.27);
--shadow-base: 0 3px 34px 0 rgba(110, 155, 198, 0.04);
--shadow-md: 5px 9px 17px 1px rgba(159, 192, 222, 0.22);
--shadow-lg: 7px 15px 24px -3px rgba(97, 141, 182, 0.11);
--shadow-xl: 0 20px 25px -5px rgba(220, 234, 243, 0.38);
--shadow-2xl: 0 25px 50px -12px rgba(103, 152, 199, 0.22);
```

## 💻 Development Workflow

### Available Scripts

```bash
# Start development server with hot reload
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview

# Format code with Prettier
npx prettier --write .
```

### Development Server Features

- **Hot Module Replacement (HMR)** - Instant updates without page refresh
- **Fast Refresh** - Preserve component state during edits
- **Error Overlay** - Clear error messages in browser
- **Source Maps** - Debug original source code

### Building for Production

```bash
npm run build
```

This creates an optimized build in the `dist/` directory with:
- Minified CSS
- Optimized assets
- Tree-shaken unused styles
- Production-ready output

## ⚙️ Configuration

### Vite Configuration

The project uses Vite with the Tailwind CSS plugin:

```javascript
// vite.config.js
import { defineConfig } from 'vite'
import tailwindcss from '@tailwindcss/vite'

export default defineConfig({
  plugins: [
    tailwindcss(),
  ],
})
```

### Tailwind CSS 4 Configuration

Tailwind CSS 4 uses a CSS-first configuration approach with the `@theme` directive:

```css
@theme {
  --color-light-blue-700: #0070a9;
  --font-family-sans: "Proxima Nova", system-ui, ...;
  --shadow-base: 0 3px 34px 0 rgba(110, 155, 198, 0.04);
}
```

### Prettier Configuration

The project includes Prettier with the Tailwind CSS plugin for consistent code formatting:

```bash
npx prettier --write .
```

Note: Tailwind CSS 4 uses CSS-based configuration, not a traditional config file.

## 📱 Example Layouts

The project includes four production-ready layout examples:

### 1. Dashboard Layout (`/layouts/dashboard.html`)
- Admin dashboard with sidebar navigation
- Stats cards and data visualization areas
- Responsive grid layout
- User profile section

### 2. Form Layout (`/layouts/form-layout.html`)
- Multi-step form interface
- Form validation examples
- Various input types showcase
- Submit and cancel actions

### 3. Kanban Board (`/layouts/kanban.html`)
- Drag-and-drop card interface
- Column-based task organization
- Card states and priorities
- Team collaboration features

### 4. Landing Page (`/layouts/landing.html`)
- Marketing page layout
- Hero section with CTA
- Feature highlights
- Pricing tables
- Footer with links

### Interactive Viewport Testing

The main `index.html` includes an interactive viewport tester:
- Switch between Mobile, Tablet, Desktop, and Full HD views
- Custom viewport dimensions
- Live preview of responsive behavior
- Layout selector for quick switching

## 📚 Best Practices

### Component Usage

1. **Semantic HTML First**
   ```html
   <!-- Good -->
   <button class="btn btn-primary">Submit</button>
   
   <!-- Avoid -->
   <div class="btn btn-primary">Submit</div>
   ```

2. **Consistent Naming**
   ```html
   <!-- Good -->
   <div class="card">
     <div class="card-header">Title</div>
     <div class="card-body">Content</div>
   </div>
   
   <!-- Avoid -->
   <div class="card">
     <div class="header">Title</div>
     <div class="content">Content</div>
   </div>
   ```

3. **Accessibility**
   ```html
   <!-- Good -->
   <button class="btn btn-primary" aria-label="Save document">
     <svg class="btn-icon">...</svg>
   </button>
   
   <!-- Good -->
   <input class="input" aria-invalid="true" aria-describedby="error-msg">
   <span id="error-msg" class="text-red-600">Required field</span>
   ```

4. **State Management**
   ```html
   <!-- Loading State -->
   <button class="btn btn-primary" disabled>
     <span class="spinner spinner-sm"></span>
     <span class="btn-text">Loading...</span>
   </button>
   
   <!-- Error State -->
   <input class="input input-error" aria-invalid="true">
   ```

### Performance Optimization

1. **Use Production Build**
   ```bash
   npm run build
   ```

2. **Lazy Load Images**
   ```html
   <img src="hero.jpg" loading="lazy" alt="Hero image">
   ```

3. **Minimize Custom CSS**
   - Prefer utility classes over custom CSS
   - Use component classes for repeated patterns
   - Avoid deep nesting

### Customization

1. **Extending Colors**
   ```css
   @theme {
     --color-brand-500: #your-color;
   }
   ```

2. **Adding Components**
   ```css
   @layer components {
     .btn-brand {
       @apply bg-brand-500 text-white hover:bg-brand-600;
     }
   }
   ```

3. **Overriding Defaults**
   ```css
   .btn-primary {
     /* Your custom styles */
     background: linear-gradient(...);
   }
   ```

## 🌐 Browser Support

- Chrome/Edge (last 2 versions)
- Firefox (last 2 versions)
- Safari 14+
- iOS Safari 14+
- Chrome for Android (last version)

### Required Features
- CSS Grid
- CSS Custom Properties
- CSS `:has()` selector (for tabs - limited support in older browsers)
- CSS `@layer` support

## 🤝 Contributing

We welcome contributions! Please follow these guidelines:

### Development Process

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```

3. **Make your changes**
   - Follow the naming conventions
   - Add documentation for new components
   - Test across browsers

4. **Commit with descriptive message**
   ```bash
   git commit -m "Add: New tooltip component with animations"
   ```

5. **Push and create PR**
   ```bash
   git push origin feature/your-feature-name
   ```

### Code Style

- Use Prettier for formatting
- Follow existing naming patterns
- Comment complex implementations
- Maintain accessibility standards

### Component Checklist

When adding new components:
- [ ] Follows naming convention
- [ ] Includes all necessary variants
- [ ] Has hover/focus/active states
- [ ] Is keyboard accessible
- [ ] Works on mobile devices
- [ ] Documented in README
- [ ] Added to index.html showcase

## 📄 License

This project is licensed under the ISC License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Tailwind CSS](https://tailwindcss.com/) team for the amazing framework
- [Vite](https://vitejs.dev/) for the blazing fast build tool
- [Proxima Nova](https://fonts.adobe.com/fonts/proxima-nova) by Mark Simonson
- Community contributors and users

## 📞 Support

- **Issues**: [GitHub Issues](https://github.com/barry-napier/Styleguide/issues)
- **Discussions**: [GitHub Discussions](https://github.com/barry-napier/Styleguide/discussions)
- **Email**: Contact the maintainer

## 🚀 Roadmap

### Upcoming Features

- [ ] Dark mode support
- [ ] RTL language support
- [ ] More animation utilities
- [ ] Component playground
- [ ] Figma design kit
- [ ] React/Vue component library
- [ ] Storybook integration
- [ ] A11y testing suite
- [ ] Performance monitoring
- [ ] CI/CD pipeline

---

<div align="center">
  <strong>Built with ❤️ using Tailwind CSS 4.0</strong>
  <br>
  <a href="https://github.com/barry-napier/Styleguide">Star on GitHub</a>
  ·
  <a href="https://github.com/barry-napier/Styleguide/issues">Report Bug</a>
  ·
  <a href="https://github.com/barry-napier/Styleguide/issues">Request Feature</a>
</div>