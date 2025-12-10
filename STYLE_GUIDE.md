# Myles Owens Website - Style Guide

## Brand Identity

This website represents Myles Owens as an economics professional, data storyteller, and policy researcher. The design should feel:
- **Professional** - Suitable for academic and consulting audiences
- **Clean** - Minimalist with purposeful whitespace
- **Dynamic** - Subtle animations that engage without distracting
- **Data-Forward** - Visual elements that hint at quantitative expertise

---

## Color Palette

### Primary Colors

| Color Name | Hex Code | RGB | Usage |
|------------|----------|-----|-------|
| **Bright Blue** | `#007BFF` | rgb(0, 123, 255) | Hero name, primary buttons, links, accents |
| **Dark Blue** | `#0056b3` | rgb(0, 86, 179) | Hover states, emphasis |
| **Light Blue** | `#e7f1ff` | rgb(231, 241, 255) | Subtle backgrounds |

### Neutral Colors

| Color Name | Hex Code | RGB | Usage |
|------------|----------|-----|-------|
| **Black** | `#1a1a1a` | rgb(26, 26, 26) | Headings |
| **Dark Gray** | `#333333` | rgb(51, 51, 51) | Body text |
| **Medium Gray** | `#666666` | rgb(102, 102, 102) | Secondary text |
| **Light Gray** | `#f5f5f5` | rgb(245, 245, 245) | Section backgrounds |
| **White** | `#FFFFFF` | rgb(255, 255, 255) | Main background |

### Accent Colors (for scrolling background)

| Color Name | Hex Code | Opacity | Usage |
|------------|----------|---------|-------|
| **Faint Blue** | `#007BFF` | 10-15% | Scrolling buzzwords |
| **Faint Gray** | `#333333` | 8-12% | Scrolling equations |

---

## Typography

### Font Stack

```css
/* Primary font - clean, professional */
font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, sans-serif;

/* Code/equations font */
font-family: 'JetBrains Mono', 'Fira Code', 'Consolas', monospace;
```

### Font Sizes

| Element | Size | Weight | Line Height |
|---------|------|--------|-------------|
| Hero Name | 4rem (64px) | 700 (Bold) | 1.1 |
| H1 | 2.5rem (40px) | 600 (Semi-bold) | 1.2 |
| H2 | 2rem (32px) | 600 (Semi-bold) | 1.3 |
| H3 | 1.5rem (24px) | 500 (Medium) | 1.4 |
| Body | 1rem (16px) | 400 (Regular) | 1.6 |
| Small | 0.875rem (14px) | 400 (Regular) | 1.5 |
| Scrolling BG | 1.25rem (20px) | 300 (Light) | 1.0 |

---

## Hero Section Specifications

### Layout
- **Height:** 100vh (full viewport) or min-height 600px
- **Display:** Flexbox, centered horizontally and vertically
- **Position:** Relative (for background layer)

### Hero Name Styling
```css
.hero-name {
  font-size: 4rem;
  font-weight: 700;
  color: #007BFF;
  text-align: center;
  z-index: 10;
  position: relative;
}
```

### Scrolling Background

The hero section features economics/econometrics terms and equations scrolling horizontally in faint colors behind the main content.

**Buzzwords to include:**
- ECONOMETRICS
- DATA ANALYSIS
- STATISTICAL MODELING
- TIME SERIES ANALYSIS
- REGRESSION
- ECONOMIC POLICY
- MARKET ANALYSIS
- VISUALIZATION
- POLICY RESEARCH
- ECONOMIC THEORY
- QUANTITATIVE METHODS
- R&D
- LATEX
- EXCEL
- VEGA-LITE

**Equations to include:**
- Y = α + βX + ε
- E[Y|X] = β₀ + β₁X
- ΔY/ΔX = β
- R² = 1 - SSres/SStot
- σ² = Σ(xᵢ - μ)²/n
- GDP = C + I + G + (X-M)

**Animation CSS:**
```css
.scrolling-row {
  display: flex;
  white-space: nowrap;
  animation: scroll-left 30s linear infinite;
}

.scrolling-row.reverse {
  animation: scroll-right 25s linear infinite;
}

@keyframes scroll-left {
  0% { transform: translateX(0); }
  100% { transform: translateX(-50%); }
}

@keyframes scroll-right {
  0% { transform: translateX(-50%); }
  100% { transform: translateX(0); }
}

.scrolling-text {
  color: rgba(0, 123, 255, 0.12);
  font-size: 1.25rem;
  font-weight: 300;
  padding: 0 2rem;
  text-transform: uppercase;
  letter-spacing: 0.1em;
}
```

---

## Substack Carousel

