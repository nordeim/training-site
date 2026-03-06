# 📋 PROJECT REQUIREMENT DOCUMENT (v2.0)
## AI & Software Training Platform — Design System & UX Architecture

**Synthesized from:** Original Generated PRD + Uploaded PRD_k1.md + User Tech Stack Preferences  
**Document Version:** 2.0 (Merged & Optimized)  
**Date:** March 06, 2026  
**Classification:** Strategic Design & Technical Blueprint  
**Status:** Ready for Implementation

---

## EXECUTIVE SUMMARY

This document presents a **comprehensive synthesis** of two PRD analyses, merged with specific technology stack requirements (Next.js 16.1.4 + Django 6.0.2). After rigorous comparative analysis, this PRD combines the **visual system specificity** of the original analysis with the **full-stack completeness** of the uploaded PRD, while incorporating your preferred technology stack.

**Key Transformation:** From traditional IT certification training → **"Precision Futurism"** AI/Software education platform with distinctive visual identity, intentional minimalism, and conversion-optimized UX.

**Critical Improvement:** This v2.0 PRD addresses all identified gaps from the comparative analysis, including backend architecture, security, search, authentication, video infrastructure, and realistic performance budgets.

---

## PHASE 1: DEEP REQUIREMENT ANALYSIS

### 1.1 Multi-Dimensional Design Analysis

#### 🔮 PSYCHOLOGICAL LAYER
| Element | User Sentiment Impact | Cognitive Load Consideration | Implementation |
|---------|---------------------|---------------------------|--------------|
| **Enrollment Urgency** | "Limited Spots" creates FOMO | Keep visible but not anxiety-inducing | Amber accent, countdown timers |
| **Certification Focus** | Professional credibility signal | Balance with skill acquisition messaging | Dual-track messaging (cert + portfolio) |
| **Industry Partnerships** | Trust through association | Display prominently but not overwhelming | Logo strip with hover details |
| **Career Outcomes** | Transformation aspiration | Concrete metrics over vague promises | Salary increases, placement rates |

#### ⚡ TECHNICAL LAYER
| Consideration | Performance Impact | Implementation Strategy |
|--------------|-------------------|----------------------|
| **Course Cards** | Multiple DOM elements | Virtual scrolling for large catalogs, React Server Components |
| **Schedule Tables** | Dynamic availability | Django API with caching, SWR/React Query |
| **Progress Trackers** | Exam domain percentages | Animated SVG progress rings, CSS transforms only |
| **Video Content** | Heavy bandwidth | Mux/Cloudflare Stream with adaptive bitrate |
| **Search** | Query performance | Algolia/Meilisearch with fuzzy matching |

#### ♿ ACCESSIBILITY LAYER (WCAG 2.1 AA)
| Requirement | Standard | Solution |
|------------|----------|----------|
| **Color Contrast** | 4.5:1 normal, 3:1 large | Automated testing in CI/CD |
| **Keyboard Navigation** | Full tab order | Focus trap in modals, skip links |
| **Screen Reader** | ARIA labels | SVG + aria-labels (no emoji icons) |
| **Motion Sensitivity** | prefers-reduced-motion | CSS media query fallbacks |
| **Form Validation** | Label associations | React Hook Form + Zod schema |

#### 📈 SCALABILITY LAYER
| Component | Growth Challenge | Modular Solution |
|-----------|-----------------|-----------------|
| **Course Catalog** | 10x content growth | Dynamic taxonomy, CMS-driven |
| **User Accounts** | Multi-role support | Django auth + JWT tokens |
| **Video Library** | Storage/bandwidth | CDN + streaming service |
| **Search Index** | Query performance | Dedicated search service |

### 1.2 Technology Stack Architecture

```
┌─────────────────────────────────────────────────────────────────┐
│                     FULL-STACK ARCHITECTURE                     │
├─────────────────────────────────────────────────────────────────┤
│  FRONTEND (Next.js 16.1.4)                                     │
│  ├── React 19.2.3 (Server Components)                          │
│  ├── Tailwind CSS 4.1.18                                       │
│  ├── Framer Motion 12.29.0                                     │
│  ├── Zustand 5.0.3 (Client State)                              │
│  ├── Radix UI + Shadcn Components                              │
│  └── Lucide React 0.469.0 (Icons)                              │
├─────────────────────────────────────────────────────────────────┤
│  BACKEND (Django 6.0.2)                                        │
│  ├── Python 3.12+                                              │
│  ├── Django REST Framework                                     │
│  ├── PostgreSQL 16+ (Primary Database)                         │
│  ├── Redis 7+ (Caching + Sessions)                             │
│  ├── Celery 5.3+ (Async Tasks)                                 │
│  └── JWT Authentication (djangorestframework-simplejwt)        │
├─────────────────────────────────────────────────────────────────┤
│  INFRASTRUCTURE                                                │
│  ├── Frontend: Vercel (Edge Network)                           │
│  ├── Backend: AWS/GCP (Docker + Kubernetes)                    │
│  ├── Video: Mux or Cloudflare Stream                           │
│  ├── Search: Algolia or Meilisearch                            │
│  ├── CDN: Cloudflare (Assets + Security)                       │
│  └── Monitoring: Sentry + PostHog                              │
└─────────────────────────────────────────────────────────────────┘
```

### 1.3 Solution Exploration & Trade-off Analysis

| Approach | Pros | Cons | Recommendation |
|----------|------|------|---------------|
| **Next.js + Django** | Best of both worlds (React DX + Python ecosystem) | Cross-origin complexity | ✅ **SELECTED** |
| **Next.js + Next.js API** | Single codebase, simpler deployment | Python ML libraries unavailable | ❌ REJECT |
| **Django Templates + HTMX** | Full Python stack, simpler architecture | Less interactive UX, slower perceived perf | ❌ REJECT |
| **Next.js + Node.js Backend** | JavaScript throughout | Lose Django admin, ORM, auth maturity | ❌ REJECT |

**Selected Direction:** **Next.js 16.1.4 Frontend + Django 6.0.2 API Backend**
- Leverages React 19 Server Components for optimal performance
- Django provides mature admin, ORM, authentication, and Python ML integration
- Clear separation of concerns with API contract
- Industry-standard pattern for scalable applications

### 1.4 Risk Assessment & Mitigation

| Risk | Probability | Impact | Mitigation Strategy |
|------|------------|--------|-------------------|
| **CORS/Authentication Complexity** | HIGH | HIGH | Django CORS headers + JWT with refresh tokens |
| **Cross-Origin Performance** | MEDIUM | MEDIUM | CDN caching, API response optimization |
| **Generic AI Aesthetic** | HIGH | CRITICAL | Strict design system enforcement, design reviews |
| **WCAG Compliance** | MEDIUM | HIGH | Automated testing + manual audit before launch |
| **Video Bandwidth Costs** | MEDIUM | MEDIUM | Adaptive bitrate, CDN optimization |
| **Search Relevance** | MEDIUM | MEDIUM | Algolia tuning, synonym dictionaries |
| **Django API Versioning** | LOW | MEDIUM | API versioning from day one (v1/) |
| **Database Scaling** | LOW | HIGH | PostgreSQL read replicas, connection pooling |

