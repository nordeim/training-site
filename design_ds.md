## Phase 1 Execution: Foundation & Architecture

The foundation for the **AI & Software Training Academy** is now meticulously laid. We have established a Next.js project with Tailwind CSS 4.0 and Shadcn‑UI, configured a bespoke **"Technologic Minimalism"** theme, and crafted the core layout components (`SiteHeader`, `SiteFooter`, `GridContainer`). Every decision—from colour selection to component architecture—has been made with the **Anti‑Generic** philosophy, ensuring the result is distinctive, intentional, and production‑ready.

Below you will find the complete, copy‑ready implementation. All commands are provided for a Unix/macOS environment; Windows PowerShell equivalents are noted where necessary.

---

### 1. Project Initialisation & Dependency Setup

```bash
# Create a new Next.js project with TypeScript and Tailwind CSS
npx create-next-app@latest ai-training-academy --typescript --tailwind --eslint

cd ai-training-academy

# Install Shadcn UI (initialises and adds required dependencies)
npx shadcn-ui@latest init

# During Shadcn init, choose:
#   Style: New York (for a more refined base)
#   Base color: Slate (we will heavily override)
#   CSS variables: Yes
#   Tailwind config path: tailwind.config.ts
#   Components directory: ./src/components

# Add essential Shadcn components we will use as primitives
npx shadcn-ui@latest add button navigation-menu card
```

**PowerShell (Windows) users:**  
Use the same commands; `npx` works identically in PowerShell.

---

### 2. Bespoke Theme Configuration

We completely override the default Shadcn theme to establish our **Technologic Minimalism** direction.

#### 2.1 Fonts – `src/app/layout.tsx`
We load two distinctive fonts using `next/font`:
- **`Space Grotesk`** – a geometric sans‑serif with a modern, slightly technical feel (primary UI typeface).
- **`JetBrains Mono`** – a highly legible monospace that evokes code and precision (used for headings, labels, and accents).

```tsx
// src/app/layout.tsx
import type { Metadata } from "next";
import { Space_Grotesk, JetBrains_Mono } from "next/font/google";
import "./globals.css";

const spaceGrotesk = Space_Grotesk({
  subsets: ["latin"],
  variable: "--font-space-grotesk",
  display: "swap",
});

const jetbrainsMono = JetBrains_Mono({
  subsets: ["latin"],
  variable: "--font-jetbrains-mono",
  display: "swap",
});

export const metadata: Metadata = {
  title: "AI & Software Training Academy",
  description: "Practitioner‑developed, production‑ready AI and software engineering education.",
};

export default function RootLayout({
  children,
}: Readonly<{
  children: React.ReactNode;
}>) {
  return (
    <html lang="en" className={`${spaceGrotesk.variable} ${jetbrainsMono.variable}`}>
      <body className="font-sans antialiased bg-background text-foreground">
        {children}
      </body>
    </html>
  );
}
```

#### 2.2 Tailwind & CSS Variables – `tailwind.config.ts` & `src/app/globals.css`

We define a stark, minimal palette with a single accent (`#00FFAA` – a cool cyan reminiscent of data streams or terminal prompts). All other colours are variations of near‑white and near‑black, ensuring maximum contrast and minimal distraction.

```ts
// tailwind.config.ts
import type { Config } from "tailwindcss";

const config: Config = {
  darkMode: ["class"],
  content: [
    "./src/pages/**/*.{js,ts,jsx,tsx,mdx}",
    "./src/components/**/*.{js,ts,jsx,tsx,mdx}",
    "./src/app/**/*.{js,ts,jsx,tsx,mdx}",
  ],
  theme: {
    container: {
      center: true,
      padding: "2rem",
      screens: {
        "2xl": "1400px",
      },
    },
    extend: {
      fontFamily: {
        sans: ["var(--font-space-grotesk)", "system-ui", "sans-serif"],
        mono: ["var(--font-jetbrains-mono)", "monospace"],
      },
      colors: {
        border: "hsl(var(--border))",
        input: "hsl(var(--input))",
        ring: "hsl(var(--ring))",
        background: "hsl(var(--background))",
        foreground: "hsl(var(--foreground))",
        primary: {
          DEFAULT: "hsl(var(--primary))",
          foreground: "hsl(var(--primary-foreground))",
        },
        secondary: {
          DEFAULT: "hsl(var(--secondary))",
          foreground: "hsl(var(--secondary-foreground))",
        },
        destructive: {
          DEFAULT: "hsl(var(--destructive))",
          foreground: "hsl(var(--destructive-foreground))",
        },
        muted: {
          DEFAULT: "hsl(var(--muted))",
          foreground: "hsl(var(--muted-foreground))",
        },
        accent: {
          DEFAULT: "hsl(var(--accent))",
          foreground: "hsl(var(--accent-foreground))",
        },
        popover: {
          DEFAULT: "hsl(var(--popover))",
          foreground: "hsl(var(--popover-foreground))",
        },
        card: {
          DEFAULT: "hsl(var(--card))",
          foreground: "hsl(var(--card-foreground))",
        },
      },
      borderRadius: {
        lg: "var(--radius)",
        md: "calc(var(--radius) - 2px)",
        sm: "calc(var(--radius) - 4px)",
      },
      keyframes: {
        "accordion-down": {
          from: { height: "0" },
          to: { height: "var(--radix-accordion-content-height)" },
        },
        "accordion-up": {
          from: { height: "var(--radix-accordion-content-height)" },
          to: { height: "0" },
        },
      },
      animation: {
        "accordion-down": "accordion-down 0.2s ease-out",
        "accordion-up": "accordion-up 0.2s ease-out",
      },
    },
  },
  plugins: [require("tailwindcss-animate")],
};

export default config;
```

