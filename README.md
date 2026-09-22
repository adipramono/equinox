# Equinox Business Law Group — Website Redesign & Mockups

Welcome to the **Equinox Business Law Group** redesign workspace. This repository contains the local HTML mockups, design tokens, asset library, and strategic context for the website rebuild and facelift project.

---

## 📌 Project Quick Links

| Item | Details / Link |
|---|---|
| **Live Production Website** | [https://equinoxbusinesslaw.com/](https://equinoxbusinesslaw.com/) |
| **Demo Staging URL** | `https://equinoxbusinesslaw.demoing.info/wp-content/mockups/` *(Password protected)* |
| **Design Direction** | Direction A (Elevated, editorial, fractional general counsel focus) |
| **Primary Fonts** | Montserrat (Google Fonts with local fallback) |
| **Primary Colors** | Deep Midnight `#002B3D`, Oceanic Blue `#027CA1`, Warm Amber `#F3B233`, Coral `#E26D5C` |

---

## 🖥️ Local Mockups Inventory

All mockups are configured with clean relative paths and work seamlessly offline and locally:

1. **[index.html](file:///J:/My%20Drive/Projects/Equinox/index.html)** — **Homepage**
   - Elevated hero section with value proposition, interactive multi-column mega-menus, client trust proof logos, fee structure / general counsel tier accordion, case studies, and consultation CTA block.
2. **[about.html](file:///J:/My%20Drive/Projects/Equinox/about.html)** — **About Us**
   - Firm narrative, core beliefs, leadership team, approach explanation, and closing CTA.
3. **[team.html](file:///J:/My%20Drive/Projects/Equinox/team.html)** — **Our Team**
   - Team bios, attorney and paralegal roster, and pod structure.
4. **[careers.html](file:///J:/My%20Drive/Projects/Equinox/careers.html)** — **Careers**
   - Firm culture, benefits, open roles overview, and applicant journey.
5. **[career-single.html](file:///J:/My%20Drive/Projects/Equinox/career-single.html)** — **Career Posting Details**
   - Interactive role breakdown with dynamic title/job specification loader.
6. **[events.html](file:///J:/My%20Drive/Projects/Equinox/events.html)** — **Events & Workshops**
   - Executive roundtables, webinars, speaking requests, and event calendar.
7. **[services.html](file:///J:/My%20Drive/Projects/Equinox/services.html)** — **Services & Practice Areas Directory**
   - Practice areas hub, business function index, and legal health assessment entry.
8. **[service-contract-negotiation.html](file:///J:/My%20Drive/Projects/Equinox/service-contract-negotiation.html)** — **Practice Area Detail**
   - In-depth service page for Contract Negotiation and Maintenance.
9. **[blog.html](file:///J:/My%20Drive/Projects/Equinox/blog.html)** — **Blog & Insights Index**
   - Strategic legal briefings with About-style category sidebar, live search, featured editorial analysis, article grid, and legal health diagnostic callout.
10. **[blog-single.html](file:///J:/My%20Drive/Projects/Equinox/blog-single.html)** — **Single Blog Post / Article**
   - In-depth editorial post with Table of Contents jump sidebar, clause comparison redline matrix, author bio card, and related insights.

*(Note: Prior draft versions and exploration files are safely preserved in the `_archive/` directory).*

---

## 🚀 How to View the Mockups

### Option 1: Direct File Opening
Double-click any `.html` file (`index.html`, `about.html`, `services.html`, etc.) in Windows Explorer to open it in Chrome, Edge, Brave, or Safari.

### Option 2: Local HTTP Server (Recommended for dev)
Open a terminal in this directory (`J:\My Drive\Projects\Equinox`) and run:
```bash
# Using Python
python -m http.server 8000

# Using Node (npx)
npx serve .
```
Then navigate to `http://localhost:8000` in your browser.

---

## 📁 Workspace Structure

```
Equinox/
├── index.html                               # Default entry point (Home Direction A v1.1)
├── home-A-v1-1.html                         # Home Page mockup
├── about-A-v1.html                          # About Us mockup
├── services-A-v1.html                       # Services / Practice Areas mockup
├── README.md                                # This main documentation file
├── MOCKUP_NOTES.md                          # In-depth mockup breakdown & junior guide
├── assets/
│   ├── css/
│   │   └── fonts.css                        # Local Montserrat @font-face fallback definitions
│   └── img/
│       ├── equinox-logo-tag.png             # Primary dark logo with tagline
│       ├── equinox-logo-tag-reverse.png     # White reverse logo for dark footers/headers
│       ├── cta-47103.jpg                    # CTA background photography
│       ├── s4-baseplate.jpg                 # Hero / architectural texture
│       ├── s4-team.jpg                      # Team photo
│       ├── s8-meeting.jpg                   # Client collaboration photo
│       ├── s9-417.jpg                       # Secondary feature photo
│       └── logos/                           # Client / partner logos
│           ├── alliance.png
│           ├── architextures.png
│           ├── darwins.png
│           ├── dicks.png
│           ├── ejp.png
│           ├── piroshky.png
│           ├── pmh.png
│           └── tritec.png
└── notes/                                   # Source documentation, audit & brand materials
    ├── client-correspondence.md             # Email threads & client onboarding decisions
    ├── design-notes.md                      # Phase notes, deferred requests, design fence
    ├── site-audit-2026-07.md                # Comprehensive audit of live equinoxbusinesslaw.com
    ├── mockups/shared-v1/
    │   ├── copy-deck.md                     # Sanctioned copy & messaging deck
    │   ├── design-system.md                 # Design system tokens, typography & spacing
    │   └── directions-and-placeholders.md   # Placeholders & replacement inventory
    └── source/
        ├── brand-kit/                       # Brand guides, logos, color concepts
        ├── photos/                          # High-resolution shoot photos
        └── aisv-brand-story.md              # AISV marketing strategy & StoryBrand copy
```

---

## 🎨 Design System & Brand Identity

### Color Palette
- **Primary Brand Dark:** `#002B3D` (Deep Midnight Blue — headings, dark backgrounds, footer)
- **Primary Brand Accent:** `#027CA1` (Oceanic Blue — buttons, active links, icons)
- **Secondary Accent Gold:** `#F3B233` (Warm Amber / Gold — badges, highlights)
- **Warm Accent Coral:** `#E26D5C` (Secondary CTA highlights)
- **Neutral Light Background:** `#F4F5F7` (Section cards, soft backgrounds)
- **Pure White:** `#FFFFFF` (Main page background, elevated cards)
- **Text Body:** `#333333` (High legibility body text)
- **Text Muted:** `#666666` (Captions, subheaders, breadcrumb separators)

### Typography
- **Primary Font Family:** `'Montserrat', -apple-system, BlinkMacSystemFont, sans-serif`
- **Font Weights Used:**
  - `300` (Light — subtle labels)
  - `400` (Regular — body paragraphs)
  - `500` (Medium — navigation items, tags)
  - `600` (Semi-bold — subheaders, card titles)
  - `700` (Bold — section headings, primary CTAs)
  - `800` (Extra Bold — hero headlines)

---

## 📋 Client Key Directives & Rules

Based on client correspondence and audit findings (`notes/client-correspondence.md`):
1. **Elevated Look:** Clean, modern, authoritative aesthetic representing sophisticated strategic legal counsel.
2. **Photography Rules:**
   - No generic/cheesy stock photos of people in suits shaking hands.
   - Use authentic firm photography (`notes/source/photos/`) or architectural / contextual textures (`s4-baseplate.jpg`, `cta-47103.jpg`).
3. **Fractional General Counsel Positioning:** Clear emphasis on Equinox's proactive, business-first fractional general counsel model rather than reactive hourly billing.
4. **No Price Disclosure:** No specific pricing figures appear in public mockups or shared markdown notes.

---

## 👨‍💻 For Junior Developers: Next Steps

1. Review [MOCKUP_NOTES.md](file:///J:/My%20Drive/Projects/Equinox/MOCKUP_NOTES.md) for individual component guidelines.
2. When creating new subpages, inherit the header, mega-menu, and footer from `home-A-v1-1.html`.
3. Check `notes/mockups/shared-v1/copy-deck.md` before adding or modifying any copy.
4. All static assets must be placed inside `assets/img/` or `assets/img/logos/` and referenced with relative URLs.
