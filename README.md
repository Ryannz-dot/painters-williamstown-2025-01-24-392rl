# Landing Page Maintenance Guide

Welcome to the maintenance guide for the Painters Williamstown landing page. This document will help you make common updates and modifications to the website, even if you're new to HTML and CSS.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text**: Find this line and change "PW":
```html
<a href="/" class="text-2xl font-bold text-blue-600">PW</a>
```

2. **Navigation Menu Items**: Located in the header section:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>
    <a href="#benefits">Benefits</a>
    <!-- Add or modify menu items here -->
</div>
```

### Hero Section
To update the main headline and subheading:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Painters Williamstown <!-- Change this text -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10">
    Reliable Painting Services Near You <!-- Change this text -->
</p>
```

### Tailwind CSS Classes Explained

Common classes used throughout:
- `text-{size}`: Controls text size (xl, 2xl, 3xl, etc.)
- `mb-{number}`: Adds margin bottom (4, 6, 8, etc.)
- `py-{number}`: Adds padding top and bottom
- `bg-{color}-{shade}`: Sets background color (blue-600, gray-50, etc.)

Example of modifying a button:
```html
<!-- Original -->
<a href="#" class="bg-blue-600 text-white px-6 py-2 rounded-full">

<!-- Modified for larger size and different color -->
<a href="#" class="bg-green-600 text-white px-8 py-3 rounded-full">
```

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Links:
```html
<!-- Update this URL with your actual quote page -->
<a href="http://www.painterwilliamstown.com.au" class="bg-blue-600">Get Quote</a>
```

3. Email Links:
```html
<!-- Update with your actual email address -->
<a href="mailto:info@prestigehousepainting.com.au">
```

To update any link:
1. Locate the `<a>` tag
2. Change the `href` attribute
3. Update the text between the opening and closing tags

Example:
```html
<!-- Before -->
<a href="http://www.painterwilliamstown.com.au">Get Quote</a>

<!-- After -->
<a href="https://your-new-domain.com/quote">Get Quote</a>
```

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Locate the footer section and add the new links:

```html
<div class="border-t border-gray-800 mt-12 pt-8 text-center">
    <p class="text-gray-400">&copy; 2024 Painters Williamstown. All rights reserved.</p>
    <!-- Add these lines below the copyright notice -->
    <div class="mt-4 space-x-4">
        <a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
        <a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
    </div>
</div>
```

### Step 2: Create New Pages
Create two new files in your website directory:
- `privacy.html`
- `terms.html`

Use this basic template for both:

```html
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <!-- Copy the head section from index.html -->
</head>
<body class="font-['Inter'] antialiased bg-white text-gray-900">
    <!-- Copy the header section from index.html -->
    
    <main class="pt-32 pb-24">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl font-bold mb-8">Privacy Policy</h1>
            <!-- Add your policy content here -->
        </div>
    </main>

    <!-- Copy the footer section from index.html -->
</body>
</html>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Layout**
   - Check that you haven't removed any important Tailwind classes
   - Verify all opening tags have matching closing tags
   - Ensure the Tailwind CDN link is present in the head section

2. **Links Not Working**
   - Verify that all `href` attributes start with either `#`, `/`, or `http://`
   - Check for typos in the URL
   - Ensure section IDs match their corresponding links

3. **Images Not Loading**
   - Confirm image paths are correct
   - Verify image files exist in the specified directory
   - Check image file names for case sensitivity

Need more help? Contact your web developer or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).