# Mammoth Party Landing Page - Maintenance Guide

This guide will help you maintain and customize the Mammoth Party landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions to make updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<a href="/" class="text-2xl font-bold text-purple-600">Mammoth Party</a>
```
- Replace "Mammoth Party" with your desired text
- Keep the classes to maintain styling

2. **Navigation Menu Items:**
```html
<a href="#features" class="text-gray-600 hover:text-purple-600 transition-colors duration-300">Features</a>
```
- Update text between `<a>` tags
- Maintain the `class` attributes to preserve hover effects

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Capture Unforgettable Moments with Mammoth Party
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Fun Photos, Unforgettable Experiences
</p>
```

**Tailwind Class Explanation:**
- `text-4xl`: Large text on mobile
- `md:text-5xl`: Larger text on medium screens
- `lg:text-6xl`: Largest text on large screens
- `mb-6`: Margin bottom spacing
- `text-gray-900`: Dark gray text color

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-2xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <!-- Icon container -->
    <div class="w-12 h-12 bg-purple-100 rounded-full flex items-center justify-center mb-6">
        <!-- SVG icon here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Feature Title</h3>
    <p class="text-gray-600">Feature description</p>
</div>
```

To update:
1. Change the title text in `<h3>`
2. Modify description in `<p>`
3. Keep all classes for consistent styling

## Managing Links

### Current Link Inventory
1. Navigation Menu:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="mailto:info@mammothparty.com">Contact Us</a>
```

2. Call-to-Action Buttons:
```html
<a href="https://www.mammothparty.com">Book Your Experience</a>
```

### Updating Links
To update any link:
1. Locate the `<a>` tag
2. Modify the `href` attribute:
   - For internal sections: Use `#section-name`
   - For external links: Use full URL starting with `https://`
   - For email: Use `mailto:email@address.com`

Example:
```html
<!-- Before -->
<a href="https://www.mammothparty.com">Book Your Experience</a>

<!-- After -->
<a href="https://www.yournewdomain.com">Book Your Experience</a>
```

## Adding Privacy and Terms Pages

### Footer Link Updates
Locate the legal section in the footer:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link to privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your project folder
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Styles**
- Verify the Tailwind CDN link is present in the `<head>`
- Check for typos in class names
- Ensure all closing tags are present

2. **Non-Working Links**
- Confirm file paths are correct
- Check for proper URL formatting
- Verify files exist in the specified location

3. **Responsive Design Issues**
- Keep the responsive classes (`md:`, `lg:`) intact
- Test on different screen sizes
- Don't remove the viewport meta tag

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools to inspect elements
- Keep a backup copy of the original HTML before making changes

Remember to test all changes across different devices and browsers to ensure consistency in appearance and functionality.