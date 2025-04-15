# Landing Page Maintenance Guide

This guide will help you maintain and customize your web agency landing page. Follow these detailed instructions to make updates while preserving the design and functionality.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your brand name and navigation menu. To update:

1. Change the brand name:
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-white hover:text-blue-400 transition-colors duration-300">
    WebAgency  <!-- Replace this text -->
</a>
```

2. Modify navigation items:
```html
<div class="hidden md:flex space-x-8">
    <!-- Each link can be updated here -->
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
</div>
```

### Hero Section
Update the main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 tracking-tight">
    Best Web Agency In Sydney  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Grow your business with clicks  <!-- Subheading -->
</p>
```

### Features Section
Each feature card follows this structure:
```html
<div class="bg-gray-700 rounded-2xl p-8">
    <h3 class="text-xl font-semibold mb-4">Easy to Use</h3>  <!-- Feature title -->
    <p class="text-gray-300">Intuitive interface designed...</p>  <!-- Feature description -->
</div>
```

Common Tailwind CSS Classes Explained:
- `text-4xl`: Large text size
- `md:text-5xl`: Larger text on medium screens
- `font-bold`: Bold text weight
- `mb-8`: Bottom margin spacing
- `bg-gray-700`: Dark gray background
- `rounded-2xl`: Rounded corners
- `hover:scale-105`: Slight enlargement on hover

## Fixing Broken Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. For internal sections, keep the `#` prefix
2. For external links, use the full URL:
```html
<a href="https://your-domain.com/page">Page Name</a>
```

### Call-to-Action Buttons
Update the "Get Started" links:
```html
<!-- Current placeholder link -->
<a href="https://fixrr.online" class="inline-block px-8 py-4 bg-blue-600">
```
Replace with your actual URL:
```html
<a href="https://your-domain.com/start" class="inline-block px-8 py-4 bg-blue-600">
```

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links in the Quick Links section:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Quick Links</h4>
    <ul class="space-y-2">
        <!-- Existing links -->
        <li><a href="#features" class="text-gray-400 hover:text-white transition-colors duration-300">Features</a></li>
        <!-- Add new links -->
        <li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

## Troubleshooting

Common Issues:
1. **Broken Internal Links**: Ensure section IDs match the href attributes
   ```html
   <!-- Link in navigation -->
   <a href="#features">
   <!-- Must match section ID -->
   <section id="features">
   ```

2. **Responsive Design Issues**: Check media query classes
   - `md:` prefix works on screens 768px and larger
   - `lg:` prefix works on screens 1024px and larger

3. **Animation Not Working**: Verify AOS attributes
   ```html
   <!-- Correct format -->
   <div data-aos="fade-up" data-aos-delay="100">
   ```

4. **Styling Inconsistencies**: Maintain consistent color classes
   - Use `bg-gray-900` for dark backgrounds
   - Use `text-gray-300` for muted text
   - Use `text-white` for prominent text

Need help? Contact your web developer or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).