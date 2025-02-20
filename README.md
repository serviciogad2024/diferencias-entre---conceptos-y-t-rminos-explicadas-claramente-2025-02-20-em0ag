# DiferenciasEntre Landing Page - Maintenance Guide

This guide will help you maintain and customize the DiferenciasEntre landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text:**
```html
<a href="/" class="text-2xl font-bold text-gray-800 hover:text-blue-600 transition-colors duration-300">
    DiferenciasEntre
</a>
```
- Replace "DiferenciasEntre" with your desired text
- Keep the existing classes to maintain styling

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#caracteristicas" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Características</a>
    <!-- Additional menu items -->
</div>
```
- Update text between `<a>` tags
- Maintain the `class` attributes for consistent styling

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-8">
    Diferencias Entre | Conceptos y Términos Explicadas Claramente
</h1>
```
- Update the heading text while keeping the responsive size classes (`text-4xl`, `md:text-5xl`, `lg:text-6xl`)
- The `mb-8` class adds margin bottom spacing - adjust if needed (1-16 scale)

### Understanding Tailwind Classes
Common classes used throughout:
- Text sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`, etc.
- Colors: `text-gray-600`, `bg-blue-600`, etc.
- Spacing: `p-8` (padding), `m-4` (margin)
- Responsive prefixes: `md:`, `lg:` (activate at specific breakpoints)

## Managing Links

### Navigation Links
Current navigation links are:
```html
<a href="#caracteristicas">Características</a>
<a href="#beneficios">Beneficios</a>
<a href="#faq">FAQ</a>
<a href="#contacto">Contacto</a>
```

To update:
1. Internal links (same page):
   - Use `#section-id` format
   - Ensure corresponding section has matching ID
   ```html
   <a href="#new-section">New Section</a>
   <section id="new-section">...</section>
   ```

2. External links:
   - Use full URL
   ```html
   <a href="https://your-site.com/page">Page Name</a>
   ```

### Footer Links
Current placeholder links need updating:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Inicio</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Sobre Nosotros</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Blog</a></li>
</ul>
```

Replace `#` with actual URLs:
```html
<li><a href="https://your-site.com">Inicio</a></li>
<li><a href="https://your-site.com/about">Sobre Nosotros</a></li>
<li><a href="https://your-site.com/blog">Blog</a></li>
```

## Adding Privacy and Terms Pages

### Step 1: Update Footer Links
Locate the legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacidad</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Términos</a></li>
    </ul>
</div>
```

Replace with:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacidad</a></li>
        <li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Términos</a></li>
    </ul>
</div>
```

### Step 2: Create Policy Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Use consistent styling with the main page
3. Include navigation back to the main page

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Check that section IDs match exactly with href values
   - IDs are case-sensitive
   - Remove any spaces in IDs

2. **Responsive Design Issues**
   - Verify media query prefixes (`md:`, `lg:`)
   - Test at different screen sizes
   - Don't remove responsive classes unless intended

3. **Styling Problems**
   - Keep Tailwind CSS link in header
   - Check for typos in class names
   - Maintain spacing between multiple classes

For additional help:
- Consult [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools to inspect elements
- Test all changes in multiple browsers

Remember to always backup your files before making significant changes, and test thoroughly on a development environment before pushing to production.