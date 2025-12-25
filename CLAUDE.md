# Project Instructions - Brasa Ampare

## Metasystem Inheritance

**INHERITS:** `/Users/nalve/.claude/CLAUDE.md` (Global metasystem)

All global principles, protocols, and standards apply. This document extends with project-specific context only.

## Project Domain

**Purpose:** Marketing website for Brasa Ampare premium BBQ catering service in Xalapa, Veracruz.

**Business Context:**
- Service: Professional BBQ/grilling catering for home events
- Target Market: Xalapa and surrounding areas (Coatepec, Banderilla, Emiliano Zapata)
- Value Proposition: Chef-prepared grilled meats, complete setup, full service, client relaxation
- Pricing: $280 MXN per person (minimum 40 people)

**Core Functions:**
- Present service offerings and package details
- Communicate brand value and professional quality
- Facilitate customer contact via WhatsApp
- Provide SEO-optimized content for local search
- Convert visitors to quote requests

## Tech Stack

**Architecture:** Static website (Jamstack approach)

**Core Technologies:**
- HTML5 (semantic, accessible markup)
- CSS3 (modular architecture with @import)
- Vanilla JavaScript (no frameworks)

**CSS Architecture:**
```
styles/
├── main.css          # Import orchestrator
├── variables.css     # Design tokens (colors, spacing, typography)
├── base.css          # Reset and foundational styles
├── components.css    # Reusable UI components
├── sections.css      # Page section styles
├── animations.css    # Motion and transitions
└── responsive.css    # Mobile and tablet breakpoints
```

**External Dependencies:**
- Google Fonts (Montserrat family)
- No JavaScript frameworks or libraries

## Deployment

**Platform:** Vercel

**CI/CD Pipeline:**
- Push to `main` branch triggers GitHub Actions workflow
- Workflow calls Vercel deploy hook via secret
- Vercel auto-deploys and provides preview URL
- Production URL: https://brasa-ampare.vercel.app

**Configuration:**
- `vercel.json`: Minimal config (GitHub auto-job cancellation disabled)
- `.github/workflows/deploy.yml`: Deployment automation

**Environment:**
- No build step required (static files served directly)
- No environment variables needed for production

## Development Workflow

**Local Development:**
```bash
# Serve locally (any static file server)
python3 -m http.server 8000
# or
npx serve .
```

**File Organization:**
```
brasa-ampare/
├── index.html           # Main landing page
├── styles/              # Modular CSS architecture
├── images/              # Optimized web assets
│   ├── logo-2.png
│   ├── feature-*.jpeg   # Feature cards
│   ├── chef.jpeg
│   ├── party.jpeg
│   └── og-image.jpg     # Social sharing
├── components/          # (Empty - future component library)
├── favicon.ico
├── apple-touch-icon.png
├── icon-*.png           # PWA icons
└── vercel.json
```

**Asset Management:**
- Images stored in `/images/`
- Optimize images before commit (JPEGs for photos, PNGs for logos)
- Include social sharing images (og-image.jpg for Open Graph)

## Content Structure

**Sections (Single-page layout):**
1. **Hero:** Value proposition, primary CTAs
2. **Features (Por Qué):** 4 feature cards (taste, quality, setup, convenience)
3. **Chef:** Professional service explanation with image
4. **Package (Paquete):** Detailed offering, pricing, inclusions
5. **Party:** Lifestyle/occasion imagery and messaging
6. **How it Works (Cómo Funciona):** 4-step process
7. **Coverage (Cobertura):** Service area description
8. **Final CTA (Contacto):** Conversion-focused WhatsApp contact
9. **Footer:** Branding and Ampare link

**Navigation:**
- Header with desktop menu + mobile hamburger
- Section navigation dots (right sidebar)
- Smooth scroll anchors
- WhatsApp CTA buttons throughout

## SEO and Metadata

**Optimization Features:**
- Semantic HTML5 structure
- Meta descriptions with local keywords
- Open Graph tags (Facebook/WhatsApp sharing)
- Twitter Card metadata
- Structured data (JSON-LD) for FoodService schema
- Canonical URL
- Mobile-responsive meta viewport
- Proper heading hierarchy

**Target Keywords:**
- Parrillada, domicilio, Xalapa, catering, carne asada, eventos

## Interaction Patterns

**Mobile Menu:**
- Hamburger toggle (☰ / ✕)
- Slide-in navigation
- Auto-close on link click

**Scroll Reveal:**
- Intersection Observer for section visibility
- Staggered animation delays on feature cards and steps
- Section navigation dots track scroll position

**CTAs:**
- WhatsApp links with pre-filled message templates
- Primary action: "Cotiza tu Evento"
- Multiple conversion points throughout page

## Quality Standards

**Code Quality:**
- Semantic, accessible HTML
- Valid CSS (no errors)
- Performant JavaScript (no external libraries)
- Mobile-first responsive design
- Cross-browser compatibility

**Content Quality:**
- Clear, concise copy in Spanish
- Consistent brand voice (professional yet approachable)
- High-quality imagery
- Fast loading times

**Accessibility:**
- ARIA labels on interactive elements
- Keyboard navigation support
- Semantic landmarks
- Alt text on images

## Maintenance Procedures

**Content Updates:**
1. Edit `index.html` directly for text/structure changes
2. Update styles in appropriate CSS module
3. Test locally before commit
4. Push to main for auto-deploy

**Image Updates:**
1. Optimize images (JPEGmini, TinyPNG, or similar)
2. Replace in `/images/` directory
3. Update references in HTML if renaming
4. Test social sharing preview

**Deployment Verification:**
1. Check Vercel deployment status in dashboard
2. Verify production URL reflects changes
3. Test WhatsApp CTAs on mobile
4. Validate social sharing cards (LinkedIn/Facebook debugger)

## Relationship to Ampare Ecosystem

**Brand Hierarchy:**
- Parent: Ampare (https://ampare.mx)
- Project: Brasa Ampare (BBQ catering vertical)

**Footer Attribution:**
"Un servicio de Ampare" links to parent brand

**Future Integration:**
- May integrate with Ampare booking system
- Potential shared design system with other Ampare verticals
- Could consolidate under main Ampare domain structure

## Design System

**Brand Colors:** (from variables.css)
- Primary: Warm browns/orange (#D2691E theme color)
- Accent: Highlights for CTAs
- Neutral: Text and backgrounds

**Typography:**
- Font Family: Montserrat (400, 600, 700, 800 weights)
- Responsive sizing via CSS custom properties

**Spacing System:**
- Consistent spacing scale via CSS variables
- Grid-based layouts

## Notes

**Business Constraints:**
- Minimum 40 people for standard package
- Custom quotes available for smaller events
- Service area: 30km radius from Xalapa

**Technical Constraints:**
- Static site (no backend, no CMS)
- No analytics configured (can add Google Analytics/Plausible if needed)
- No A/B testing infrastructure
- No form validation (WhatsApp-only contact)

**Future Enhancements:**
- Progressive Web App (PWA) capabilities
- Image lazy loading for performance
- Google Analytics integration
- Booking form with backend integration
- Gallery section with event photos
- Customer testimonials section
- Blog/recipes section

## Alignment with Global System

This project exemplifies global principles:
- **Minimalism:** Clean, focused single-page design
- **Single source of truth:** One canonical landing page
- **Modular architecture:** CSS split by concern, reusable components
- **Quality over speed:** Performance and SEO optimized
- **Clear communication:** Direct value proposition and CTAs

All global orchestration protocols, communication standards, and execution protocols apply without modification.
