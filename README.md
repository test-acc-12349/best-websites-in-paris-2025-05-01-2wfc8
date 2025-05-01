# Landing Page Maintenance Guide

This guide will help you maintain and customize the Best Websites In Paris landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your company name and navigation menu. To update:

1. **Company Name:**
```html
<div class="text-2xl font-bold text-gray-800">
    Best Websites In Paris  <!-- Replace this text -->
</div>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Update text here -->
    <a href="#benefits">Benefits</a>  <!-- Update text here -->
    <a href="#faq">FAQ</a>           <!-- Update text here -->
    <a href="#contact">Contact</a>    <!-- Update text here -->
</div>
```

### Hero Section
Update your main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-8">
    Custom Websites For Your Business  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Professional web development services tailored for businesses in Paris  <!-- Subheading -->
</p>
```

### Understanding Tailwind Classes
Common classes used in this template:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `font-[weight]`: Controls text weight (e.g., `font-bold`, `font-semibold`)
- `mb-[size]`: Adds margin bottom (e.g., `mb-8`, `mb-12`)
- `py-[size]`: Adds padding top and bottom (e.g., `py-24`)
- `bg-[color]`: Sets background color (e.g., `bg-white`, `bg-blue-600`)

## Managing Links

### Navigation Menu Links
The page uses anchor links to scroll to sections:
```html
<!-- In the header navigation -->
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>

<!-- Corresponding section IDs -->
<section id="features">
<section id="benefits">
<section id="faq">
```

To update:
1. Find the section you want to link to
2. Note its `id` attribute
3. Use that id in your link with a # prefix
4. Example: `<a href="#new-section">New Section</a>`

### Call-to-Action Links
Update the "Get Started" and "Contact Us" buttons:
```html
<!-- Hero section button -->
<a href="https://sigmaseo.io" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">
    Get Started Today
</a>

<!-- CTA section button -->
<a href="https://sigmaseo.io" class="inline-block bg-white text-blue-600 px-8 py-4 rounded-lg">
    Contact Us Now
</a>
```

Replace `https://sigmaseo.io` with your desired URL.

## Adding Privacy and Terms Pages

### Footer Links Setup
Locate the footer legal section:
```html
<div>
    <h4 class="text-lg font-semibold mb-4 text-white">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your project folder
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Links Not Working**
   - Check if the `href` attribute matches exactly with the section `id`
   - Ensure section IDs don't contain spaces
   - Verify file paths for external pages are correct

2. **Styling Problems**
   - Make sure Tailwind CSS is properly loaded
   - Check for typos in class names
   - Maintain responsive classes (e.g., `md:`, `lg:` prefixes)

3. **Mobile Menu Issues**
   - Verify Alpine.js is properly loaded
   - Check if `x-data` and `x-show` directives are present
   - Ensure mobile menu HTML structure remains intact

### Need Help?
If you encounter issues:
1. Check the browser console for errors (F12 key)
2. Verify all required files are present
3. Double-check your changes against the original code
4. Test on multiple devices and browsers

Remember to always backup your files before making changes!