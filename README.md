# PulseAI Studio — Modern Responsive Landing Page

A modern, high-performance, and visually captivating landing page developed with pure **HTML5**, **CSS3**, and **Vanilla JavaScript (ES6+)**. Built from scratch without any external CSS or JavaScript frameworks (No Bootstrap, Tailwind, React, or jQuery).

---

## 🚀 Live Demo & Project Overview

- **Theme Concept:** PulseAI Studio — Next-Generation Spatial Intelligence & Creative Generative Canvas.
- **Target Audience:** Digital artists, creative directors, 3D technical artists, software developers, and product teams.
- **Color Scheme:** Dark mode default with rich indigo, violet, cyan, and magenta radiant glows, balanced with full instant light mode toggle support.
- **Accessibility:** WCAG 2.1 AA compliant, semantic landmarks, high contrast ratios, and keyboard navigation.

---

## 📁 Project Directory Structure

```text
Responsive-Landing-Page/
│
├── index.html              # Main semantic HTML5 document containing all landing page sections
│
├── css/
│   └── style.css           # Complete CSS3 stylesheet (CSS variables, Grid, Flexbox, media queries)
│
├── js/
│   └── script.js           # Pure Vanilla JavaScript ES6+ application logic & micro-interactions
│
├── assets/
│   └── images/             # Vector graphic assets (SVGs) for sharp, resolution-independent display
│       ├── logo.svg
│       ├── hero-illustration.svg
│       ├── about-illustration.svg
│       ├── partner-1.svg to partner-5.svg
│       └── avatar-1.svg to avatar-3.svg
│
├── PROJECT_DESCRIPTION.md   # Comprehensive standalone architectural & functional project description
├── PROJECT_REPORT.docx      # Professionally formatted academic project report in Word (.docx) format
└── README.md                # Technical setup, file explanations, and feature documentation
```

---

## 🛠️ File-by-File Purpose & Architecture

### 1. `index.html`
- **Purpose:** Forms the semantic backbone of the application.
- **Key Sections:**
  1. **Header & Navigation:** Sticky glassmorphic navbar with SVG logo, active scroll spy links, Dark/Light mode toggle, desktop CTA buttons, and an accessible mobile hamburger trigger.
  2. **Mobile Slide-Over Drawer:** Off-canvas menu with background blur overlay and escape key dismissal.
  3. **Hero Section:** Value proposition, announcement badge, gradient title typography, dual CTA buttons, live user proof counter, and an interactive spatial canvas preview card with an embedded interactive prompt playground.
  4. **Partner Logo Marquee:** Infinite CSS-animated ticker showcasing enterprise adopters.
  5. **Feature Highlights:** 6 distinct capability cards arranged in a responsive CSS Grid with custom gradient icon boxes, badge labels, and hover lifts.
  6. **Interactive Workflow Showcase:** 3 tabbed workflow demonstrations (Generative Diffusion, Spatial 3D Studio with interactive 3D CSS cube, and Real-Time Multiplayer Sync).
  7. **Live Platform Stats:** Animated numerical indicators showcasing uptime, latency, asset count, and active creators.
  8. **About Section:** Narrative storytelling on mission and architectural pillars paired with an architectural infographic.
  9. **Testimonials Section:** Verified customer reviews with 5-star ratings, author roles, and vector portraits.
  10. **Pricing & Plans Section:** Dynamic billing toggle (Monthly vs. Annual with 20% discount) adjusting 3 pricing tiers (Starter, Pro, Enterprise).
  11. **FAQ Section:** Expandable accordion with smooth transitions and keyboard navigation.
  12. **Call-to-Action (CTA):** High-conversion banner with ambient lighting and email input with client-side regex validation.
  13. **Footer:** Comprehensive 5-column navigation, live status beacon, social media links, and copyright notices.
  14. **Floating Widgets:** Reading scroll progress bar, floating back-to-top button, and interactive video demo modal.