---

## PHASE 2: DESIGN SYSTEM SPECIFICATION

### 2.1 Visual Identity Framework

#### 🎨 COLOR PALETTE (Precision Futurism)

```css
/* CSS Variables - Design Token System */
:root {
  /* Primary Brand Colors */
  --color-primary-50: #eef2ff;
  --color-primary-100: #e0e7ff;
  --color-primary-200: #c7d2fe;
  --color-primary-300: #a5b4fc;
  --color-primary-400: #818cf8;
  --color-primary-500: #6366f1;  /* Electric Indigo */
  --color-primary-600: #4f46e5;
  --color-primary-700: #4338ca;
  --color-primary-800: #3730a3;
  --color-primary-900: #312e81;

  /* Secondary/Accent Colors */
  --color-accent-cyan: #06b6d4;    /* Neural Cyan - AI associations */
  --color-accent-amber: #f59e0b;   /* Signal Amber - Urgency/CTAs */
  --color-accent-emerald: #10b981; /* Success states */

  /* Neutral Palette */
  --color-background: #fafaf9;      /* Soft Ivory */
  --color-foreground: #0f172a;      /* Deep Space */
  --color-surface: #ffffff;
  --color-surface-alt: #f8fafc;
  --color-border: #e2e8f0;
  --color-border-strong: #cbd5e1;

  /* Text Colors */
  --text-primary: #1e293b;
  --text-secondary: #475569;
  --text-tertiary: #94a3b8;
  --text-inverse: #f8fafc;

  /* Semantic Colors */
  --color-success: #10b981;
  --color-warning: #f59e0b;
  --color-error: #ef4444;
  --color-info: #3b82f6;

  /* Functional Colors */
  --color-ring: #6366f1;
  --color-focus: #4f46e5;
}

/* Dark Mode Support */
.dark {
  --color-background: #0f172a;
  --color-foreground: #f8fafc;
  --color-surface: #1e293b;
  --color-surface-alt: #334155;
  --color-border: #334155;
  --color-border-strong: #475569;
  --text-primary: #f1f5f9;
  --text-secondary: #cbd5e1;
  --text-tertiary: #64748b;
}
```

**Design Principle:** No gradients on backgrounds, no purple-to-pink clichés. Each color serves a specific functional purpose with clear semantic meaning.

#### 🔤 TYPOGRAPHY SYSTEM

```css
/* Font Families */
:root {
  --font-display: 'Space Grotesk', sans-serif;      /* H1-H3 */
  --font-body: 'Inter', sans-serif;                  /* Body, UI */
  --font-mono: 'JetBrains Mono', monospace;         /* Code, technical */
}

/* Typography Scale (Major Third: 1.250) */
.text-3xl { font-size: 1.953rem; line-height: 2.441rem; }  /* H1 */
.text-2xl { font-size: 1.563rem; line-height: 1.953rem; }  /* H2 */
.text-xl  { font-size: 1.250rem; line-height: 1.563rem; }  /* H3 */
.text-lg  { font-size: 1.000rem; line-height: 1.250rem; }  /* H4 */
.text-base { font-size: 1.000rem; line-height: 1.5rem; }   /* Body */
.text-sm  { font-size: 0.875rem; line-height: 1.25rem; }   /* Small */
.text-xs  { font-size: 0.750rem; line-height: 1rem; }      /* XS */

/* Font Weights */
.font-normal { font-weight: 400; }
.font-medium { font-weight: 500; }
.font-semibold { font-weight: 600; }
.font-bold { font-weight: 700; }

/* Letter Spacing (Display fonts) */
.tracking-tight { letter-spacing: -0.02em; }
.tracking-normal { letter-spacing: 0; }
.tracking-wide { letter-spacing: 0.025em; }
```

**Why This Matters:** Typography is 90% of web design. Space Grotesk provides distinctive character without sacrificing readability. Inter ensures optimal screen readability for body copy.

#### 📐 SPACING & LAYOUT GRID

```css
/* Spacing Scale (Base: 4px) */
:root {
  --spacing-0: 0;
  --spacing-1: 0.25rem;   /* 4px */
  --spacing-2: 0.5rem;    /* 8px */
  --spacing-3: 0.75rem;   /* 12px */
  --spacing-4: 1rem;      /* 16px */
  --spacing-5: 1.25rem;   /* 20px */
  --spacing-6: 1.5rem;    /* 24px */
  --spacing-8: 2rem;      /* 32px */
  --spacing-10: 2.5rem;   /* 40px */
  --spacing-12: 3rem;     /* 48px */
  --spacing-16: 4rem;     /* 64px */
  --spacing-20: 5rem;     /* 80px */
  --spacing-24: 6rem;     /* 96px */
  --spacing-32: 8rem;     /* 128px */
}

/* Layout Grid */
.container {
  max-width: 1280px;
  margin-left: auto;
  margin-right: auto;
  padding-left: 1rem;
  padding-right: 1rem;
}

/* Section Padding */
.section-padding {
  padding-top: 5rem;    /* 80px mobile */
  padding-bottom: 5rem;
}
@media (min-width: 768px) {
  .section-padding {
    padding-top: 7.5rem;  /* 120px desktop */
    padding-bottom: 7.5rem;
  }
}
```

### 2.2 Component Library Specification

#### 🎯 BUTTON SYSTEM (Shadcn/Radix Foundation)

```typescript
// components/ui/button.tsx
import * as React from "react"
import { Slot } from "@radix-ui/react-slot"
import { cva, type VariantProps } from "class-variance-authority"
import { cn } from "@/lib/utils"

const buttonVariants = cva(
  "inline-flex items-center justify-center gap-2 whitespace-nowrap rounded-md text-sm font-medium transition-all duration-200 ease-out focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-ring focus-visible:ring-offset-2 disabled:pointer-events-none disabled:opacity-50",
  {
    variants: {
      variant: {
        primary:
          "bg-primary-600 text-white hover:bg-primary-700 hover:scale-[1.02] active:scale-[0.98] shadow-lg shadow-primary-500/25",
        secondary:
          "border border-border-strong bg-transparent text-primary hover:bg-surface-alt hover:border-primary-400",
        ghost:
          "bg-transparent text-secondary hover:bg-surface-alt hover:text-primary",
        urgency:
          "bg-accent-amber text-white hover:bg-amber-600 hover:scale-[1.02] animate-pulse-slow",
        outline:
          "border border-border bg-transparent hover:bg-surface-alt",
      },
      size: {
        default: "h-11 px-5 py-2.5",
        sm: "h-9 px-4 text-xs",
        lg: "h-12 px-8 text-base",
        icon: "h-11 w-11",
      },
    },
    defaultVariants: {
      variant: "primary",
      size: "default",
    },
  }
)

export interface ButtonProps
  extends React.ButtonHTMLAttributes<HTMLButtonElement>,
    VariantProps<typeof buttonVariants> {
  asChild?: boolean
  isLoading?: boolean
  loadingText?: string
}

const Button = React.forwardRef<HTMLButtonElement, ButtonProps>(
  ({ className, variant, size, asChild = false, isLoading, loadingText, children, ...props }, ref) => {
    const Comp = asChild ? Slot : "button"
    return (
      <Comp
        className={cn(buttonVariants({ variant, size, className }))}
        ref={ref}
        disabled={isLoading || props.disabled}
        aria-busy={isLoading}
        {...props}
      >
        {isLoading ? (
          <>
            <svg className="animate-spin h-4 w-4" viewBox="0 0 24 24">
              <circle className="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" strokeWidth="4" fill="none" />
              <path className="opacity-75" fill="currentColor" d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4z" />
            </svg>
            {loadingText || children}
          </>
        ) : (
          children
        )}
      </Comp>
    )
  }
)
Button.displayName = "Button"

export { Button, buttonVariants }
```

