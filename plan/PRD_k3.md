# **PROJECT REQUIREMENT DOCUMENT (v3.0 - FINAL)**
## **AI & Software Training Platform — Complete Design & Technical Specification**

**Synthesized from:** Original Generated PRD + PRD_q2.md + iTrust Academy Competitive Analysis  
**Document Version:** 3.0 (Merged & Optimized)  
**Date:** March 06, 2026  
**Classification:** Strategic Design & Technical Blueprint  
**Status:** Ready for Implementation  
**Design Philosophy:** Precision Futurism  
**Tech Stack:** Next.js 16.1.4 + React 19.2.3 + Django 6.0.2 + PostgreSQL 16

---

## **EXECUTIVE SUMMARY**

This document represents the **definitive synthesis** of strategic design analysis and technical implementation specifications. After rigorous comparative analysis of the iTrust Academy design language against modern AI/software training platform requirements, this PRD establishes a **"Precision Futurism"** aesthetic direction—maintaining professional authority while signaling innovation and technical excellence.

**Key Differentiators:**
- **Anti-Generic Design:** Rejects template aesthetics for bespoke "Precision Futurism" visual identity
- **Exact Version Alignment:** Every dependency pinned to your specified versions (Next.js 16.1.4, Django 6.0.2, etc.)
- **Production-Ready Code:** Copy-pasteable TypeScript/React components with full Django backend
- **Psychological Optimization:** Enrollment psychology, cognitive load management, trust signal architecture
- **Full-Stack Completeness:** Frontend + Backend + DevOps + QA in unified specification

**Critical Success Factor:** This platform must differentiate from traditional IT certification sites (like iTrust Academy) through **dynamic intelligence-forward visual metaphors** while maintaining the **conversion-optimized clarity** that makes training platforms successful.

---

## **PHASE 1: STRATEGIC FOUNDATION**

### **1.1 Competitive Analysis: iTrust Academy Deconstruction**

#### **What iTrust Does Well (To Emulate):**
| Element | Implementation | Our Adaptation |
|---------|---------------|--------------|
| **Authority Positioning** | Vendor authorization badges | AI industry partnership logos + instructor credentials |
| **Certification Clarity** | SCP exam domain breakdown | Learning path visualization with skill tree progression |
| **Schedule Transparency** | Specific dates with availability | Real-time cohort capacity with urgency indicators |
| **Trust Signals** | "Authorized Training Partner" | "Hiring Partner Network" + salary outcome statistics |
| **Regional Expertise** | Multi-language support | Timezone-aware cohort scheduling |

#### **Where iTrust Falls Short (To Differentiate):**
| iTrust Limitation | Our Opportunity | Implementation |
|-------------------|----------------|----------------|
| Static, corporate aesthetic | Dynamic, intelligence-forward design | Animated data visualizations, code sandbox integration |
| Vendor-locked content | Platform-agnostic, project-based learning | Multi-cloud curriculum (AWS/Azure/GCP) |
| Certification-only focus | Portfolio + career outcomes | GitHub-integrated project showcases |
| Traditional classroom model | AI-enhanced personalized learning | Adaptive learning paths, AI tutor integration |
| Generic imagery | Abstract technical visualizations | Generative code art, neural network visualizations |

### **1.2 Design Philosophy: "Precision Futurism"**

**Core Tenets:**
1. **Intentional Minimalism:** Every element earns its place through calculated purpose
2. **Technical Authority:** Design signals expertise without corporate sterility
3. **Dynamic Intelligence:** Motion and interaction suggest AI/ML capabilities
4. **Conversion Clarity:** Enrollment paths are frictionless and urgency-optimized
5. **Anti-Generic Enforcement:** Zero tolerance for template aesthetics

**Visual Metaphor Translation:**
- **iTrust's "Corporate Blue"** → **Our "Electric Indigo"** (#4f46e5) + **Neural Cyan** (#06b6d4)
- **iTrust's "Certification Badges"** → **Our "Skill Tree Progression"** (visual learning paths)
- **iTrust's "Vendor Logos"** → **Our "Hiring Partner Network"** (outcome-focused social proof)
- **iTrust's "Static Schedules"** → **Our "Live Capacity Indicators"** (real-time urgency)

### **1.3 Psychological UX Architecture**

#### **User Sentiment Mapping**

| Journey Stage | Emotional State | Design Response | Implementation |
|--------------|----------------|-----------------|----------------|
| **Awareness** | Skeptical, overwhelmed | Instant credibility + clarity | Hero: "Build Production-Grade AI Systems" + partner logos |
| **Interest** | Curious, evaluating | Social proof + specificity | Stats: "85% salary increase", "92% placement rate" |
| **Consideration** | Anxious, risk-averse | Risk reversal + urgency | "7-day money-back guarantee" + "Only 3 spots left" |
| **Enrollment** | Committed, excited | Frictionless + celebration | One-click enrollment + confirmation animation |
| **Learning** | Challenged, supported | Progress visibility + support | Skill tree + AI tutor + community access |

#### **Cognitive Load Optimization**

| Element | iTrust Approach | Our Optimization | Rationale |
|---------|----------------|------------------|-----------|
| Course cards | Dense text blocks | Bento grid with visual hierarchy | Reduces scanning effort |
| Curriculum | Bulleted lists | Accordion with progress indicators | Progressive disclosure |
| Pricing | Single price | Payment plans + ROI calculator | Reduces sticker shock |
| Scheduling | Static table | Interactive calendar with filters | Reduces decision fatigue |

---

## **PHASE 2: DESIGN SYSTEM SPECIFICATION**

### **2.1 Visual Identity Framework**

#### **Color Palette (CSS Custom Properties)**

```css
/* design-tokens/colors.css */
:root {
  /* Primary Brand: Electric Indigo */
  --color-primary-50: #eef2ff;
  --color-primary-100: #e0e7ff;
  --color-primary-200: #c7d2fe;
  --color-primary-300: #a5b4fc;
  --color-primary-400: #818cf8;
  --color-primary-500: #6366f1;  /* Base */
  --color-primary-600: #4f46e5;  /* Primary Action */
  --color-primary-700: #4338ca;
  --color-primary-800: #3730a3;
  --color-primary-900: #312e81;

  /* Secondary: Neural Cyan (AI/ML associations) */
  --color-cyan-400: #22d3ee;
  --color-cyan-500: #06b6d4;  /* Accent */
  --color-cyan-600: #0891b2;

  /* Tertiary: Signal Amber (Urgency/CTAs) */
  --color-amber-400: #fbbf24;
  --color-amber-500: #f59e0b;  /* Urgency */
  --color-amber-600: #d97706;

  /* Success: Emerald */
  --color-emerald-500: #10b981;
  --color-emerald-600: #059669;

  /* Neutral: Sophisticated Slate (not pure gray) */
  --color-background: #fafaf9;      /* Warm ivory */
  --color-surface: #ffffff;
  --color-surface-alt: #f8fafc;
  --color-border: #e2e8f0;
  --color-border-strong: #cbd5e1;
  
  /* Text Hierarchy */
  --text-primary: #0f172a;          /* Deep space */
  --text-secondary: #475569;        /* Slate 600 */
  --text-tertiary: #94a3b8;         /* Slate 400 */
  --text-inverse: #f8fafc;          /* Off-white */

  /* Functional */
  --color-ring: #6366f1;
  --color-focus: #4f46e5;
  --color-error: #ef4444;
  --color-warning: #f59e0b;
}

/* Dark Mode (Systematic Inversion) */
.dark {
  --color-background: #0f172a;
  --color-surface: #1e293b;
  --color-surface-alt: #334155;
  --color-border: #334155;
  --color-border-strong: #475569;
  --text-primary: #f1f5f9;
  --text-secondary: #cbd5e1;
  --text-tertiary: #64748b;
}
```

**Design Enforcement Rule:** No gradients on backgrounds. No purple-to-pink clichés. Each color serves a specific functional purpose.

#### **Typography System**

```css
/* design-tokens/typography.css */
:root {
  /* Font Families */
  --font-display: 'Space Grotesk', system-ui, sans-serif;
  --font-body: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
  --font-mono: 'JetBrains Mono', 'Fira Code', monospace;

  /* Type Scale (Major Third: 1.250) */
  --text-xs: 0.75rem;      /* 12px */
  --text-sm: 0.875rem;     /* 14px */
  --text-base: 1rem;       /* 16px */
  --text-lg: 1.125rem;     /* 18px */
  --text-xl: 1.25rem;      /* 20px */
  --text-2xl: 1.5rem;      /* 24px */
  --text-3xl: 1.875rem;    /* 30px */
  --text-4xl: 2.25rem;     /* 36px */
  --text-5xl: 3rem;        /* 48px */
  --text-6xl: 3.75rem;     /* 60px */

  /* Line Heights */
  --leading-none: 1;
  --leading-tight: 1.25;
  --leading-snug: 1.375;
  --leading-normal: 1.5;
  --leading-relaxed: 1.625;

  /* Letter Spacing */
  --tracking-tight: -0.02em;
  --tracking-normal: 0;
  --tracking-wide: 0.025em;
}

/* Utility Classes */
.font-display { font-family: var(--font-display); }
.font-body { font-family: var(--font-body); }
.font-mono { font-family: var(--font-mono); }

/* Hierarchy Specifications */
.heading-1 {
  font-family: var(--font-display);
  font-size: var(--text-5xl);
  font-weight: 700;
  line-height: var(--leading-tight);
  letter-spacing: var(--tracking-tight);
}

.heading-2 {
  font-family: var(--font-display);
  font-size: var(--text-3xl);
  font-weight: 600;
  line-height: var(--leading-snug);
}

.body-large {
  font-family: var(--font-body);
  font-size: var(--text-lg);
  line-height: var(--leading-relaxed);
  color: var(--text-secondary);
}
```