### 2. `css/style.css`
- **Purpose:** Controls styling, theming, layout, responsiveness, and micro-interactions.
- **Core Architecture:**
  - **CSS Custom Properties (Variables):** Complete design tokens for colors, surfaces, glassmorphism filters, elevations, typography, and borders for both Dark and Light modes.
  - **CSS Grid & Flexbox:** Robust modern layouts without float or framework hacks.
  - **Responsive Media Queries:**
    - Desktop: `min-width: 1024px`
    - Tablet: `max-width: 1024px` and `768px - 1023px`
    - Mobile: `max-width: 768px`
    - Small Mobile: `max-width: 480px`
  - **Animations & Keyframes:** `@keyframes marqueeScroll`, `@keyframes pulseDot`, `@keyframes rotateCube`, and scroll-reveal transitions.
  - **Accessibility:** Respects `@media (prefers-reduced-motion: reduce)`. Zero horizontal scrolling on all mobile viewports.

### 3. `js/script.js`
- **Purpose:** Handles all client-side logic, interactivity, and accessibility enhancements.
- **Core Modules:**
  - **Mobile Drawer:** Handles opening, closing, overlay click, and `Escape` key capture.
  - **Theme Switcher:** Toggles `[data-theme="light|dark"]`, synchronizes with `localStorage`, and falls back to system preferences.
  - **Scroll Progress & Header Blur:** Computes document scroll percentage for top progress indicator and toggles `.scrolled` state on the navbar.
  - **Scroll Spy:** Observes section offsets to activate corresponding nav items during scrolling.
  - **Scroll Reveal:** Employs `IntersectionObserver` to trigger fade-and-slide entrances for cards and headings.
  - **Live Animated Counters:** Computes smooth numerical easing via `requestAnimationFrame` when the stats section enters the viewport.
  - **Interactive Workflow Tabs:** Manages active tab state and ARIA tabpanel switching.
  - **Pricing Billing Switcher:** Dynamically swaps pricing values with smooth opacity transitions.
  - **FAQ Accordion:** Manages accordion trigger clicks and accessibility attributes.
  - **Interactive Prompt Generator:** Simulates neural model synthesis with interactive feedback.
  - **Form Validation & Toast Alerts:** Validates email format using regex and triggers animated toast notification alerts.
  - **Demo Modal Dialog:** Manages modal state, backdrop click dismissal, and keyboard accessibility.
  - **Back-to-Top Button:** Detects scroll position (> 350px) and smoothly scrolls the user back to the top.

### 4. `assets/images/`
- **Purpose:** Self-contained, high-resolution SVG graphics ensuring fast load times and clean presentation on high-DPI displays.

---

## ⚡ How to Run Locally

Because the project uses standard web technologies, **no build step, package manager, or compilation is required**.

### Method 1: Direct Browser Launch
1. Navigate to the project folder.
2. Double-click `index.html` to open it directly in any modern browser (Google Chrome, Mozilla Firefox, Microsoft Edge, Safari).

### Method 2: Local HTTP Server (Recommended)
Running through a local web server allows optimal asset resolution:
```bash
# Using Python (if available):
python -m http.server 8000

# Using Node.js npx:
npx serve .

# Or using VS Code "Live Server" extension:
# Right-click on index.html and select "Open with Live Server"
```
Then visit `http://localhost:8000` in your web browser.

---

## 📱 Responsive Testing Matrix

The layout has been tested and verified across key screen sizes:
- **Mobile Phones (320px – 480px):** Single-column stacked cards, off-canvas navigation drawer, responsive buttons, zero horizontal overflow.
- **Tablets (768px – 1023px):** 2-column feature and stats grids, responsive flex layouts.
- **Laptops & Desktops (1024px – 1440px+):** Full multi-column grids, horizontal desktop navigation, floating spatial visual preview card, and interactive demo tabs.

---

## 📄 Documentation & Project Deliverables

This workspace contains **three independent, non-combined deliverables**:
1. **Source Code:** `index.html`, `css/style.css`, `js/script.js`, and `assets/images/`.
2. **Professional Project Report:** Available as `PROJECT_REPORT.docx` (Word format) and `PROJECT_REPORT.md` (Markdown format).
3. **Standalone Project Description:** Detailed technical, design, and user journey documentation in `PROJECT_DESCRIPTION.md`.
