# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. Change the logo text:
```html
<!-- Find this line in the header -->
<div class="text-2xl font-bold text-blue-600">TWD</div>
<!-- Replace "TWD" with your desired text -->
```

2. Modify navigation menu items:
```html
<div class="hidden md:flex space-x-8">
    <!-- Each link can be modified here -->
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
</div>
```

### Hero Section
Update your main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-8">Best Websites In Texas</p>
```

The text sizes are controlled by these Tailwind classes:
- `text-4xl`: Large on mobile
- `md:text-5xl`: Larger on medium screens
- `lg:text-6xl`: Largest on large screens

### Features and Benefits Sections
Each card follows this structure:
```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="text-blue-600 mb-4">
        <i class="fas fa-server text-4xl"></i> <!-- Icon -->
    </div>
    <h3 class="text-xl font-bold mb-4">Free Hosting</h3> <!-- Title -->
    <p class="text-gray-600">Premium hosting included...</p> <!-- Description -->
</div>
```

To modify:
1. Change the icon: Update the `fa-server` class with any [Font Awesome](https://fontawesome.com/icons) icon
2. Update the title text inside the `<h3>` tag
3. Modify the description inside the `<p>` tag

## Managing Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. The `#` symbol indicates an internal page section
2. Match the href value to the section's ID
3. Example: `href="#features"` links to `<section id="features">`

### Call-to-Action Links
Update the main CTA buttons:
```html
<!-- Hero section button -->
<a href="https://twd.com" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">Get Started</a>

<!-- CTA section button -->
<a href="https://twd.com" class="inline-block bg-white text-blue-600 px-8 py-4 rounded-lg">Contact Us Today</a>
```

Replace `https://twd.com` with your actual website URL or contact page.

## Adding Privacy and Terms Pages

### Footer Link Setup
Locate the legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link to privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your website folder
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match href values exactly
   - IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - These control how elements appear on different screen sizes
   - Example: `md:text-5xl` means "apply text-5xl on medium screens and up"

3. **Icon Not Showing**
   - Verify Font Awesome is loaded properly
   - Check if the icon class name is correct
   - Example: `fa-server` should have `fas` prefix: `<i class="fas fa-server">`

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all files are in the correct folders
3. Ensure all links use the correct file paths
4. Double-check class names for typos

Remember: Always make a backup before making changes to your website files.