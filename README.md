# Texas Web Design Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Texas Web Design landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company logo and navigation menu. To modify:

1. **Company Logo**
```html
<a href="/" class="text-2xl font-bold text-blue-600">TWD</a>
```
- Replace "TWD" with your desired text
- Adjust size using `text-2xl` (options: text-sm, text-lg, text-3xl, etc.)
- Change color using `text-blue-600` (options: text-red-600, text-green-600, etc.)

### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Best Websites In Texas</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10">Professional web design services...</p>
```
- Main heading: Replace "Best Websites In Texas"
- Subheading: Update the descriptive text
- Responsive sizes are preset (don't change `md:` and `lg:` prefixes unless you understand responsive design)

### Features Cards
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold text-gray-900 mb-4">Free Hosting</h3>
    <p class="text-gray-600">Premium hosting included...</p>
</div>
```
To modify:
1. Locate the feature card you want to change
2. Update the `<h3>` heading text
3. Modify the description in the `<p>` tag
4. Keep the existing classes to maintain styling

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Internal links (same page sections):
   - Keep the `#` prefix
   - Ensure the ID matches your section (e.g., `href="#features"` links to `<section id="features">`)

2. External links:
   - Replace `href="https://twd.com"` with your actual URL
   - Example: `href="https://your-domain.com/page"`

### Call-to-Action (CTA) Links
Located in multiple sections:
```html
<a href="https://twd.com" class="inline-block px-8 py-4 bg-blue-600 text-white rounded-lg">Start Your Project</a>
```
- Replace `https://twd.com` with your actual contact or signup page URL
- Maintain the existing classes to keep the button styling

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your website directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate this section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Replace the `#` placeholders:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match exactly with href attributes
   - IDs are case-sensitive: `href="#FAQ"` won't link to `id="faq"`

2. **Styling Changes Not Appearing**
   - Verify Tailwind CSS is properly loaded in the head section
   - Check for typos in class names
   - Remember that Tailwind classes must be exact (e.g., `text-blue-600` not `text-blue`)

3. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Test your changes at different screen sizes
   - Use browser developer tools to check responsive breakpoints

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs) for styling options
- Use browser developer tools (F12) to inspect elements
- Keep a backup copy of the original HTML before making changes

Remember to test all changes across different browsers and screen sizes before publishing to your live site.