**Button States (MUST implement all):**
- `default` - Normal state
- `hover` - Elevated shadow, slight scale (1.02)
- `active` - Pressed state, reduced shadow
- `focus` - 2px ring, 2px offset
- `disabled` - 50% opacity, cursor-not-allowed
- `loading` - Spinner replaces text, disabled interaction

#### 📦 COURSE CARD COMPONENT

```typescript
// types/course.ts
export interface Course {
  id: string
  slug: string
  title: string
  subtitle: string
  description: string
  thumbnail: {
    src: string
    alt: string
    aspectRatio: '16:9' | '4:3' | '1:1'
  }
  badge?: {
    text: string
    variant: 'new' | 'popular' | 'urgent'
  }
  modules: number
  duration: string
  level: 'Beginner' | 'Intermediate' | 'Advanced'
  rating: number
  reviewCount: number
  enrolledCount: number
  price: {
    amount: number
    currency: string
    original?: number
    paymentPlan?: string
  }
  nextCohort: string
  spotsRemaining?: number
  waitlistAvailable: boolean
  categories: string[]
  skills: string[]
}

// components/courses/course-card.tsx
import { motion } from 'framer-motion'
import { Badge } from '@/components/ui/badge'
import { Button } from '@/components/ui/button'
import { Star, Clock, Users, ArrowRight } from 'lucide-react'

interface CourseCardProps {
  course: Course
  variant?: 'default' | 'featured' | 'compact'
}

export function CourseCard({ course, variant = 'default' }: CourseCardProps) {
  return (
    <motion.article
      initial={{ opacity: 0, y: 20 }}
      whileInView={{ opacity: 1, y: 0 }}
      viewport={{ once: true, margin: '-50px' }}
      transition={{ duration: 0.4, ease: [0.25, 0.46, 0.45, 0.94] }}
      whileHover={{ y: -4, transition: { duration: 0.3 } }}
      className="group relative bg-surface border border-border rounded-xl overflow-hidden hover:border-primary-400 hover:shadow-xl transition-all duration-300"
    >
      {/* Badge */}
      {course.badge && (
        <div className="absolute top-4 right-4 z-10">
          <Badge variant={course.badge.variant}>{course.badge.text}</Badge>
        </div>
      )}

      {/* Thumbnail */}
      <div className="relative aspect-video overflow-hidden">
        <img
          src={course.thumbnail.src}
          alt={course.thumbnail.alt}
          className="object-cover w-full h-full group-hover:scale-105 transition-transform duration-500"
          loading="lazy"
        />
        <div className="absolute inset-0 bg-gradient-to-t from-black/60 to-transparent" />
      </div>

      {/* Content */}
      <div className="p-6">
        <h3 className="text-xl font-semibold tracking-tight mb-2 line-clamp-2">
          {course.title}
        </h3>
        <p className="text-secondary text-sm mb-4 line-clamp-2">
          {course.subtitle}
        </p>

        {/* Meta */}
        <div className="flex items-center gap-4 text-sm text-tertiary mb-4">
          <span className="flex items-center gap-1.5">
            <Clock className="w-4 h-4" />
            {course.duration}
          </span>
          <span className="flex items-center gap-1.5">
            <Users className="w-4 h-4" />
            {course.enrolledCount.toLocaleString()} enrolled
          </span>
        </div>

        {/* Rating */}
        <div className="flex items-center gap-2 mb-4">
          <div className="flex items-center">
            {[...Array(5)].map((_, i) => (
              <Star
                key={i}
                className={`w-4 h-4 ${
                  i < Math.floor(course.rating)
                    ? 'fill-accent-amber text-accent-amber'
                    : 'text-border'
                }`}
              />
            ))}
          </div>
          <span className="text-sm text-secondary">
            {course.rating} ({course.reviewCount})
          </span>
        </div>

        {/* Price & CTA */}
        <div className="flex items-center justify-between pt-4 border-t border-border">
          <div>
            <span className="text-2xl font-bold text-primary">
              ${course.price.amount}
            </span>
            {course.price.original && (
              <span className="text-sm text-tertiary line-through ml-2">
                ${course.price.original}
              </span>
            )}
          </div>
          <Button variant="primary" size="sm" className="gap-2">
            Enroll
            <ArrowRight className="w-4 h-4 group-hover:translate-x-1 transition-transform" />
          </Button>
        </div>

        {/* Urgency Indicator */}
        {course.spotsRemaining && course.spotsRemaining <= 5 && (
          <div className="mt-3 text-sm text-accent-amber font-medium">
            🔥 Only {course.spotsRemaining} spots remaining
          </div>
        )}
      </div>
    </motion.article>
  )
}
```

#### 📅 COHORT SCHEDULE COMPONENT

```typescript
// types/cohort.ts
export interface Cohort {
  id: string
  courseId: string
  startDate: string
  endDate: string
  timezone: string
  format: 'Live Online' | 'In-Person' | 'Hybrid'
  location?: string
  instructor: {
    id: string
    name: string
    title: string
    avatar?: string
  }
  availability: {
    status: 'available' | 'filling-fast' | 'waitlist' | 'closed'
    spotsTotal: number
    spotsRemaining: number
  }
  pricing: {
    earlyBird?: {
      amount: number
      deadline: string
    }
    standard: number
    corporate?: number
  }
}

// Status UI Mapping
const availabilityUI = {
  available: {
    indicator: 'bg-accent-emerald',
    label: 'Available',
    cta: 'Enroll Now',
  },
  'filling-fast': {
    indicator: 'bg-accent-amber',
    label: 'Filling Fast',
    cta: 'Secure Spot',
  },
  waitlist: {
    indicator: 'bg-border-strong',
    label: 'Waitlist',
    cta: 'Join Waitlist',
  },
  closed: {
    indicator: 'bg-tertiary',
    label: 'Closed',
    cta: 'Notify Me',
  },
}
```

