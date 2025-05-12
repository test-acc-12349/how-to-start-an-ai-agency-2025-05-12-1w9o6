# AI Agency Landing Page - Maintenance Guide

This guide will help you maintain and customize the AI Agency landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. Change the logo text:
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold text-blue-600">AI Agency</a>
```
Simply replace "AI Agency" with your desired text.

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight text-gray-900 mb-8">
    How To Start An <span class="text-blue-600">AI Agency</span>
</h1>
```

To modify:
- Change the main text between the `<h1>` tags
- The `<span>` with `text-blue-600` creates the blue highlighted text
- Adjust text size by modifying these classes:
  - `text-4xl`: Mobile size
  - `md:text-5xl`: Tablet size
  - `lg:text-6xl`: Desktop size

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-all duration-300 transform hover:scale-105">
    <i class='bx bx-bulb text-4xl text-blue-600 mb-4'></i>
    <h3 class="text-xl font-semibold mb-4">Get Ideas</h3>
    <p class="text-gray-600">Access our comprehensive database...</p>
</div>
```

To update:
1. Change the icon by replacing `bx-bulb` with another [Boxicons](https://boxicons.com/) class
2. Modify the heading text within `<h3>` tags
3. Update the description in the `<p>` tags

### Understanding Tailwind Classes
Common classes used throughout:
- Layout:
  - `container`: Centers content
  - `mx-auto`: Centers horizontally
  - `px-4`: Horizontal padding
  - `py-24`: Vertical padding
- Text:
  - `text-xl`: Text size
  - `text-gray-600`: Text color
  - `font-bold`: Font weight
- Responsive:
  - `md:`: Tablet breakpoint
  - `lg:`: Desktop breakpoint

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

To update:
1. Locate the `href` attribute
2. Replace the value with:
   - Internal links: Use `#section-id`
   - External links: Use full URL (e.g., `https://example.com`)

### Call-to-Action Buttons
Current CTA links point to "https://ninja200.online". To update:

1. Find all instances:
```html
<a href="https://ninja200.online" class="inline-flex items-center...">
```

2. Replace the URL with your desired destination

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate these lines in the footer:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Terms of Service</a></li>
</ul>
```

Replace the `#` with:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match exactly:
   ```html
   <!-- Link in navigation -->
   <a href="#features">Features</a>
   
   <!-- Matching section ID -->
   <section id="features">
   ```

2. **Responsive Issues**
   - Check that you're using responsive classes correctly:
   ```html
   text-base md:text-lg lg:text-xl
   ```
   - Order matters: mobile first, then tablet (`md:`), then desktop (`lg:`)

3. **Icon Not Showing**
   - Verify the Boxicons CDN is properly loaded in the `<head>`
   - Check icon class names match exactly with Boxicons documentation

### Need Help?
- Double-check your changes against the original code
- Use browser developer tools (F12) to inspect elements
- Ensure all HTML tags are properly closed
- Maintain the existing class structure when making changes

Remember to test all changes across different screen sizes using browser developer tools.