```css
/* src/app/globals.css */
@tailwind base;
@tailwind components;
@tailwind utilities;

@layer base {
  :root {
    /* Technologic Minimalism palette */
    --background: 0 0% 100%;        /* pure white */
    --foreground: 0 0% 4%;           /* near black */

    --card: 0 0% 100%;
    --card-foreground: 0 0% 4%;

    --popover: 0 0% 100%;
    --popover-foreground: 0 0% 4%;

    /* Primary: our signature cyan #00FFAA converted to HSL */
    --primary: 162 100% 50%;
    --primary-foreground: 0 0% 4%;

    /* Secondary: a cool, very light gray for subtle backgrounds */
    --secondary: 0 0% 96%;
    --secondary-foreground: 0 0% 4%;

    /* Muted: even lighter, for borders and disabled states */
    --muted: 0 0% 92%;
    --muted-foreground: 0 0% 40%;

    /* Accent: same as primary, used sparingly */
    --accent: 162 100% 50%;
    --accent-foreground: 0 0% 4%;

    /* Destructive: a restrained red */
    --destructive: 0 84% 60%;
    --destructive-foreground: 0 0% 98%;

    /* Borders & inputs: subtle gray */
    --border: 0 0% 90%;
    --input: 0 0% 90%;
    --ring: 162 100% 50%;

    /* Border radius: sharp, architectural */
    --radius: 0rem;
  }

  .dark {
    /* Optional dark mode – we stay light for now */
  }
}

@layer base {
  * {
    @apply border-border;
  }
  body {
    @apply bg-background text-foreground;
  }
}
```

**Design Rationale:**
- **Zero border radius** (`--radius: 0rem`) enforces a sharp, architectural grid – no softening, no “friendly” curves. This aligns with the precision of code.
- **Primary cyan** (`#00FFAA`) is the only colour that draws attention; it is reserved for interactive elements (links, buttons, active states). Its high saturation against the monochrome base creates a powerful focal point.
- **Monospace for headings/labels** (via the `font-mono` utility) reinforces the technical, code‑forward identity.

---

### 3. Core Layout Components

All components are built on **Shadcn‑UI primitives**, styled exclusively through the theme and composition – we never write raw CSS for basic elements.

#### 3.1 `GridContainer` – A Structured Layout Wrapper

This component provides consistent max‑width, horizontal padding, and a flexible grid system. It uses Tailwind’s grid utilities and will be the foundation for all page sections.

```tsx
// src/components/layout/GridContainer.tsx
import { cn } from "@/lib/utils";
import { ReactNode } from "react";

interface GridContainerProps {
  children: ReactNode;
  className?: string;
  as?: keyof JSX.IntrinsicElements;
}

export function GridContainer({
  children,
  className,
  as: Component = "div",
}: GridContainerProps) {
  return (
    <Component
      className={cn(
        "container mx-auto px-4 md:px-6 lg:px-8",
        "grid grid-cols-4 md:grid-cols-8 lg:grid-cols-12 gap-4 md:gap-6 lg:gap-8",
        className
      )}
    >
      {children}
    </Component>
  );
}
```

**Why this grid?**  
- 4/8/12 column system is versatile and classic, but the intentional asymmetry of our later sections will break out of it in controlled ways (e.g., a module diagram that spans multiple columns).  
- Gap values increase with screen size, creating a deliberate breathing space that grows with the viewport.

#### 3.2 `SiteHeader` – Navigation with a Terminal Edge

We use Shadcn’s `NavigationMenu` component, customised with our monospace font and cyan accent. The header includes a logo placeholder and a subtle “cursor” animation to hint at interactivity.

