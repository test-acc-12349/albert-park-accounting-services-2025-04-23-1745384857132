# Albert Park Accounting Landing Page - Maintenance Guide

This guide will help you maintain and customize the Albert Park Accounting landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name**
```html
<!-- Located in header, find this div: -->
<div class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    Albert Park
</div>
```
Simply replace "Albert Park" with your desired company name.

### Hero Section
The main headline and subheading are in the hero section:

```html
<h1 class="text-4xl md:text-5xl lg:text-7xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    Your financial success is our bottom line
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Expert accounting services tailored to elevate your business performance
</p>
```

To modify:
- Replace the text between the `<h1>` tags for the main headline
- Update the text between the `<p>` tags for the subheading
- Keep the classes intact to maintain styling

### Understanding Tailwind Classes
Key classes explained:
- `text-4xl`: Large text size (mobile)
- `md:text-5xl`: Larger text on medium screens
- `lg:text-7xl`: Largest text on large screens
- `text-gray-300`: Light gray text color
- `mb-8`: Margin bottom spacing

## Managing Links

### Navigation Menu Links
The navigation menu contains internal anchor links:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
    <a href="#contact" class="text-gray-300 hover:text-white transition-colors duration-300">Contact</a>
</div>
```

To update:
1. Locate the `href` attribute
2. Change the value to your desired section ID
3. Update the link text between the `<a>` tags

### External Links
The page contains placeholder external links:

```html
<!-- Main CTA Button -->
<a href="https://theaccountants.com" class="inline-block px-8 py-4 bg-gradient-to-r from-purple-600 to-pink-600 rounded-full">
    Transform Your Finances
</a>

<!-- Contact Email -->
<a href="mailto:support@example.com" class="text-lg text-gray-300">
    support@example.com
</a>
```

Replace:
- `https://theaccountants.com` with your actual website URL
- `support@example.com` with your actual email address

## Adding Privacy and Terms Pages

### Footer Links Setup
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

To link privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your project directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Ensure section IDs match exactly (case-sensitive)
   - Example: `href="#Features"` won't link to `id="features"`

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - These control how elements appear on different screen sizes

3. **Gradient Text Not Showing**
   - All gradient text requires these classes together:
     ```html
     bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent
     ```

4. **Mobile Menu Not Working**
   - Verify Alpine.js is properly loaded
   - Check that `x-data` and `x-show` attributes are present

Remember to:
- Test all links after updating
- View changes on multiple screen sizes
- Keep backup copies of working code
- Maintain consistent styling across all pages

Need more help? Consult the [Tailwind CSS documentation](https://tailwindcss.com/docs) or [Alpine.js documentation](https://alpinejs.dev/docs).