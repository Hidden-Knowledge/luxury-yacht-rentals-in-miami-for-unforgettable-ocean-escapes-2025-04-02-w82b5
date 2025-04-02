# Magic City Yachts Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Magic City Yachts landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu. To update:

```html
<!-- Located at the top of the page -->
<a href="/" class="text-2xl font-['Playfair_Display'] font-bold">Magic City Yachts</a>
```

To change the company name:
1. Locate this line in the header section
2. Replace "Magic City Yachts" with your desired text
3. Keep the existing classes to maintain styling

### Hero Section
The hero section contains the main headline and tagline:

```html
<h1 class="font-['Playfair_Display'] text-4xl md:text-5xl lg:text-6xl font-bold text-white mb-6 leading-tight">
    Luxury Yacht Rentals in Miami for Unforgettable Ocean Escapes
</h1>
<p class="text-xl md:text-2xl text-white/90 mb-12 font-light">
    "Sail Miami in Style. Unforgettable Views."
</p>
```

To modify:
1. Change the text between the `<h1>` tags for the main headline
2. Update the text between the `<p>` tags for the tagline
3. Keep the Tailwind classes intact to maintain responsive design

### Understanding Key Tailwind Classes
- `text-4xl md:text-5xl lg:text-6xl`: Makes text responsive (larger on bigger screens)
- `font-['Playfair_Display']`: Applies the Playfair Display font
- `mb-6`: Adds margin bottom spacing (6 units)
- `text-white/90`: Makes text white with 90% opacity

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="px-6 py-2 bg-blue-600 text-white rounded-full hover:bg-blue-700">Book Now</a>
</div>
```

To update links:
1. Locate the `href` attribute in each `<a>` tag
2. Replace the value with your desired URL:
   - For internal sections, use `#section-name`
   - For external pages, use the full URL (e.g., `https://example.com`)
3. Example:
   ```html
   <a href="https://booking.magiccityyachts.com" class="px-6 py-2 bg-blue-600 text-white rounded-full">Book Now</a>
   ```

### Social Media Links
Located in the footer:

```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">
        <!-- Twitter icon -->
    </a>
    <a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">
        <!-- Instagram icon -->
    </a>
</div>
```

Replace the `#` with your social media profile URLs:
```html
<a href="https://twitter.com/magiccityyachts" class="text-gray-400 hover:text-white transition-colors duration-300">
```

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the Quick Links section in the footer:

```html
<div>
    <h4 class="text-lg font-semibold mb-6">Quick Links</h4>
    <ul class="space-y-3">
        <li><a href="#features" class="text-gray-400 hover:text-white transition-colors duration-300">Features</a></li>
        <!-- Add these new lines -->
        <li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Layout After Text Changes**
   - Verify all opening and closing tags are present
   - Check that Tailwind classes remain unchanged
   - Ensure new text content isn't breaking layout constraints

2. **Links Not Working**
   - Confirm href attributes start with `/` for root-relative paths
   - Verify external URLs include `https://`
   - Check that internal section IDs match their targets

3. **Responsive Design Issues**
   - Keep the responsive Tailwind classes (e.g., `md:`, `lg:` prefixes)
   - Test on multiple screen sizes using browser dev tools
   - Maintain the existing container and padding classes

### Need Help?
If you encounter issues:
1. Check the browser's developer console (F12) for errors
2. Verify all changes against the original code
3. Test the page across different devices and browsers
4. Consider using the browser's inspect element tool to debug styling issues

Remember to always backup your code before making changes and test thoroughly after each modification.