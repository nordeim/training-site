# **PROJECT REQUIREMENT DOCUMENT**
## **iTrust Academy Website — Design System & UX Architecture Analysis**
### **Adapted for AI & Software Training Business Vertical**

---

## **EXECUTIVE SUMMARY**

This document presents a comprehensive analysis of the iTrust Academy website (https://www.itrust.academy/) design language, extracted into an actionable Project Requirement Document (PRD) for adaptation to AI and software training businesses. The analysis follows systematic deconstruction of visual hierarchy, interaction patterns, content architecture, and brand positioning.

**Key Finding:** iTrust Academy employs a **"Corporate-Technical Authority"** aesthetic—clean, certification-focused, vendor-aligned design that prioritizes trust signals and conversion clarity over visual experimentation. For AI/software training adaptation, we pivot toward **"Precision Futurism"**—maintaining authority while introducing dynamic, intelligence-forward visual metaphors.

---

## **PHASE 1: DESIGN LANGUAGE ANALYSIS**

### **1.1 Visual Identity System**

#### **Color Palette Architecture**
| Role | Current iTrust Value | AI/Software Adaptation | Rationale |
|------|---------------------|------------------------|-----------|
| **Primary** | Deep Navy `#1e3a5f` | Electric Indigo `#4f46e5` + Deep Space `#0f172a` | Shift from traditional corporate blue to AI-forward gradient; maintains authority while signaling innovation |
| **Secondary** | Teal Accent `#0d9488` | Neural Cyan `#06b6d4` + Signal Amber `#f59e0b` | Cyan for AI/data visualization associations; amber for attention/urgency in CTAs |
| **Background** | Pure White `#ffffff` | Soft Ivory `#fafaf9` + Dark Mode Charcoal `#171717` | Reduced eye strain for technical content; modern dual-mode support |
| **Text** | Charcoal `#1f2937` | Slate `#334155` / Off-White `#f8fafc` | Improved readability for code snippets and technical documentation |
| **Success/CTA** | Emerald `#10b981` | Neon Emerald `#10b981` with glow effects | High-contrast action states for enrollment conversion |

#### **Typography System**
**Current State Analysis:**
- **Primary:** Sans-serif system stack (likely Inter/Roboto equivalent)
- **Hierarchy:** Clear H1→H6 progression with weight differentiation
- **Density:** Medium line-height (1.5-1.6) for technical content readability

**AI/Software Adaptation:**
- **Display/Headlines:** `Space Grotesk` or `Satoshi` — geometric, technical character with personality
- **Body/UI:** `Inter` or `Plus Jakarta Sans` — optimized for screen readability at small sizes (code documentation)
- **Monospace/Code:** `JetBrains Mono` or `Fira Code` — essential for AI/software training (code examples, CLI demonstrations)
- **Scale:** Major Third (1.250) or Perfect Fourth (1.333) ratio for dramatic hierarchy
- **Weights:** 400 (body), 500 (UI), 600 (subheads), 700 (display)

#### **Spacing System**
- **Base Unit:** 4px grid system
- **Section Padding:** 80px-120px vertical (desktop), 48px-64px (mobile)
- **Content Max-Width:** 1280px (xl) with 768px (md) reading column constraint
- **Component Density:** Generous whitespace (anti-generic minimalism) with 24px-32px internal padding

---

### **1.2 Layout Architecture**

#### **Grid System**
**Current Pattern:** 
- Single-column hero with centered text
- 2-column feature grids (icon + text)
- 3-column vendor showcase
- 4-column "Why Choose Us" benefits

**Adaptation Strategy:**
- **Asymmetric Editorial Grid:** 60/40 splits for hero sections (text dominant)
- **Bento Box Layouts:** For course feature showcases (trending in AI/tech interfaces)
- **Masonry for Testimonials:** Breaking rigid grids for social proof
- **Sticky Sidebar Navigation:** For course detail pages (long-form technical content)

#### **Responsive Breakpoints**
| Breakpoint | Width | Adaptation |
|------------|-------|------------|
| `sm` | 640px | Stacked layouts, reduced typography scale |
| `md` | 768px | 2-column grids emerge, navigation condenses |
| `lg` | 1024px | Full layout expression, sidebar navigation |
| `xl` | 1280px | Max content width, enhanced spacing |
| `2xl` | 1536px | Ultra-wide optimizations, expanded grids |

---

### **1.3 Component Library Specifications**

#### **Buttons**
**Current Style:** Solid fill, rounded corners (4-6px), uppercase text tracking

**AI/Software Adaptation:**
- **Primary:** Solid indigo with subtle gradient shift on hover, 8px border-radius
- **Secondary:** Outlined with 1.5px stroke, transparent background
- **Ghost:** Text-only with arrow icon animation (→ transforms into ↗ on hover)
- **Micro-interactions:** 
  - 200ms ease-out transitions
  - Scale 1.02 on hover
  - Ripple effect on click (material design inspired)
  - Loading state with animated ellipsis

#### **Cards**
**Current Pattern:** White background, subtle shadow, icon-top layout

**Enhanced Specifications:**
- **Course Cards:** 
  - Glassmorphism backdrop (blur 12px, rgba white 0.7)
  - Hover lift: translateY(-4px) + shadow intensification
  - Badge positioning: Top-right (vendor certification logos)
  - Progress indicators: For enrolled courses (circular SVG progress)
  
- **Feature Cards:**
  - Icon container: 48px×48px rounded-2xl with gradient background
  - Border: 1px solid slate-200, transitioning to indigo-400 on hover

#### **Navigation**
**Current Structure:** Horizontal top nav, simple link list

**Adaptation:**
- **Sticky Header:** Glassmorphism effect on scroll (backdrop-blur-md)
- **Mega Menu:** For course categories (AI/ML, Data Science, DevOps, etc.)
- **Search:** Command palette style (⌘K shortcut) with fuzzy matching
- **Mobile:** Full-screen overlay with accordion sections

---

### **1.4 Animation & Interaction Design**

#### **Motion Philosophy**
- **Purposeful:** Every animation guides attention or provides feedback
- **Performant:** CSS transforms only (no layout thrashing)
- **Accessible:** Respect `prefers-reduced-motion`

#### **Specific Patterns**
| Element | Animation | Specs |
|---------|-----------|-------|
| **Page Load** | Staggered fade-up | Y: 20px→0, Opacity: 0→1, Duration: 600ms, Stagger: 100ms |
| **Scroll Reveal** | Intersection Observer triggered | Threshold: 0.1, Root margin: 0px |
| **Hero Text** | Character/word stagger | Delay: 20ms per character, Easing: cubic-bezier(0.25, 0.46, 0.45, 0.94) |
| **Button Hover** | Scale + Shadow | Transform: scale(1.02), Box-shadow expansion, Duration: 200ms |
| **Card Hover** | Lift + Border glow | TranslateY: -4px, Border-color transition, Duration: 300ms |
| **Icon Micro** | Subtle rotation/pulse | Rotate: 5deg on hover or continuous subtle pulse for "live" indicators |

#### **Technical Implementation**
- **Library:** Framer Motion (React) or GSAP for complex sequences
- **CSS:** Tailwind `transition-*` utilities for simple states
- **Performance:** `will-change: transform` on animated elements
- **Reduced Motion:** `@media (prefers-reduced-motion: reduce)` fallbacks

---

## **PHASE 2: CONTENT ARCHITECTURE ANALYSIS**

### **2.1 Information Hierarchy**

#### **Current Site Structure (iTrust)**
```
Homepage
├── Hero (Value Prop + CTA)
├── Vendor Partners (SolarWinds, Securden, Quest, Ivanti)
├── Value Proposition (Why Choose Us)
├── Featured Course Detail
├── Course Schedule/Calendar
└── Professional Services Cross-sell
```

#### **AI/Software Training Adaptation**
```
Homepage
├── Hero (Dynamic headline rotation + Primary CTA)
├── Social Proof (Logos of hiring partners)
├── Course Categories (Bento grid: AI/ML, Data, DevOps, Security)
├── Featured Learning Paths (Vertical progression visualization)
├── Instructor Showcase (Expert credibility)
├── Student Outcomes (Stats + Testimonials)
└── Certification Partners (AWS, Azure, Google, etc.)

Course Detail Page
├── Sticky Nav (Overview, Curriculum, Instructor, Reviews, Enrollment)
├── Hero (Title, Meta, Rating, CTA)
├── Learning Objectives (Bullet grid)
├── Curriculum Accordion (Module expansion)
├── Instructor Bio (Credibility signals)
├── Student Reviews (Masonry grid)
└── Enrollment Card (Sticky sidebar)
```

### **2.2 Copy & Messaging Strategy**

#### **Tone Analysis (Current)**
- **Voice:** Professional, authoritative, vendor-aligned
- **Focus:** Certification outcomes, exam preparation, vendor authorization
- **Keywords:** "Certified," "Authorized," "Exam," "SCP," "Training"

#### **AI/Software Adaptation**
- **Voice:** Expert but accessible, forward-looking, transformation-focused
- **Focus:** Career outcomes, skill application, portfolio building
- **Keywords:** "Hands-on," "Production-ready," "AI-powered," "Real-world," "Portfolio"

**Messaging Hierarchy:**
1. **Headline:** Outcome-focused (not feature-focused)
   - *Instead of:* "AI Training Course"
   - *Use:* "Build Production-Grade AI Systems in 12 Weeks"
2. **Subhead:** Specificity + credibility
   - "Learn from ex-Google AI engineers. Deploy 6 portfolio projects."
3. **CTA:** Action + benefit
   - "Start Learning" → "Enroll Now — Next Cohort Starts March 15"

---

## **PHASE 3: UX ENGINEERING SPECIFICATIONS**

### **3.1 Technical Stack Recommendations**

Based on the requirements for modern AI/software training platforms:

| Layer | Recommendation | Justification |
|-------|---------------|---------------|
| **Framework** | Next.js 14+ (App Router) | SSR for SEO, API routes for backend, Image optimization |
| **Styling** | Tailwind CSS 4.0 | Rapid development, design system consistency, purge optimization |
| **UI Components** | Shadcn/ui + Radix | Accessible primitives, customizable, no style lock-in |
| **Animation** | Framer Motion | React-native animations, gesture support, AnimatePresence |
| **CMS** | Sanity or Contentful | Structured content for courses, instructors, schedules |
| **Auth** | Clerk or NextAuth | Secure enrollment, progress tracking, multi-role support |
| **Database** | PostgreSQL + Prisma | Relational data for courses, users, enrollments |
| **Search** | Algolia or Meilisearch | Instant course search, typo tolerance, faceting |
| **Video** | Mux or Cloudflare Stream | Adaptive bitrate, analytics, secure playback |
| **Deployment** | Vercel | Edge network, preview deployments, analytics |

### **3.2 Accessibility Requirements (WCAG 2.1 AA)**

- **Color Contrast:** Minimum 4.5:1 for normal text, 3:1 for large text
- **Focus States:** Visible 2px outline offset for keyboard navigation
- **ARIA Labels:** Descriptive labels for icon buttons, form errors announced
- **Semantic HTML:** Proper heading hierarchy, landmark regions, list structures
- **Alt Text:** Descriptive for images, empty for decorative
- **Motion:** Respect `prefers-reduced-motion` media query
- **Forms:** Label associations, error prevention, clear error messages

### **3.3 Performance Budget**

| Metric | Target | Maximum |
|--------|--------|---------|
| **Lighthouse Performance** | 90+ | 85 |
| **First Contentful Paint** | < 1.5s | < 2.5s |
| **Largest Contentful Paint** | < 2.5s | < 4s |
| **Time to Interactive** | < 3.5s | < 5s |
| **Cumulative Layout Shift** | < 0.1 | < 0.25 |
| **Total Bundle Size** | < 200KB (gzipped) | < 500KB |

---

## **PHASE 4: ADAPTATION STRATEGY FOR AI/SOFTWARE TRAINING**

### **4.1 Differentiation from iTrust Model**

| Aspect | iTrust Academy (IT Vendor Training) | AI/Software Training Adaptation |
|--------|-------------------------------------|--------------------------------|
| **Visual Metaphor** | Corporate certification, authority badges | Innovation, intelligence, future-forward |
| **Color Psychology** | Trust blue, stability | Innovation purple/cyan, energy amber |
| **Imagery** | Vendor logos, classroom photos | Abstract data viz, code interfaces, AI visualizations |
| **Social Proof** | Vendor authorization, exam pass rates | Hiring partner logos, student salary increases, portfolio quality |
| **Content Density** | Moderate, exam-focused | High, project-heavy, code-rich |
| **Interaction Model** | Browse → Select → Enroll | Assess → Recommend Path → Enroll → Learn |

### **4.2 Unique Features for AI/Software Vertical**

1. **AI Learning Path Finder:** Interactive assessment tool that recommends courses based on current skills and career goals
2. **Code Sandbox Integration:** Embedded live coding environments (CodePen, StackBlitz, or custom)
3. **Project Showcase:** Student portfolio gallery with filtering by technology/stack
4. **Progress Visualization:** Skill tree visualization showing learning progression
5. **Community Integration:** Discord/Slack community access, peer learning features
6. **AI Tutor Interface:** Chat-based assistant for course questions (positioned as learning aid, not replacement)

---

## **PHASE 5: IMPLEMENTATION ROADMAP**

### **Phase 1: Foundation (Weeks 1-2)**
- [ ] Design system setup (colors, typography, spacing tokens)
- [ ] Component library initialization (Shadcn/ui base)
- [ ] Layout grid system implementation
- [ ] Navigation architecture (responsive)

### **Phase 2: Core Pages (Weeks 3-4)**
- [ ] Homepage (Hero, features, courses, social proof)
- [ ] Course listing page (filtering, search, sorting)
- [ ] Course detail page (curriculum, instructor, enrollment)
- [ ] Static pages (About, Contact, FAQ)

### **Phase 3: Interactive Features (Weeks 5-6)**
- [ ] User authentication flow
- [ ] Enrollment/checkout process
- [ ] Student dashboard (progress, certificates)
- [ ] Search functionality (Algolia integration)

### **Phase 4: Polish & Launch (Weeks 7-8)**
- [ ] Animation implementation
- [ ] Accessibility audit
- [ ] Performance optimization
- [ ] Content population
- [ ] QA testing
- [ ] Launch

---

## **PHASE 6: QUALITY ASSURANCE CHECKLIST**

### **Pre-Launch Validation**
- [ ] Cross-browser testing (Chrome, Safari, Firefox, Edge)
- [ ] Mobile responsiveness (iOS Safari, Android Chrome)
- [ ] Accessibility audit (axe-core, Lighthouse)
- [ ] Performance benchmarking (WebPageTest, Lighthouse)
- [ ] SEO validation (meta tags, structured data, sitemap)
- [ ] Security headers check (CSP, HSTS, X-Frame-Options)
- [ ] Form validation and error handling
- [ ] Payment flow testing (if applicable)
- [ ] Analytics instrumentation (GA4, Mixpanel, or PostHog)

### **Design System Consistency**
- [ ] Color contrast ratios verified
- [ ] Typography scale applied consistently
- [ ] Spacing system adherence
- [ ] Component behavior uniformity
- [ ] Animation timing consistency

---

## **DELIVERABLES SUMMARY**

1. **Design Tokens:** Color palette, typography scale, spacing system (JSON/CSS variables)
2. **Component Library:** React components with Storybook documentation
3. **Page Templates:** Homepage, Course Listing, Course Detail, Dashboard
4. **Interaction Specifications:** Animation timing, easing functions, state transitions
5. **Content Strategy:** Messaging framework, copy guidelines, SEO recommendations
6. **Technical Architecture:** Stack recommendations, API specifications, deployment guide

---

## **RISK ASSESSMENT & MITIGATION**

| Risk | Impact | Mitigation |
|------|--------|------------|
| **Performance degradation with rich media** | High | Lazy loading, CDN optimization, video compression |
| **Accessibility gaps in custom components** | Medium | Radix UI primitives, automated a11y testing |
| **Content management complexity** | Medium | Structured CMS schema, content validation |
| **Cross-browser animation inconsistencies** | Low | CSS-first animations, feature detection |
| **SEO challenges with client-side rendering** | Medium | Next.js SSR/SSG, proper meta tag implementation |

---

## **CONCLUSION**

This Project Requirement Document provides a comprehensive blueprint for adapting the iTrust Academy design language to the AI and software training vertical. The approach maintains the core strengths of the original (authority, clarity, conversion focus) while evolving the aesthetic toward "Precision Futurism"—appropriate for cutting-edge technical education.

**Next Steps:**
1. Review and validate this PRD against business requirements
2. Create low-fidelity wireframes for key page templates
3. Develop high-fidelity mockups for homepage and course detail
4. Set up technical infrastructure per Phase 5 roadmap
5. Begin component library development

**Success Metrics:**
- Homepage conversion rate > 3%
- Course page enrollment rate > 8%
- Lighthouse performance score > 90
- Accessibility compliance: WCAG 2.1 AA
- User satisfaction (NPS) > 50

---

*Document Version: 1.0*
*Prepared by: Frontend Architect & Avant-Garde UI Designer*
*Date: March 6, 2026*
