# Nachtbril Fiets Landing Page - Maintenance Guide

This guide will help you maintain and customize the Nachtbril Fiets landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text:**
```html
<a href="/" class="text-2xl font-bold text-indigo-600">Nachtbril Fiets</a>
```
- Replace "Nachtbril Fiets" with your desired text
- The `text-indigo-600` class controls the purple color

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-indigo-600">Voordelen</a>
    <a href="#benefits" class="text-gray-600 hover:text-indigo-600">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-indigo-600">FAQ</a>
</div>
```
- Replace "Voordelen", "Benefits", and "FAQ" with new menu items
- Keep the `href` attributes matching your section IDs

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-extrabold text-gray-900 mb-8">
    Nachtbril Fiets
    <span class="block text-indigo-600 mt-2">Tijdelijk 20% KORTING</span>
</h1>
```
- Update the main heading and discount text
- The responsive text sizes are controlled by `text-4xl`, `md:text-5xl`, and `lg:text-6xl`

### Tailwind CSS Quick Reference
Common classes used in this page:
- Text sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`, etc.
- Colors: `text-indigo-600`, `text-gray-900`, `bg-white`
- Spacing: `px-4`, `py-2`, `m-4`, `mb-8`
- Flex: `flex`, `items-center`, `justify-between`

## Managing Links

### Navigation Links
1. **Internal Section Links:**
```html
<!-- Current internal links -->
<a href="#features">Voordelen</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
```
To update:
- Ensure the `href` matches the `id` of your target section
- Example: `<a href="#new-section">New Section</a>`

2. **Call-to-Action Buttons:**
```html
<!-- Update this URL -->
<a href="https://nachtbril.com/shop" class="inline-flex items-center...">
    Bestel Nu
</a>
```
- Replace `https://nachtbril.com/shop` with your shop URL
- Keep the existing classes for consistent styling

### Footer Links
Current footer structure:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
</ul>
```
- Replace `#` with actual URLs
- Maintain the hover effect classes

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new HTML files in your project directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
```html
<!-- Replace these placeholder links -->
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

### Step 3: Maintain Consistent Styling
Copy these classes to maintain consistent link styling:
```html
class="text-gray-400 hover:text-white transition-colors duration-300"
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
- Check that section IDs match exactly with href attributes
- Example: `href="#features"` must match `id="features"`

2. **Responsive Design Issues**
- Check mobile view using browser dev tools
- Ensure you're not removing important responsive classes like `md:` prefixed ones

3. **Style Changes Not Applying**
- Verify Tailwind CSS is properly loaded
- Check for typos in class names
- Make sure you're not overriding classes unintentionally

### Need Help?
If you encounter issues:
1. Check the browser console for errors
2. Verify all files are in the correct directory
3. Ensure all links use the correct relative or absolute paths
4. Double-check class names against Tailwind CSS documentation

Remember to always test changes across different screen sizes and browsers before deploying to production.