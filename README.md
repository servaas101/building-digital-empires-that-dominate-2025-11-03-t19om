# Dormache Empire Landing Page - Maintenance & Customization Guide

A comprehensive guide for maintaining, updating, and customizing the Dormache Empire landing page. This document is designed for developers of all skill levels.

---

## Table of Contents

1. [Overview](#overview)
2. [File Structure](#file-structure)
3. [Updating Text Content](#updating-text-content)
4. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
5. [Fixing and Managing Links](#fixing-and-managing-links)
6. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
7. [Color and Theme Customization](#color-and-theme-customization)
8. [Responsive Design Adjustments](#responsive-design-adjustments)
9. [Troubleshooting Guide](#troubleshooting-guide)
10. [Best Practices](#best-practices)

---

## Overview

The Dormache Empire landing page is a modern, responsive website built with:
- **HTML5** for structure
- **Tailwind CSS** for styling (loaded via CDN)
- **Font Awesome** for icons
- **Vanilla JavaScript** for interactive features

The page includes:
- Sticky navigation header
- Hero section with animated background
- Features showcase
- Benefits section
- Testimonials
- FAQ accordion
- Call-to-action sections
- Footer with links

**Key Features:**
- Fully responsive (mobile, tablet, desktop)
- Dark theme with purple/pink gradient accents
- Interactive elements (mobile menu, FAQ accordion)
- Smooth scrolling navigation
- Professional animations and hover effects

---

## File Structure

### Current Setup

```
project-root/
├── index.html          (Main landing page - the file you have)
├── privacy.html        (To be created)
├── terms.html          (To be created)
├── blog.html           (Referenced in footer)
└── [optional] assets/
    ├── css/
    ├── js/
    └── images/
```

### Important Notes

- The page uses **Tailwind CSS via CDN**, so no separate CSS file is needed
- All styling is done directly in HTML using Tailwind classes
- JavaScript is embedded in the `<script>` tag at the bottom
- External resources (Font Awesome, Tailwind) require internet connection

---

## Updating Text Content

### Understanding the Page Structure

The landing page is divided into logical sections. Here's how to find and update text:

### 1. Header & Navigation Text

**Location:** Lines 14-15 (Company name in header)

```html
<span class="text-xl font-bold gradient-text">Dormache Empire</span>
```

**How to Update:**
1. Find this line in your `index.html` file
2. Replace `Dormache Empire` with your company name
3. Save the file and refresh your browser

**Navigation Links Text:**

**Location:** Lines 22-26 (Desktop menu items)

```html
<a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
<a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
<a href="#testimonials" class="text-gray-300 hover:text-white transition-colors duration-300">Testimonials</a>
<a href="#faq" class="text-gray-300 hover:text-white transition-colors duration-300">FAQ</a>
<a href="#about" class="text-gray-300 hover:text-white transition-colors duration-300">About</a>
```

**How to Update:**
1. Change the text between the `>` and `</a>` tags
2. Keep the `href="#"` attributes the same (they link to sections on the page)
3. Example: Change `Features` to `Our Services`

**Important:** The mobile menu (lines 42-49) contains the same links. Update both places to keep them consistent.

### 2. Hero Section (Main Title & Subtitle)

**Location:** Lines 81-95 (Hero content)

```html
<h1 class="text-4xl sm:text-5xl lg:text-7xl font-bold tracking-tight mb-6 leading-tight">
    <span class="block text-white">Building Digital</span>
    <span class="gradient-text block">Empires That Dominate</span>
</h1>

<p class="text-xl sm:text-2xl text-gray-300 mb-8 max-w-3xl mx-auto leading-relaxed">
    We Turn Your Vision Into a Digital Powerhouse
</p>

<p class="text-lg text-gray-400 mb-12 max-w-2xl mx-auto leading-relaxed">
    Transform your business with cutting-edge technology solutions that scale...
</p>
```

**How to Update:**

**For the Main Heading:**
1. The heading is split into two lines for styling purposes
2. Change `Building Digital` to your first line
3. Change `Empires That Dominate` to your second line (this one has the gradient color)
4. Keep the structure the same

**For the Subtitle (smaller text):**
1. Find `We Turn Your Vision Into a Digital Powerhouse`
2. Replace with your subtitle (keep it short - 5-10 words)

**For the Description (larger paragraph):**
1. Find the longer paragraph starting with `Transform your business...`
2. Replace with your description (2-3 sentences)

**Example Update:**
```html
<h1 class="text-4xl sm:text-5xl lg:text-7xl font-bold tracking-tight mb-6 leading-tight">
    <span class="block text-white">Your Company Name</span>
    <span class="gradient-text block">Leads Your Industry</span>
</h1>

<p class="text-xl sm:text-2xl text-gray-300 mb-8 max-w-3xl mx-auto leading-relaxed">
    Innovative Solutions for Modern Challenges
</p>

<p class="text-lg text-gray-400 mb-12 max-w-2xl mx-auto leading-relaxed">
    Discover how our cutting-edge platform helps businesses streamline operations and achieve growth.
</p>
```

### 3. Hero Section Buttons

**Location:** Lines 98-107

```html
<a href="https://dormacheempire.com/contact" class="cta-button px-8 py-4 rounded-lg text-white font-bold text-lg">
    Start Your Transformation
</a>
<button class="px-8 py-4 rounded-lg border-2 border-purple-500 text-purple-400 font-bold text-lg hover:bg-purple-500 hover:text-white transition-all duration-300">
    Watch Demo
</button>
```

**How to Update:**
1. Change `Start Your Transformation` to your button text
2. Change `Watch Demo` to your secondary button text
3. Update the `href="https://dormacheempire.com/contact"` to your contact page URL

### 4. Features Section

**Location:** Lines 119-200 (Three feature cards)

Each feature card follows this structure:

```html
<div class="feature-card p-8 rounded-xl hover-lift">
    <div class="w-14 h-14 bg-gradient-to-r from-purple-500 to-pink-500 rounded-lg flex items-center justify-center mb-6">
        <i class="fas fa-code text-white text-2xl"></i>
    </div>
    <h3 class="text-2xl font-bold mb-4">Custom Web Development</h3>
    <p class="text-gray-300 mb-4 leading-relaxed">
        Bespoke web solutions tailored to your unique business requirements...
    </p>
    <ul class="space-y-2 text-gray-400">
        <li class="flex items-center"><i class="fas fa-check text-purple-500 mr-3"></i>Responsive Design</li>
        <li class="flex items-center"><i class="fas fa-check text-purple-500 mr-3"></i>SEO Optimized</li>
        <li class="flex items-center"><i class="fas fa-check text-purple-500 mr-3"></i>Fast Loading</li>
    </ul>
</div>
```

**How to Update Each Card:**

**Step 1: Change the Icon**
- Find `<i class="fas fa-code text-white text-2xl"></i>`
- Visit [Font Awesome Icons](https://fontawesome.com/icons) to find icon names
- Replace `fa-code` with your chosen icon (e.g., `fa-rocket`, `fa-star`, `fa-database`)
- Example: `<i class="fas fa-rocket text-white text-2xl"></i>`

**Step 2: Change the Title**
- Find `<h3 class="text-2xl font-bold mb-4">Custom Web Development</h3>`
- Replace `Custom Web Development` with your feature title

**Step 3: Change the Description**
- Find the paragraph starting with `Bespoke web solutions...`
- Replace with your feature description (2-3 sentences)

**Step 4: Update the Bullet Points**
- Change each `<li>` item text
- You can add more or fewer items by copying/deleting `<li>` lines
- Keep the `<i class="fas fa-check text-purple-500 mr-3"></i>` structure

**Example Update:**
```html
<div class="feature-card p-8 rounded-xl hover-lift">
    <div class="w-14 h-14 bg-gradient-to-r from-purple-500 to-pink-500 rounded-lg flex items-center justify-center mb-6">
        <i class="fas fa-mobile text-white text-2xl"></i>
    </div>
    <h3 class="text-2xl font-bold mb-4">Mobile App Development</h3>
    <p class="text-gray-300 mb-4 leading-relaxed">
        Create powerful iOS and Android applications that engage users and drive business growth.
    </p>
    <ul class="space-y-2 text-gray-400">
        <li class="flex items-center"><i class="fas fa-check text-purple-500 mr-3"></i>Native Performance</li>
        <li class="flex items-center"><i class="fas fa-check text-purple-500 mr-3"></i>Cross-Platform</li>
        <li class="flex items-center"><i class="fas fa-check text-purple-500 mr-3"></i>App Store Ready</li>
    </ul>
</div>
```

### 5. Benefits Section

**Location:** Lines 219-300 (Three benefit cards)

Each benefit card has this structure:

```html
<div class="bg-gradient-to-br from-gray-700 to-gray-800 p-8 rounded-xl border border-purple-500 border-opacity-20 hover:border-opacity-50 transition-all duration-300 hover:shadow-lg hover:shadow-purple-500/20">
    <div class="flex items-start mb-6">
        <div class="w-12 h-12 bg-purple-500 rounded-lg flex items-center justify-center flex-shrink-0">
            <i class="fas fa-rocket text-white text-xl"></i>
        </div>
        <h3 class="text-2xl font-bold ml-4">Boost Your Online Presence</h3>
    </div>
    <p class="text-gray-300 leading-relaxed mb-4">
        Dominate search results and social media...
    </p>
    <div class="space-y-3">
        <p class="flex items-center text-gray-300"><i class="fas fa-star text-yellow-400 mr-3"></i>Increased brand visibility</p>
        <p class="flex items-center text-gray-300"><i class="fas fa-star text-yellow-400 mr-3"></i>Higher conversion rates</p>
    </div>
</div>
```

**How to Update:**

**Step 1: Change the Icon**
- Find `<i class="fas fa-rocket text-white text-xl"></i>`
- Replace `fa-rocket` with your icon (e.g., `fa-chart-line`, `fa-clock`, `fa-shield`)

**Step 2: Change the Title**
- Find `<h3 class="text-2xl font-bold ml-4">Boost Your Online Presence</h3>`
- Replace with your benefit title

**Step 3: Change the Description**
- Replace the paragraph text with your benefit description

**Step 4: Update the Benefit Points**
- Change each line's text (the part after `</i>`)
- Add or remove lines by copying/deleting `<p class="flex items-center...">` lines

### 6. Testimonials Section

**Location:** Lines 348-400 (Customer testimonials)

Each testimonial follows this pattern:

```html
<div class="testimonial-card p-8 rounded-xl">
    <div class="flex items-center mb-4">
        <div class="w-12 h-12 bg-gradient-to-r from-purple-500 to-pink-500 rounded-full flex items-center justify-center">
            <span class="text-white font-bold">JM</span>
        </div>
        <div class="ml-4">
            <p class="font-bold text-white">James Mitchell</p>
            <p class="text-gray-400 text-sm">CEO, TechVenture Solutions</p>
        </div>
    </div>
    <div class="flex mb-4">
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
    </div>
    <p class="text-gray-300 leading-relaxed">
        "Dormache Empire completely transformed our digital infrastructure..."
    </p>
</div>
```

**How to Update:**

**Step 1: Change Customer Initials**
- Find `<span class="text-white font-bold">JM</span>`
- Replace `JM` with customer's initials (2 letters)

**Step 2: Change Customer Name**
- Find `<p class="font-bold text-white">James Mitchell</p>`
- Replace with actual customer name

**Step 3: Change Customer Title/Company**
- Find `<p class="text-gray-400 text-sm">CEO, TechVenture Solutions</p>`
- Replace with their actual title and company

**Step 4: Adjust Star Rating**
- Count the `<i class="fas fa-star text-yellow-400"></i>` lines
- Remove stars for lower ratings (copy the entire line and delete)
- Add more for perfect ratings

**Step 5: Change Testimonial Text**
- Find the quoted paragraph
- Replace with the actual customer testimonial
- Keep the opening and closing quotation marks

### 7. FAQ Section

**Location:** Lines 471-560 (Five FAQ items)

Each FAQ item has this structure:

```html
<div class="faq-item bg-gradient-to-r from-gray-800 to-gray-700 rounded-lg border border-purple-500 border-opacity-20">
    <div class="faq-question p-6 flex items-center justify-between">
        <h3 class="text-lg font-semibold text-white">What makes Dormache Empire different from other digital agencies?</h3>
        <i class="faq-icon fas fa-chevron-down text-purple-500"></i>
    </div>
    <div class="faq-answer hidden px-6 pb-6">
        <p class="text-gray-300 leading-relaxed">
            Dormache Empire stands out through our unique combination of expertise...
        </p>
    </div>
</div>
```

**How to Update:**

**Step 1: Change the Question**
- Find the `<h3>` tag with the question text
- Replace with your FAQ question

**Step 2: Change the Answer**
- Find the `<p>` tag inside `faq-answer`
- Replace with your answer text
- You can add multiple paragraphs by adding more `<p>` tags

**Step 3: Add or Remove FAQ Items**
- To add a new FAQ: Copy an entire `faq-item` div and paste it below
- To remove: Delete the entire `faq-item` div
- Update the question and answer for each

**Example New FAQ:**
```html
<div class="faq-item bg-gradient-to-r from-gray-800 to-gray-700 rounded-lg border border-purple-500 border-opacity-20">
    <div class="faq-question p-6 flex items-center justify-between">
        <h3 class="text-lg font-semibold text-white">Can I integrate this with my existing systems?</h3>
        <i class="faq-icon fas fa-chevron-down text-purple-500"></i>
    </div>
    <div class="faq-answer hidden px-6 pb-6">
        <p class="text-gray-300 leading-relaxed">
            Yes, our platform is designed to integrate seamlessly with your existing tools and systems.
        </p>
    </div>
</div>
```

### 8. About Section

**Location:** Lines 413-470

```html
<p class="text-lg text-gray-300 leading-relaxed mb-6">
    Founded in 2018 by a team of visionary technologists...
</p>

<p class="text-lg text-gray-300 leading-relaxed">
    Today, our mission remains unwavering...
</p>
```

**How to Update:**
1. Find the two paragraphs in the About section
2. Replace with your company story
3. Keep the styling classes the same

**Statistics Section** (Lines 449-465):
```html
<div class="text-center">
    <p class="text-4xl font-bold gradient-text mb-2">500+</p>
    <p class="text-gray-400">Satisfied Clients</p>
</div>
```

Update the numbers and labels to match your company statistics.

### 9. Footer Content

**Location:** Lines 587-650 (Footer sections)

**Company Info:**
```html
<p class="text-gray-400 text-sm leading-relaxed">
    Building digital empires that dominate. Transform your vision into a digital powerhouse...
</p>
```

**Footer Links:**
- Update text in `<a>` tags under Services, Company, and Legal sections
- Keep the `href` attributes pointing to correct pages

---

## Modifying Tailwind CSS Classes

### Understanding Tailwind CSS

Tailwind CSS is a utility-first framework where styling is done with small, single-purpose classes. You don't need a separate CSS file—all styling is in the HTML.

### Common Tailwind Classes on This Page

| Class | Purpose | Example |
|-------|---------|---------|
| `text-white` | White text color | `<p class="text-white">` |
| `text-gray-300` | Light gray text | `<p class="text-gray-300">` |
| `bg-gray-900` | Dark gray background | `<section class="bg-gray-900">` |
| `px-4` | Padding left/right (4 units) | `<div class="px-4">` |
| `py-24` | Padding top/bottom (24 units) | `<section class="py-24">` |
| `mb-6` | Margin bottom (6 units) | `<h1 class="mb-6">` |
| `text-4xl` | Font size (4xl) | `<h1 class="text-4xl">` |
| `font-bold` | Bold text | `<h1 class="font-bold">` |
| `rounded-lg` | Rounded corners | `<button class="rounded-lg">` |
| `hover:text-white` | White text on hover | `<a class="hover:text-white">` |
| `transition-colors` | Smooth color transitions | `<a class="transition-colors">` |
| `duration-300` | Animation duration (300ms) | `<a class="duration-300">` |

### Text Color Changes

**Current Color Scheme:**
- Primary Text: `text-white`
- Secondary Text: `text-gray-300`
- Tertiary Text: `text-gray-400`
- Accent Color: Purple/Pink gradient

**How to Change Text Colors:**

**Example 1: Change a heading from white to light gray**

Before:
```html
<h2 class="text-4xl font-bold text-white mb-4">Powerful Features That Drive Results</h2>
```

After:
```html
<h2 class="text-4xl font-bold text-gray-300 mb-4">Powerful Features That Drive Results</h2>
```

**Available Text Colors in Tailwind:**
- `text-white` - Pure white
- `text-gray-100` - Very light gray
- `text-gray-300` - Light gray
- `text-gray-400` - Medium gray
- `text-gray-500` - Darker gray
- `text-purple-500` - Purple
- `text-pink-500` - Pink
- `text-blue-500` - Blue
- `text-red-500` - Red
- `text-yellow-400` - Yellow

### Background Color Changes

**Current Backgrounds:**
- Main: `bg-gray-900` (dark)
- Secondary: `bg-gray-800` (slightly lighter)
- Accent sections: `bg-purple-900` or `bg-pink-900`

**How to Change Background Colors:**

Example: Change hero section background

Before:
```html
<section class="relative min-h-screen flex items-center justify-center overflow-hidden bg-gray-900">
```

After:
```html
<section class="relative min-h-screen flex items-center justify-center overflow-hidden bg-blue-900">
```

### Font Size Changes

**Current Sizes:**
- `text-4xl` - Large headings
- `text-5xl` - Larger headings
- `text-7xl` - Hero title
- `text-2xl` - Feature titles
- `text-lg` - Body text
- `text-xl` - Slightly larger body

**How to Change Font Sizes:**

Before:
```html
<h1 class="text-7xl font-bold">Building Digital Empires That Dominate</h1>
```

After (make smaller):
```html
<h1 class="text-5xl font-bold">Building Digital Empires That Dominate</h1>
```

**Available Sizes:**
- `text-xs`, `text-sm`, `text-base`, `text-lg`, `text-xl`
- `text-2xl`, `text-3xl`, `text-4xl`, `text-5xl`, `text-6xl`, `text-7xl`, `text-8xl`, `text-9xl`

### Spacing (Padding & Margin) Changes

**How to Adjust Spacing:**

The number in padding/margin classes represents units (1 unit = 0.25rem = 4px)

- `p-4` = 4 × 4px = 16px padding all sides
- `px-8` = 8 × 4px = 32px padding left/right
- `py-24` = 24 × 4px = 96px padding top/bottom
- `mb-6` = 6 × 4px = 24px margin bottom

**Example: Increase spacing in a section**

Before:
```html
<section class="py-24 bg-gray-900">
```

After (more spacing):
```html
<section class="py-32 bg-gray-900">
```

**Common Spacing Values:**
- `2`, `4`, `6`, `8`, `12`, `16`, `24`, `32`, `40`, `48`, `64`

### Responsive Design Classes

This page uses responsive prefixes to adjust styling for different screen sizes:

| Prefix | Screen Size |
|--------|------------|
| (none) | Mobile (default) |
| `sm:` | Small (640px and up) |
| `md:` | Medium (768px and up) |
| `lg:` | Large (1024px and up) |
| `xl:` | Extra Large (1280px and up) |

**Example: Text size changes by device**

```html
<h1 class="text-4xl sm:text-5xl lg:text-7xl font-bold">
    Building Digital Empires That Dominate
</h1>
```

This means:
- Mobile: `text-4xl` (36px)
- Tablet (sm): `text-5xl` (48px)
- Desktop (lg): `text-7xl` (48px)

### Hover Effects

**Common Hover Classes:**

Before:
```html
<a class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
```

This means:
- Default: Gray text (`text-gray-300`)
- On hover: White text (`hover:text-white`)
- Animation: Smooth color transition (`transition-colors duration-300`)

**How to Modify Hover Effects:**

Change hover color:
```html
<a class="text-gray-300 hover:text-purple-500 transition-colors duration-300">Features</a>
```

Add scale effect on hover:
```html
<button class="px-8 py-4 hover:scale-105 transition-transform duration-300">Click Me</button>
```

### Gradient Text

**Current Gradient:**
```html
<span class="gradient-text">Empires That Dominate</span>
```

This uses a custom CSS class (lines 12-16):
```css
.gradient-text {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
}
```

**How to Change Gradient Colors:**

In the `<style>` section (around line 12), modify the hex colors:

Before:
```css
.gradient-text {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    ...
}
```

After (blue to purple):
```css
.gradient-text {
    background: linear-gradient(135deg, #3b82f6 0%, #8b5cf6 100%);
    ...
}
```

**Common Color Hex Codes:**
- Purple: `#667eea`, `#8b5cf6`
- Pink: `#764ba2`, `#ec4899`
- Blue: `#3b82f6`, `#06b6d4`
- Green: `#10b981`, `#34d399`
- Orange: `#f97316`, `#fb923c`

### Box Shadows and Glows

**Current Shadow Classes:**

```html
<div class="glow-effect">...</div>
```

This uses custom CSS (lines 17-19):
```css
.glow-effect {
    box-shadow: 0 0 30px rgba(102, 126, 234, 0.3);
}
```

**How to Change Shadow Intensity:**

Increase glow:
```css
.glow-effect {
    box-shadow: 0 0 50px rgba(102, 126, 234, 0.5);
}
```

The values mean:
- `0 0 30px` = blur radius (30px)
- `rgba(102, 126, 234, 0.3)` = color and opacity (0.3 = 30% opacity)

---

## Fixing and Managing Links

### Understanding Links in This Page

The landing page has three types of links:

1. **Internal Navigation Links** - Jump to sections on the same page
2. **External Links** - Go to external websites
3. **Contact/CTA Links** - Direct to contact page or external site

### Identifying All Links

**Navigation Links (Header)**

Location: Lines 22-26 (Desktop) and 42-49 (Mobile)

```html
<a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
<a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
<a href="#testimonials" class="text-gray-300 hover:text-white transition-colors duration-300">Testimonials</a>
<a href="#faq" class="text-gray-300 hover:text-white transition-colors duration-300">FAQ</a>
<a href="#about" class="text-gray-300 hover:text-white transition-colors duration-300">About</a>
```

**Current Status:** ✅ These work correctly (they link to sections with matching IDs)

**CTA Links (Call-to-Action Buttons)**

Location: Lines 29, 50, 108, 312, 530

```html
<a href="https://dormacheempire.com/contact" class="cta-button px-6 py-2 rounded-lg text-white font-semibold">
    Get Started
</a>
```

**Current Status:** ⚠️ These need updating with your actual contact page URL

**Footer Links**

Location: Lines 600-625

```html
<a href="blog.html" class="text-gray-400 hover:text-white transition-colors duration-300">Blog</a>
<a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
```

**Current Status:** ⚠️ These files need to be created

**Social Media Links**

Location: Lines 627-641

```html
<a href="#" class="w-10 h-10 bg-gray-800 rounded-lg flex items-center justify-center hover:bg-purple-500 transition-colors duration-300">
    <i class="fab fa-facebook-f text-white"></i>
</a>
```

**Current Status:** ⚠️ These are placeholder links (`href="#"`) and need updating

### Step-by-Step: Updating CTA Links

**What are CTA Links?**
CTA stands for "Call-To-Action." These are buttons/links that encourage users to take action (like contacting you).

**Current CTA Links to Update:**

1. **Header "Get Started" button** (Line 29)
2. **Mobile menu "Get Started" button** (Line 50)
3. **Hero section "Start Your Transformation" button** (Line 108)
4. **Middle CTA "Schedule Your Free Consultation"** (Line 312)
5. **Final CTA "Get Started Now"** (Line 530)

**How to Update Each One:**

**Step 1: Find the link**

Search for: `https://dormacheempire.com/contact`

All instances will be highlighted.

**Step 2: Determine your contact URL**

Options:
- If you have a contact form page: `contact.html` or `contact/index.html`
- If you use an external service: `https://yourwebsite.com/contact`
- If you use a form service like Formspree: `https://formspree.io/f/YOUR_ID`

**Step 3: Replace the URL**

Example 1: Replace with local contact page
```html
<!-- Before -->
<a href="https://dormacheempire.com/contact" class="cta-button px-6 py-2 rounded-lg text-white font-semibold">
    Get Started
</a>

<!-- After -->
<a href="contact.html" class="cta-button px-6 py-2 rounded-lg text-white font-semibold">
    Get Started
</a>
```

Example 2: Replace with external contact form
```html
<!-- Before -->
<a href="https://dormacheempire.com/contact" class="cta-button px-6 py-2 rounded-lg text-white font-semibold">
    Get Started
</a>

<!-- After -->
<a href="https://yourcompany.com/contact" class="cta-button px-6 py-2 rounded-lg text-white font-semibold">
    Get Started
</a>
```

**Step 4: Update ALL instances**

Use your text editor's "Find and Replace" feature:

**In VS Code:**
1. Press `Ctrl+H` (Windows/Linux) or `Cmd+H` (Mac)
2. Find: `https://dormacheempire.com/contact`
3. Replace with: Your new URL
4. Click "Replace All"

**Step 5: Verify**

1. Save the file
2. Open the page in your browser
3. Click each button to confirm it goes to the correct page

### Step-by-Step: Updating Email Links

**Location:** Line 531 (Footer email)

```html
<a href="mailto:info@dormacheempire.com" class="hover:underline">info@dormacheempire.com</a>
```

**How to Update:**

1. Replace `info@dormacheempire.com` with your email address (appears twice)
2. Keep the `mailto:` part

**Example:**
```html
<!-- Before -->
<a href="mailto:info@dormacheempire.com" class="hover:underline">info@dormacheempire.com</a>

<!-- After -->
<a href="mailto:hello@yourcompany.com" class="hover:underline">hello@yourcompany.com</a>
```

### Step-by-Step: Updating Social Media Links

**Location:** Lines 627-641 (Footer social links)

```html
<a href="#" class="w-10 h-10 bg-gray-800 rounded-lg flex items-center justify-center hover:bg-purple-500 transition-colors duration-300">
    <i class="fab fa-facebook-f text-white"></i>
</a>
```

**Current Status:** All social links are placeholder (`href="#"`)

**How to Update:**

**Step 1: Find your social media URLs**

Get these from your social media profiles:
- Facebook: `https://facebook.com/yourpage`
- Twitter: `https://twitter.com/yourhandle`
- LinkedIn: `https://linkedin.com/company/yourcompany`
- Instagram: `https://instagram.com/yourhandle`

**Step 2: Replace the href**

**Facebook:**
```html
<!-- Before -->
<a href="#" class="w-10 h-10 bg-gray-800 rounded-lg flex items-center justify-center hover:bg-purple-500 transition-colors duration-300">
    <i class="fab fa-facebook-f text-white"></i>
</a>

<!-- After -->
<a href="https://facebook.com/yourpage" class="w-10 h-10 bg-gray-800 rounded-lg flex items-center justify-center hover:bg-purple-500 transition-colors duration-300">
    <i class="fab fa-facebook-f text-white"></i>
</a>
```

**Twitter:**
```html
<a href="https://twitter.com/yourhandle" class="w-10 h-10 bg-gray-800 rounded-lg flex items-center justify-center hover:bg-purple-500 transition-colors duration-300">
    <i class="fab fa-twitter text-white"></i>
</a>
```

**LinkedIn:**
```html
<a href="https://linkedin.com/company/yourcompany" class="w-10 h-10 bg-gray-800 rounded-lg flex items-center justify-center hover:bg-purple-500 transition-colors duration-300">
    <i class="fab fa-linkedin-in text-white"></i>
</a>
```

**Instagram:**
```html
<a href="https://instagram.com/yourhandle" class="w-10 h-10 bg-gray-800 rounded-lg flex items-center justify-center hover:bg-purple-500 transition-colors duration-300">
    <i class="fab fa-instagram text-white"></i>
</a>
```

**Step 3: Add target="_blank"**

To open links in a new tab, add `target="_blank"`:

```html
<a href="https://facebook.com/yourpage" target="_blank" class="w-10 h-10 bg-gray-800 rounded-lg flex items-center justify-center hover:bg-purple-500 transition-colors duration-300">
    <i class="fab fa-facebook-f text-white"></i>
</a>
```

### Step-by-Step: Updating Footer Links

**Location:** Lines 600-625 (Footer navigation)

```html
<li><a href="blog.html" class="text-gray-400 hover:text-white transition-colors duration-300">Blog</a></li>
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

**Current Status:**
- ✅ `contact.html` - Exists (update this link)
- ⚠️ `blog.html` - Needs to be created
- ⚠️ `privacy.html` - Needs to be created
- ⚠️ `terms.html` - Needs to be created

**How to Update:**

**For existing pages:**
```html
<!-- Update contact link if your file is named differently -->
<li><a href="contact.html" class="text-gray-400 hover:text-white transition-colors duration-300">Contact</a></li>
```

**For external pages:**
```html
<!-- If blog is on external site -->
<li><a href="https://yourblog.com" class="text-gray-400 hover:text-white transition-colors duration-300">Blog</a></li>
```

### Link Best Practices

**1. Always Use Descriptive Text**
```html
<!-- ❌ Bad -->
<a href="contact.html">Click here</a>

<!-- ✅ Good -->
<a href="contact.html">Get in Touch</a>
```

**2. Add target="_blank" for External Links**
```html
<!-- Opens in new tab -->
<a href="https://external-site.com" target="_blank">Visit External Site</a>
```

**3. Keep Relative Paths for Internal Links**
```html
<!-- ✅ Good - works from any location -->
<a href="contact.html">Contact</a>

<!-- ⚠️ Avoid absolute paths -->
<a href="https://yoursite.com/contact.html">Contact</a>
```

**4. Test All Links After Updates**

Create a link testing checklist:
- [ ] All navigation links scroll to correct sections
- [ ] All CTA buttons go to contact page
- [ ] All social links open in new tab
- [ ] Email link opens email client
- [ ] Footer links work correctly

---

## Adding Privacy and Terms Pages

### Understanding Why You Need These Pages

Privacy Policy and Terms of Service are legal documents that:
- Explain how you collect and use user data
- Set expectations for how users can use your services
- Protect your business legally
- Build trust with users

### Step-by-Step: Create Privacy Policy Page

**Step 1: Create the File**

1. In the same folder as `index.html`, create a new file named `privacy.html`
2. Copy the basic structure from `index.html`

**Step 2: Create privacy.html**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Dormache Empire">
    <meta name="keywords" content="privacy, policy, data protection">
    <meta name="author" content="Dormache Empire">
    <title>Privacy Policy - Dormache Empire</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
        
        .gradient-text {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
    </style>
</head>
<body class="bg-gray-900 text-white">
    <!-- Header & Navigation (Copy from index.html) -->
    <header class="sticky top-0 z-50 bg-gray-900 border-b border-gray-800">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-r from-purple-500 to-pink-500 rounded-lg flex items-center justify-center">
                    <i class="fas fa-crown text-white font-bold"></i>
                </div>
                <span class="text-xl font-bold gradient-text">Dormache Empire</span>
            </div>
            
            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html" class="text-gray-300 hover:text-white transition-colors duration-300">Home</a>
                <a href="index.html#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
                <a href="index.html#about" class="text-gray-300 hover:text-white transition-colors duration-300">About</a>
            </div>
            
            <div class="hidden md:block">
                <a href="contact.html" class="bg-gradient-to-r from-purple-500 to-pink-500 px-6 py-2 rounded-lg text-white font-semibold hover:opacity-90 transition-opacity duration-300">
                    Contact
                </a>
            </div>
            
            <button class="md:hidden mobile-menu-button p-2 rounded-lg hover:bg-gray-800 transition-colors duration-300">
                <i class="fas fa-bars text-white text-xl"></i>
            </button>
            
            <div class="mobile-menu hidden absolute top-16 left-0 right-0 bg-gray-800 border-b border-gray-700 md:hidden">
                <div class="flex flex-col space-y-4 p-6">
                    <a href="index.html" class="text-gray-300 hover:text-white transition-colors duration-300">Home</a>
                    <a href="index.html#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
                    <a href="index.html#about" class="text-gray-300 hover:text-white transition-colors duration-300">About</a>
                    <a href="contact.html" class="bg-gradient-to-r from-purple-500 to-pink-500 px-6 py-2 rounded-lg text-white font-semibold text-center">
                        Contact
                    </a>
                </div>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-24 bg-gray-900">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-5xl font-bold mb-2">Privacy Policy</h1>
            <p class="text-gray-400 mb-12">Last updated: [Current Date]</p>
            
            <div class="prose prose-invert max-w-none">
                <h2 class="text-3xl font-bold mt-8 mb-4">1. Introduction</h2>
                <p class="text-gray-300 mb-6 leading-relaxed">
                    Dormache Empire ("we," "us," "our," or "Company") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website [yourwebsite.com] (the "Site").
                </p>

                <h2 class="text-3xl font-bold mt-8 mb-4">2. Information We Collect</h2>
                <p class="text-gray-300 mb-4 leading-relaxed">
                    We may collect information about you in a variety of ways. The information we may collect on the Site includes:
                </p>
                <ul class="text-gray-300 mb-6 leading-relaxed list-disc list-inside">
                    <li>Personal Data: Name, email address, phone number, company name</li>
                    <li>Device Information: Browser type, IP address, operating system</li>
                    <li>Usage Data: Pages visited, time spent on pages, links clicked</li>
                    <li>Communication Data: Messages you send us through contact forms</li>
                </ul>

                <h2 class="text-3xl font-bold mt-8 mb-4">3. Use of Your Information</h2>
                <p class="text-gray-300 mb-4 leading-relaxed">
                    Having accurate information about you permits us to provide you with a smooth, efficient, and customized experience. Specifically, we may use information collected about you via the Site to:
                </p>
                <ul class="text-gray-300 mb-6 leading-relaxed list-disc list-inside">
                    <li>Generate a personal profile about you so that future visits to the Site are personalized</li>
                    <li>Increase the efficiency and operation of the Site</li>
                    <li>Monitor and analyze usage and trends to improve your experience with the Site</li>
                    <li>Notify you of updates to the Site</li>
                    <li>Respond to your inquiries and customer service requests</li>
                </ul>

                <h2 class="text-3xl font-bold mt-8 mb-4">4. Disclosure of Your Information</h2>
                <p class="text-gray-300 mb-6 leading-relaxed">
                    We may share information we have collected about you in certain situations:
                </p>
                <ul class="text-gray-300 mb-6 leading-relaxed list-disc list-inside">
                    <li><strong>By Law or to Protect Rights:</strong> If required by law or if we believe in good faith that disclosure is necessary</li>
                    <li><strong>Third-Party Service Providers:</strong> We may share your information with vendors, consultants, and service providers</li>
                    <li><strong>Business Transfers:</strong> We may share or transfer your information in connection with a merger, sale, or acquisition</li>
                </ul>

                <h2 class="text-3xl font-bold mt-8 mb-4">5. Security of Your Information</h2>
                <p class="text-gray-300 mb-6 leading-relaxed">
                    We use administrative, technical, and physical security measures to protect your personal information. However, no method of transmission over the Internet or electronic storage is completely secure.
                </p>

                <h2 class="text-3xl font-bold mt-8 mb-4">6. Contact Us</h2>
                <p class="text-gray-300 mb-6 leading-relaxed">
                    If you have questions or comments about this Privacy Policy, please contact us at:
                </p>
                <p class="text-gray-300 leading-relaxed">
                    Email: <a href="mailto:privacy@dormacheempire.com" class="text-purple-400 hover:text-purple-300">privacy@dormacheempire.com</a>
                </p>
            </div>
        </div>
    </section>

    <!-- Footer (Copy from index.html) -->
    <footer class="bg-gray-900 border-t border-gray-800 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-12 mb-8">
                <div>
                    <div class="flex items-center space-x-2 mb-4">
                        <div class="w-10 h-10 bg-gradient-to-r from-purple-500 to-pink-500 rounded-lg flex items-center justify-center">
                            <i class="fas fa-crown text-white font-bold"></i>
                        </div>
                        <span class="text-xl font-bold gradient-text">Dormache Empire</span>
                    </div>
                    <p class="text-gray-400 text-sm leading-relaxed">
                        Building digital empires that dominate.
                    </p>
                </div>
                
                <div>
                    <h3 class="text-white font-bold mb-4">Quick Links</h3>
                    <ul class="space-y-2">
                        <li><a href="index.html" class="text-gray-400 hover:text-white transition-colors duration-300">Home</a></li>
                        <li><a href="index.html#features" class="text-gray-400 hover:text-white transition-colors duration-300">Features</a></li>
                        <li><a href="index.html#about" class="text-gray-400 hover:text-white transition-colors duration-300">About</a></li>
                    </ul>
                </div>
                
                <div>
                    <h3 class="text-white font-bold mb-4">Legal</h3>
                    <ul class="space-y-2">
                        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
                        <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
                    </ul>
                </div>
                
                <div>
                    <h3 class="text-white font-bold mb-4">Contact</h3>
                    <p class="text-gray-400 text-sm">
                        <a href="mailto:info@dormacheempire.com" class="hover:text-white transition-colors duration-300">info@dormacheempire.com</a>
                    </p>
                </div>
            </div>
            
            <div class="border-t border-gray-800 pt-8 text-center">
                <p class="text-gray-400 text-sm">
                    &copy; 2025 Dormache Empire. All rights reserved.
                </p>
            </div>
        </div>
    </footer>

    <!-- JavaScript -->
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const mobileMenuButton = document.querySelector('header nav .mobile-menu-button');
            const mobileMenu = document.querySelector('header nav .mobile-menu');
            
            if (mobileMenuButton && mobileMenu) {
                mobileMenuButton.addEventListener('click', () => {
                    mobileMenu.classList.toggle('hidden');
                    const icon = mobileMenuButton.querySelector('i');
                    if (icon) {
                        icon.classList.toggle('fa-bars');
                        icon.classList.toggle('fa-times');
                    }
                });

                const mobileMenuLinks = mobileMenu.querySelectorAll('a');
                mobileMenuLinks.forEach(link => {
                    link.addEventListener('click', () => {
                        mobileMenu.classList.add('hidden');
                        const icon = mobileMenuButton.querySelector('i');
                        if (icon) {
                            icon.classList.remove('fa-times');
                            icon.classList.add('fa-bars');
                        }
                    });
                });
            }
        });
    </script>
</body>
</html>
```

**Step 3: Customize the Privacy Policy**

Replace the placeholder content with your actual privacy policy:

1. Update `[Current Date]` with today's date
2. Replace `[yourwebsite.com]` with your actual website URL
3. Update email addresses to your company email
4. Customize each section based on your actual practices

**Tips for Writing Privacy Policy:**
- Be clear and specific about what data you collect
- Explain exactly how you use the data
- Mention any third-party tools (Google Analytics, email services, etc.)
- Explain user rights (how they can request data deletion)
- Keep it simple and avoid legal jargon

### Step-by-Step: Create Terms of Service Page

**Step 1: Create the File**

Create a new file named `terms.html` in the same folder as `index.html`

**Step 2: Create terms.html**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - Dormache Empire">
    <meta name="keywords" content="terms, service, agreement">
    <meta name="author" content="Dormache Empire">
    <title>Terms of Service - Dormache Empire</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
        
        .gradient-text {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
    </style>
</head>
<body class="bg-gray-900 text-white">
    <!-- Header & Navigation -->
    <header class="sticky top-0 z-50 bg-gray-900 border-b border-gray-800">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-r from-purple-500 to-pink-500 rounded-lg flex items-center justify-center">
                    <i class="fas fa-crown text-white font-bold"></i>
                </div>
                <span class="text-xl font-bold gradient-text">Dormache Empire</span>
            </div>
            
            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html" class="text-gray-300 hover:text-white transition-colors duration-300">Home</a>
                <a href="index.html#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
                <a href="index.html#about" class="text-gray-300 hover:text-white transition-colors duration-300">About</a>
            </div>
            
            <div class="hidden md:block">
                <a href="contact.html" class="bg-gradient-to-r from-purple-500 to-pink-500 px-6 py-2 rounded-lg text-white font-semibold hover:opacity-90 transition-opacity duration-300">
                    Contact
                </a>
            </div>
            
            <button class="md:hidden mobile-menu-button p-2 rounded-lg hover:bg-gray-800 transition-colors duration-300">
                <i class="fas fa-bars text-white text-xl"></i>
            </button>
            
            <div class="mobile-menu hidden absolute top-16 left-0 right-0 bg-gray-800 border-b border-gray-700 md:hidden">
                <div class="flex flex-col space-y-4 p-6">
                    <a href="index.html" class="text-gray-300 hover:text-white transition-colors duration-300">Home</a>
                    <a href="index.html#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
                    <a href="index.html#about" class="text-gray-300 hover:text-white transition-colors duration-300">About</a>
                    <a href="contact.html" class="bg-gradient-to-r from-purple-500 to-pink-500 px-6 py-2 rounded-lg text-white font-semibold text-center">
                        Contact
                    </a>
                </div>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-24 bg-gray-900">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-5xl font-bold mb-2">Terms of Service</h1>
            <p class="text-gray-400 mb-12">Last updated: [Current Date]</p>
            
            <div class="prose prose-invert max-w-none">
                <h2 class="text-3xl font-bold mt-8 mb-4">1. Agreement to Terms</h2>
                <p class="text-gray-300 mb-6 leading-relaxed">
                    By accessing and using this website, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                </p>

                <h2 class="text-3xl font-bold mt-8 mb-4">2. Use License</h2>
                <p class="text-gray-300 mb-4 leading-relaxed">
                    Permission is granted to temporarily download one copy of the materials (information or software) on Dormache Empire's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                </p>
                <ul class="text-gray-300 mb-6 leading-relaxed list-disc list-inside">
                    <li>Modifying or copying the materials</li>
                    <li>Using the materials for any commercial purpose or for any public display</li>
                    <li>Attempting to decompile or reverse engineer any software contained on the website</li>
                    <li>Removing any copyright or other proprietary notations from the materials</li>
                    <li>Transferring the materials to another person or "mirroring" the materials on any other server</li>
                </ul>

                <h2 class="text-3xl font-bold mt-8 mb-4">3. Disclaimer</h2>
                <p class="text-gray-300 mb-6 leading-relaxed">
                    The materials on Dormache Empire's website are provided on an 'as is' basis. Dormache Empire makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                </p>

                <h2 class="text-3xl font-bold mt-8 mb-4">4. Limitations</h2>
                <p class="text-gray-300 mb-6 leading-relaxed">
                    In no event shall Dormache Empire or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on Dormache Empire's website.
                </p>

                <h2 class="text-3xl font-bold mt-8 mb-4">5. Accuracy of Materials</h2>
                <p class="text-gray-300 mb-6 leading-relaxed">
                    The materials appearing on Dormache Empire's website could include technical, typographical, or photographic errors. Dormache Empire does not warrant that any of the materials on its website are accurate, complete, or current. Dormache Empire may make changes to the materials contained on its website at any time without notice.
                </p>

                <h2 class="text-3xl font-bold mt-8 mb-4">6. Links</h2>
                <p class="text-gray-300 mb-6 leading-relaxed">
                    Dormache Empire has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by Dormache Empire of the site. Use of any such linked website is at the user's own risk.
                </p>

                <h2 class="text-3xl font-bold mt-8 mb-4">7. Modifications</h2>
                <p class="text-gray-300 mb-6 leading-relaxed">
                    Dormache Empire may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                </p>

                <h2 class="text-3xl font-bold mt-8 mb-4">8. Governing Law</h2>
                <p class="text-gray-300 mb-6 leading-relaxed">
                    These terms and conditions are governed by and construed in accordance with the laws of [Your Country/State] and you irrevocably submit to the exclusive jurisdiction of the courts located in that location.
                </p>

                <h2 class="text-3xl font-bold mt-8 mb-4">9. Contact Information</h2>
                <p class="text-gray-300 mb-6 leading-relaxed">
                    If you have any questions about these Terms of Service, please contact us at:
                </p>
                <p class="text-gray-300 leading-relaxed">
                    Email: <a href="mailto:legal@dormacheempire.com" class="text-purple-400 hover:text-purple-300">legal@dormacheempire.com</a>
                </p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 border-t border-gray-800 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-12 mb-8">
                <div>
                    <div class="flex items-center space-x-2 mb-4">
                        <div class="w-10 h-10 bg-gradient-to-r from-purple-500 to-pink-500 rounded-lg flex items-center justify-center">
                            <i class="fas fa-crown text-white font-bold"></i>
                        </div>
                        <span class="text-xl font-bold gradient-text">Dormache Empire</span>
                    </div>
                    <p class="text-gray-400 text-sm leading-relaxed">
                        Building digital empires that dominate.
                    </p>
                </div>
                
                <div>
                    <h3 class="text-white font-bold mb-4">Quick Links</h3>
                    <ul class="space-y-2">
                        <li><a href="index.html" class="text-gray-400 hover:text-white transition-colors duration-300">Home</a></li>
                        <li><a href="index.html#features" class="text-gray-400 hover:text-white transition-colors duration-300">Features</a></li>
                        <li><a href="index.html#about" class="text-gray-400 hover:text-white transition-colors duration-300">About</a></li>
                    </ul>
                </div>
                
                <div>
                    <h3 class="text-white font-bold mb-4">Legal</h3>
                    <ul class="space-y-2">
                        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
                        <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
                    </ul>
                </div>
                
                <div>
                    <h3 class="text-white font-bold mb-4">Contact</h3>
                    <p class="text-gray-400 text-sm">
                        <a href="mailto:info@dormacheempire.com" class="hover:text-white transition-colors duration-300">info@dormacheempire.com</a>
                    </p>
                </div>
            </div>
            
            <div class="border-t border-gray-800 pt-8 text-center">
                <p class="text-gray-400 text-sm">
                    &copy; 2025 Dormache Empire. All rights reserved.
                </p>
            </div>
        </div>
    </footer>

    <!-- JavaScript -->
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const mobileMenuButton = document.querySelector('header nav .mobile-menu-button');
            const mobileMenu = document.querySelector('header nav .mobile-menu');
            
            if (mobileMenuButton && mobileMenu) {
                mobileMenuButton.addEventListener('click', () => {
                    mobileMenu.classList.toggle('hidden');
                    const icon = mobileMenuButton.querySelector('i');
                    if (icon) {
                        icon.classList.toggle('fa-bars');
                        icon.classList.toggle('fa-times');
                    }
                });

                const mobileMenuLinks = mobileMenu.querySelectorAll('a');
                mobileMenuLinks.forEach(link => {
                    link.addEventListener('click', () => {
                        mobileMenu.classList.add('hidden');
                        const icon = mobileMenuButton.querySelector('i');
                        if (icon) {
                            icon.classList.remove('fa-times');
                            icon.classList.add('fa-bars');
                        }
                    });
                });
            }
        });
    </script>
</body>
</html>
```

**Step 3: Customize the Terms of Service**

1. Update `[Current Date]` with today's date
2. Update `[Your Country/State]` with your jurisdiction
3. Customize each section based on your business practices
4. Update email addresses to your company email

### Step 4: Update index.html Footer Links

Now that you have created `privacy.html` and `terms.html`, verify the links in your `index.html` footer are correct.

**Location:** Lines 620-621 (Footer legal links)

```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

**Verify:**
- ✅ These links are already correct in your `index.html`
- ✅ The files `privacy.html` and `terms.html` now exist
- ✅ Links will work when you save and test

### Step 5: Test the Links

1. Save all three files (`index.html`, `privacy.html`, `terms.html`) in the same folder
2. Open `index.html` in your browser
3. Scroll to the footer
4. Click on "Privacy Policy" - should open `privacy.html`
5. Click on "Terms of Service" - should open `terms.html`
6. On the policy pages, click "Home" to return to `index.html`

### File Structure After Adding Pages

```
project-root/
├── index.html          ✅ Main landing page (already exists)
├── privacy.html        ✅ New - Privacy policy page
├── terms.html          ✅ New - Terms of service page
├── contact.html        (Create if you don't have this)
└── blog.html           (Optional - for blog link in footer)
```

### Best Practices for Legal Pages

**1. Keep Them Updated**
- Review annually
- Update when business practices change
- Update when laws change

**2. Make Them Accessible**
- Link from footer (✅ Already done)
- Link from header (optional)
- Use clear language

**3. Customize for Your Business**
- Don't use generic templates
- Specify what data you actually collect
- Explain your actual practices

**4. Consider Legal Review**
- Have a lawyer review your policies
- Especially important for sensitive industries
- Protects your business legally

---

## Color and Theme Customization

### Understanding the Current Color Scheme

The landing page uses:
- **Dark background:** `#111827` (gray-900)
- **Accent color:** Purple/Pink gradient
- **Text colors:** White and various grays

### Changing the Primary Color Scheme

**Current Gradient (Purple to Pink):**
```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

**Step 1: Locate All Color References**

The purple/pink gradient appears in several places:

1. **Custom CSS gradient** (Line 12-16)
2. **Icon backgrounds** (multiple locations)
3. **Button backgrounds** (multiple locations)
4. **Border colors** (multiple locations)
5. **Hover effects** (multiple locations)

**Step 2: Choose Your New Colors**

**Option 1: Blue Gradient**
```css
background: linear-gradient(135deg, #3b82f6 0%, #1e40af 100%);
```

**Option 2: Green Gradient**
```css
background: linear-gradient(135deg, #10b981 0%, #059669 100%);
```

**Option 3: Orange Gradient**
```css
background: linear-gradient(135deg, #f97316 0%, #ea580c 100%);
```

**Option 4: Red Gradient**
```css
background: linear-gradient(135deg, #ef4444 0%, #dc2626 100%);
```

**Step 3: Update the Gradient**

Find this section in your `<style>` tag (around line 12):

```css
.gradient-text {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
}
```

Replace with your new gradient. Example for blue:

```css
.gradient-text {
    background: linear-gradient(135deg, #3b82f6 0%, #1e40af 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
}
```

**Step 4: Update Icon Backgrounds**

Find all instances of:
```html
<div class="w-14 h-14 bg-gradient-to-r from-purple-500 to-pink-500 rounded-lg flex items-center justify-center mb-6">
```

Replace `from-purple-500 to-pink-500` with your colors. Example for blue:

```html
<div class="w-14 h-14 bg-gradient-to-r from-blue-500 to-blue-700 rounded-lg flex items-center justify-center mb-6">
```

**Tailwind Color Pairs:**
- Blue: `from-blue-500 to-blue-700`
- Green: `from-green-500 to-green-700`
- Orange: `from-orange-500 to-orange-700`
- Red: `from-red-500 to-red-700`

**Step 5: Update Button Backgrounds**

Find all instances of:
```html
<a class="cta-button px-6 py-2 rounded-lg text-white font-semibold">
```

The `.cta-button` class uses the gradient from your CSS. It will automatically update when you change the gradient.

**Step 6: Update Border Colors**

Find instances of:
```html
<div class="border border-purple-500 border-opacity-20">
```

Replace `border-purple-500` with your color. Example for blue:

```html
<div class="border border-blue-500 border-opacity-20">
```

**Step 7: Update Hover Effects**

Find instances of:
```html
<a class="hover:bg-purple-500">
```

Replace `hover:bg-purple-500` with your color. Example for blue:

```html
<a class="hover:bg-blue-500">
```

### Changing Background Colors

**Current Backgrounds:**
- Main sections: `bg-gray-900`
- Secondary sections: `bg-gray-800`
- Accent sections: `bg-purple-900` or `bg-pink-900`

**How to Change:**

**Example: Change main background from dark gray to dark blue**

Find:
```html
<section class="py-24 bg-gray-900">
```

Replace with:
```html
<section class="py-24 bg-blue-900">
```

**Available Dark Background Colors:**
- `bg-gray-900` - Current dark gray
- `bg-slate-900` - Slate gray
- `bg-blue-900` - Dark blue
- `bg-purple-900` - Dark purple
- `bg-indigo-900` - Dark indigo

### Creating a Complete Color Theme

**Example: Change from Purple/Pink to Teal/Cyan**

**Step 1: Update CSS Gradient**
```css
.gradient-text {
    background: linear-gradient(135deg, #14b8a6 0%, #0891b2 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
}

.glow-effect {
    box-shadow: 0 0 30px rgba(20, 184, 166, 0.3);
}
```

**Step 2: Find and Replace All Colors**

Use "Find and Replace" in your editor:

| Find | Replace |
|------|---------|
| `from-purple-500 to-pink-500` | `from-teal-500 to-cyan-500` |
| `border-purple-500` | `border-teal-500` |
| `hover:bg-purple-500` | `hover:bg-teal-500` |
| `text-purple-500` | `text-teal-500` |
| `text-purple-400` | `text-teal-400` |

**Step 3: Update Glow Effects**

Find:
```css
.glow-effect {
    box-shadow: 0 0 30px rgba(102, 126, 234, 0.3);
}
```

Replace with:
```css
.glow-effect {
    box-shadow: 0 0 30px rgba(20, 184, 166, 0.3);
}
```

### Color Palette Reference

**Tailwind Color Names:**
- `gray`, `slate`, `zinc`, `neutral`, `stone`
- `red`, `orange`, `amber`, `yellow`, `lime`, `green`
- `emerald`, `teal`, `cyan`, `sky`, `blue`, `indigo`
- `violet`, `purple`, `fuchsia`, `pink`, `rose`

**Color Intensity Levels:**
- `50` - Lightest
- `100`, `200`, `300` - Light
- `400`, `500` - Medium
- `600`, `700` - Dark
- `800`, `900` - Darkest

---

## Responsive Design Adjustments

### Understanding Responsive Breakpoints

This page uses Tailwind CSS responsive prefixes to adjust layout for different screen sizes:

| Prefix | Screen Size | Device Type |
|--------|------------|-------------|
| (none) | 0-639px | Mobile phones |
| `sm:` | 640px+ | Small tablets |
| `md:` | 768px+ | Tablets and large phones |
| `lg:` | 1024px+ | Laptops and desktops |
| `xl:` | 1280px+ | Large desktops |
| `2xl:` | 1536px+ | Extra large desktops |

### How Responsive Classes Work

```html
<!-- Example: Text size changes based on screen size -->
<h1 class="text-4xl sm:text-5xl lg:text-7xl font-bold">
    Building Digital Empires That Dominate
</h1>
```

This means:
- **Mobile (0-639px):** `text-4xl` (36px)
- **Tablet (640px+):** `text-5xl` (48px)
- **Desktop (1024px+):** `text-7xl` (48px)

### Adjusting Mobile Layout

**Problem: Content is too cramped on mobile**

**Solution 1: Adjust padding**

Find:
```html
<section class="py-24 bg-gray-900">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
```

Change to:
```html
<section class="py-12 sm:py-24 bg-gray-900">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
```

This makes padding smaller on mobile (`py-12` = 48px) and normal on desktop (`sm:py-24` = 96px).

**Solution 2: Adjust font sizes for mobile**

Find:
```html
<h1 class="text-4xl sm:text-5xl lg:text-7xl font-bold">
```

Make mobile text smaller:
```html
<h1 class="text-3xl sm:text-5xl lg:text-7xl font-bold">
```

### Adjusting Tablet Layout

**Problem: Grid layout looks wrong on tablets**

**Solution: Adjust grid columns**

Find:
```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
```

This means:
- Mobile: 1 column
- Tablet (768px+): 3 columns

To show 2 columns on tablets:
```html
<div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-8">
```

### Adjusting Desktop Layout

**Problem: Content is too wide on large screens**

**Solution: Adjust max-width**

Find:
```html
<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
```

Change to:
```html
<div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
```

**Max-width options:**
- `max-w-4xl` - 56rem (896px)
- `max-w-5xl` - 64rem (1024px)
- `max-w-6xl` - 72rem (1152px)
- `max-w-7xl` - 80rem (1280px) - Current

### Common Responsive Adjustments

**1. Hide elements on specific screen sizes**

Show only on desktop:
```html
<div class="hidden lg:block">
    This only shows on desktop
</div>
```

Show only on mobile:
```html
<div class="lg:hidden">
    This only shows on mobile
</div>
```

**2. Change spacing on different devices**

```html
<div class="p-4 sm:p-6 md:p-8 lg:p-12">
    <!-- Padding: 16px mobile, 24px tablet, 32px desktop, 48px large desktop -->
</div>
```

**3. Change text alignment**

```html
<p class="text-center sm:text-left">
    <!-- Centered on mobile, left-aligned on tablet+ -->
</p>
```

**4. Change flex direction**

```html
<div class="flex flex-col sm:flex-row gap-4">
    <!-- Column on mobile, row on tablet+ -->
</div>
```

### Testing Responsive Design

**In Your Browser:**

1. Open your page in Chrome/Firefox
2. Press `F12` to open Developer Tools
3. Click the device icon (looks like a phone/tablet)
4. Select different devices to test

**Devices to Test:**
- iPhone 12 (390px)
- iPad (768px)
- iPad Pro (1024px)
- Desktop (1440px)

**Common Issues to Check:**
- [ ] Text is readable on mobile
- [ ] Images don't overflow
- [ ] Buttons are easy to tap (at least 44px)
- [ ] Navigation works on mobile
- [ ] No horizontal scrolling

---

## Troubleshooting Guide

### Common Issues and Solutions

#### Issue 1: Links Not Working

**Problem:** Clicking a link does nothing

**Possible Causes:**

1. **Incorrect href attribute**

```html
<!-- ❌ Wrong - no value -->
<a href="">Link</a>

<!-- ✅ Correct -->
<a href="contact.html">Link</a>
```

2. **File doesn't exist**

```html
<!-- ❌ Wrong - file doesn't exist -->
<a href="about.html">About</a>

<!-- ✅ Solution: Create the file or update the link -->
<a href="index.html#about">About</a>
```

3. **Wrong file path**

```html
<!-- ❌ Wrong - file in different folder -->
<a href="pages/contact.html">Contact</a>

<!-- ✅ Correct - files in same folder -->
<a href="contact.html">Contact</a>
```

**Solution:**
1. Check the `href` value matches your file name exactly (case-sensitive)
2. Verify the file exists in the correct location
3. Use browser developer tools to check for errors (F12 > Console)

---

#### Issue 2: Styles Not Applying

**Problem:** CSS classes don't seem to work

**Possible Causes:**

1. **Typo in class name**

```html
<!-- ❌ Wrong - typo -->
<div class="text-whte">Wrong color</div>

<!-- ✅ Correct -->
<div class="text-white">Correct color</div>
```

2. **Missing Tailwind CSS CDN**

Check that this line is in your `<head>`:
```html
<script src="https://cdn.tailwindcss.com"></script>
```

3. **Conflicting styles**

If you have custom CSS, it might override Tailwind. Use `!important`:
```html
<div class="text-white !text-blue-500">Blue text</div>
```

**Solution:**
1. Check spelling of all class names
2. Verify Tailwind CDN is loaded
3. Open Developer Tools (F12) and inspect the element to see which styles are applied

---

#### Issue 3: Mobile Menu Not Working

**Problem:** Mobile menu button doesn't open/close

**Possible Causes:**

1. **JavaScript not loading**

Check that JavaScript is at the bottom of your file:
```html
<script>
    document.addEventListener('DOMContentLoaded', function() {
        // Mobile menu code...
    });
</script>
```

2. **Wrong selector in JavaScript**

The JavaScript looks for:
```javascript
const mobileMenuButton = document.querySelector('header nav .mobile-menu-button');
const mobileMenu = document.querySelector('header nav .mobile-menu');
```

Make sure your HTML has these exact classes:
```html
<button class="mobile-menu-button">...</button>
<div class="mobile-menu">...</div>
```

**Solution:**
1. Open Developer Tools (F12) > Console tab
2. Look for JavaScript errors
3. Verify the mobile menu button and menu div have correct class names

---

#### Issue 4: FAQ Accordion Not Working

**Problem:** FAQ items don't expand/collapse

**Possible Causes:**

1. **Missing FAQ classes**

Each FAQ item needs these classes:
```html
<div class="faq-item">
    <div class="faq-question">Question</div>
    <div class="faq-answer hidden">Answer</div>
    <i class="faq-icon"></i>
</div>
```

2. **JavaScript not running**

Same as Issue 3 - check console for errors

**Solution:**
1. Verify HTML structure matches the original
2. Check browser console for JavaScript errors
3. Ensure you didn't accidentally delete the JavaScript code

---

#### Issue 5: Images Not Loading

**Problem:** Images show broken icon instead of picture

**Possible Causes:**

1. **Wrong image path**

```html
<!-- ❌ Wrong path -->
<img src="images/photo.jpg" alt="Photo">

<!-- ✅ Correct path -->
<img src="photo.jpg" alt="Photo">
```

2. **Image file doesn't exist**

3. **Wrong file name (case-sensitive)**

```html
<!-- ❌ Wrong - lowercase -->
<img src="Photo.jpg" alt="Photo">

<!-- ✅ Correct - matches actual filename -->
<img src="photo.jpg" alt="Photo">
```

**Solution:**
1. Check the image file exists in your project
2. Verify the file name matches exactly (including uppercase/lowercase)
3. Use correct relative path from your HTML file

---

#### Issue 6: Gradient Text Not Showing

**Problem:** Text with `gradient-text` class appears invisible

**Possible Causes:**

1. **CSS gradient not defined**

Check that this is in your `<style>` tag:
```css
.gradient-text {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
}
```

2. **Text color overriding gradient**

```html
<!-- ❌ Wrong - text color overrides gradient -->
<span class="gradient-text text-white">Text</span>

<!-- ✅ Correct - remove text color -->
<span class="gradient-text">Text</span>
```

**Solution:**
1. Verify the CSS is in your `<style>` tag
2. Remove any `text-*` color classes from gradient text
3. Check browser console for CSS errors

---

#### Issue 7: Page Not Responsive

**Problem:** Page doesn't adjust for mobile/tablet

**Possible Causes:**

1. **Missing viewport meta tag**

Check that this is in your `<head>`:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

2. **Hardcoded widths**

```html
<!-- ❌ Wrong - hardcoded width -->
<div style="width: 1000px">Content</div>

<!-- ✅ Correct - responsive -->
<div class="max-w-7xl mx-auto">Content</div>
```

3. **Tailwind CDN not loading**

Verify this is in your `<head>`:
```html
<script src="https://cdn.tailwindcss.com"></script>
```

**Solution:**
1. Check viewport meta tag is present
2. Remove inline `style` attributes with fixed widths
3. Test on different devices using browser DevTools

---

#### Issue 8: Colors Not Changing

**Problem:** Updated color classes but nothing changed

**Possible Causes:**

1. **Browser cache**

Browser is showing old cached version

2. **Typo in color class**

```html
<!-- ❌ Wrong - not a real Tailwind color -->
<div class="bg-purplee-500">Wrong</div>

<!-- ✅ Correct -->
<div class="bg-purple-500">Correct</div>
```

3. **Color not available in Tailwind**

Not all colors have all shades

**Solution:**
1. Hard refresh browser: `Ctrl+Shift+R` (Windows/Linux) or `Cmd+Shift+R` (Mac)
2. Check Tailwind color names are spelled correctly
3. Use browser DevTools to verify which styles are applied

---

### Debugging Checklist

When something isn't working:

1. **Open Developer Tools**
   - Press `F12` or right-click > Inspect
   - Check Console tab for errors

2. **Check HTML Structure**
   - Verify all tags are properly closed
   - Check for typos in class names

3. **Check CSS Classes**
   - Use Inspector to see which styles are applied
   - Verify class names are spelled correctly

4. **Check File Paths**
   - Verify all linked files exist
   - Check paths are relative to the HTML file

5. **Hard Refresh Browser**
   - Clear cache: `Ctrl+Shift+R`
   - Sometimes old files are cached

6. **Check JavaScript Console**
   - F12 > Console tab
   - Look for red error messages

---

## Best Practices

### File Organization

```
project-root/
├── index.html           (Main landing page)
├── contact.html         (Contact page)
├── privacy.html         (Privacy policy)
├── terms.html           (Terms of service)
├── blog.html            (Blog page - optional)
├── assets/
│   ├── css/
│   │   └── custom.css   (Optional custom styles)
│   ├── js/
│   │   └── custom.js    (Optional custom JavaScript)
│   └── images/
│       └── logo.png     (Your logo)
└── README.md            (Documentation)
```

### Code Organization

**1. Keep HTML Clean**
- Use proper indentation (2 or 4 spaces)
- Group related elements
- Use comments to mark sections

```html
<!-- Header Section -->
<header>
    <!-- Navigation -->
    <nav>...</nav>
</header>

<!-- Main Content -->
<main>
    <!-- Hero Section -->
    <section id="hero">...</section>
    
    <!-- Features Section -->
    <section id="features">...</section>
</main>

<!-- Footer -->
<footer>...</footer>
```

**2. Use Semantic HTML**
```html
<!-- ✅ Good - semantic tags -->
<header>Navigation</header>
<main>Content</main>
<section>Features</section>
<footer>Footer</footer>

<!-- ❌ Avoid - non-semantic -->
<div>Navigation</div>
<div>Content</div>
<div>Features</div>
<div>Footer</div>
```

**3. Keep IDs Unique**
- Use IDs for linking sections
- Make them descriptive
- Use lowercase with hyphens

```html
<!-- ✅ Good -->
<section id="features">Features</section>
<section id="testimonials">Testimonials</section>

<!-- ❌ Avoid -->
<section id="section1">Features</section>
<section id="section2">Testimonials</section>
```

### Performance Tips

**1. Optimize Images**
- Use appropriate image formats (JPEG for photos, PNG for graphics)
- Compress images to reduce file size
- Use descriptive alt text

**2. Minimize External Requests**
- Use CDN for libraries (already done with Tailwind)
- Combine CSS files if you have multiple
- Minimize JavaScript

**3. Use Caching**
- Set browser cache headers
- Minify CSS and JavaScript
- Use a CDN for static files

### Security Best Practices

**1. Validate Form Input**
- Always validate user input on server
- Sanitize data before storing
- Use HTTPS for sensitive data

**2. Keep Secrets Secret**
- Never put API keys in HTML
- Never commit passwords to version control
- Use environment variables

**3. Update Dependencies**
- Keep Tailwind CDN updated
- Update Font Awesome when new versions release
- Monitor security advisories

### Maintenance Checklist

**Monthly:**
- [ ] Check all links work
- [ ] Verify contact form sends emails
- [ ] Test on different browsers
- [ ] Check for broken images

**Quarterly:**
- [ ] Update testimonials
- [ ] Refresh content
- [ ] Check SEO metrics
- [ ] Review analytics

**Annually:**
- [ ] Update privacy policy
- [ ] Update terms of service
- [ ] Review design trends
- [ ] Plan updates

### Version Control

**Use Git to track changes:**

```bash
# Initialize git repository
git init

# Add all files
git add .

# Create initial commit
git commit -m "Initial landing page"

# View change history
git log

# See what changed
git diff
```

**Commit messages should be:**
- Clear and descriptive
- Start with action verb
- Be specific about changes

```
✅ Good:
"Update testimonials section with new client quotes"
"Fix mobile menu toggle functionality"
"Add privacy policy page"

❌ Avoid:
"Fixed stuff"
"Updates"
"Changes"
```

### Documentation

**Keep a README.md file:**

# Dormache Empire Landing Page

## Description
Professional landing page for digital transformation services.

## Files
- index.html - Main landing page
- privacy.html - Privacy policy
- terms.html - Terms of service

## How to Update
1. Edit HTML files in text editor
2. Update content in sections
3. Test changes in browser
4. Deploy to hosting

## Technologies
- HTML5
- Tailwind CSS (CDN)
- Font Awesome Icons
- Vanilla JavaScript

## Support
For questions, contact: info@dormacheempire.com
```

---

## Summary

This comprehensive guide covers:

✅ **Updating Text Content** - Step-by-step instructions for every section
✅ **Modifying CSS Classes** - Understanding and changing colors, sizes, spacing
✅ **Fixing Links** - Updating all CTA, navigation, and footer links
✅ **Adding Legal Pages** - Creating privacy and terms pages
✅ **Customizing Colors** - Changing the entire color theme
✅ **Responsive Design** - Adjusting layout for different devices
✅ **Troubleshooting** - Solutions for common problems
✅ **Best Practices** - Professional development standards

### Quick Reference

| Task | Location | How To |
|------|----------|-------|
| Change company name | Line 15 | Replace "Dormache Empire" |
| Update hero title | Lines 82-84 | Modify text in `<h1>` tags |
| Change colors | Lines 12-16 (CSS) | Update gradient hex codes |
| Update CTA links | Multiple | Replace href URLs |
| Add privacy page | New file | Create `privacy.html` |
| Fix mobile menu | Line 14-51 | Check class names match |
| Change font sizes | Various | Update `text-*` classes |
| Adjust spacing | Various | Update `p-*`, `m-*` classes |

**Remember:**
- Always test changes in your browser
- Keep backups of original files
- Use browser DevTools to debug issues
- Keep code organized and well-commented

Good luck with your landing page customization!