---
sidebar_position: 7
---

# UI Customization

This section guides developers through the process of customizing the visual appearance of the TestWorthy application, focusing on modifying themes, styles, and layout components to match branding or user preferences.

## Accessing the Stylesheets

1. Locate the main CSS file:  
   - Typically named `style.css` or similar, found in the `assets/css/` directory.
   - This file contains global styles, font definitions, icon fonts, and component-specific styles.

2. Open the stylesheet in your preferred code editor.

## Modifying Global Styles

1. **Fonts and Icons**  
   - To change the default font, locate the `@font-face` declarations and `body` font-family settings.  
   - To customize icons, modify the `@font-face` source URLs or replace the icon font files with your own.

2. **Colors and Backgrounds**  
   - Search for CSS variables or classes defining primary, secondary, or accent colors (e.g., `.btn-primary`, `.navbar`, `.card`).  
   - Update color codes (`#hex`, `rgb()`, or `rgba()`) to match your branding palette.

3. **Layout Adjustments**  
   - Adjust container widths, paddings, margins, and grid layouts to modify spacing and responsiveness.  
   - For example, modify `.container`, `.sidebar`, `.header`, `.footer` classes.

## Customizing UI Components

1. **Buttons**  
   - Locate button classes such as `.btn`, `.btn-primary`, `.btn-secondary`.  
   - Change background-color, border, font-size, or padding to alter appearance.

2. **Navigation Menus**  
   - Modify `.navbar`, `.nav-link`, `.dropdown-menu` classes for colors, hover effects, and spacing.

3. **Cards and Panels**  
   - Change `.card`, `.panel`, or `.box` styles for borders, shadows, and background colors.

4. **Modals and Popovers**  
   - Adjust `.modal`, `.popover`, `.tooltip` classes for background, border, and arrow styles.

5. **Progress Bars and Loaders**  
   - Locate `.progress`, `.loader`, or custom classes and update colors, sizes, or animations.

## Theming and Custom Themes

1. **Creating a New Theme**  
   - Duplicate an existing theme CSS file, e.g., `themes/blue-theme.css`.  
   - Rename and modify color variables, fonts, and component styles.

2. **Applying a Theme**  
   - Link your custom theme CSS in the HTML `<head>` section after the main stylesheet.  
   - For example:  
     `<link rel="stylesheet" href="assets/css/my-custom-theme.css">`

3. **Switching Themes Dynamically**  
   - Use JavaScript to change the `href` attribute of the theme `<link>` element based on user selection or preferences.

## Customizing Specific Components

### Test Suites and Test Cases

- Locate styles for `.test-suite`, `.test-case`, `.milestone`, etc.  
- Change background colors, borders, or font styles to distinguish different statuses or categories.

### Dashboard and Reports

- Modify `.dashboard`, `.report`, `.chart-container` classes for layout and color schemes.  
- Adjust axes, grid lines, and labels in chart styles if using inline SVG or Canvas.

### Responsive Design

- Use media queries to tweak styles on different screen sizes:  
  ```css
  @media (max-width: 768px) {
    /* Adjust sidebar, font sizes, or layout for mobile */
  }
  ```

## Best Practices

- Use CSS variables (custom properties) for colors and fonts for easier theme switching:  
  ```css
  :root {
    --primary-color: #007bff;
    --secondary-color: #6c757d;
    --font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
  }
  body {
    font-family: var(--font-family);
    color: var(--primary-color);
  }
  ```
- Keep custom styles in separate files or under a dedicated theme directory for maintainability.
- Use browser developer tools to inspect elements and experiment with style changes in real-time before applying them to your CSS files.

## Finalizing Your Customization

- Save your CSS modifications.
- Clear browser cache or use hard reload to see changes.
- Test across different browsers and devices for consistency.

## Summary

Customizing the appearance of TestWorthy involves editing the main stylesheet and theme files, adjusting colors, fonts, component styles, and layout properties. By leveraging CSS variables and modular stylesheets, you can efficiently implement branding updates, visual themes, or user interface tweaks to match your organization’s branding guidelines or user preferences.