**Anti-Generic Enforcement:** Space Grotesk provides distinctive geometric character without sacrificing readability. Inter ensures optimal screen performance.

#### **Spacing System (4px Base Grid)**

```css
/* design-tokens/spacing.css */
:root {
  --space-0: 0;
  --space-1: 0.25rem;   /* 4px */
  --space-2: 0.5rem;    /* 8px */
  --space-3: 0.75rem;   /* 12px */
  --space-4: 1rem;      /* 16px */
  --space-5: 1.25rem;   /* 20px */
  --space-6: 1.5rem;    /* 24px */
  --space-8: 2rem;      /* 32px */
  --space-10: 2.5rem;   /* 40px */
  --space-12: 3rem;     /* 48px */
  --space-16: 4rem;     /* 64px */
  --space-20: 5rem;     /* 80px */
  --space-24: 6rem;     /* 96px */
  --space-32: 8rem;     /* 128px */
}

/* Section Spacing (Responsive) */
.section-padding {
  padding-top: var(--space-20);      /* 80px mobile */
  padding-bottom: var(--space-20);
}

@media (min-width: 768px) {
  .section-padding {
    padding-top: var(--space-24);    /* 96px tablet */
    padding-bottom: var(--space-24);
  }
}

@media (min-width: 1024px) {
  .section-padding {
    padding-top: var(--space-32);    /* 128px desktop */
    padding-bottom: var(--space-32);
  }
}
```

### **2.2 Animation & Motion System**

#### **Motion Philosophy**
- **Purposeful:** Every animation guides attention or provides feedback
- **Performant:** CSS transforms only, `will-change` optimization
- **Accessible:** Respects `prefers-reduced-motion`
- **Brand-Aligned:** Motion suggests precision, intelligence, and modernity

#### **Animation Specifications**

```typescript
// lib/animations.ts
export const easings = {
  // Smooth deceleration for UI elements
  smooth: [0.25, 0.46, 0.45, 0.94],
  // Snappy for micro-interactions
  snappy: [0.4, 0, 0.2, 1],
  // Bounce for celebratory moments
  bounce: [0.68, -0.55, 0.265, 1.55],
  // Linear for continuous animations
  linear: [0, 0, 1, 1],
} as const;

export const durations = {
  instant: 0.1,
  fast: 0.2,
  normal: 0.3,
  slow: 0.5,
  dramatic: 0.8,
} as const;

// Page load stagger
export const staggerContainer = {
  hidden: { opacity: 0 },
  visible: {
    opacity: 1,
    transition: {
      staggerChildren: 0.1,
      delayChildren: 0.1,
    },
  },
};

export const fadeUpItem = {
  hidden: { opacity: 0, y: 20 },
  visible: {
    opacity: 1,
    y: 0,
    transition: {
      duration: durations.slow,
      ease: easings.smooth,
    },
  },
};

// Card hover lift
export const cardHover = {
  rest: { y: 0, boxShadow: '0 1px 3px rgba(0,0,0,0.1)' },
  hover: { 
    y: -4, 
    boxShadow: '0 20px 40px rgba(0,0,0,0.1)',
    transition: { duration: durations.normal, ease: easings.smooth }
  },
};

// Button press
export const buttonTap = {
  scale: 0.98,
  transition: { duration: durations.instant },
};

// Progress ring animation
export const progressRing = {
  hidden: { pathLength: 0, opacity: 0 },
  visible: { 
    pathLength: 1, 
    opacity: 1,
    transition: { duration: 1.5, ease: easings.smooth }
  },
};
```

#### **Specific Interaction Patterns**

| Element | Trigger | Animation | Specs |
|---------|---------|-----------|-------|
| **Page Sections** | Scroll into view | Fade up + stagger | Y: 20px→0, Opacity: 0→1, Stagger: 100ms |
| **Course Cards** | Hover | Lift + shadow intensify | Y: -4px, Shadow: 0 20px 40px rgba(0,0,0,0.1) |
| **Buttons** | Hover | Scale + shadow | Scale: 1.02, Shadow expansion |
| **Buttons** | Tap | Press feedback | Scale: 0.98, Duration: 100ms |
| **Navigation** | Scroll > 50px | Glassmorphism | Backdrop-blur: 12px, BG: rgba(255,255,255,0.8) |
| **Progress Rings** | Load | SVG path draw | PathLength: 0→1, Duration: 1.5s |
| **Accordion** | Click | Height expand | Height: auto, Duration: 300ms |
| **Modal** | Open | Scale + fade | Scale: 0.95→1, Opacity: 0→1 |

---

## **PHASE 3: COMPONENT LIBRARY**

### **3.1 Button System (Shadcn/Radix Foundation)**

```typescript
// components/ui/button.tsx
import * as React from "react"
import { Slot } from "@radix-ui/react-slot"
import { cva, type VariantProps } from "class-variance-authority"
import { cn } from "@/lib/utils"
import { motion } from "framer-motion"

const buttonVariants = cva(
  "inline-flex items-center justify-center gap-2 whitespace-nowrap rounded-lg text-sm font-medium transition-all duration-200 focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-[var(--color-ring)] focus-visible:ring-offset-2 disabled:pointer-events-none disabled:opacity-50",
  {
    variants: {
      variant: {
        primary:
          "bg-[var(--color-primary-600)] text-white hover:bg-[var(--color-primary-700)] shadow-lg shadow-[var(--color-primary-500)]/25 hover:shadow-xl hover:shadow-[var(--color-primary-500)]/30",
        secondary:
          "border border-[var(--color-border-strong)] bg-transparent text-[var(--color-primary-600)] hover:bg-[var(--color-surface-alt)] hover:border-[var(--color-primary-400)]",
        ghost:
          "bg-transparent text-[var(--text-secondary)] hover:bg-[var(--color-surface-alt)] hover:text-[var(--text-primary)]",
        urgency:
          "bg-[var(--color-amber-500)] text-white hover:bg-[var(--color-amber-600)] shadow-lg shadow-[var(--color-amber-500)]/25 animate-pulse-slow",
        outline:
          "border border-[var(--color-border)] bg-transparent hover:bg-[var(--color-surface-alt)]",
        danger:
          "bg-red-600 text-white hover:bg-red-700 shadow-lg shadow-red-500/25",
      },
      size: {
        default: "h-11 px-6 py-2.5",
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
  withMotion?: boolean
}

const Button = React.forwardRef<HTMLButtonElement, ButtonProps>(
  ({ className, variant, size, asChild = false, isLoading, loadingText, withMotion = true, children, ...props }, ref) => {
    const Comp = asChild ? Slot : "button"
    
    const buttonContent = (
      <Comp
        className={cn(buttonVariants({ variant, size, className }))}
        ref={ref}
        disabled={isLoading || props.disabled}
        aria-busy={isLoading}
        {...props}
      >
        {isLoading ? (
          <>
            <svg className="animate-spin h-4 w-4" viewBox="0 0 24 24" aria-hidden="true">
              <circle className="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" strokeWidth="4" fill="none" />
              <path className="opacity-75" fill="currentColor" d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4z" />
            </svg>
            <span>{loadingText || children}</span>
          </>
        ) : (
          children
        )}
      </Comp>
    )

    if (!withMotion) return buttonContent

    return (
      <motion.div
        whileHover={{ scale: 1.02 }}
        whileTap={{ scale: 0.98 }}
        transition={{ duration: 0.2 }}
      >
        {buttonContent}
      </motion.div>
    )
  }
)
Button.displayName = "Button"

export { Button, buttonVariants }
```

**Button States (All Required):**
- `default` - Normal state with shadow
- `hover` - Elevated shadow, slight scale (1.02), color darken
- `active` - Pressed state (scale 0.98), reduced shadow
- `focus` - 2px ring, 2px offset, high contrast
- `disabled` - 50% opacity, cursor-not-allowed, no hover effects
- `loading` - Spinner replaces icon, disabled interaction, aria-busy="true"

### **3.2 Course Card Component**