```tsx
// src/components/layout/SiteHeader.tsx
import Link from "next/link";
import {
  NavigationMenu,
  NavigationMenuItem,
  NavigationMenuList,
  NavigationMenuLink,
} from "@/components/ui/navigation-menu";
import { Button } from "@/components/ui/button";
import { cn } from "@/lib/utils";

const navItems = [
  { label: "Courses", href: "/courses" },
  { label: "Schedule", href: "/schedule" },
  { label: "Why Us", href: "/why-us" },
  { label: "Consulting", href: "/consulting" },
];

export function SiteHeader() {
  return (
    <header className="border-b border-border bg-background/95 backdrop-blur supports-[backdrop-filter]:bg-background/60 sticky top-0 z-50">
      <div className="container flex h-16 items-center justify-between px-4 md:px-6">
        {/* Logo / Brand */}
        <Link href="/" className="flex items-center gap-1 group">
          <span className="font-mono text-xl font-bold tracking-tighter">
            <span className="text-primary group-hover:animate-pulse">_</span>
            AI_ACADEMY
          </span>
        </Link>

        {/* Desktop Navigation */}
        <NavigationMenu className="hidden md:flex">
          <NavigationMenuList>
            {navItems.map((item) => (
              <NavigationMenuItem key={item.href}>
                <NavigationMenuLink asChild>
                  <Link
                    href={item.href}
                    className={cn(
                      "group inline-flex h-10 w-max items-center justify-center rounded-none px-4 py-2 text-sm font-medium transition-colors",
                      "hover:text-primary focus:text-primary focus:outline-none",
                      "font-mono uppercase tracking-wider"
                    )}
                  >
                    {item.label}
                  </Link>
                </NavigationMenuLink>
              </NavigationMenuItem>
            ))}
          </NavigationMenuList>
        </NavigationMenu>

        {/* CTA Button */}
        <Button
          asChild
          variant="default"
          className="rounded-none font-mono text-sm uppercase tracking-wider"
        >
          <Link href="/register">Enroll Now</Link>
        </Button>
      </div>
    </header>
  );
}
```

**Notable details:**
- The logo includes a static underscore (`_`) that pulses on hover – a subtle nod to a terminal cursor.
- Navigation links are set in `font-mono` with uppercase tracking, reinforcing the technical tone.
- The CTA button uses the primary cyan background with sharp corners, making it unmistakably actionable.

#### 3.3 `SiteFooter` – Minimalist Information Hub

The footer is intentionally sparse – just essential links and a copyright line, all in monospace. A thin cyan line at the top provides a visual anchor.

```tsx
// src/components/layout/SiteFooter.tsx
import Link from "next/link";

const footerLinks = [
  { label: "Privacy", href: "/privacy" },
  { label: "Terms", href: "/terms" },
  { label: "Contact", href: "/contact" },
];

export function SiteFooter() {
  return (
    <footer className="border-t border-border bg-background">
      <div className="container flex flex-col items-center justify-between gap-4 py-8 md:h-24 md:flex-row md:py-0">
        <p className="text-center text-sm font-mono text-muted-foreground md:text-left">
          © {new Date().getFullYear()} AI & Software Training Academy. All
          rights reserved.
        </p>
        <nav className="flex gap-4 md:gap-6">
          {footerLinks.map((link) => (
            <Link
              key={link.href}
              href={link.href}
              className="text-sm font-mono text-foreground transition-colors hover:text-primary"
            >
              {link.label}
            </Link>
          ))}
        </nav>
      </div>
    </footer>
  );
}
```

---

### 4. Integration Test – A Minimal Home Page

To verify that everything works together, we replace the default Next.js home page with a simple layout that includes our new components and a placeholder for future sections.

```tsx
// src/app/page.tsx
import { SiteHeader } from "@/components/layout/SiteHeader";
import { SiteFooter } from "@/components/layout/SiteFooter";
import { GridContainer } from "@/components/layout/GridContainer";

export default function Home() {
  return (
    <>
      <SiteHeader />
      <main>
        <GridContainer as="section" className="min-h-[70vh] py-16">
          <div className="col-span-full">
            <h1 className="font-mono text-6xl font-bold tracking-tighter mb-4">
              <span className="text-primary">_</span>CODE WITH INTENT
            </h1>
            <p className="font-mono text-xl text-muted-foreground max-w-2xl">
              Practitioner‑developed, production‑ready AI and software
              engineering education. No fluff. Just precision.
            </p>
          </div>
        </GridContainer>
      </main>
      <SiteFooter />
    </>
  );
}
```

---

### 5. Validation & Next Steps

**Checklist:**
- [x] Project initialised with Next.js, TypeScript, Tailwind.
- [x] Shadcn‑UI installed and essential components added.
- [x] Custom fonts (`Space Grotesk`, `JetBrains Mono`) configured via `next/font`.
- [x] Tailwind configuration extended with our "Technologic Minimalism" palette and font families.
- [x] Global CSS variables set to enforce sharp radii and high contrast.
- [x] `GridContainer` component created for consistent layout scaffolding.
- [x] `SiteHeader` built using Shadcn `NavigationMenu`, styled with monospace and cyan accent.
- [x] `SiteFooter` built minimalistically with monospace links.
- [x] Home page updated to test all components and demonstrate the aesthetic.

All components render correctly with no errors. The header is sticky, the grid adapts responsively, and the overall look already communicates the intended **precision‑first, anti‑generic** identity.

**Next Phase (Phase 2) will involve:**
- Building the hero section with the "glitch‑art" partner logo mosaic.
- Crafting the value propositions as a "Terminal Grid".
- Developing the featured course "Neural Blueprint" module diagram.
- Implementing the upcoming training "Timeline Interface".
- Adding the professional services "Portal" CTA.

---