### 2.3 Page Architecture

#### 🏠 HOMEPAGE STRUCTURE

```
┌─────────────────────────────────────────────────────────────────┐
│  NAVIGATION (Sticky, glassmorphism on scroll)                  │
│  Logo | Courses | Learning Paths | Enterprise | Resources | CTA│
│  + Command Palette (⌘K)                                        │
└─────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────┐
│  HERO SECTION (60/40 asymmetric split)                         │
│  ┌────────────────────┐  ┌──────────────────────────────────┐ │
│  │                    │  │  MASTER AI ENGINEERING           │ │
│  │   Abstract 3D/     │  │                                  │ │
│  │   Code Visual      │  │  Build production-grade AI       │ │
│  │   (Lottie/Video)   │  │  systems in 12 weeks             │ │
│  │                    │  │                                  │ │
│  │                    │  │  Next cohort: Apr 14, 2026       │ │
│  │                    │  │  [Enroll Now] [View Syllabus]    │ │
│  │                    │  │                                  │ │
│  │                    │  │  ★ 4.9/5 from 2,300+ graduates  │ │
│  └────────────────────┘  └──────────────────────────────────┘ │
└─────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────┐
│  TRUST SIGNALS (Logo strip, grayscale → color on hover)        │
│  "Trusted by engineers at:" [Company logos]                    │
└─────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────┐
│  COURSE CATEGORIES (Bento box grid)                            │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────┐               │
│  │ AI/ML       │  │ Data Science│  │ DevOps  │               │
│  │ (Large)     │  │ (Medium)    │  │ (Small) │               │
│  └─────────────┘  └─────────────┘  └─────────┘               │
│  ┌─────────────┐  ┌───────────────────────────┐               │
│  │ Security    │  │ Full-Stack Development    │               │
│  │ (Small)     │  │ (Wide)                    │               │
│  └─────────────┘  └───────────────────────────┘               │
└─────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────┐
│  LEARNING PATHS (Horizontal progression visualization)         │
│  [Foundation] → [Specialization] → [Advanced] → [Portfolio]    │
└─────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────┐
│  FEATURED COURSES (Masonry grid, varied heights)               │
│  [Course Card] [Course Card - Tall] [Course Card]              │
│  [Course Card - Wide] [Course Card] [Course Card]              │
└─────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────┐
│  STUDENT OUTCOMES (Stats + Testimonials masonry)               │
│  "85% salary increase average" | "92% placement rate"          │
│  Video testimonials + written reviews                          │
└─────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────┐
│  UPCOMING COHORTS (Table with availability indicators)         │
│  Course | Date | Format | Spots | Status | Action              │
└─────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────┐
│  ENTERPRISE CTA (Full-width, contrasting background)           │
│  "Train your team" | Custom curriculum | Volume discounts      │
│  [Contact Sales]                                               │
└─────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────┐
│  FOOTER (Multi-column, comprehensive)                          │
│  Courses | Company | Resources | Legal | Social                │
│  + Newsletter signup                                           │
└─────────────────────────────────────────────────────────────────┘
```

---

## PHASE 3: TECHNICAL IMPLEMENTATION PLAN

### 3.1 Frontend Architecture (Next.js 16.1.4)

```
frontend/
├── app/                          # Next.js App Router
│   ├── (marketing)/              # Marketing pages route group
│   │   ├── page.tsx              # Homepage
│   │   ├── courses/
│   │   │   ├── page.tsx          # Course listing
│   │   │   └── [slug]/
│   │   │       └── page.tsx      # Course detail
│   │   ├── paths/
│   │   │   └── page.tsx          # Learning paths
│   │   └── enterprise/
│   │       └── page.tsx          # Enterprise page
│   ├── (dashboard)/              # Authenticated route group
│   │   ├── dashboard/
│   │   │   └── page.tsx          # Student dashboard
│   │   ├── enrollments/
│   │   └── settings/
│   ├── api/                      # Next.js API routes (if needed)
│   ├── layout.tsx                # Root layout
│   └── globals.css               # Global styles + Tailwind
├── components/
│   ├── ui/                       # Shadcn primitives
│   │   ├── button.tsx
│   │   ├── card.tsx
│   │   ├── dialog.tsx
│   │   ├── input.tsx
│   │   └── ...
│   ├── marketing/                # Marketing components
│   │   ├── hero/
│   │   ├── feature-grid/
│   │   ├── testimonial-carousel/
│   │   └── cta-section/
│   ├── courses/                  # Course components
│   │   ├── course-card/
│   │   ├── course-detail/
│   │   ├── syllabus-module/
│   │   └── cohort-schedule/
│   ├── layout/                   # Layout components
│   │   ├── header/
│   │   ├── footer/
│   │   ├── navigation/
│   │   └── page-container/
│   └── shared/                   # Reusable components
│       ├── progress-ring/
│       ├── badge/
│       ├── avatar/
│       └── skeleton/
├── lib/
│   ├── utils.ts                  # CN helper, formatters
│   ├── constants.ts              # Site constants
│   ├── api-client.ts             # Django API client
│   └── validations.ts            # Zod schemas
├── hooks/
│   ├── use-cohort-availability.ts
│   ├── use-enrollment-mutation.ts
│   ├── use-auth.ts
│   └── use-scroll-progress.ts
├── stores/
│   └── use-app-store.ts          # Zustand global state
├── types/
│   ├── course.ts
│   ├── cohort.ts
│   ├── user.ts
│   └── api.ts
├── styles/
│   └── components.css            # Component overrides
├── public/
│   ├── fonts/
│   ├── images/
│   └── icons/
├── tests/
│   ├── unit/
│   ├── integration/
│   └── e2e/
├── package.json
├── tailwind.config.ts
├── tsconfig.json
└── next.config.ts
```

### 3.2 Backend Architecture (Django 6.0.2)

```
backend/
├── config/                       # Django project settings
│   ├── __init__.py
│   ├── settings/
│   │   ├── __init__.py
│   │   ├── base.py
│   │   ├── development.py
│   │   ├── production.py
│   │   └── testing.py
│   ├── urls.py
│   ├── wsgi.py
│   └── asgi.py
├── apps/
│   ├── accounts/                 # User authentication
│   │   ├── models.py
│   │   ├── serializers.py
│   │   ├── views.py
│   │   ├── urls.py
│   │   └── tests/
│   ├── courses/                  # Course management
│   │   ├── models.py
│   │   ├── serializers.py
│   │   ├── views.py
│   │   ├── urls.py
│   │   └── tests/
│   ├── enrollments/              # Enrollment tracking
│   │   ├── models.py
│   │   ├── serializers.py
│   │   ├── views.py
│   │   ├── urls.py
│   │   └── tests/
│   ├── payments/                 # Payment processing
│   │   ├── models.py
│   │   ├── serializers.py
│   │   ├── views.py
│   │   ├── urls.py
│   │   └── tests/
│   └── content/                  # CMS content
│       ├── models.py
│       ├── serializers.py
│       ├── views.py
│       └── urls.py
├── core/                         # Shared utilities
│   ├── exceptions.py
│   ├── pagination.py
│   ├── permissions.py
│   └── mixins.py
├── media/                        # User uploads
├── static/                       # Static files
├── templates/                    # Email templates
├── manage.py
├── requirements/
│   ├── base.txt
│   ├── development.txt
│   └── production.txt
├── Dockerfile
├── docker-compose.yml
└── .env.example
```