```typescript
// components/courses/course-card.tsx
"use client"

import { motion } from "framer-motion"
import Image from "next/image"
import Link from "next/link"
import { Badge } from "@/components/ui/badge"
import { Button } from "@/components/ui/button"
import { Star, Clock, Users, ArrowRight, Zap } from "lucide-react"
import { fadeUpItem, cardHover } from "@/lib/animations"

export interface Course {
  id: string
  slug: string
  title: string
  subtitle: string
  description: string
  thumbnail: {
    src: string
    alt: string
  }
  badge?: {
    text: string
    variant: "new" | "popular" | "urgent" | "bestseller"
  }
  modules: number
  duration: string
  level: "Beginner" | "Intermediate" | "Advanced"
  rating: number
  reviewCount: number
  enrolledCount: number
  price: {
    amount: number
    currency: string
    original?: number
  }
  nextCohort: string
  spotsRemaining?: number
  waitlistAvailable: boolean
  categories: string[]
  skills: string[]
}

interface CourseCardProps {
  course: Course
  variant?: "default" | "featured" | "compact"
  index?: number
}

export function CourseCard({ course, variant = "default", index = 0 }: CourseCardProps) {
  const isUrgent = course.spotsRemaining && course.spotsRemaining <= 5
  
  return (
    <motion.article
      variants={fadeUpItem}
      initial="hidden"
      whileInView="visible"
      viewport={{ once: true, margin: "-50px" }}
      whileHover="hover"
      className="group relative bg-[var(--color-surface)] border border-[var(--color-border)] rounded-2xl overflow-hidden transition-colors hover:border-[var(--color-primary-400)]"
    >
      <motion.div variants={cardHover} className="h-full flex flex-col">
        {/* Badge */}
        {course.badge && (
          <div className="absolute top-4 right-4 z-10">
            <Badge 
              variant={course.badge.variant}
              className="shadow-lg"
            >
              {course.badge.text}
            </Badge>
          </div>
        )}

        {/* Thumbnail */}
        <Link href={`/courses/${course.slug}`} className="relative aspect-video overflow-hidden block">
          <Image
            src={course.thumbnail.src}
            alt={course.thumbnail.alt}
            fill
            className="object-cover transition-transform duration-500 group-hover:scale-105"
            sizes="(max-width: 768px) 100vw, (max-width: 1200px) 50vw, 33vw"
          />
          <div className="absolute inset-0 bg-gradient-to-t from-black/60 via-black/20 to-transparent" />
          
          {/* Level Badge */}
          <div className="absolute bottom-4 left-4">
            <span className={cn(
              "px-3 py-1 rounded-full text-xs font-medium text-white backdrop-blur-md",
              course.level === "Beginner" && "bg-emerald-500/80",
              course.level === "Intermediate" && "bg-[var(--color-amber-500)]/80",
              course.level === "Advanced" && "bg-[var(--color-primary-600)]/80"
            )}>
              {course.level}
            </span>
          </div>
        </Link>

        {/* Content */}
        <div className="flex-1 p-6 flex flex-col">
          {/* Categories */}
          <div className="flex flex-wrap gap-2 mb-3">
            {course.categories.slice(0, 2).map((cat) => (
              <span key={cat} className="text-xs text-[var(--text-tertiary)]">
                {cat}
              </span>
            ))}
          </div>

          <Link href={`/courses/${course.slug}`}>
            <h3 className="text-xl font-semibold tracking-tight mb-2 line-clamp-2 group-hover:text-[var(--color-primary-600)] transition-colors">
              {course.title}
            </h3>
          </Link>
          
          <p className="text-[var(--text-secondary)] text-sm mb-4 line-clamp-2 flex-1">
            {course.subtitle}
          </p>

          {/* Meta Row */}
          <div className="flex items-center gap-4 text-sm text-[var(--text-tertiary)] mb-4">
            <span className="flex items-center gap-1.5">
              <Clock className="w-4 h-4" aria-hidden="true" />
              {course.duration}
            </span>
            <span className="flex items-center gap-1.5">
              <Users className="w-4 h-4" aria-hidden="true" />
              {course.enrolledCount.toLocaleString()}
            </span>
            <span className="flex items-center gap-1.5">
              <Zap className="w-4 h-4" aria-hidden="true" />
              {course.modules} modules
            </span>
          </div>

          {/* Rating */}
          <div className="flex items-center gap-2 mb-4">
            <div className="flex items-center" aria-label={`Rating: ${course.rating} out of 5 stars`}>
              {[...Array(5)].map((_, i) => (
                <Star
                  key={i}
                  className={cn(
                    "w-4 h-4",
                    i < Math.floor(course.rating)
                      ? "fill-[var(--color-amber-400)] text-[var(--color-amber-400)]"
                      : "text-[var(--color-border)]"
                  )}
                  aria-hidden="true"
                />
              ))}
            </div>
            <span className="text-sm font-medium text-[var(--text-primary)]">
              {course.rating}
            </span>
            <span className="text-sm text-[var(--text-tertiary)]">
              ({course.reviewCount.toLocaleString()})
            </span>
          </div>

          {/* Price & CTA */}
          <div className="flex items-center justify-between pt-4 border-t border-[var(--color-border)]">
            <div className="flex flex-col">
              <span className="text-2xl font-bold text-[var(--color-primary-600)]">
                ${course.price.amount}
              </span>
              {course.price.original && (
                <span className="text-sm text-[var(--text-tertiary)] line-through">
                  ${course.price.original}
                </span>
              )}
            </div>
            <Button variant="primary" size="sm" className="gap-2">
              Enroll
              <ArrowRight className="w-4 h-4 transition-transform group-hover:translate-x-1" aria-hidden="true" />
            </Button>
          </div>

          {/* Urgency Indicator */}
          {isUrgent && (
            <div className="mt-3 flex items-center gap-2 text-sm text-[var(--color-amber-600)] font-medium animate-pulse">
              <Zap className="w-4 h-4" aria-hidden="true" />
              Only {course.spotsRemaining} spots remaining
            </div>
          )}
        </div>
      </motion.div>
    </motion.article>
  )
}
```

### **3.3 Cohort Schedule Component**

```typescript
// components/courses/cohort-schedule.tsx
"use client"

import { useState } from "react"
import { motion, AnimatePresence } from "framer-motion"
import { format, parseISO } from "date-fns"
import { Badge } from "@/components/ui/badge"
import { Button } from "@/components/ui/button"
import { Calendar, MapPin, Globe, Users, CheckCircle } from "lucide-react"

export interface Cohort {
  id: string
  courseId: string
  startDate: string
  endDate: string
  timezone: string
  format: "Live Online" | "In-Person" | "Hybrid"
  location?: string
  instructor: {
    id: string
    name: string
    title: string
    avatar?: string
    company?: string
  }
  availability: {
    status: "available" | "filling-fast" | "waitlist" | "closed"
    spotsTotal: number
    spotsRemaining: number
  }
  pricing: {
    earlyBird?: {
      amount: number
      deadline: string
    }
    standard: number
  }
  schedule: {
    days: string[]
    time: string
  }
}

const availabilityConfig = {
  available: {
    indicator: "bg-[var(--color-emerald-500)]",
    label: "Available",
    cta: "Enroll Now",
    badge: "default" as const,
  },
  "filling-fast": {
    indicator: "bg-[var(--color-amber-500)]",
    label: "Filling Fast",
    cta: "Secure Spot",
    badge: "urgent" as const,
  },
  waitlist: {
    indicator: "bg-[var(--text-tertiary)]",
    label: "Waitlist",
    cta: "Join Waitlist",
    badge: "secondary" as const,
  },
  closed: {
    indicator: "bg-[var(--color-border-strong)]",
    label: "Closed",
    cta: "Notify Me",
    badge: "outline" as const,
  },
}

interface CohortScheduleProps {
  cohorts: Cohort[]
  courseSlug: string
}

export function CohortSchedule({ cohorts, courseSlug }: CohortScheduleProps) {
  const [selectedCohort, setSelectedCohort] = useState<string | null>(null)

  return (
    <div className="space-y-4">
      <h3 className="text-2xl font-semibold mb-6">Upcoming Cohorts</h3>
      
      <div className="grid gap-4">
        {cohorts.map((cohort) => {
          const config = availabilityConfig[cohort.availability.status]
          const isSelected = selectedCohort === cohort.id
          
          return (
            <motion.div
              key={cohort.id}
              initial={{ opacity: 0, y: 10 }}
              animate={{ opacity: 1, y: 0 }}
              className={cn(
                "border rounded-xl p-6 transition-all cursor-pointer",
                isSelected 
                  ? "border-[var(--color-primary-400)] bg-[var(--color-primary-50)]" 
                  : "border-[var(--color-border)] hover:border-[var(--color-primary-300)]"
              )}
              onClick={() => setSelectedCohort(isSelected ? null : cohort.id)}
              role="button"
              tabIndex={0}
              aria-expanded={isSelected}
            >
              <div className="flex flex-col lg:flex-row lg:items-center justify-between gap-4">
                {/* Date & Format */}
                <div className="flex items-start gap-4">
                  <div className="flex-shrink-0 w-16 h-16 bg-[var(--color-surface-alt)] rounded-lg flex flex-col items-center justify-center border border-[var(--color-border)]">
                    <span className="text-xs text-[var(--text-tertiary)] uppercase">
                      {format(parseISO(cohort.startDate), "MMM")}
                    </span>
                    <span className="text-xl font-bold text-[var(--text-primary)]">
                      {format(parseISO(cohort.startDate), "d")}
                    </span>
                  </div>
                  
                  <div>
                    <div className="flex items-center gap-2 mb-1">
                      <h4 className="font-semibold text-lg">
                        {format(parseISO(cohort.startDate), "MMMM d")} - {format(parseISO(cohort.endDate), "MMMM d, yyyy")}
                      </h4>
                      <Badge variant={config.badge}>{config.label}</Badge>
                    </div>
                    
                    <div className="flex flex-wrap items-center gap-4 text-sm text-[var(--text-secondary)]">
                      <span className="flex items-center gap-1">
                        <Calendar className="w-4 h-4" />
                        {cohort.schedule.days.join(", ")}
                      </span>
                      <span className="flex items-center gap-1">
                        <Globe className="w-4 h-4" />
                        {cohort.timezone}
                      </span>
                      <span className="flex items-center gap-1">
                        {cohort.format === "Live Online" ? <Globe className="w-4 h-4" /> : <MapPin className="w-4 h-4" />}
                        {cohort.format}
                        {cohort.location && ` • ${cohort.location}`}
                      </span>
                    </div>
                  </div>
                </div>

                {/* Availability & Price */}
                <div className="flex items-center gap-6">
                  <div className="text-right">
                    <div className="flex items-center gap-2 justify-end mb-1">
                      <span className={cn("w-2 h-2 rounded-full", config.indicator)} />
                      <span className="text-sm font-medium">
                        {cohort.availability.spotsRemaining} spots left
                      </span>
                    </div>
                    <div className="text-2xl font-bold text-[var(--color-primary-600)]">
                      ${cohort.pricing.earlyBird?.amount || cohort.pricing.standard}
                    </div>
                    {cohort.pricing.earlyBird && (
                      <div className="text-xs text-[var(--text-tertiary)]">
                        Early bird ends {format(parseISO(cohort.pricing.earlyBird.deadline), "MMM d")}
                      </div>
                    )}
                  </div>
                  
                  <Button 
                    variant={cohort.availability.status === "available" ? "primary" : "secondary"}
                    className="min-w-[140px]"
                  >
                    {config.cta}
                  </Button>
                </div>
              </div>

              {/* Expanded Details */}
              <AnimatePresence>
                {isSelected && (
                  <motion.div
                    initial={{ height: 0, opacity: 0 }}
                    animate={{ height: "auto", opacity: 1 }}
                    exit={{ height: 0, opacity: 0 }}
                    transition={{ duration: 0.3 }}
                    className="overflow-hidden"
                  >
                    <div className="pt-6 mt-6 border-t border-[var(--color-border)]">
                      <div className="grid md:grid-cols-2 gap-6">
                        <div>
                          <h5 className="font-medium mb-3">Instructor</h5>
                          <div className="flex items-center gap-3">
                            {cohort.instructor.avatar ? (
                              <img 
                                src={cohort.instructor.avatar} 
                                alt="" 
                                className="w-12 h-12 rounded-full object-cover"
                              />
                            ) : (
                              <div className="w-12 h-12 rounded-full bg-[var(--color-primary-100)] flex items-center justify-center text-[var(--color-primary-600)] font-bold">
                                {cohort.instructor.name.charAt(0)}
                              </div>
                            )}
                            <div>
                              <div className="font-medium">{cohort.instructor.name}</div>
                              <div className="text-sm text-[var(--text-secondary)]">{cohort.instructor.title}</div>
                              {cohort.instructor.company && (
                                <div className="text-xs text-[var(--text-tertiary)]">{cohort.instructor.company}</div>
                              )}
                            </div>
                          </div>
                        </div>
                        
                        <div>
                          <h5 className="font-medium mb-3">What&apos;s Included</h5>
                          <ul className="space-y-2">
                            {[
                              "Live instruction + recordings",
                              "Hands-on lab environments",
                              "Certification exam voucher",
                              "1-year community access",
                              "Career support & job referrals"
                            ].map((item) => (
                              <li key={item} className="flex items-center gap-2 text-sm text-[var(--text-secondary)]">
                                <CheckCircle className="w-4 h-4 text-[var(--color-emerald-500)]" />
                                {item}
                              </li>
                            ))}
                          </ul>
                        </div>
                      </div>
                    </div>
                  </motion.div>
                )}
              </AnimatePresence>
            </motion.div>
          )
        })}
      </div>
    </div>
  )
}
```

