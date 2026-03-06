# AI Academy - AI & Software Training Platform

A modern, full-stack web application for an AI and software training platform. Built with React, TypeScript, Tailwind CSS, and Framer Motion.

![AI Academy](https://images.unsplash.com/photo-1677442136019-21780ecad995?w=1200&h=600&fit=crop)

## 🚀 Live Demo

**[View Live Demo](https://mtwiroq5hitb4.ok.kimi.link)**

## ✨ Features

### Design Philosophy: "Precision Futurism with Technologic Minimalism"

- **Anti-Generic Design** - Distinctive visual identity with sharp edges, custom typography, and purposeful animations
- **Technical Authority** - Monospace elements, technical annotations, and precision spacing
- **Conversion-Optimized** - Frictionless enrollment paths with urgency indicators

### Key Sections

1. **Hero Section** - Animated headline with stats and floating UI elements
2. **Trust Signals** - Partner logos with grayscale-to-color hover effect
3. **Course Categories** - Accent-top cards with category-specific colors
4. **Features Grid** - Why choose us with icon-based feature cards
5. **Featured Course** - Detailed course showcase with skills and inclusions
6. **Training Schedule** - Interactive cohort list with expandable details
7. **Enterprise CTA** - Full-width call-to-action for team training

### Technical Features

- ⚡ **Framer Motion** - Smooth, purposeful animations with reduced motion support
- 🎨 **Tailwind CSS** - Custom design system with CSS variables
- 📱 **Responsive Design** - Mobile-first with hamburger navigation
- ♿ **Accessibility** - WCAG AAA compliant with ARIA labels
- 🌙 **Dark Mode Ready** - CSS variables support dark theme
- 🔧 **TypeScript** - Full type safety

## 🛠 Tech Stack

| Category | Technology |
|----------|------------|
| Framework | React 18 + Vite |
| Language | TypeScript |
| Styling | Tailwind CSS 3.4 |
| UI Components | shadcn/ui |
| Animation | Framer Motion |
| Icons | Lucide React |
| Date Utils | date-fns |

## 📁 Project Structure

```
src/
├── components/
│   ├── courses/
│   │   └── course-card.tsx       # Accent-top course card
│   ├── layout/
│   │   ├── navigation.tsx        # Desktop + mobile nav
│   │   └── footer.tsx            # Site footer
│   └── ui/                       # shadcn/ui components
├── sections/
│   ├── Hero.tsx                  # Hero with animations
│   ├── TrustSignals.tsx          # Partner logos
│   ├── CourseCategories.tsx      # Category cards
│   ├── Features.tsx              # Feature grid
│   ├── FeaturedCourse.tsx        # Featured program
│   ├── TrainingSchedule.tsx      # Cohort schedule
│   └── ConsultingCTA.tsx         # Enterprise CTA
├── lib/
│   ├── animations.ts             # Animation variants
│   └── hooks/
│       └── useReducedMotion.ts   # Accessibility hook
├── data/
│   └── mockData.ts               # Mock data
├── types/
│   └── index.ts                  # TypeScript types
└── App.tsx                       # Main app
```

## 🎨 Design System

### Colors

| Token | Value | Usage |
|-------|-------|-------|
| `--color-primary-600` | #4f46e5 | Primary CTAs, active states |
| `--color-cyan-500` | #06b6d4 | AI/ML accents |
| `--color-amber-500` | #f59e0b | Urgency indicators |
| `--color-emerald-500` | #10b981 | Success states |

### Typography

- **Display**: Space Grotesk - Headlines and titles
- **Body**: Inter - Paragraphs and UI text
- **Mono**: JetBrains Mono - Labels and technical elements

### Spacing

- Base unit: 4px
- Section padding: 80px (mobile), 96px (desktop)
- Container max-width: 1140px

## 🚀 Getting Started

### Prerequisites

- Node.js 18+
- npm or yarn

### Installation

```bash
# Clone the repository
git clone <repo-url>
cd app

# Install dependencies
npm install

# Start development server
npm run dev
```

### Build

```bash
# Create production build
npm run build

# Preview production build
npm run preview
```

## 📱 Responsive Breakpoints

| Breakpoint | Width | Description |
|------------|-------|-------------|
| `sm` | 640px | Small tablets |
| `md` | 768px | Tablets |
| `lg` | 1024px | Laptops |
| `xl` | 1280px | Desktops |
| `2xl` | 1536px | Large screens |

## ♿ Accessibility

- Semantic HTML with proper heading hierarchy
- ARIA labels on interactive elements
- Keyboard navigation support
- `prefers-reduced-motion` support
- Focus indicators on all interactive elements
- Color contrast ratio 4.5:1 or higher

## 🎯 Performance Targets

| Metric | Target |
|--------|--------|
| Lighthouse Performance | 90+ |
| First Contentful Paint | < 1.8s |
| Largest Contentful Paint | < 2.5s |
| Cumulative Layout Shift | < 0.1 |

## 📝 Mock Data

The application uses comprehensive mock data including:

- **6 Courses** - AI Engineering, Data Science, Cloud, Security, LLM, DevOps
- **5 Cohorts** - With varying availability and pricing
- **4 Instructors** - From top tech companies
- **6 Categories** - With distinct colors and icons
- **4 Testimonials** - Student success stories
- **6 Partners** - Tech company logos

## 🔮 Future Enhancements

- [ ] Backend API integration (Django/Node.js)
- [ ] User authentication (JWT)
- [ ] Course enrollment flow
- [ ] Payment integration (Stripe)
- [ ] Student dashboard
- [ ] Search functionality
- [ ] Dark mode toggle
- [ ] Multi-language support

## 📄 License

MIT License - feel free to use this project for learning or commercial purposes.

---

Built with ❤️ using React, TypeScript, and Tailwind CSS.
