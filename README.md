# Centered Dashboard Template

A modern, fixed-width dashboard template with dark/light theme support, sidebar navigation, and content switching functionality.

## Features

- **Fixed-Width Layout**: Centered design with fixed sidebar and content width
- **Dark/Light Theme**: Toggle between themes with persistent storage of preferences
- **Dedicated Sidebar**: Fixed-width sidebar with logo and navigation
- **Dynamic Content Switching**: Content sections update based on navigation selection
- **Floating Header Icons**: Theme toggle and profile button positioned in the top-right corner
- **Minimal Dependencies**: Self-contained with no external JavaScript libraries
- **CSS Variables**: Easy customization of colors and dimensions
- **Clean UI Elements**: Modern, minimalist design approach

## Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- Basic knowledge of HTML, CSS, and JavaScript

### Installation

1. Download or clone the repository
2. Open `templates2.html` in your browser to preview the dashboard

## Usage

This dashboard is contained in a single HTML file with inline CSS and JavaScript for simplicity. To use it in your project:

1. Copy the `templates2.html` file to your project directory
2. Modify the content sections as needed
3. Customize the styling by adjusting the CSS variables

### Layout Structure

Unlike typical full-width dashboards, this template uses a fixed-width centered layout:

```css
:root {
  --sidebar-width: 250px;
  --content-width: 1150px;
}

.layout {
  width: calc(var(--sidebar-width) + var(--content-width));
  margin: 0 auto;
}
```

### Navigation Structure

The sidebar contains navigation links that update the content area. Each link corresponds to a content section via the URL hash.

```html
<div class="nav-item">
  <a href="#link-1" class="nav-link" data-title="Link 1">
    <!-- Icon SVG -->
    Link 1
  </a>
</div>
```

With its corresponding content section:

```html
<div class="section" id="link-1">
  <h1>Link 1 Content!</h1>
  <!-- Your content goes here -->
</div>
```

## Customization

### Theme Customization

The template uses CSS variables for easy theming. Modify the `:root` and `[data-theme="light"]` selectors to change colors:

```css
:root {
  --bg-primary: #0f0f0f;
  --bg-secondary: #161616;
  --text-color: #ffffff;
  --accent-color: #3b82f6;
  --border-color: #2a2a2a;
}

[data-theme="light"] {
  --bg-primary: #ffffff;
  --bg-secondary: #f5f5f5;
  --text-color: #333333;
  --border-color: #e0e0e0;
}
```

### Layout Dimensions

Adjust the width of the sidebar and content area by changing the corresponding variables:

```css
:root {
  --sidebar-width: 250px;
  --content-width: 1150px;
  --header-height: 56px;
}
```

### Content Design

Each content section can be customized with additional elements. The template includes styling for content boxes, titles, and text elements.

## Structure

The template consists of:

- **Header Icons**: Floating controls in the top-right corner
- **Sidebar**: Fixed-width navigation panel with logo and menu links
- **Content Area**: Main content with header and dynamic sections
- **Content Header**: Title bar that updates based on the selected navigation item

## JavaScript Functionality

The template includes two main JavaScript functions:

1. `initThemeToggle()`: Manages theme switching and persistence
2. `initRouter()`: Handles navigation and content display based on URL hash

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

This template is available for personal and commercial use.

---

**Note**: This is a centered, fixed-width variation of the dashboard template. For a full-width responsive version, see the first template in this collection.