### **3.4 Navigation Component**

```typescript
// components/layout/navigation.tsx
"use client"

import { useState, useEffect } from "react"
import Link from "next/link"
import { usePathname } from "next/navigation"
import { motion, AnimatePresence } from "framer-motion"
import { Button } from "@/components/ui/button"
import { Menu, X, Search, Command } from "lucide-react"
import { cn } from "@/lib/utils"

const navItems = [
  { label: "Courses", href: "/courses" },
  { label: "Learning Paths", href: "/paths" },
  { label: "Enterprise", href: "/enterprise" },
  { label: "Resources", href: "/resources" },
]

export function Navigation() {
  const [isScrolled, setIsScrolled] = useState(false)
  const [isMobileMenuOpen, setIsMobileMenuOpen] = useState(false)
  const pathname = usePathname()

  useEffect(() => {
    const handleScroll = () => {
      setIsScrolled(window.scrollY > 50)
    }
    window.addEventListener("scroll", handleScroll)
    return () => window.removeEventListener("scroll", handleScroll)
  }, [])

  return (
    <>
      <motion.header
        initial={{ y: -100 }}
        animate={{ y: 0 }}
        className={cn(
          "fixed top-0 left-0 right-0 z-50 transition-all duration-300",
          isScrolled 
            ? "bg-[var(--color-surface)]/80 backdrop-blur-xl border-b border-[var(--color-border)] shadow-sm" 
            : "bg-transparent"
        )}
      >
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="flex items-center justify-between h-16 lg:h-20">
            {/* Logo */}
            <Link href="/" className="flex items-center gap-2">
              <div className="w-8 h-8 bg-[var(--color-primary-600)] rounded-lg flex items-center justify-center">
                <span className="text-white font-bold text-lg">A</span>
              </div>
              <span className="font-display font-bold text-xl tracking-tight">
                Academy
              </span>
            </Link>

            {/* Desktop Navigation */}
            <nav className="hidden lg:flex items-center gap-8">
              {navItems.map((item) => (
                <Link
                  key={item.href}
                  href={item.href}
                  className={cn(
                    "text-sm font-medium transition-colors hover:text-[var(--color-primary-600)]",
                    pathname === item.href 
                      ? "text-[var(--color-primary-600)]" 
                      : "text-[var(--text-secondary)]"
                  )}
                >
                  {item.label}
                </Link>
              ))}
            </nav>

            {/* Desktop Actions */}
            <div className="hidden lg:flex items-center gap-4">
              <button 
                className="flex items-center gap-2 text-sm text-[var(--text-secondary)] hover:text-[var(--text-primary)] transition-colors"
                aria-label="Search"
              >
                <Search className="w-4 h-4" />
                <span className="hidden xl:inline">Search</span>
                <kbd className="hidden xl:inline-flex items-center gap-1 px-2 py-0.5 text-xs bg-[var(--color-surface-alt)] border border-[var(--color-border)] rounded">
                  <Command className="w-3 h-3" />
                  K
                </kbd>
              </button>
              
              <Button variant="ghost" size="sm">
                Sign In
              </Button>
              <Button variant="primary" size="sm">
                Get Started
              </Button>
            </div>

            {/* Mobile Menu Button */}
            <button
              className="lg:hidden p-2"
              onClick={() => setIsMobileMenuOpen(!isMobileMenuOpen)}
              aria-label={isMobileMenuOpen ? "Close menu" : "Open menu"}
              aria-expanded={isMobileMenuOpen}
            >
              {isMobileMenuOpen ? (
                <X className="w-6 h-6" />
              ) : (
                <Menu className="w-6 h-6" />
              )}
            </button>
          </div>
        </div>
      </motion.header>

      {/* Mobile Menu */}
      <AnimatePresence>
        {isMobileMenuOpen && (
          <motion.div
            initial={{ opacity: 0, y: -20 }}
            animate={{ opacity: 1, y: 0 }}
            exit={{ opacity: 0, y: -20 }}
            className="fixed inset-0 z-40 lg:hidden"
          >
            <div 
              className="absolute inset-0 bg-black/20 backdrop-blur-sm"
              onClick={() => setIsMobileMenuOpen(false)}
            />
            <motion.nav
              initial={{ x: "100%" }}
              animate={{ x: 0 }}
              exit={{ x: "100%" }}
              transition={{ type: "spring", damping: 25, stiffness: 200 }}
              className="absolute right-0 top-0 bottom-0 w-full max-w-sm bg-[var(--color-surface)] border-l border-[var(--color-border)] p-6 pt-20"
            >
              <div className="flex flex-col gap-4">
                {navItems.map((item) => (
                  <Link
                    key={item.href}
                    href={item.href}
                    className="text-lg font-medium py-2 border-b border-[var(--color-border)]"
                    onClick={() => setIsMobileMenuOpen(false)}
                  >
                    {item.label}
                  </Link>
                ))}
                <div className="flex flex-col gap-3 mt-4">
                  <Button variant="secondary" className="w-full">
                    Sign In
                  </Button>
                  <Button variant="primary" className="w-full">
                    Get Started
                  </Button>
                </div>
              </div>
            </motion.nav>
          </motion.div>
        )}
      </AnimatePresence>
    </>
  )
}
```

---

## **PHASE 4: PAGE ARCHITECTURE**

### **4.1 Homepage Structure**

