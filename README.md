# CraftsPro Landing Page - Maintenance Guide

This guide will help you maintain and customize the CraftsPro landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Fixing and Managing Links](#fixing-and-managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your company name and navigation menu. To update:

1. **Company Name:**
```html
<a href="/" class="text-2xl font-bold text-white hover:text-blue-400 transition duration-300">
    CraftsPro  <!-- Change this text to your company name -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>  <!-- Update menu item text here -->
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
</div>
```

### Hero Section
Update the main headline and subheading:
```html
<h1 class="text-4xl md:text-6xl font-bold leading-tight mb-6">
    Expert Carpentry & Painting Services for a Beautiful, Lasting Home
    <!-- Change this headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    From Precision Carpentry to Flawless Paint Finishes
    <!-- Change this subheading -->
</p>
```

### Understanding Tailwind Classes
Common classes used in this template:
- `text-4xl`: Large text size
- `md:text-6xl`: Larger text on medium screens
- `mb-6`: Bottom margin spacing
- `bg-gray-900`: Dark background color
- `hover:text-blue-400`: Blue text on hover

To modify styling, replace existing classes with new ones from the [Tailwind documentation](https://tailwindcss.com/docs).

## Fixing and Managing Links

### Navigation Menu Links
Current links that need updating:
```html
<!-- In the header navigation -->
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact Us</a>
```

To update these:
1. For internal section links, ensure the `href` matches the `id` of the target section
2. For external links, replace with full URLs:
```html
<a href="https://yourwebsite.com/services">Services</a>
```

### Call-to-Action Links
Update these important links:
```html
<!-- Hero section CTA -->
<a href="https://yourpaintingdomain.com/contact" 
   class="inline-block px-8 py-4 bg-blue-600">
    Get Your Free Quote
</a>

<!-- Bottom CTA -->
<a href="https://yourpaintingdomain.com/contact" 
   class="inline-block px-8 py-4 bg-white">
    Schedule Your Consultation
</a>
```

Replace `yourpaintingdomain.com` with your actual domain.

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Add these links to the footer section:
```html
<div class="grid grid-cols-1 md:grid-cols-4 gap-12">
    <!-- Existing footer content -->
    <div>
        <h3 class="text-xl font-bold mb-4">Legal</h3>
        <ul class="space-y-2">
            <li><a href="/privacy.html" class="text-gray-300 hover:text-blue-400 transition duration-300">Privacy Policy</a></li>
            <li><a href="/terms.html" class="text-gray-300 hover:text-blue-400 transition duration-300">Terms of Service</a></li>
        </ul>
    </div>
</div>
```

### Step 2: Create Policy Pages
1. Create two new files: `privacy.html` and `terms.html`
2. Copy the header and footer from `index.html`
3. Add your policy content between them

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match exactly with href attributes
   - Example: `href="#faq"` must match `id="faq"`

2. **Responsive Design Issues**
   - Look for classes starting with `md:` or `lg:`
   - These control appearance on different screen sizes
   - Example: `text-4xl md:text-6xl` means normal size is 4xl, medium screens use 6xl

3. **Images Not Loading**
   - Check the URL in background image classes:
   ```html
   bg-[url('https://source.unsplash.com/random/1920x1080?carpentry')]
   ```
   - Replace with your actual image URLs

4. **Styling Not Applied**
   - Verify the Tailwind CSS link is working:
   ```html
   <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
   ```

Remember to:
- Always test changes in multiple browsers
- Check mobile responsiveness
- Keep backups before making major changes
- Validate links before publishing updates

Need more help? Contact your web developer or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).