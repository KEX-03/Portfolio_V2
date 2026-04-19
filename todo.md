# Portfolio Website Todo List

Based on analysis of:
- `portfolio-prd-v3.docx` (Product Requirements Document v1.0 - April 2025)
- `Portfolio_Design_Document.docx` (Design Document - Dark Theme)

---

## Phase 1: Scaffold (0.5 day)
- [ ] Initialize Vite + React project
- [ ] Configure Tailwind CSS with `darkMode: class`
- [ ] Set up React Router (installed from day one for future scalability)
- [ ] Create folder structure (components/layout, components/sections, components/ui, data, hooks, services, pages, assets)
- [ ] Define design tokens in tailwind.config.js (colors, fonts, spacing for both dark/light themes)
- [ ] Build Navbar component
- [ ] Build Footer component

## Phase 2: Theme System (0.5 day)
- [ ] Create useTheme hook
- [ ] Create ThemeProvider context
- [ ] Build settings drawer (floating button, slide-in panel)
- [ ] Implement 3-option segment: System / Light / Dark
- [ ] Add localStorage persistence
- [ ] Add OS preference listener

## Phase 3: Hero + About (1 day)
- [ ] Build Hero section with typewriter effect
- [ ] Add 3D avatar with purple radial glow
- [ ] Build About section with stat chips
- [ ] Initialize data files (projects.js, skills.js, experience.js)
- [ ] Create stub routes for future pages

## Phase 4: Projects + Skills (1 day)
- [ ] Build GlassCard component (theme-aware with glassmorphism)
- [ ] Create Projects section with project grid
- [ ] Populate projects with real content from data/projects.js
- [ ] Build Skills section with icon grid
- [ ] Add tooltips for skills

## Phase 5: Experience + Contact (1 day)
- [ ] Build Timeline component for experience section
- [ ] Create Experience section with 2x2 grid layout
- [ ] Build Contact form component
- [ ] Wire form to Web3Forms via services/contact.js
- [ ] Create Toast component for form feedback

## Phase 6: Polish + Stubs (1 day)
- [ ] Add Framer Motion scroll animations
- [ ] Create Testimonials.jsx stub (for v1.5)
- [ ] Implement hover states across all components
- [ ] Perform theme QA across all sections
- [ ] Conduct mobile responsive QA

## Phase 7: Deploy (0.5 day)
- [ ] Push to GitHub
- [ ] Connect to Vercel
- [ ] Configure custom domain
- [ ] Create OG images (both dark and light themes)
- [ ] Run Lighthouse audit (target: Performance ≥90, Accessibility ≥95, SEO ≥90)
- [ ] Enable analytics

---

## v1.5: Testimonials (1 day)
- [ ] Build out Testimonials.jsx component
- [ ] Populate data/testimonials.js with real content

## v2.0: CMS + Blog (3-4 days)
- [ ] Set up Sanity (or Contentful) CMS
- [ ] Define content schemas
- [ ] Migrate data files to CMS
- [ ] Build Blog route (/blog)
- [ ] Build BlogPost route (/blog/:slug)
- [ ] Create case study pages (/projects/:slug)

---

## Design Requirements Summary

### Color Palette
- **Background**: Deep Space/Dark Purple (#0D0B1E dark, #F5F3FF light)
- **Primary Text**: White (#FFFFFF dark, #0D0B1E light)
- **Secondary Text**: Light Gray (#C4C4C4 dark, #4B5563 light)
- **Accent**: Neon Purple (#6C63FF)
- **Accent Light**: #A78BFA (dark) / #7C3AED (light)

### Typography
- **Display Font**: Syne (hero headlines, section headings)
- **Body Font**: Inter (paragraphs, nav, labels)

### Visual Elements
- 3D Memoji-style avatar with soft purple radial glow
- Glassmorphism cards with backdrop blur (12px)
- 3D rendered UI icons (star, lightbulb, coffee cup, dropper)
- Tech stack icons in flat grid layout

### Interactions
- Typing effect for main bio headline
- Hover: intensified purple glow on cards
- Smooth scrolling and button fill animations
- Keyboard navigation support
- Reduced motion support (useReducedMotion hook)

### Performance Targets
- Lighthouse Performance ≥90
- Lighthouse Accessibility ≥95
- Lighthouse SEO ≥90
- LCP <2.5s
- CLS <0.1
- Bundle size <200KB (gzip)

---

## Out of Scope for v1.0
- Live CMS integration (architecture ready, implementation v2)
- Testimonials section (structure defined, implementation v1.5)
- Blog (full spec in PRD, implementation v2)
- Dark/light mode toggle (theme system covers this)
- Backend server (contact form uses Web3Forms)
- Authentication