```typescript
// app/(marketing)/page.tsx
import { Metadata } from "next"
import { Hero } from "@/components/marketing/hero"
import { TrustSignals } from "@/components/marketing/trust-signals"
import { CourseCategories } from "@/components/marketing/course-categories"
import { LearningPaths } from "@/components/marketing/learning-paths"
import { FeaturedCourses } from "@/components/marketing/featured-courses"
import { StudentOutcomes } from "@/components/marketing/student-outcomes"
import { UpcomingCohorts } from "@/components/marketing/upcoming-cohorts"
import { EnterpriseCTA } from "@/components/marketing/enterprise-cta"

export const metadata: Metadata = {
  title: "Master AI Engineering | Production-Grade AI Training",
  description: "Build production-grade AI systems in 12 weeks. Live instruction, hands-on labs, and career support from industry experts.",
  openGraph: {
    title: "Master AI Engineering | Academy",
    description: "Build production-grade AI systems in 12 weeks",
    type: "website",
  },
}

export default function HomePage() {
  return (
    <main>
      <Hero />
      <TrustSignals />
      <CourseCategories />
      <LearningPaths />
      <FeaturedCourses />
      <StudentOutcomes />
      <UpcomingCohorts />
      <EnterpriseCTA />
    </main>
  )
}
```

#### **Hero Section Specification**

```typescript
// components/marketing/hero.tsx
"use client"

import { motion } from "framer-motion"
import Link from "next/link"
import { Button } from "@/components/ui/button"
import { ArrowRight, Play, Star } from "lucide-react"
import { staggerContainer, fadeUpItem } from "@/lib/animations"

export function Hero() {
  return (
    <section className="relative min-h-screen flex items-center pt-20 overflow-hidden">
      {/* Background Elements */}
      <div className="absolute inset-0 -z-10">
        <div className="absolute top-0 right-0 w-1/2 h-full bg-gradient-to-l from-[var(--color-primary-50)] to-transparent" />
        <div className="absolute bottom-0 left-0 w-96 h-96 bg-[var(--color-cyan-500)]/10 rounded-full blur-3xl" />
      </div>

      <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 w-full">
        <div className="grid lg:grid-cols-2 gap-12 lg:gap-20 items-center">
          {/* Content */}
          <motion.div
            variants={staggerContainer}
            initial="hidden"
            animate="visible"
            className="max-w-2xl"
          >
            <motion.div variants={fadeUpItem} className="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-[var(--color-primary-100)] text-[var(--color-primary-700)] text-sm font-medium mb-6">
              <Star className="w-4 h-4 fill-current" />
              Now enrolling — April 2026 cohort
            </motion.div>

            <motion.h1 
              variants={fadeUpItem}
              className="heading-1 mb-6"
            >
              Master{" "}
              <span className="text-[var(--color-primary-600)]">AI Engineering</span>
              {" "}in 12 Weeks
            </motion.h1>

            <motion.p 
              variants={fadeUpItem}
              className="body-large mb-8 max-w-xl"
            >
              Build production-grade AI systems with hands-on training from ex-Google, 
              OpenAI, and Meta engineers. Deploy 6 portfolio projects and join our 
              hiring partner network.
            </motion.p>

            <motion.div variants={fadeUpItem} className="flex flex-col sm:flex-row gap-4 mb-8">
              <Button variant="primary" size="lg" className="gap-2">
                Enroll Now
                <ArrowRight className="w-5 h-5" />
              </Button>
              <Button variant="secondary" size="lg" className="gap-2">
                <Play className="w-5 h-5" />
                Watch Demo
              </Button>
            </motion.div>

            <motion.div variants={fadeUpItem} className="flex items-center gap-6 text-sm text-[var(--text-secondary)]">
              <div className="flex items-center gap-2">
                <div className="flex -space-x-2">
                  {[1,2,3,4].map((i) => (
                    <div key={i} className="w-8 h-8 rounded-full border-2 border-[var(--color-surface)] bg-[var(--color-surface-alt)]" />
                  ))}
                </div>
                <span>2,300+ graduates</span>
              </div>
              <div className="flex items-center gap-1">
                <Star className="w-4 h-4 fill-[var(--color-amber-400)] text-[var(--color-amber-400)]" />
                <span className="font-medium text-[var(--text-primary)]">4.9/5</span>
                <span>from 800+ reviews</span>
              </div>
            </motion.div>
          </motion.div>

          {/* Visual */}
          <motion.div
            initial={{ opacity: 0, scale: 0.95 }}
            animate={{ opacity: 1, scale: 1 }}
            transition={{ duration: 0.8, delay: 0.2 }}
            className="relative hidden lg:block"
          >
            <div className="relative aspect-square rounded-2xl bg-gradient-to-br from-[var(--color-primary-500)] to-[var(--color-cyan-500)] p-1">
              <div className="absolute inset-0 rounded-2xl bg-[var(--color-surface)] m-1 flex items-center justify-center">
                {/* Abstract code/AI visualization */}
                <div className="w-full h-full rounded-xl bg-[var(--color-surface-alt)] p-8 flex flex-col gap-4">
                  <div className="flex items-center gap-2 mb-4">
                    <div className="w-3 h-3 rounded-full bg-red-500" />
                    <div className="w-3 h-3 rounded-full bg-amber-500" />
                    <div className="w-3 h-3 rounded-full bg-emerald-500" />
                  </div>
                  <div className="space-y-3 font-mono text-sm">
                    <div className="text-[var(--text-tertiary)]"># Training neural network...</div>
                    <div className="text-[var(--color-primary-600)]">epoch 45/100 <span className="text-[var(--text-secondary)]">loss: 0.0234</span></div>
                    <div className="h-2 bg-[var(--color-border)] rounded-full overflow-hidden">
                      <div className="h-full w-[75%] bg-[var(--color-primary-500)] rounded-full" />
                    </div>
                    <div className="grid grid-cols-3 gap-2 mt-4">
                      {[...Array(6)].map((_, i) => (
                        <div key={i} className="h-16 bg-[var(--color-primary-100)] rounded-lg animate-pulse" style={{ animationDelay: `${i * 0.1}s` }} />
                      ))}
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </motion.div>
        </div>
      </div>
    </section>
  )
}
```

### **4.2 Course Detail Page**

```typescript
// app/(marketing)/courses/[slug]/page.tsx
import { Metadata } from "next"
import { notFound } from "next/navigation"
import { CourseHero } from "@/components/courses/course-hero"
import { CourseCurriculum } from "@/components/courses/course-curriculum"
import { CourseInstructor } from "@/components/courses/course-instructor"
import { CourseReviews } from "@/components/courses/course-reviews"
import { CohortSchedule } from "@/components/courses/cohort-schedule"
import { StickyEnrollment } from "@/components/courses/sticky-enrollment"
import { getCourseBySlug, getCourseCohorts } from "@/lib/api"

interface CoursePageProps {
  params: { slug: string }
}

export async function generateMetadata({ params }: CoursePageProps): Promise<Metadata> {
  const course = await getCourseBySlug(params.slug)
  if (!course) return { title: "Course Not Found" }
  
  return {
    title: `${course.title} | Academy`,
    description: course.subtitle,
  }
}

export default async function CoursePage({ params }: CoursePageProps) {
  const [course, cohorts] = await Promise.all([
    getCourseBySlug(params.slug),
    getCourseCohorts(params.slug),
  ])

  if (!course) notFound()

  return (
    <main className="pt-20">
      <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div className="grid lg:grid-cols-3 gap-12">
          {/* Main Content */}
          <div className="lg:col-span-2 space-y-16 pb-20">
            <CourseHero course={course} />
            <CourseCurriculum modules={course.modules} />
            <CourseInstructor instructor={course.instructor} />
            <CourseReviews reviews={course.reviews} />
            <CohortSchedule cohorts={cohorts} courseSlug={course.slug} />
          </div>

          {/* Sidebar */}
          <aside className="hidden lg:block">
            <div className="sticky top-24">
              <StickyEnrollment course={course} cohorts={cohorts} />
            </div>
          </aside>
        </div>
      </div>
    </main>
  )
}
```

---

## **PHASE 5: BACKEND ARCHITECTURE (Django 6.0.2)**

### **5.1 Project Structure**

```
backend/
├── config/                       # Django project configuration
│   ├── __init__.py
│   ├── settings/
│   │   ├── __init__.py
│   │   ├── base.py              # Shared settings
│   │   ├── development.py
│   │   ├── production.py
│   │   └── testing.py
│   ├── urls.py                  # Root URL configuration
│   ├── wsgi.py
│   └── asgi.py
├── apps/
│   ├── accounts/                # User authentication & profiles
│   ├── courses/                 # Course & curriculum management
│   ├── cohorts/                 # Cohort scheduling & enrollment
│   ├── enrollments/             # Enrollment tracking
│   ├── payments/                # Payment processing
│   └── content/                 # CMS pages, blog, resources
├── core/                        # Shared utilities
├── media/                       # User uploads
├── static/                      # Static files
├── requirements/
│   ├── base.txt
│   ├── development.txt
│   └── production.txt
├── Dockerfile
├── docker-compose.yml
└── manage.py
```

### **5.2 Core Models**

