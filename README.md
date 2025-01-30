# Floorplan 24 Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Floorplan 24 landing page. The page is built using HTML and Tailwind CSS, with Alpine.js for interactive components.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To modify:

1. Update company name:
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-blue-600">Floorplan 24</a>
```
Simply replace "Floorplan 24" with your desired text.

### Hero Section
The main headline and subtext can be modified here:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Professional Floorplans in 24 Hours
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12 leading-relaxed">
    Precise, professional floorplans delivered within 24 hours to enhance your property listings
</p>
```

#### Understanding Tailwind Classes
- `text-4xl`: Base text size
- `md:text-5xl`: Text size on medium screens
- `lg:text-6xl`: Text size on large screens
- `mb-6`: Margin bottom spacing
- `text-gray-900`: Text color

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Easy Upload</h3>
    <p class="text-gray-600">Simple web form upload process for your convenience</p>
</div>
```

To modify a feature:
1. Locate the feature card you want to change
2. Update the `<h3>` text for the title
3. Update the `<p>` text for the description
4. Keep the existing classes to maintain styling

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors">Contact</a>
</div>
```

To update links:
1. Identify the `<a>` tag you want to modify
2. Change the `href` attribute to your desired destination:
   - For same-page sections, use `#section-id`
   - For external links, use the full URL (e.g., `https://example.com`)
   - For internal pages, use relative paths (e.g., `/about.html`)

### Call-to-Action Links
Current CTA links point to `https://floorplan24.com`. Update these in:
1. Header button
2. Hero section button
3. Final CTA section button

Example:
```html
<a href="https://your-new-url.com" class="inline-block bg-blue-600 text-white...">
```

## Adding Privacy and Terms Pages

### Footer Link Setup
Locate the legal links section in the footer:
```html
<div>
    <h4 class="text-white text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your project directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match href attributes
   - Check file paths are correct relative to index.html
   - Verify file names match exactly (case-sensitive)

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Keep the `container` class on main section divs
   - Maintain the existing grid structure in responsive sections

3. **Style Inconsistencies**
   - Copy existing classes when adding new elements
   - Use the same color classes (e.g., `text-blue-600`)
   - Maintain padding and margin patterns

### Need Help?
For additional assistance:
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify Alpine.js syntax for interactive elements
- Ensure all external resources (CSS, JS) are properly loaded

Remember to test all changes across different screen sizes using your browser's developer tools.