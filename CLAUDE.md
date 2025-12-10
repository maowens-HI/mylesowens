# Myles Owens Personal Website

## Project Overview

This is a personal portfolio website for Myles Owens, an LSE MPA student specializing in Economic Policy. The site showcases projects, links to professional profiles, and features blog content from Substack.

**Live URL:** https://mowens117.github.io/

## Tech Stack

- **Framework:** [Quarto](https://quarto.org/) - Scientific and technical publishing system
- **File Format:** `.qmd` (Quarto Markdown)
- **Styling:** Custom CSS (`styles.css`)
- **Build:** Quarto renders to static HTML
- **Hosting:** GitHub Pages

## Project Structure

```
mylesowens/
├── _quarto.yml          # Quarto project configuration
├── index.qmd            # Homepage with hero, carousel, about sections
├── about.qmd            # Detailed about page
├── projects.qmd         # Portfolio/projects page (to be created)
├── styles.css           # Custom CSS styles
├── CLAUDE.md            # This file - AI assistant documentation
├── STYLE_GUIDE.md       # Visual design and branding guidelines
├── images/
│   ├── index_images/    # Hero and homepage images
│   │   └── portrait.png # Profile photo
│   ├── project_images/  # Project screenshots and graphics
│   └── logos/           # Brand logos and icons
├── _site/               # Generated output (gitignored)
└── mylesowens.Rproj     # RStudio project file
```

## Key Features

### 1. Hero Section
- Name "Myles Owens" centered in bright blue (#007BFF)
- Background: Economics/econometrics buzzwords and equations scrolling horizontally
- Faint text colors for background elements
- Clean, professional appearance

### 2. Substack Carousel
- Displays recent posts from https://mylesowens.substack.com/
- Horizontal scrolling carousel
- Shows post titles, dates, and preview text
- Links directly to Substack posts

### 3. About Me Section
- Brief professional bio
- Current status: LSE MPA student, Economic Policy
- Background: Economist, "economics storyteller", data visualization
- Previous work: Bank for International Settlements (Project Agorà), Bank of England collaboration

### 4. Portfolio Section
- Grid/card layout for projects
- Each project shows title, description, tech used, and link
- Filterable by category (optional)

### 5. Social Links
- LinkedIn: https://www.linkedin.com/in/myles-owens/
- Substack: https://mylesowens.substack.com/
- GitHub: (if applicable)

## Development Commands

```bash
# Preview site locally
quarto preview

# Render site to _site/ directory
quarto render

# Render specific file
quarto render index.qmd
```

## Quarto Configuration Notes

The `_quarto.yml` file controls:
- Site title and navigation
- Theme (using Cosmo + custom brand)
- CSS includes
- Table of contents settings
- Output format

## CSS Architecture

See `STYLE_GUIDE.md` for detailed styling guidelines.

Key CSS classes to implement:
- `.hero-section` - Main hero container
- `.hero-name` - Centered name with bright blue color
- `.scrolling-bg` - Animated background text
- `.substack-carousel` - Carousel container
- `.about-section` - About me styling
- `.project-card` - Portfolio item cards

## Important Notes for Development

1. **Quarto Syntax:** Use Quarto markdown (`.qmd`) syntax, not plain HTML where possible
2. **YAML Headers:** Each `.qmd` file needs proper YAML front matter
3. **Custom HTML:** For complex layouts (hero, carousel), use raw HTML blocks in Quarto
4. **CSS Animations:** Background scrolling uses CSS keyframe animations
5. **Responsive Design:** Ensure mobile-friendly layouts
6. **Image Optimization:** Keep images web-optimized (compress PNGs/JPGs)

## External Dependencies

- Quarto CSS themes (Cosmo)
- Optional: Font Awesome for icons
- Optional: Google Fonts for typography

## Brand Colors

- **Primary Blue:** #007BFF (hero name, links, accents)
- **Background Faint:** rgba(0, 123, 255, 0.1) (scrolling text)
- **Text Dark:** #333333
- **Text Light:** #666666
- **Background:** #FFFFFF

## Content Sections Priority

1. Hero with name and scrolling background
2. Substack carousel (recent posts)
3. About Me section
4. Projects/Portfolio grid
5. Contact/Social links footer