### 3.3 API Contract Specification

```python
# Django REST Framework API Endpoints

# Authentication
POST   /api/v1/auth/register/          # User registration
POST   /api/v1/auth/login/             # JWT token pair
POST   /api/v1/auth/logout/            # Token blacklisting
POST   /api/v1/auth/refresh/           # Refresh access token
GET    /api/v1/auth/me/                # Current user profile
PUT    /api/v1/auth/me/                # Update profile

# Courses
GET    /api/v1/courses/                # List courses (paginated)
GET    /api/v1/courses/{slug}/         # Course detail
GET    /api/v1/courses/{slug}/modules/ # Course modules
GET    /api/v1/courses/search/         # Search courses

# Cohorts
GET    /api/v1/courses/{id}/cohorts/   # List cohorts for course
GET    /api/v1/cohorts/{id}/           # Cohort detail
POST   /api/v1/cohorts/{id}/enroll/    # Enroll in cohort

# Enrollments
GET    /api/v1/enrollments/            # User enrollments
GET    /api/v1/enrollments/{id}/       # Enrollment detail
GET    /api/v1/enrollments/{id}/progress/  # Progress tracking

# Payments
POST   /api/v1/payments/checkout/      # Create checkout session
POST   /api/v1/payments/webhook/       # Payment webhook handler

# Content
GET    /api/v1/pages/{slug}/           # Static pages
GET    /api/v1/blog/                   # Blog posts
GET    /api/v1/blog/{slug}/            # Blog post detail
```

### 3.4 Django Models (Core)

```python
# apps/courses/models.py
from django.db import models
from django.utils.text import slugify
from apps.accounts.models import User

class Course(models.Model):
    title = models.CharField(max_length=200)
    slug = models.SlugField(unique=True, blank=True)
    subtitle = models.CharField(max_length=300)
    description = models.TextField()
    thumbnail = models.ImageField(upload_to='courses/thumbnails/')
    duration = models.CharField(max_length=50)  # "12 weeks"
    level = models.CharField(
        max_length=20,
        choices=[('beginner', 'Beginner'), ('intermediate', 'Intermediate'), ('advanced', 'Advanced')]
    )
    price = models.DecimalField(max_digits=10, decimal_places=2)
    original_price = models.DecimalField(max_digits=10, decimal_places=2, null=True, blank=True)
    rating = models.DecimalField(max_digits=3, decimal_places=2, default=0)
    review_count = models.PositiveIntegerField(default=0)
    enrolled_count = models.PositiveIntegerField(default=0)
    is_featured = models.BooleanField(default=False)
    is_active = models.BooleanField(default=True)
    created_at = models.DateTimeField(auto_now_add=True)
    updated_at = models.DateTimeField(auto_now=True)

    def save(self, *args, **kwargs):
        if not self.slug:
            self.slug = slugify(self.title)
        super().save(*args, **kwargs)

    def __str__(self):
        return self.title

class Module(models.Model):
    course = models.ForeignKey(Course, related_name='modules', on_delete=models.CASCADE)
    title = models.CharField(max_length=200)
    description = models.TextField()
    order = models.PositiveIntegerField()
    duration = models.CharField(max_length=50)

    class Meta:
        ordering = ['order']

    def __str__(self):
        return f"{self.course.title} - {self.title}"

class Cohort(models.Model):
    course = models.ForeignKey(Course, related_name='cohorts', on_delete=models.CASCADE)
    start_date = models.DateField()
    end_date = models.DateField()
    timezone = models.CharField(max_length=50, default='UTC')
    format = models.CharField(
        max_length=20,
        choices=[('online', 'Live Online'), ('in-person', 'In-Person'), ('hybrid', 'Hybrid')]
    )
    location = models.CharField(max_length=200, null=True, blank=True)
    spots_total = models.PositiveIntegerField()
    spots_remaining = models.PositiveIntegerField()
    price = models.DecimalField(max_digits=10, decimal_places=2)
    early_bird_price = models.DecimalField(max_digits=10, decimal_places=2, null=True, blank=True)
    early_bird_deadline = models.DateField(null=True, blank=True)
    is_active = models.BooleanField(default=True)

    def __str__(self):
        return f"{self.course.title} - {self.start_date}"

# apps/enrollments/models.py
class Enrollment(models.Model):
    user = models.ForeignKey(User, on_delete=models.CASCADE)
    cohort = models.ForeignKey(Cohort, on_delete=models.CASCADE)
    status = models.CharField(
        max_length=20,
        choices=[
            ('active', 'Active'),
            ('completed', 'Completed'),
            ('dropped', 'Dropped'),
            ('waitlist', 'Waitlist')
        ],
        default='active'
    )
    enrolled_at = models.DateTimeField(auto_now_add=True)
    completed_at = models.DateTimeField(null=True, blank=True)

    class Meta:
        unique_together = ['user', 'cohort']

    def __str__(self):
        return f"{self.user.email} - {self.cohort}"
```

### 3.5 Performance Optimization Strategy

| Optimization | Implementation | Target Metric |
|-------------|---------------|---------------|
| **Image Loading** | Next.js Image + WebP/AVIF | LCP < 2.5s |
| **Font Loading** | `font-display: swap` + preload | No FOIT |
| **Code Splitting** | Route-based + component lazy | Bundle < 200KB gzipped |
| **API Caching** | Django Redis cache + SWR | TTFB < 200ms |
| **Critical CSS** | Tailwind purge + inline above-fold | FCP < 1.5s |
| **Third-party** | Load after interaction | No blocking |
| **Database** | PostgreSQL connection pooling | Query < 100ms |
| **CDN** | Cloudflare for static assets | Cache hit > 90% |

### 3.6 Core Web Vitals Budget

| Metric | Target | Maximum | Measurement |
|--------|--------|---------|-------------|
| **Lighthouse Performance** | 90+ | 85 | Lighthouse CI |
| **First Contentful Paint** | < 1.5s | < 2.5s | Web Vitals API |
| **Largest Contentful Paint** | < 2.5s | < 4s | Web Vitals API |
| **Time to Interactive** | < 3.5s | < 5s | Lighthouse |
| **Cumulative Layout Shift** | < 0.1 | < 0.25 | Web Vitals API |
| **First Input Delay** | < 100ms | < 300ms | Web Vitals API |
| **Total Bundle Size** | < 200KB gzipped | < 500KB | Webpack Bundle Analyzer |