```python
# apps/courses/models.py
from django.db import models
from django.utils.text import slugify
from django.core.validators import MinValueValidator, MaxValueValidator
import uuid

class Course(models.Model):
    id = models.UUIDField(primary_key=True, default=uuid.uuid4, editable=False)
    title = models.CharField(max_length=200)
    slug = models.SlugField(unique=True, max_length=200)
    subtitle = models.CharField(max_length=300)
    description = models.TextField()
    short_description = models.CharField(max_length=500, blank=True)
    
    # Media
    thumbnail = models.ImageField(upload_to='courses/thumbnails/%Y/%m/')
    cover_image = models.ImageField(upload_to='courses/covers/%Y/%m/', blank=True)
    promo_video = models.URLField(blank=True)
    
    # Metadata
    duration = models.CharField(max_length=50, help_text="e.g., '12 weeks'")
    total_hours = models.PositiveIntegerField(help_text="Total instruction hours")
    level = models.CharField(
        max_length=20,
        choices=[
            ('beginner', 'Beginner'),
            ('intermediate', 'Intermediate'),
            ('advanced', 'Advanced'),
        ]
    )
    language = models.CharField(max_length=50, default='English')
    
    # Pricing
    price = models.DecimalField(max_digits=10, decimal_places=2)
    original_price = models.DecimalField(max_digits=10, decimal_places=2, null=True, blank=True)
    currency = models.CharField(max_length=3, default='USD')
    
    # Stats
    rating = models.DecimalField(
        max_digits=3, 
        decimal_places=2, 
        default=0,
        validators=[MinValueValidator(0), MaxValueValidator(5)]
    )
    review_count = models.PositiveIntegerField(default=0)
    enrolled_count = models.PositiveIntegerField(default=0)
    
    # Status
    is_featured = models.BooleanField(default=False)
    is_active = models.BooleanField(default=True)
    is_certification = models.BooleanField(default=True)
    certification_name = models.CharField(max_length=200, blank=True)
    
    # SEO
    meta_title = models.CharField(max_length=200, blank=True)
    meta_description = models.TextField(blank=True)
    
    # Timestamps
    created_at = models.DateTimeField(auto_now_add=True)
    updated_at = models.DateTimeField(auto_now=True)
    
    class Meta:
        ordering = ['-created_at']
        indexes = [
            models.Index(fields=['slug']),
            models.Index(fields=['is_featured', 'is_active']),
            models.Index(fields=['level']),
        ]
    
    def save(self, *args, **kwargs):
        if not self.slug:
            self.slug = slugify(self.title)
        super().save(*args, **kwargs)
    
    def __str__(self):
        return self.title
    
    @property
    def discount_percentage(self):
        if self.original_price and self.original_price > self.price:
            return int((self.original_price - self.price) / self.original_price * 100)
        return 0


class Module(models.Model):
    id = models.UUIDField(primary_key=True, default=uuid.uuid4, editable=False)
    course = models.ForeignKey(Course, related_name='modules', on_delete=models.CASCADE)
    title = models.CharField(max_length=200)
    description = models.TextField()
    order = models.PositiveIntegerField(default=0)
    duration = models.CharField(max_length=50, help_text="e.g., '3 hours'")
    
    # Content
    learning_objectives = models.JSONField(default=list, help_text="List of learning objectives")
    topics = models.JSONField(default=list, help_text="List of topics covered")
    
    # Media
    video_url = models.URLField(blank=True)
    resources = models.JSONField(default=list, help_text="List of resource URLs")
    
    # Status
    is_preview = models.BooleanField(default=False, help_text="Available for preview")
    
    class Meta:
        ordering = ['order']
        unique_together = ['course', 'order']
    
    def __str__(self):
        return f"{self.course.title} - {self.title}"


class Category(models.Model):
    id = models.UUIDField(primary_key=True, default=uuid.uuid4, editable=False)
    name = models.CharField(max_length=100, unique=True)
    slug = models.SlugField(unique=True)
    description = models.TextField(blank=True)
    icon = models.CharField(max_length=50, blank=True, help_text="Lucide icon name")
    color = models.CharField(max_length=7, default="#6366f1", help_text="Hex color code")
    order = models.PositiveIntegerField(default=0)
    is_active = models.BooleanField(default=True)
    
    class Meta:
        verbose_name_plural = 'Categories'
        ordering = ['order']
    
    def save(self, *args, **kwargs):
        if not self.slug:
            self.slug = slugify(self.name)
        super().save(*args, **kwargs)
    
    def __str__(self):
        return self.name


class CourseCategory(models.Model):
    course = models.ForeignKey(Course, on_delete=models.CASCADE)
    category = models.ForeignKey(Category, on_delete=models.CASCADE)
    
    class Meta:
        unique_together = ['course', 'category']
```

```python
# apps/cohorts/models.py
from django.db import models
from django.utils import timezone
from apps.courses.models import Course
from apps.accounts.models import User
import uuid

class Cohort(models.Model):
    id = models.UUIDField(primary_key=True, default=uuid.uuid4, editable=False)
    course = models.ForeignKey(Course, related_name='cohorts', on_delete=models.CASCADE)
    
    # Scheduling
    start_date = models.DateField()
    end_date = models.DateField()
    timezone = models.CharField(max_length=50, default='America/New_York')
    
    # Format
    FORMAT_CHOICES = [
        ('online', 'Live Online'),
        ('in-person', 'In-Person'),
        ('hybrid', 'Hybrid'),
    ]
    format = models.CharField(max_length=20, choices=FORMAT_CHOICES)
    location = models.CharField(max_length=200, blank=True, help_text="City, Country for in-person")
    
    # Schedule details
    schedule_days = models.JSONField(default=list, help_text="['Monday', 'Wednesday']")
    schedule_time = models.CharField(max_length=50, help_text="e.g., '7:00 PM - 9:00 PM'")
    
    # Capacity
    max_students = models.PositiveIntegerField(default=30)
    spots_remaining = models.PositiveIntegerField(default=30)
    
    # Pricing
    price = models.DecimalField(max_digits=10, decimal_places=2)
    early_bird_price = models.DecimalField(max_digits=10, decimal_places=2, null=True, blank=True)
    early_bird_deadline = models.DateField(null=True, blank=True)
    
    # Instructor
    instructor = models.ForeignKey(
        User, 
        on_delete=models.SET_NULL, 
        null=True, 
        related_name='teaching_cohorts'
    )
    teaching_assistants = models.ManyToManyField(
        User, 
        blank=True, 
        related_name='assistant_cohorts'
    )
    
    # Status
    STATUS_CHOICES = [
        ('draft', 'Draft'),
        ('open', 'Open for Enrollment'),
        ('filling', 'Filling Fast'),
        ('waitlist', 'Waitlist Only'),
        ('closed', 'Closed'),
        ('in-progress', 'In Progress'),
        ('completed', 'Completed'),
    ]
    status = models.CharField(max_length=20, choices=STATUS_CHOICES, default='draft')
    
    # Timestamps
    created_at = models.DateTimeField(auto_now_add=True)
    updated_at = models.DateTimeField(auto_now=True)
    
    class Meta:
        ordering = ['start_date']
        indexes = [
            models.Index(fields=['course', 'status']),
            models.Index(fields=['start_date']),
        ]
    
    def __str__(self):
        return f"{self.course.title} - {self.start_date}"
    
    def save(self, *args, **kwargs):
        # Auto-update status based on spots and dates
        if self.spots_remaining <= 0:
            self.status = 'waitlist'
        elif self.spots_remaining <= 5:
            self.status = 'filling'
        
        # Check early bird deadline
        if self.early_bird_deadline and timezone.now().date() > self.early_bird_deadline:
            self.early_bird_price = None
            
        super().save(*args, **kwargs)
    
    @property
    def is_early_bird_active(self):
        if not self.early_bird_deadline:
            return False
        return timezone.now().date() <= self.early_bird_deadline
    
    @property
    def current_price(self):
        if self.is_early_bird_active and self.early_bird_price:
            return self.early_bird_price
        return self.price
```

### **5.3 API Serializers**

```python
# apps/courses/serializers.py
from rest_framework import serializers
from .models import Course, Module, Category

class ModuleSerializer(serializers.ModelSerializer):
    class Meta:
        model = Module
        fields = [
            'id', 'title', 'description', 'order', 'duration',
            'learning_objectives', 'topics', 'is_preview'
        ]

class CategorySerializer(serializers.ModelSerializer):
    class Meta:
        model = Category
        fields = ['id', 'name', 'slug', 'description', 'icon', 'color']

class CourseListSerializer(serializers.ModelSerializer):
    categories = CategorySerializer(many=True, read_only=True)
    discount_percentage = serializers.ReadOnlyField()
    
    class Meta:
        model = Course
        fields = [
            'id', 'slug', 'title', 'subtitle', 'thumbnail',
            'duration', 'level', 'price', 'original_price',
            'discount_percentage', 'rating', 'review_count',
            'enrolled_count', 'is_featured', 'categories'
        ]

class CourseDetailSerializer(serializers.ModelSerializer):
    modules = ModuleSerializer(many=True, read_only=True)
    categories = CategorySerializer(many=True, read_only=True)
    discount_percentage = serializers.ReadOnlyField()
    next_cohort = serializers.SerializerMethodField()
    
    class Meta:
        model = Course
        fields = [
            'id', 'slug', 'title', 'subtitle', 'description',
            'short_description', 'thumbnail', 'cover_image', 'promo_video',
            'duration', 'total_hours', 'level', 'language',
            'price', 'original_price', 'discount_percentage', 'currency',
            'rating', 'review_count', 'enrolled_count',
            'is_certification', 'certification_name',
            'modules', 'categories', 'next_cohort',
            'meta_title', 'meta_description',
            'created_at', 'updated_at'
        ]
    
    def get_next_cohort(self, obj):
        from apps.cohorts.models import Cohort
        from django.utils import timezone
        
        next_cohort = Cohort.objects.filter(
            course=obj,
            start_date__gte=timezone.now().date(),
            status__in=['open', 'filling']
        ).order_by('start_date').first()
        
        if next_cohort:
            return {
                'id': str(next_cohort.id),
                'start_date': next_cohort.start_date,
                'price': next_cohort.current_price,
                'spots_remaining': next_cohort.spots_remaining,
                'format': next_cohort.get_format_display(),
            }
        return None
```

