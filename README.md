# Landing Page Maintenance Guide
## For 101Headshots Corporate Photography Website

This guide provides detailed instructions for maintaining and customizing the 101Headshots landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance below.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your company name and navigation menu. To update:

```html
<!-- Located at the top of the page -->
<span class="text-xl font-bold text-gray-900">101Headshots</span>
```

1. To change the company name: Replace "101Headshots" with your desired text
2. To adjust text size: Modify `text-xl` to:
   - Smaller: `text-lg` or `text-base`
   - Larger: `text-2xl` or `text-3xl`

### Hero Section
The main headline and subtitle are in the first section after the header:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight text-gray-900 mb-6">
    Basehor, Kansas Corporate Headshot Photography Services
</h1>
<p class="text-xl md:text-2xl text-gray-600 max-w-3xl mx-auto mb-8">
    Portraits telling the unique story of Basehor's businesses.
</p>
```

To modify:
1. Replace headline text between the `<h1>` tags
2. Update subtitle text between the `<p>` tags
3. Responsive text sizes are already set up:
   - `text-4xl`: Mobile devices
   - `md:text-5xl`: Medium screens
   - `lg:text-6xl`: Large screens

### Features and Benefits Sections
Each card in these sections follows this structure:

```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition duration-300">
    <h3 class="text-xl font-semibold mb-4">Title Here</h3>
    <p class="text-gray-600">Description text here.</p>
</div>
```

To update:
1. Locate the section you want to modify (id="features" or id="benefits")
2. Find the specific card div
3. Update the text between `<h3>` and `<p>` tags
4. Keep the existing classes to maintain styling

## Managing Links

### Navigation Menu Links
Current navigation links are in the header:

```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">FAQ</a>
    <a href="https://www.101headshots.com" class="inline-flex items-center px-4 py-2 border border-transparent text-sm font-medium rounded-md text-white bg-blue-600 hover:bg-blue-700 transition-colors duration-300">Book Now</a>
</div>
```

To update links:
1. Internal links (starting with #): Match with section IDs
2. External links (starting with https://): Replace with your desired URL
3. Maintain the class structure for consistent styling

### Call-to-Action Buttons
Located in hero and bottom sections:

```html
<a href="https://www.101headshots.com" class="inline-flex items-center px-8 py-3 border border-transparent text-lg font-medium rounded-md text-white bg-blue-600 hover:bg-blue-700 hover:scale-105 transform transition duration-300">
    Schedule Your Session
</a>
```

To update:
1. Change the `href` attribute to your booking page URL
2. Modify button text between the `<a>` tags
3. Keep all classes for proper styling and hover effects

## Adding Privacy and Terms Pages

### Footer Link Setup
Locate the Legal section in the footer:

```html
<div>
    <h3 class="text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common Issues and Solutions:

1. **Broken Internal Links**
   - Ensure section IDs match exactly (case-sensitive)
   - Example: `href="#FAQ"` won't work if section is `id="faq"`

2. **Responsive Design Issues**
   - Check for missing responsive classes (md: and lg: prefixes)
   - Example: `text-xl md:text-2xl lg:text-3xl`

3. **Style Inconsistencies**
   - Copy and paste existing class strings for similar elements
   - Don't remove `transition` or `duration` classes as they control animations

4. **External Links Not Working**
   - Verify full URLs including https://
   - Test links in a private browser window

Remember:
- Always backup before making changes
- Test on multiple devices and browsers
- Maintain consistent spacing and indentation
- Keep original class structure for proper styling

Need additional help? Contact your web developer or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).