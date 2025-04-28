# Landing Page Maintenance Guide
## ComputerBril.org

This guide provides detailed instructions for maintaining and customizing the ComputerBril.org landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the site logo and navigation menu. To modify:

```html
<!-- Logo Text -->
<a href="/" class="text-2xl font-bold text-blue-600">ComputerBril.org</a>
```
- To change the logo text, simply replace "ComputerBril.org"
- Adjust size using `text-2xl` (options: text-sm, text-base, text-lg, text-2xl, text-3xl)
- Modify color using `text-blue-600` (options: text-[color]-[shade], e.g., text-red-500)

### Hero Section
Located at the top of the page with the main offer:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-8">
    Computerbril Met Blauwfilter
    <span class="block text-blue-600 mt-4">Tijdelijk 20% Korting!</span>
</h1>
```
- Update the main heading by changing "Computerbril Met Blauwfilter"
- Modify the promotional text within the `<span>` tag
- Responsive text sizes are defined as:
  - Mobile: `text-4xl`
  - Tablet: `md:text-5xl`
  - Desktop: `lg:text-6xl`

### Feature Cards
To modify feature cards in the features section:

```html
<div class="p-8 bg-white rounded-2xl shadow-lg hover:shadow-xl transition duration-300">
    <div class="text-blue-600 mb-4">
        <i class="fas fa-shield-alt text-3xl"></i>
    </div>
    <h3 class="text-xl font-bold mb-4">Maximale Bescherming</h3>
    <p class="text-gray-600">Nog maar 3 brillen beschikbaar...</p>
</div>
```
- Change icons by updating the Font Awesome class (e.g., `fa-shield-alt` to `fa-check`)
- Modify headings in the `<h3>` tag
- Update description text in the `<p>` tag

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Voordelen</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```

To update:
1. Internal links (starting with #) connect to section IDs on the same page
2. External links should include the full URL
3. Replace `href="#features"` with your desired destination
4. Ensure section IDs match exactly (case-sensitive)

### Call-to-Action Links
Update the shop links:

```html
<!-- Replace the URL in all CTA buttons -->
<a href="https://computerbril.org/winkel" class="px-8 py-4 bg-blue-600 text-white rounded-full">
    Bestel Nu
</a>
```

## Linking Privacy and Terms Pages

### Footer Links Section
Located in the footer's "Juridisch" section:

```html
<div>
    <h3 class="text-xl font-bold mb-4">Juridisch</h3>
    <ul class="space-y-2">
        <li><a href="privacy.html" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-blue-400 transition-colors duration-300">Algemene Voorwaarden</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the `href` attributes to point to these files
3. For subdirectories, use: `href="policies/privacy.html"`
4. For external policies, use the full URL: `href="https://example.com/privacy"`

## Troubleshooting

Common issues and solutions:

### Broken Internal Links
- Verify that section IDs match link hrefs exactly
- Example: `href="#features"` must match `id="features"`
- IDs are case-sensitive

### Responsive Design Issues
- Check viewport size classes:
  - Mobile (default): No prefix
  - Tablet: `md:`
  - Desktop: `lg:`
- Example: `text-4xl md:text-5xl lg:text-6xl`

### Missing Icons
- Verify Font Awesome inclusion in `<head>`
- Check icon class names at [Font Awesome](https://fontawesome.com/icons)
- Ensure proper class prefix (`fas`, `fab`, etc.)

Need additional help? Contact support@example.com for technical assistance.