### **5.4 API Views**

```python
# apps/courses/views.py
from rest_framework import viewsets, filters, status
from rest_framework.decorators import action
from rest_framework.response import Response
from django_filters.rest_framework import DjangoFilterBackend
from django.db.models import Avg, Count, Q
from .models import Course, Category
from .serializers import CourseListSerializer, CourseDetailSerializer, CategorySerializer

class CourseViewSet(viewsets.ReadOnlyModelViewSet):
    queryset = Course.objects.filter(is_active=True)
    lookup_field = 'slug'
    filter_backends = [DjangoFilterBackend, filters.SearchFilter, filters.OrderingFilter]
    filterset_fields = ['level', 'categories', 'is_featured']
    search_fields = ['title', 'subtitle', 'description']
    ordering_fields = ['price', 'rating', 'created_at', 'enrolled_count']
    ordering = ['-created_at']
    
    def get_serializer_class(self):
        if self.action == 'retrieve':
            return CourseDetailSerializer
        return CourseListSerializer
    
    def get_queryset(self):
        queryset = super().get_queryset()
        
        # Annotate with category names for filtering
        queryset = queryset.prefetch_related('categories')
        
        # Filter by price range
        min_price = self.request.query_params.get('min_price')
        max_price = self.request.query_params.get('max_price')
        if min_price:
            queryset = queryset.filter(price__gte=min_price)
        if max_price:
            queryset = queryset.filter(price__lte=max_price)
        
        return queryset
    
    @action(detail=False, methods=['get'])
    def featured(self, request):
        """Get featured courses"""
        courses = self.get_queryset().filter(is_featured=True)[:6]
        serializer = CourseListSerializer(courses, many=True)
        return Response(serializer.data)
    
    @action(detail=False, methods=['get'])
    def categories(self, request):
        """Get all course categories"""
        categories = Category.objects.filter(is_active=True)
        serializer = CategorySerializer(categories, many=True)
        return Response(serializer.data)
    
    @action(detail=True, methods=['get'])
    def related(self, request, slug=None):
        """Get related courses based on categories"""
        course = self.get_object()
        category_ids = course.categories.values_list('id', flat=True)
        
        related = Course.objects.filter(
            categories__in=category_ids,
            is_active=True
        ).exclude(id=course.id).distinct()[:4]
        
        serializer = CourseListSerializer(related, many=True)
        return Response(serializer.data)
```

---

## **PHASE 6: IMPLEMENTATION ROADMAP**

### **6.1 8-Week Development Timeline**

```
WEEK 1: FOUNDATION & DESIGN SYSTEM
├── Day 1-2: Project setup (Next.js 16.1.4 + Django 6.0.2)
├── Day 3-4: Design tokens (colors, typography, spacing)
├── Day 5-7: Component library (Button, Card, Badge, Input)
└── Deliverable: Storybook with base components

WEEK 2: BACKEND CORE & AUTH
├── Day 1-2: Django models (Course, Module, Cohort)
├── Day 3-4: Django REST API + serializers
├── Day 5-6: JWT authentication (djangorestframework-simplejwt)
└── Day 7: API documentation (Swagger/Redoc)
└── Deliverable: Working API with auth

WEEK 3: HOMEPAGE & NAVIGATION
├── Day 1-2: Navigation component (sticky, glassmorphism)
├── Day 3-4: Hero section (animations, CTA)
├── Day 5-6: Course categories (bento grid)
└── Day 7: Trust signals + social proof
└── Deliverable: Complete homepage

WEEK 4: COURSE DISCOVERY
├── Day 1-2: Course listing page (filtering, search)
├── Day 3-4: Course card components + grid
├── Day 5-6: Search integration (Algolia setup)
└── Day 7: Responsive optimization
└── Deliverable: Course catalog functionality

WEEK 5: COURSE DETAIL & ENROLLMENT
├── Day 1-2: Course detail page layout
├── Day 3-4: Curriculum accordion + instructor section
├── Day 5-6: Cohort schedule component
└── Day 7: Sticky enrollment card
└── Deliverable: Complete course pages

WEEK 6: USER FEATURES & PAYMENTS
├── Day 1-2: User authentication flow (login/register)
├── Day 3-4: Student dashboard (enrollments, progress)
├── Day 5-6: Stripe payment integration
└── Day 7: Enrollment confirmation + emails
└── Deliverable: Full enrollment flow

WEEK 7: POLISH & OPTIMIZATION
├── Day 1-2: Animation refinement (Framer Motion)
├── Day 3-4: Performance optimization (images, lazy loading)
├── Day 5-6: Accessibility audit (WCAG 2.1 AA)
└── Day 7: Cross-browser testing
└── Deliverable: Production-ready frontend

WEEK 8: QA & LAUNCH
├── Day 1-2: E2E testing (Playwright)
├── Day 3-4: Security audit + penetration testing
├── Day 5-6: Content population + SEO
└── Day 7: Deployment + monitoring setup
└── Deliverable: Live production site
```

### **6.2 Phase Checklists**

#### **Week 1: Foundation Checklist**

```markdown
Frontend Setup
[ ] Initialize Next.js 16.1.4 with Turbopack
[ ] Configure Tailwind CSS 4.1.18 with PostCSS
[ ] Install and configure Shadcn/ui
[ ] Set up Framer Motion 12.29.0
[ ] Configure Zustand 5.0.3
[ ] Set up absolute imports (@/components)
[ ] Configure ESLint + Prettier
[ ] Set up Storybook

Design System
[ ] Create CSS variables (colors, spacing, typography)
[ ] Define Tailwind config extensions
[ ] Create animation utilities (lib/animations.ts)
[ ] Set up dark mode support
[ ] Create cn() utility for class merging

Component Library
[ ] Button component (all variants + states)
[ ] Card component (with hover effects)
[ ] Badge component (all variants)
[ ] Input component (with validation states)
[ ] Accordion component (curriculum)
[ ] Dialog/Modal component
[ ] Skeleton loading states

Backend Setup
[ ] Initialize Django 6.0.2 project
[ ] Configure PostgreSQL 16 connection
[ ] Set up Django REST Framework
[ ] Configure CORS headers
[ ] Set up Redis for caching
[ ] Create Docker Compose setup
[ ] Configure environment variables
```

#### **Week 8: Launch Checklist**

```markdown
Quality Assurance
[ ] Lighthouse Performance: 90+
[ ] Lighthouse Accessibility: 100
[ ] Lighthouse SEO: 95+
[ ] Lighthouse Best Practices: 100
[ ] WCAG 2.1 AA compliance verified
[ ] Cross-browser testing (Chrome, Safari, Firefox, Edge)
[ ] Mobile responsiveness (iOS Safari, Android Chrome)
[ ] E2E tests passing (Playwright)

Security
[ ] Security headers configured (CSP, HSTS, X-Frame-Options)
[ ] JWT token rotation implemented
[ ] SQL injection protection verified
[ ] XSS protection enabled
[ ] Rate limiting configured
[ ] Input validation on all forms

Performance
[ ] Images optimized (WebP/AVIF)
[ ] Fonts preloaded with font-display: swap
[ ] Code splitting implemented
[ ] API response times < 200ms (p95)
[ ] CDN configured for static assets
[ ] Database queries optimized (N+1 eliminated)

Deployment
[ ] Production environment variables set
[ ] SSL certificates configured
[ ] Database migrations applied
[ ] Static files collected
[ ] Docker images built and tested
[ ] Monitoring configured (Sentry, PostHog)
[ ] Backup strategy implemented
[ ] Rollback plan documented

Content
[ ] SEO meta tags on all pages
[ ] Open Graph images configured
[ ] Sitemap generated
[ ] Robots.txt configured
[ ] Structured data (JSON-LD) implemented
[ ] Analytics instrumentation verified
```

---

## **PHASE 7: SUCCESS METRICS & VALIDATION**

### **7.1 Quantitative KPIs**

| Metric | Target | Measurement | Tool |
|--------|--------|-------------|------|
| Homepage Conversion Rate | > 3% | (Enrollments / Visitors) × 100 | PostHog |
| Course Page Enrollment Rate | > 8% | (Enrollments / Course Views) × 100 | PostHog |
| Time to Enroll | < 5 min | Average time from landing to enrollment | PostHog |
| Bounce Rate | < 40% | Single-page sessions / Total sessions | GA4 |
| Lighthouse Performance | 90+ | Performance score | Lighthouse CI |
| Lighthouse Accessibility | 100 | Accessibility score | Lighthouse CI |
| API Response Time (p95) | < 200ms | 95th percentile response time | Django Silk |
| Error Rate | < 0.1% | Errors / Total requests | Sentry |
| NPS Score | > 50 | Net Promoter Score | Post-enrollment survey |

