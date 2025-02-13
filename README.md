# Royal Guard Landing Page - Maintenance Guide

This guide will help you maintain and customize the Royal Guard landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To modify:

1. Company Name:
```html
<a href="/" class="text-2xl font-bold text-blue-600">Royal Guard</a>
```
- Replace "Royal Guard" with your company name
- Adjust text size using `text-2xl` (options: text-lg, text-xl, text-3xl)

2. Navigation Menu Items:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="font-medium hover:text-blue-600 transition-colors duration-300">Features</a>
    <!-- Other menu items -->
</div>
```
- Update text between `>` and `</a>` tags
- Keep the `href` attributes matching section IDs

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">Royal Guard - Best Medical Consumable Brand</h1>
<p class="text-2xl md:text-3xl text-gray-600 mb-12">Unique PU Gloves</p>
```
- Update heading text between `<h1>` tags
- Modify subheading in the `<p>` tag
- Maintain responsive classes (md: and lg: prefixes)

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Best Quality</h3>
    <p class="text-gray-600">Premium materials and rigorous quality control ensure superior protection.</p>
</div>
```
- Update feature titles in `<h3>` tags
- Modify descriptions in `<p>` tags
- Keep the styling classes intact

## Managing Links

### Navigation Links
Current internal links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Ensure section IDs match these href values
2. Add new sections by:
   - Creating a new section with matching ID: `<section id="new-section">`
   - Adding corresponding navigation link: `<a href="#new-section">`

### External Links
Current external links:
```html
<a href="https://pm.sg" class="inline-block px-6 py-2 bg-blue-600 text-white rounded-full">Get Started</a>
```
To update:
1. Replace `https://pm.sg` with your desired URL
2. Test the link thoroughly before deployment
3. Consider adding `target="_blank"` for external links

## Adding Privacy and Terms Pages

### Footer Links Setup
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To implement proper linking:
1. Create privacy.html and terms.html in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. Broken Internal Links
- Check that section IDs match href values exactly
- IDs are case-sensitive
- Example: `href="#FAQ"` won't link to `id="faq"`

2. Responsive Design Issues
- Don't remove `md:` or `lg:` prefixes from classes
- Keep the viewport meta tag:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

3. Styling Problems
- Maintain the Tailwind CSS CDN link:
```html
<script src="https://cdn.tailwindcss.com"></script>
```
- Keep font imports for consistent typography:
```html
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
```

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs) for styling options
- Verify HTML syntax using the [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser developer tools (F12)

Remember to always backup your files before making significant changes, and test thoroughly on multiple devices and browsers.