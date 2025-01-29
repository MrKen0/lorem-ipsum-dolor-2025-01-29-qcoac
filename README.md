# Landing Page Maintenance Guide

This guide will help you maintain and customize the landing page, with specific instructions for updating content, fixing links, and adding policy pages. This documentation assumes basic familiarity with HTML but explains concepts thoroughly for beginners.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text**
```html
<div class="text-2xl font-bold bg-gradient-to-r from-indigo-600 to-violet-600 bg-clip-text text-transparent">
    Logo <!-- Replace "Logo" with your company name -->
</div>
```

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#" class="text-gray-600 hover:text-indigo-600 transition-colors duration-300">Features</a>
    <!-- Repeat for each menu item -->
</div>
```

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight bg-gradient-to-r from-indigo-600 to-violet-600 bg-clip-text text-transparent mb-8">
    Lorem ipsum dolor <!-- Replace with your headline -->
</h1>
```

#### Understanding Responsive Classes
- `text-4xl`: Default text size
- `md:text-5xl`: Text size on medium screens
- `lg:text-6xl`: Text size on large screens

### Features Section
To add or modify feature cards:

1. Locate the features grid:
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
```

2. Copy and paste this template for each feature:
```html
<div class="p-8 rounded-2xl bg-white shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-12 h-12 bg-indigo-100 rounded-xl flex items-center justify-center mb-6">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Feature Name</h3>
    <p class="text-gray-600">Feature description</p>
</div>
```

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
   - Features: `<a href="#">Features</a>`
   - Benefits: `<a href="#">Benefits</a>`
   - About: `<a href="#">About</a>`
   - Contact: `<a href="#">Contact</a>`

To update links:

1. Replace the `#` with your page URL:
```html
<a href="features.html" class="text-gray-600 hover:text-indigo-600 transition-colors duration-300">Features</a>
```

2. For external links, use complete URLs:
```html
<a href="https://example.com/page" class="text-gray-600 hover:text-indigo-600 transition-colors duration-300">External Link</a>
```

### Button Links
Update the "Get Started" buttons:
```html
<a href="signup.html" class="inline-block px-8 py-4 bg-gradient-to-r from-indigo-600 to-violet-600 text-white rounded-full">
    Get Started Now
</a>
```

## Linking Privacy and Terms Pages

### Adding Footer Links
Locate the footer section and add privacy/terms links:

```html
<div class="grid grid-cols-1 md:grid-cols-4 gap-12">
    <div>
        <h3 class="text-xl font-bold mb-4">Legal</h3>
        <ul class="space-y-2">
            <!-- Add these lines -->
            <li><a href="privacy.html" class="opacity-75 hover:opacity-100 transition-opacity duration-300">Privacy Policy</a></li>
            <li><a href="terms.html" class="opacity-75 hover:opacity-100 transition-opacity duration-300">Terms of Service</a></li>
        </ul>
    </div>
</div>
```

### Alternative Navigation Menu Placement
To add legal links in the header navigation:

```html
<div class="hidden md:flex space-x-8">
    <!-- Existing navigation items -->
    <a href="privacy.html" class="text-gray-600 hover:text-indigo-600 transition-colors duration-300">Privacy</a>
    <a href="terms.html" class="text-gray-600 hover:text-indigo-600 transition-colors duration-300">Terms</a>
</div>
```

## Troubleshooting

### Common Issues

1. **Broken Gradients**
If gradients aren't showing:
```html
<!-- Correct gradient class usage -->
class="bg-gradient-to-r from-indigo-600 to-violet-600"
```

2. **Responsive Issues**
Check these class prefixes:
- `md:` for medium screens (768px+)
- `lg:` for large screens (1024px+)

3. **Missing Styles**
Ensure the Tailwind CSS link is present:
```html
<link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
```

### Need Help?
- Double-check all closing tags
- Verify file paths for links
- Ensure all copied code maintains proper indentation
- Test the page on multiple screen sizes

Remember to back up your files before making significant changes, and always test your updates in a development environment first.