### **7.2 Qualitative Success Criteria**

- [ ] **Distinctive Visual Identity:** Zero "AI slop" aesthetics, memorable "Precision Futurism" design
- [ ] **Professional Credibility:** Enterprise buyers feel confident in platform quality within 5 seconds
- [ ] **User Clarity:** Visitors understand offerings and differentiation immediately
- [ ] **Emotional Resonance:** Design inspires action (enrollment), not just informs
- [ ] **Accessibility Excellence:** Screen reader users have equivalent experience
- [ ] **Performance Perception:** Feels instant, even on slower connections
- [ ] **Scalability:** System supports 10x content growth without redesign
- [ ] **Maintainability:** New developers contribute within 1 week

---

## **PHASE 8: ANTI-GENERIC ENFORCEMENT PLEDGE**

### **8.1 Prohibited Patterns (ZERO TOLERANCE)**

| Pattern | Why Banned | Alternative |
|---------|-----------|-------------|
| **Inter/Roboto default** | Generic, overused | Space Grotesk + Inter combination |
| **Purple-to-pink gradients** | AI cliché | Solid indigo with cyan accents |
| **Generic card grids** | Template aesthetic | Bento box asymmetry, masonry layouts |
| **Stock photos of people smiling at laptops** | Inauthentic | Abstract code visualizations, neural network art |
| **Bootstrap-style components** | Dated, unoriginal | Custom components with micro-interactions |
| **Hero section + 3 features + testimonials** | Predictable pattern | Asymmetric editorial layouts |
| **Hamburger menu on desktop** | Lazy navigation | Persistent nav with command palette |
| **Loading spinners only** | Poor perceived performance | Skeleton screens + progressive loading |
| **Generic error pages** | Missed brand opportunity | Illustrated, helpful error states |
| **Cookie-cutter dashboards** | Unmemorable | Custom data visualizations, skill trees |

### **8.2 Mandatory Distinctive Elements**

- [ ] **Custom Typography Pairing:** Space Grotesk (display) + Inter (body) + JetBrains Mono (code)
- [ ] **Asymmetric Layouts:** 60/40 splits, broken grids, intentional whitespace
- [ ] **Motion Design:** Purposeful animations that suggest intelligence/precision
- [ ] **Custom Iconography:** Lucide icons with custom styling, not generic sets
- [ ] **Skill Tree Visualization:** Unique learning path representation
- [ ] **Live Data Indicators:** Real-time cohort capacity, enrollment activity
- [ ] **Code-First Aesthetic:** Monospace elements, terminal-style accents
- [ ] **Dark Mode Excellence:** Not just inversion, but intentional dark palette

---

## **PHASE 9: RISK ASSESSMENT & MITIGATION**

| Risk | Probability | Impact | Mitigation Strategy |
|------|------------|--------|---------------------|
| **Performance degradation with rich media** | Medium | High | Lazy loading, CDN optimization, video compression, adaptive bitrate streaming |
| **Accessibility gaps in custom components** | Medium | High | Radix UI primitives, automated a11y testing (axe-core), manual audit |
| **Generic aesthetic creep** | High | Critical | Design review checkpoints, anti-generic checklist enforcement |
| **CORS/auth complexity (Next.js + Django)** | Medium | High | Django CORS headers, JWT with refresh tokens, thorough testing |
| **Database scaling with growth** | Low | High | PostgreSQL read replicas, connection pooling, query optimization |
| **Payment flow failures** | Low | Critical | Stripe webhook retries, idempotency keys, manual reconciliation process |
| **Video bandwidth costs** | Medium | Medium | Mux/Cloudflare Stream adaptive bitrate, usage monitoring, caching |
| **Search relevance issues** | Medium | Medium | Algolia tuning, synonym dictionaries, analytics feedback loop |
| **Cross-browser animation bugs** | Low | Medium | CSS-first animations, feature detection, graceful degradation |
| **Content management complexity** | Medium | Medium | Structured CMS schema, validation, content team training |

---

## **PHASE 10: VALIDATION CHECKPOINT**

### **10.1 PRD Completeness Verification**

| Criterion | Status | Evidence |
|-----------|--------|----------|
| **Exact tech stack versions** | ✅ Complete | Next.js 16.1.4, Django 6.0.2, React 19.2.3 specified |
| **Full-stack architecture** | ✅ Complete | Frontend + Backend + DevOps + QA |
| **Design system specificity** | ✅ Complete | CSS variables, exact values, component code |
| **Production-ready code** | ✅ Complete | TypeScript components, Django models, API contracts |
| **Accessibility standards** | ✅ Complete | WCAG 2.1 AA with implementation details |
| **Performance budget** | ✅ Complete | Core Web Vitals with targets |
| **Security considerations** | ✅ Complete | JWT, CORS, headers, penetration testing |
| **Timeline realism** | ✅ Complete | 8-week phased approach with daily breakdown |
| **Risk assessment** | ✅ Complete | 10 risks with probability/impact/mitigation |
| **Anti-generic enforcement** | ✅ Complete | Prohibited patterns + mandatory distinctive elements |
| **Competitive differentiation** | ✅ Complete | iTrust Academy analysis + differentiation strategy |
| **Psychological optimization** | ✅ Complete | User sentiment mapping + cognitive load optimization |

### **10.2 Approval to Proceed**

**This PRD is ready for implementation upon confirmation of:**

- [ ] **Tech Stack Frozen:** Next.js 16.1.4 + Django 6.0.2 + PostgreSQL 16 (no changes)
- [ ] **Design Direction Approved:** "Precision Futurism" aesthetic accepted
- [ ] **Anti-Generic Commitment:** Zero tolerance for template aesthetics agreed
- [ ] **Accessibility Non-Negotiable:** WCAG 2.1 AA mandatory, not aspirational
- [ ] **Timeline Realistic:** 8 weeks with available resources confirmed
- [ ] **Success Metrics Aligned:** Quantitative KPIs + qualitative criteria agreed

**Your approval triggers Week 1: Foundation (Day 1)**

---

## **APPENDICES**

### **Appendix A: Package.json (Frontend)**

```json
{
  "name": "ai-academy-frontend",
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
    "@radix-ui/react-accordion": "^1.2.2",
    "@radix-ui/react-navigation-menu": "^1.2.3",
    "class-variance-authority": "^0.7.1",
    "clsx": "^2.1.1",
    "tailwind-merge": "^2.6.0",
    "date-fns": "^4.1.0",
    "@tanstack/react-query": "^5.64.0",
    "axios": "^1.7.9"
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
    "prettier": "^3.4.2",
    "prettier-plugin-tailwindcss": "^0.6.9"
  }
}
```

### **Appendix B: Django Requirements**

```txt
# requirements/base.txt
Django==6.0.2
djangorestframework==3.15.2
djangorestframework-simplejwt==5.4.0
django-cors-headers==4.6.0
django-filter==24.3
django-storages==1.14.4
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
django-silk==5.3.0

# requirements/production.txt
-r base.txt
```

### **Appendix C: Environment Variables**

```bash
# Frontend (.env.local)
NEXT_PUBLIC_API_URL=http://localhost:8000/api/v1
NEXT_PUBLIC_SITE_URL=http://localhost:3000
NEXT_PUBLIC_ALGOLIA_APP_ID=XXX
NEXT_PUBLIC_ALGOLIA_SEARCH_KEY=XXX
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=pk_test_XXX
NEXT_PUBLIC_SENTRY_DSN=XXX
NEXT_PUBLIC_POSTHOG_KEY=XXX

# Backend (.env)
DEBUG=True
SECRET_KEY=your-secret-key-here
ALLOWED_HOSTS=localhost,127.0.0.1
CORS_ALLOWED_ORIGINS=http://localhost:3000,http://127.0.0.1:3000

# Database
DATABASE_URL=postgresql://user:password@localhost:5432/academy_db

# Redis
REDIS_URL=redis://localhost:6379/0

# JWT
JWT_ACCESS_TOKEN_LIFETIME=60
JWT_REFRESH_TOKEN_LIFETIME=1440

# Email
EMAIL_BACKEND=django.core.mail.backends.smtp.EmailBackend
EMAIL_HOST=smtp.sendgrid.net
EMAIL_PORT=587
EMAIL_HOST_USER=apikey
EMAIL_HOST_PASSWORD=XXX
DEFAULT_FROM_EMAIL=noreply@academy.com

# Stripe
STRIPE_SECRET_KEY=sk_test_XXX
STRIPE_WEBHOOK_SECRET=whsec_XXX

# AWS S3 (Media storage)
AWS_ACCESS_KEY_ID=XXX
AWS_SECRET_ACCESS_KEY=XXX
AWS_STORAGE_BUCKET_NAME=academy-media
AWS_S3_REGION_NAME=us-east-1

# Sentry
SENTRY_DSN=XXX
```

---

*Document Version: 3.0 FINAL*  
*Status: Ready for Implementation*  
*Design Philosophy: Precision Futurism*  
*Tech Stack: Next.js 16.1.4 + Django 6.0.2 + PostgreSQL 16*  
*Classification: Production-Ready Specification*

**This PRD represents the definitive synthesis of strategic design analysis and technical implementation depth. Every specification is backed by competitive analysis, psychological optimization, and exact version alignment with your preferred stack.**