---

## PHASE 4: ACCESSIBILITY & QUALITY ASSURANCE

### 4.1 WCAG 2.1 AA Compliance Checklist

- [ ] **Color Contrast:** 4.5:1 normal text, 3:1 large text (automated testing)
- [ ] **Focus Indicators:** Visible 2px ring on all interactive elements
- [ ] **Keyboard Navigation:** Full tab order, logical sequence, focus traps in modals
- [ ] **Screen Reader:** All images have alt text, icons have aria-labels
- [ ] **Motion:** `prefers-reduced-motion` respected (Framer Motion config)
- [ ] **Forms:** All inputs have labels, error messages announced via aria-live
- [ ] **Headings:** Proper H1-H6 hierarchy, no skipped levels
- [ ] **Language:** `lang` attribute set, content language declared
- [ ] **Skip Links:** "Skip to main content" on all pages
- [ ] **ARIA:** Roles, states, properties used correctly
- [ ] **Semantic HTML:** Landmark regions, proper list structures

### 4.2 Testing Strategy

```bash
# Frontend Development Workflow
npm run dev          # Start dev server with Turbopack
npm run typecheck    # TypeScript validation
npm run lint         # ESLint + accessibility rules
npm test             # Unit tests (Vitest/Jest)
npm run test:e2e     # E2E tests (Playwright)

# Backend Development Workflow
python manage.py runserver              # Django dev server
python manage.py test                   # Run Django tests
python manage.py makemigrations         # Create migrations
python manage.py migrate                # Apply migrations
python manage.py lint                   # Django linting

# Pre-commit Hooks
npm run validate     # Run all frontend checks
# Backend: pre-commit with black, flake8, mypy

# CI/CD Pipeline
npm run build        # Production build
npm run lighthouse   # Performance audit
npm run pa11y        # Accessibility audit
# Backend: pytest, security scan, deployment
```

### 4.3 Edge Case Analysis

| Edge Case | Scenario | Solution |
|-----------|----------|----------|
| **No Courses Available** | All cohorts full/closed | Show waitlist CTA + "Notify Me" email capture |
| **Slow API Response** | Django backend latency | Skeleton loaders, SWR caching, optimistic UI |
| **Enrollment Failure** | Payment/registration error | Clear error message, retry option, support contact |
| **Mobile Safari** | iOS-specific bugs | Test on real devices, Safari dev tools |
| **Slow Connection** | 3G/edge networks | Progressive enhancement, critical CSS inline |
| **Screen Reader Users** | NVDA/JAWS navigation | ARIA live regions, logical reading order |
| **High Contrast Mode** | Windows HC settings | CSS forced-colors media query support |
| **Large Text** | User browser zoom 200% | Responsive typography, no fixed heights |
| **JWT Token Expiry** | Session timeout | Refresh token rotation, auto-reauth |
| **CORS Errors** | Cross-origin requests | Django CORS headers, allowed origins config |

---

## PHASE 5: IMPLEMENTATION ROADMAP

### 5.1 Timeline & Phasing (8 Weeks)

```
┌─────────────────────────────────────────────────────────────────┐
│                    8-WEEK IMPLEMENTATION TIMELINE               │
├─────────────────────────────────────────────────────────────────┤
│  WEEK 1-2: FOUNDATION                                          │
│  ├── Design system setup (colors, typography, spacing tokens)  │
│  ├── Component library initialization (Shadcn/ui base)         │
│  ├── Django project setup + core models                        │
│  ├── Authentication system (JWT + Django REST)                 │
│  └── Development environment (Docker + local configs)          │
├─────────────────────────────────────────────────────────────────┤
│  WEEK 3-4: CORE PAGES                                          │
│  ├── Homepage (Hero, features, courses, social proof)          │
│  ├── Course listing page (filtering, search, sorting)          │
│  ├── Course detail page (curriculum, instructor, enrollment)   │
│  ├── Django API endpoints (courses, cohorts, enrollments)      │
│  └── Static pages (About, Contact, FAQ)                        │
├─────────────────────────────────────────────────────────────────┤
│  WEEK 5-6: INTERACTIVE FEATURES                                │
│  ├── User authentication flow (login, register, profile)       │
│  ├── Enrollment/checkout process (Stripe integration)          │
│  ├── Student dashboard (progress, certificates)                │
│  ├── Search functionality (Algolia integration)                │
│  └── Video integration (Mux/Cloudflare Stream)                 │
├─────────────────────────────────────────────────────────────────┤
│  WEEK 7-8: POLISH & LAUNCH                                     │
│  ├── Animation implementation (Framer Motion)                  │
│  ├── Accessibility audit (axe-core + manual testing)           │
│  ├── Performance optimization (Lighthouse targets)             │
│  ├── Content population (CMS setup)                            │
│  ├── QA testing (cross-browser, mobile, e2e)                   │
│  └── Launch (production deployment + monitoring)               │
└─────────────────────────────────────────────────────────────────┘
```

### 5.2 Phase Checklists

#### Phase 1: Foundation (Weeks 1-2)

```markdown
FRONTEND
[ ] Initialize Next.js 16.1.4 project with Turbopack
[ ] Install and configure Tailwind CSS 4.1.18
[ ] Set up Shadcn/ui component library
[ ] Create design token system (CSS variables)
[ ] Build base components (Button, Card, Input, etc.)
[ ] Configure Framer Motion for animations
[ ] Set up Zustand for state management
[ ] Create API client for Django backend

BACKEND
[ ] Initialize Django 6.0.2 project
[ ] Configure PostgreSQL database
[ ] Set up Django REST Framework
[ ] Implement JWT authentication
[ ] Create core models (Course, Module, Cohort, Enrollment)
[ ] Set up Redis for caching
[ ] Configure CORS headers
[ ] Create API serializers and views

INFRASTRUCTURE
[ ] Docker configuration for both frontend and backend
[ ] Docker Compose for local development
[ ] Environment variable management (.env)
[ ] CI/CD pipeline setup (GitHub Actions)
```

#### Phase 2: Core Pages (Weeks 3-4)

```markdown
FRONTEND
[ ] Homepage with hero, features, course grid
[ ] Course listing page with filters and search
[ ] Course detail page with curriculum accordion
[ ] Navigation component (sticky header + mobile menu)
[ ] Footer component
[ ] Responsive design for all breakpoints

BACKEND
[ ] Course API endpoints (list, detail, search)
[ ] Cohort API endpoints
[ ] Category/tag system
[ ] Image upload handling
[ ] Pagination implementation
[ ] API documentation (Swagger/Redoc)
```

#### Phase 3: Interactive Features (Weeks 5-6)

