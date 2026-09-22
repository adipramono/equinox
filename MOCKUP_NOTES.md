# Equinox Business Law — Mockup Technical & Design Notes

This document provides a detailed technical breakdown of the HTML mockups for **Equinox Business Law Group (Direction A)**, explaining the structure, interactive elements, placeholders, and implementation notes.

---

## 1. Mockup Files Overview

| File | Canonical Name | Purpose | Status |
|---|---|---|---|
| `index.html` | Homepage | Main landing page showcasing fractional general counsel model, client proof, core offerings, and consultation CTA. | Complete & Verified |
| `about.html` | About Us | Firm story, mission, core values, leadership team, and differentiation. | Complete & Verified |
| `team.html` | Meet the Team | Attorney and operations roster with full bios and pod structure. | Complete & Verified |
| `careers.html` | Careers | Firm culture, benefits, open roles, and employee testimonials. | Complete & Verified |
| `career-single.html` | Career Detail | Interactive job opportunity posting with dynamic title switcher. | Complete & Verified |
| `events.html` | Events & Workshops | Event schedule, speaker requests, and past recordings. | Complete & Verified |
| `services.html` | Services Directory | Practice area hub and business function directory. | Complete & Verified |
| `service-contract-negotiation.html` | Contract Negotiation | In-depth practice area page for contracts & agreements. | Complete & Verified |
| `our-approach.html` | Our Approach | Strategic legal model, 3 value pillars, readiness diagnostic, 3-way comparison matrix, and onboarding paths. | Complete & Verified |
| `blog.html` | Blog & Insights Index | Filterable legal briefings feed, featured lead story, and sidebar widgets. | Complete & Verified |
| `blog-single.html` | Single Blog Post / Article | Editorial layout with TOC sidebar, redline comparison matrix, author bio, and Kadence Simple Share suite. | Complete & Verified |
| `_archive/` | Historical Drafts | Prior iterations, -A-v1 drafts, and exploration files. | Preserved |

---

## 2. Interactive Components Breakdown

### A. Navigation & Sticky Header (`.hdr`, `.hdrrow`, `.megapanel`)
- **Sticky & Elevation Behavior:**
  - Header is fixed/sticky at the top with `position: sticky; top: 0; z-index: 60;`.
  - When scrolling, the header adds a subtle elevation shadow (`@keyframes hdrlift`).
  - **Logo Scale & Padding:** The logo maintains its full, crisp size (`height: 52px;`) across both idle and scroll states without shrinking or aggressive vertical squashing.
  - Idle header padding is set to a spacious `padding: 24px 64px;` aligned cleanly within `max-width: 1440px;`.
- **Mega-Menu Structure:**
  - `Services` dropdown contains a 4-column layout: Practice Areas, By Business Function (with post counts), Industries We Serve, and an interactive CTA card ("Take the Assessment").
  - `Our Approach` dropdown includes a 3-column breakdown explaining the proactive Equinox methodology.
- **Mobile Responsive Drawer:** Embedded mobile navigation drawer with touch-friendly accordion links.

### B. Logo Bar & Social Proof (`.logotrack`)
- Displays grayscale / unified client logos: Alliance, Architextures, Darwin's, Dick's Drive-In, EJP, Piroshky Piroshky, PMH, and Tritec.
- Assets located in `assets/img/logos/`.

### C. Tiered General Counsel Accordion / Tab Panels
- Features interactive expanding/collapsing cards comparing Fractional General Counsel tiers against traditional law firms.
- State is managed cleanly with semantic HTML/CSS and lightweight vanilla JavaScript helpers.

### D. Global Footer (`.ftr`, `.ftwrap`)
- Dark Midnight (`#002B3D`) theme with reverse white logo (`equinox-logo-tag-reverse.png`).
- 4-column layout: Firm Description & Certifications, Quick Links, Practice Areas, and Contact Details.

### E. Kadence Simple Share Integration & Zero-Shift Performance (`blog-single.html`)
- **Built for Kadence Social / Kadence Simple Share WordPress Plugin:**
  - Mirrors official Kadence Simple Share plugin output (`https://docs.nexcess.com/software/kadence/simple-share/`).
  - **Style 1 (Solid Round):** 32px × 32px circular buttons with authentic brand colors (Facebook `#3B5998`, X/Twitter `#00ACED`, LinkedIn `#0077B5`, Email `#027CA1`).
  - **Style 3 (Outlined Round):** Clean border-outlined alternate included in CSS for one-click theme switching.
  - **Placement Matching Kadence Settings:**
    - **Before Post Content:** Placed directly beneath the author byline in the hero header, exactly matching the Kadence preview screenshot.
    - **After Post Content:** Clean bottom share strip aligned opposite article topic tags.
  - **Zero Layout Shift (CLS = 0):** Fixed button dimensions (32px × 32px), `flex: none`, 1px fixed border geometry, and composited opacity/brightness hover transitions (`opacity: 0.86; filter: brightness(1.08);`). Zero layout shifts or element repositioning on interaction.
  - **Native & Lightweight:** 100% native URLs (`target="_blank" rel="noopener noreferrer"`) requiring zero external JavaScript libraries or runtime dependencies.
  - **Print Optimization:** Dedicated `@media print` stylesheet automatically hides sharing buttons, header chrome, and sidebars for clean legal brief printing.

---

## 3. Asset Mapping Reference

All assets are standardized in the `assets/` directory:

```
assets/
├── css/
│   └── fonts.css                       <-- Montserrat font-face rules
└── img/
    ├── equinox-logo-tag.png            <-- Primary dark logo (Header)
    ├── equinox-logo-tag-reverse.png    <-- White logo (Footer & dark sections)
    ├── cta-47103.jpg                   <-- CTA background texture
    ├── s4-baseplate.jpg                <-- Architectural steel texture
    ├── s4-team.jpg                     <-- Equinox full team photo
    ├── s8-meeting.jpg                  <-- Client strategy session photo
    ├── s9-417.jpg                      <-- Modern architectural glass texture
    └── logos/
        ├── alliance.png
        ├── architextures.png
        ├── darwins.png
        ├── dicks.png
        ├── ejp.png
        ├── piroshky.png
        ├── pmh.png
        └── tritec.png
```

---

## 4. Key Client Directives & Design Rules

Reference source: `notes/client-correspondence.md` and `notes/design-notes.md`.

1. **Tagline Consistency:** Always use "Strategic Legal Counsel for All" or "Strategic Legal Counsel for Entrepreneurs" as defined in the approved brand guide.
2. **Imagery Tone:** Avoid traditional law firm cliches (gavel, scales of justice, lawyers in generic boardrooms). Maintain an architectural, modern, confident Pacific Northwest feel.
3. **Typography Standards:** Montserrat exclusively across all headings and body copy to match brand guidelines.
4. **No Pricing Disclosures:** Keep all pricing numbers out of public code and shared documentation.

---

## 5. Junior Developer Implementation Checklist

When building or updating mockups:
- [x] Ensure all image `src` paths point to `./assets/img/...` or `assets/img/...`.
- [x] Check that all links between pages (`about.html`, `services.html`, `index.html`, `our-approach.html`, `blog.html`, `blog-single.html`) resolve locally.
- [x] Verify that Google Fonts (`Montserrat`) loads with fallback to `assets/css/fonts.css` when offline.
- [x] Test responsive breakpoints at 1440px, 1200px, 992px, 768px, and 375px.
- [x] Confirm all text copy aligns with `notes/mockups/shared-v1/copy-deck.md`.
