# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

GHX is a 12-month financial transformation program website for GRYTTE Financial Services, targeting young men (20-35) in Cleveland, Ohio. The site converts visitors into discovery call bookings.

## Tech Stack

- **Static HTML/CSS/JS** - No build process required
- **TailwindCSS** - Via CDN (`cdn.tailwindcss.com`) with inline config
- **Vercel** - Hosting and deployment (see `vercel.json`)
- **Google Fonts** - Poppins (headings) + Inter (body)

## Development

**Local Development:**
```bash
# Use any static file server, e.g.:
npx serve .
# or
python -m http.server 8000
```

**Deployment:**
Push to main branch triggers Vercel auto-deploy.

## Project Structure

```
/
├── index.html          # Homepage
├── about.html          # About page
├── program.html        # Program details (belt system, timeline)
├── results.html        # Success stories & testimonials
├── pricing.html        # Pricing tiers
├── resources.html      # Blog, lead magnets
├── faq.html            # FAQ
├── apply.html          # Pre-qualification form + Calendly
├── login.html          # Client portal placeholder
├── css/styles.css      # Custom CSS (beyond Tailwind)
├── js/main.js          # Mobile menu, accordion, form handling
├── sitemap.xml         # SEO sitemap
├── robots.txt          # SEO robots file
└── vercel.json         # Vercel config (clean URLs)
```

## Tailwind Configuration

Colors and fonts are configured inline in each HTML file's `<head>`:
```javascript
tailwind.config = {
  theme: {
    extend: {
      colors: {
        primary: '#FF9EB5',      // Coral Pink - CTAs, accents
        'primary-dark': '#E88A9F',
        secondary: '#000000',    // Black - text, headers
        background: '#F8F8F8',   // Off-white - page backgrounds
      },
      fontFamily: {
        heading: ['Poppins', 'sans-serif'],
        body: ['Inter', 'sans-serif'],
      }
    }
  }
}
```

## Key Patterns

**Header/Footer:** Duplicated across all pages. When updating navigation or footer, update all 9 HTML files.

**CTAs:** All "Book Free Discovery Call" buttons link to `https://calendly.com/evan-gryttehouse/30min`

**Mobile Sticky CTA:** Each page has a sticky mobile CTA at the bottom (visible on screens < 768px).

**JavaScript Features** (`js/main.js`):
- Mobile menu toggle
- FAQ accordion (`.accordion-btn`, `.accordion-content`)
- Form validation (`data-validate` attribute)
- Smooth scroll for anchor links
- Intersection Observer for `.animate-on-scroll` elements

## Content Guidelines

- Primary stat: "18+ Cleveland men transformed" (update as needed)
- Credit score targets: 720+ score, $10K savings, 23% income increase
- Tone: Confident, direct, uses "you/your", real numbers not vague promises
- Pricing tiers: GHX Foundations, GHX Program, GHX for Business

## Analytics Placeholders

Analytics scripts in `index.html` `<head>` are commented out - add actual IDs when ready:
- Google Analytics 4
- Facebook Pixel
- Hotjar