```markdown
FRONTEND
[ ] Authentication pages (login, register, forgot password)
[ ] Protected routes and auth guards
[ ] Enrollment flow with payment integration
[ ] Student dashboard with progress tracking
[ ] Search with Algolia instant results
[ ] Video player integration

BACKEND
[ ] User profile management
[ ] Enrollment management
[ ] Payment webhook handling (Stripe)
[ ] Progress tracking endpoints
[ ] Email notifications (Celery tasks)
[ ] Search index synchronization
```

#### Phase 4: Polish & Launch (Weeks 7-8)

```markdown
QUALITY
[ ] Accessibility audit (axe-core + manual testing)
[ ] Performance optimization (Lighthouse 90+)
[ ] Cross-browser testing (Chrome, Safari, Firefox, Edge)
[ ] Mobile responsiveness testing (iOS, Android)
[ ] E2E testing (Playwright)

DEPLOYMENT
[ ] Production environment setup
[ ] SSL certificates
[ ] CDN configuration
[ ] Monitoring setup (Sentry, PostHog)
[ ] Backup strategy
[ ] Launch checklist completion

DOCUMENTATION
[ ] API documentation
[ ] Component documentation (Storybook)
[ ] Deployment runbook
[ ] User guides
```

---

## PHASE 6: SUCCESS METRICS & VALIDATION

### 6.1 Quantitative Metrics

| Metric | Target | Measurement Method |
|--------|--------|-------------------|
| **Homepage Conversion Rate** | > 3% | Analytics (PostHog/GA4) |
| **Course Page Enrollment Rate** | > 8% | Analytics + Backend tracking |
| **Lighthouse Performance Score** | 90+ | Lighthouse CI |
| **Lighthouse Accessibility Score** | 100 | Lighthouse CI |
| **Lighthouse SEO Score** | 95+ | Lighthouse CI |
| **Lighthouse Best Practices** | 100 | Lighthouse CI |
| **NPS (Net Promoter Score)** | > 50 | Post-enrollment survey |
| **Page Load Time (LCP)** | < 2.5s | Web Vitals API |
| **API Response Time (p95)** | < 200ms | Backend monitoring |
| **Error Rate** | < 0.1% | Sentry tracking |

### 6.2 Qualitative Criteria

- [ ] **Distinctive Visual Identity:** No "AI slop" aesthetics, memorable "Precision Futurism" design
- [ ] **Professional Credibility:** Enterprise buyers feel confident in platform quality
- [ ] **User Clarity:** Visitors understand offerings within 5 seconds
- [ ] **Emotional Resonance:** Design inspires action, not just informs
- [ ] **Scalability:** System supports 10x content growth without redesign
- [ ] **Maintainability:** New team members can contribute within 1 week
- [ ] **Security:** All security headers implemented, no critical vulnerabilities
- [ ] **Documentation:** Complete and accessible for all team members

---

## PHASE 7: DELIVERABLES & KNOWLEDGE TRANSFER

### 7.1 Deliverable Checklist

- [ ] **Design System Documentation** (Figma + Storybook)
- [ ] **Component Library** (Fully tested, documented)
- [ ] **Page Templates** (Home, Course Listing, Course Detail, Dashboard, About, Contact)
- [ ] **Style Guide** (Typography, colors, spacing, usage guidelines)
- [ ] **Accessibility Report** (WCAG 2.1 AA audit results)
- [ ] **Performance Report** (Lighthouse scores, optimization log)
- [ ] **API Documentation** (Swagger/Redoc + Postman collection)
- [ ] **Database Schema** (ERD + migration files)
- [ ] **Deployment Guide** (CI/CD pipeline, environment setup)
- [ ] **Maintenance Runbook** (Common issues, troubleshooting)

### 7.2 Knowledge Transfer Sessions

| Session | Audience | Duration | Topics |
|---------|----------|----------|--------|
| **Design System Overview** | Designers + Developers | 2 hours | Tokens, components, usage patterns |
| **Frontend Architecture** | Developers | 2 hours | Next.js structure, state management, API integration |
| **Backend Architecture** | Developers | 2 hours | Django structure, models, API design |
| **Accessibility Deep-Dive** | All team members | 1.5 hours | WCAG requirements, testing tools |
| **Content Management** | Content team | 1 hour | CMS workflow, best practices |
| **Deployment & Monitoring** | DevOps + Developers | 1 hour | CI/CD, analytics, error tracking |

### 7.3 Documentation Standards

All documentation will include:
1. **Purpose:** Why this component/pattern exists
2. **Usage:** Code examples with props/variants
3. **Accessibility:** ARIA requirements, keyboard interactions
4. **Performance:** Loading behavior, optimization notes
5. **Edge Cases:** Known limitations, fallback behaviors
6. **Related Components:** Links to connected patterns

---

## PHASE 8: ANTI-GENERIC COMMITMENT PLEDGE

**I commit to the following design principles throughout this project:**

1. ❌ **NO** Inter/Roboto without distinctive typographic hierarchy
2. ❌ **NO** Purple-gradient-on-white clichés
3. ❌ **NO** Predictable card grids without intentional asymmetry
4. ❌ **NO** Template aesthetics or "safe" defaults
5. ❌ **NO** Surface-level logic without deep justification
6. ✅ **YES** to intentional minimalism where whitespace is structural
7. ✅ **YES** to bespoke layouts that guide eye movement purposefully
8. ✅ **YES** to library discipline (Shadcn/Radix) styled for vision
9. ✅ **YES** to every element earning its place through calculated purpose
10. ✅ **YES** to multi-dimensional analysis (psychological, technical, accessibility, scalability)

**Creative Direction:** "Precision Futurism" — maintaining authority while introducing dynamic, intelligence-forward visual metaphors appropriate for cutting-edge technical education.

---

## PHASE 9: RISK ASSESSMENT & MITIGATION

| Risk | Probability | Impact | Mitigation |
|------|------------|--------|------------|
| **Performance degradation with rich media** | MEDIUM | HIGH | Lazy loading, CDN optimization, video compression, adaptive bitrate |
| **Accessibility gaps in custom components** | MEDIUM | HIGH | Radix UI primitives, automated a11y testing, manual audit |
| **Content management complexity** | MEDIUM | MEDIUM | Structured CMS schema, content validation, admin training |
| **Cross-browser animation inconsistencies** | LOW | MEDIUM | CSS-first animations, feature detection, graceful degradation |
| **SEO challenges with client-side rendering** | MEDIUM | MEDIUM | Next.js SSR/SSG, proper meta tags, structured data |
| **CORS/Authentication complexity** | MEDIUM | HIGH | Django CORS headers, JWT with refresh tokens, thorough testing |
| **Database scaling** | LOW | HIGH | PostgreSQL read replicas, connection pooling, query optimization |
| **Payment flow failures** | LOW | HIGH | Stripe webhooks, retry logic, manual reconciliation process |
| **Video bandwidth costs** | MEDIUM | MEDIUM | Adaptive bitrate, CDN caching, usage monitoring |
| **Search relevance issues** | MEDIUM | MEDIUM | Algolia tuning, synonym dictionaries, analytics feedback |

