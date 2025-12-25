# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Status

This project is currently in the **PRD/Planning Phase**. The main artifact is `ghx_website_prd.md`, a comprehensive Product Requirements Document for the GHX (GRYTTE Financial Services) website.

**No codebase exists yet.** The developer will choose a tech stack and build according to the PRD specifications.

## Project Overview

GHX is a 12-month financial transformation program targeting young men (20-35) in Cleveland, Ohio. The website needs to convert visitors into discovery call bookings (primary goal: 20-30 qualified leads/month).

### Recommended Tech Stacks (from PRD)

1. **Webflow** (Primary recommendation) - No-code, fast to market, hosting included
2. **WordPress + Elementor** - Budget-conscious, flexible
3. **Next.js + TailwindCSS** - Maximum control for custom features like client portal

## Key Design Requirements

**Brand Colors:**
- Primary: `#FF9EB5` (Coral Pink)
- Secondary: `#000000` (Black)
- Background: `#F8F8F8` (Off-white)
- Success/Warning/Error: `#4CAF50` / `#FFC107` / `#F44336`

**Typography:**
- Headings: Poppins or Montserrat (700/600 weight)
- Body: Inter or Open Sans (400/600 weight)

**Responsive Breakpoints:**
- Mobile: 320px-767px
- Tablet: 768px-1023px
- Desktop: 1024px-1439px
- Large Desktop: 1440px+

## Site Structure

```
/              - Homepage
/about         - Our Story, Why Cleveland, Team
/program       - Belt System, 12-Month Timeline, What's Included
/results       - Success Stories, Case Studies, Testimonials
/pricing       - 3 Tiers: Standard ($123), Enhanced ($163), Premium ($251)
/resources     - Blog, Lead Magnets (Credit Guide, Budget Template)
/faq           - Categorized FAQ
/apply         - Pre-qualification form + Calendly integration
/login         - Client dashboard/portal
```

## Required Integrations

- **Calendly** - Discovery call booking
- **Email Marketing** - ConvertKit or Mailchimp
- **CRM** - HubSpot (free) or Pipedrive
- **Analytics** - Google Analytics 4, Google Tag Manager, Hotjar, Facebook Pixel

## Performance Targets

- First Contentful Paint: <1.5s
- Time to Interactive: <3s
- Total page size: <2MB
- Google PageSpeed score: >90

## Content & Tone Guidelines

- Confident but not arrogant
- Straight-talking, no corporate jargon
- Action-oriented, direct address ("you/your")
- Use real numbers and specifics (e.g., "720 credit score" not "better credit")
- Challenge the reader appropriately

## Key Conversion Elements

- Primary CTA: "Book Free Discovery Call"
- Above-fold CTA on every page
- Sticky mobile CTA button
- Trust signals: testimonials, video testimonials, stats ("127+ clients transformed")
- 10K Graduation Guarantee as risk reversal