### Container
- **Width:** 100%
- **Padding:** 4rem 2rem
- **Background:** #f5f5f5 (light gray)
- **Overflow:** Hidden (with horizontal scroll for cards)

### Carousel Cards
```css
.substack-card {
  min-width: 300px;
  max-width: 350px;
  background: #FFFFFF;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
  padding: 1.5rem;
  margin-right: 1.5rem;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.substack-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.12);
}
```

### Card Content
- **Title:** H3, #1a1a1a, 1.25rem, font-weight 600
- **Date:** Small text, #666666, 0.875rem
- **Preview:** Body text, #333333, 2-3 lines max with ellipsis
- **Read More Link:** #007BFF, hover underline

---

## About Me Section

### Layout
- **Two-column on desktop:** Text left (60%), Image right (40%)
- **Single column on mobile:** Image on top, text below
- **Max-width:** 1200px
- **Padding:** 5rem 2rem

### Image Styling
```css
.about-image {
  border-radius: 8px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
  max-width: 100%;
  height: auto;
}
```

### Affiliations/Logos Grid
- Display logos of LSE, Bank for International Settlements, Howard University, etc.
- Grid layout: 3-4 columns on desktop
- Grayscale by default, color on hover (optional)

---

## Project Cards

### Grid Layout
```css
.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 2rem;
  padding: 2rem;
}
```

### Card Design
```css
.project-card {
  background: #FFFFFF;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 2px 12px rgba(0, 0, 0, 0.08);
  transition: transform 0.3s ease;
}

.project-card:hover {
  transform: translateY(-8px);
}

.project-card-image {
  width: 100%;
  height: 200px;
  object-fit: cover;
}

.project-card-content {
  padding: 1.5rem;
}
```

---

## Buttons and Links

### Primary Button
```css
.btn-primary {
  background-color: #007BFF;
  color: #FFFFFF;
  padding: 0.75rem 1.5rem;
  border-radius: 6px;
  font-weight: 500;
  border: none;
  cursor: pointer;
  transition: background-color 0.2s ease;
}

.btn-primary:hover {
  background-color: #0056b3;
}
```

### Text Links
```css
a {
  color: #007BFF;
  text-decoration: none;
  transition: color 0.2s ease;
}

a:hover {
  color: #0056b3;
  text-decoration: underline;
}
```

---

## Social Icons

### Icon Buttons (LinkedIn, GitHub, Substack)
```css
.social-icon {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: 44px;
  height: 44px;
  border-radius: 50%;
  background-color: #007BFF;
  color: #FFFFFF;
  margin: 0 0.5rem;
  transition: background-color 0.2s ease, transform 0.2s ease;
}

.social-icon:hover {
  background-color: #0056b3;
  transform: scale(1.1);
}
```

---

## Spacing System

Use consistent spacing based on 8px increments:

| Name | Value | Usage |
|------|-------|-------|
| xs | 4px | Tight spacing |
| sm | 8px | Compact elements |
| md | 16px | Default spacing |
| lg | 24px | Section padding |
| xl | 32px | Large gaps |
| 2xl | 48px | Section margins |
| 3xl | 64px | Major sections |

---

## Breakpoints

```css
/* Mobile first approach */
/* Small devices (phones) */
@media (min-width: 576px) { }

/* Medium devices (tablets) */
@media (min-width: 768px) { }

/* Large devices (desktops) */
@media (min-width: 992px) { }

/* Extra large devices */
@media (min-width: 1200px) { }
```

---

## Image Guidelines

### Directory Structure
```
images/
├── index_images/
│   ├── portrait.png      # Main profile photo (recommended: 800x800px)
│   └── hero-bg.png       # Optional hero background
├── project_images/
│   ├── project-1.png     # Project thumbnails (recommended: 600x400px)
│   └── project-2.png
└── logos/
    ├── lse.png           # Institution logos
    ├── bis.png
    └── substack.png
```

### Image Specifications
- **Profile Photo:** 800x800px minimum, PNG or JPG, < 200KB
- **Project Thumbnails:** 600x400px (3:2 ratio), PNG or JPG, < 150KB
- **Logos:** PNG with transparency, max height 60px for display

---

## Accessibility

- Maintain color contrast ratio of at least 4.5:1 for text
- All images must have descriptive alt text
- Interactive elements must have :focus states
- Use semantic HTML elements
- Ensure keyboard navigation works throughout

---

## Animation Guidelines

- Keep animations subtle and purposeful
- Default duration: 200-300ms for UI transitions
- Use `ease` or `ease-out` timing functions
- Scrolling background: slower (20-30s) for ambient effect
- Respect `prefers-reduced-motion` media query