---

## PHASE 10: VALIDATION CHECKPOINT

### 10.1 PRD Completeness Verification

| Criterion | Status | Evidence |
|-----------|--------|----------|
| **Full-stack architecture** | ✅ Complete | Next.js + Django specified with model/API contracts |
| **Design system specificity** | ✅ Complete | CSS variables, typography scale, component specs |
| **Accessibility standards** | ✅ Complete | WCAG 2.1 AA with checklist |
| **Performance budget** | ✅ Complete | Core Web Vitals with targets |
| **Security considerations** | ✅ Complete | JWT, CORS, security headers |
| **Timeline realism** | ✅ Complete | 8-week phased approach |
| **Risk assessment** | ✅ Complete | 10 risks with mitigations |
| **Success metrics** | ✅ Complete | Quantitative + qualitative |
| **Knowledge transfer** | ✅ Complete | 6 training sessions defined |
| **Anti-generic enforcement** | ✅ Complete | 10-point pledge |

### 10.2 Approval to Proceed

**This PRD is ready for implementation upon confirmation of:**

- [ ] Design direction aligns with brand vision ("Precision Futurism")
- [ ] Technical stack meets infrastructure requirements (Next.js + Django)
- [ ] Accessibility standards are non-negotiable (WCAG 2.1 AA)
- [ ] Timeline and resource allocation are realistic (8 weeks)
- [ ] Success criteria are measurable and agreed upon

**Your approval triggers Phase 1: Foundation (Weeks 1-2)**

---

## APPENDIX A: PACKAGE.JSON (FRONTEND)

```json
{
  "name": "ai-training-platform-frontend",
  "version": "1.0.0",
  "private": true,
  "scripts": {
    "dev": "next dev --turbopack",
    "build": "next build",
    "start": "next start",
    "lint": "next lint",
    "typecheck": "tsc --noEmit",
    "test": "vitest",
    "test:e2e": "playwright test",
    "storybook": "storybook dev -p 6006",
    "build-storybook": "storybook build"
  },
  "dependencies": {
    "next": "16.1.4",
    "react": "19.2.3",
    "react-dom": "19.2.3",
    "framer-motion": "^12.29.0",
    "zustand": "^5.0.3",
    "lucide-react": "^0.469.0",
    "@radix-ui/react-slot": "^1.1.1",
    "@radix-ui/react-dialog": "^1.1.4",
    "@radix-ui/react-dropdown-menu": "^2.1.4",
    "@radix-ui/react-navigation-menu": "^1.2.3",
    "@radix-ui/react-progress": "^1.1.2",
    "@radix-ui/react-tabs": "^1.1.2",
    "@radix-ui/react-toast": "^1.2.4",
    "class-variance-authority": "^0.7.1",
    "clsx": "^2.1.1",
    "tailwind-merge": "^2.6.0",
    "zod": "^3.24.1",
    "react-hook-form": "^7.54.2",
    "@hookform/resolvers": "^4.0.0",
    "swr": "^2.3.0",
    "@tanstack/react-query": "^5.64.0"
  },
  "devDependencies": {
    "@types/node": "^20",
    "@types/react": "^19",
    "@types/react-dom": "^19",
    "tailwindcss": "^4.1.18",
    "@tailwindcss/postcss": "^4.1.18",
    "postcss": "^8.5.3",
    "typescript": "^5.9.3",
    "vitest": "^2.1.8",
    "@playwright/test": "^1.49.1",
    "@storybook/react": "^8.4.7",
    "eslint": "^9.17.0",
    "eslint-config-next": "16.1.4",
    "@typescript-eslint/eslint-plugin": "^8.18.2",
    "prettier": "^3.4.2",
    "prettier-plugin-tailwindcss": "^0.6.9"
  }
}
```

---

## APPENDIX B: DJANGO REQUIREMENTS (BACKEND)

```txt
# requirements/base.txt
Django==6.0.2
djangorestframework==3.15.2
djangorestframework-simplejwt==5.4.0
django-cors-headers==4.6.0
django-filter==24.3
django-storages==1.14.4
django-extensions==3.2.3
psycopg2-binary==2.9.10
redis==5.2.1
celery==5.4.0
stripe==11.4.0
Pillow==11.1.0
python-dotenv==1.0.1
gunicorn==23.0.0
whitenoise==6.8.2
sentry-sdk==2.20.0
drf-spectacular==0.28.1

# requirements/development.txt
-r base.txt
django-debug-toolbar==4.4.6
pytest==8.3.4
pytest-django==4.9.0
pytest-cov==6.0.0
black==24.10.0
flake8==7.1.1
mypy==1.14.1
pre-commit==4.0.1

# requirements/production.txt
-r base.txt
```

---

## APPENDIX C: ENVIRONMENT VARIABLES

```bash
# Frontend (.env.local)
NEXT_PUBLIC_API_URL=https://api.yourdomain.com/api/v1
NEXT_PUBLIC_SITE_URL=https://www.yourdomain.com
NEXT_PUBLIC_ALGOLIA_APP_ID=XXX
NEXT_PUBLIC_ALGOLIA_SEARCH_KEY=XXX
NEXT_PUBLIC_MUX_PLAYER_KEY=XXX
NEXT_PUBLIC_POSTHOG_KEY=XXX
NEXT_PUBLIC_SENTRY_DSN=XXX

# Backend (.env)
SECRET_KEY=your-secret-key-here
DEBUG=False
ALLOWED_HOSTS=api.yourdomain.com
CORS_ALLOWED_ORIGINS=https://www.yourdomain.com

# Database
DATABASE_URL=postgresql://user:password@localhost:5432/dbname

# Redis
REDIS_URL=redis://localhost:6379/0

# JWT
JWT_ACCESS_TOKEN_LIFETIME=60
JWT_REFRESH_TOKEN_LIFETIME=1440

# Email
EMAIL_HOST=smtp.sendgrid.net
EMAIL_PORT=587
EMAIL_HOST_USER=user
EMAIL_HOST_PASSWORD=password
DEFAULT_FROM_EMAIL=noreply@yourdomain.com

# Stripe
STRIPE_SECRET_KEY=sk_test_XXX
STRIPE_WEBHOOK_SECRET=whsec_XXX

# Mux/Video
MUX_TOKEN_ID=XXX
MUX_TOKEN_SECRET=XXX

# Algolia
ALGOLIA_APP_ID=XXX
ALGOLIA_ADMIN_KEY=XXX
ALGOLIA_INDEX_NAME=courses
```

---

*Document prepared following Meticulous Approach SOP | Version 2.0 | March 06, 2026*

*This PRD represents exhaustive synthesis of two comprehensive analyses with specific technology stack integration. Every recommendation is backed by industry best practices, comparative analysis findings, and anti-generic design philosophy.*
