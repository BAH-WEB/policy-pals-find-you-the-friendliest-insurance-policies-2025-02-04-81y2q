# PolicyPals Landing Page Maintenance Guide

This guide will help you maintain and customize the PolicyPals landing page. It's designed for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu:

```html
<div class="text-2xl font-bold text-blue-500">
    PolicyPals
</div>
```

To update:
1. Change "PolicyPals" to your company name
2. Adjust text size using `text-2xl` (options: `text-sm`, `text-lg`, `text-3xl`)
3. Change color using `text-blue-500` (options: `text-red-500`, `text-green-500`)

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Policy Pals Find You The Friendliest Insurance Policies
</h1>
```

To modify:
1. Update headline text between the `<h1>` tags
2. Adjust responsive text sizes:
   - Mobile: `text-4xl`
   - Tablet: `md:text-5xl`
   - Desktop: `lg:text-6xl`

### Features Section
Each feature card follows this structure:

```html
<div class="bg-gray-700 rounded-xl p-8 hover:transform hover:scale-105">
    <div class="text-blue-500 text-4xl mb-4">
        <i class="fas fa-user-check"></i>
    </div>
    <h3 class="text-xl font-semibold mb-4">Personalised Policy Matching</h3>
    <p class="text-gray-300">Advanced algorithms match you...</p>
</div>
```

To customize:
1. Change icon: Replace `fa-user-check` with any [Font Awesome icon](https://fontawesome.com/icons)
2. Update heading: Modify text in `<h3>` tags
3. Update description: Change text in `<p>` tags
4. Adjust colors: 
   - Background: `bg-gray-700`
   - Icon color: `text-blue-500`
   - Text color: `text-gray-300`

## Fixing Broken Links

### Navigation Menu Links
Current navigation structure:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="hover:text-blue-400">Features</a>
    <a href="#benefits" class="hover:text-blue-400">Benefits</a>
    <a href="#faq" class="hover:text-blue-400">FAQ</a>
    <a href="#contact" class="hover:text-blue-400">Contact</a>
</div>
```

To update internal links:
1. Locate the section ID you want to link to (e.g., `id="features"`)
2. Update the `href` attribute with `#` followed by the ID
3. Example: `<a href="#features">Features</a>`

### External Links
The "Get Started" button links:

```html
<a href="https://PolicyPals.Co.Uk" class="bg-blue-600">
    Get Started
</a>
```

To update:
1. Replace `https://PolicyPals.Co.Uk` with your website URL
2. Ensure the URL includes `https://` or `http://`
3. Test the link after updating

## Linking Privacy and Terms Pages

### Footer Legal Links
Located in the footer section:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-blue-400">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-blue-400">Terms of Service</a></li>
        <li><a href="#" class="text-gray-400 hover:text-blue-400">Cookie Policy</a></li>
    </ul>
</div>
```

To add policy pages:
1. Create your policy pages (e.g., `privacy.html`, `terms.html`)
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-blue-400">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-blue-400">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match exactly with href attributes
   - IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
   - Mobile classes: No prefix (e.g., `text-xl`)
   - Tablet classes: Start with `md:` (e.g., `md:text-2xl`)
   - Desktop classes: Start with `lg:` (e.g., `lg:text-3xl`)

3. **Icons Not Showing**
   - Verify Font Awesome link in header is working
   - Check icon class names on [Font Awesome website](https://fontawesome.com)
   - Ensure proper prefix: `fas` for solid icons, `fab` for brands

4. **Colors Not Updating**
   - Tailwind colors use format: `{type}-{color}-{shade}`
   - Types: `text`, `bg`, `border`
   - Colors: `blue`, `gray`, `red`, etc.
   - Shades: `100` to `900`
   - Example: `text-blue-500`

Remember to:
- Always test changes on multiple devices
- Keep a backup of the original code
- Use browser developer tools (F12) to inspect elements
- Maintain consistent styling across all pages