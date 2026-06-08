# Portfolio Rebuild: Learning-Focused Agent Guide

## Project Overview

**Goal:** Rebuild the portfolio to be **visually stunning**—minimalist + elegant with smooth scroll animations, interactive micro-interactions, and advanced effects.

**Approach:** Teaching-focused. Agents guide and teach the user; user drives implementation.

**Current Status:** Phase 0 (Design Vision & Aesthetics) — Planning stage
- ✓ Plan created
- ⏳ Next: Gather design inspiration and create mockups

---

## Key Principles for Agents

When helping with this project:

1. **Teach, don't code for.** Explain concepts, show examples, point to resources. Let the user implement.
2. **Ask why before jumping to solutions.** Help them think through architecture and design decisions.
3. **Emphasize design thinking first.** Before writing code, nail the visual direction.
4. **Connect to learning goals.** Frame tasks in terms of skills they're practicing.
5. **Keep notes.** Update this file with progress so agents stay aligned.

---

## Learning Phases

### Phase 0: Design Vision & Aesthetics
**Status:** 🟡 IN PROGRESS  
**Learning Goal:** Design thinking, visual hierarchy, animation strategy

**Objectives:**
- [ ] Gather 5-10 design references the user loves
- [ ] Analyze inspiration for patterns (minimalist, animations, color, typography)
- [ ] Create rough mockups/wireframes (Figma, pen-and-paper, or screenshots)
- [ ] Define design tokens (colors, fonts, spacing, border-radius)
- [ ] Write animation strategy (where animations happen + timing)

**Guidance for Agents:**
- Ask: "What design portfolios inspire you? Why do they work?"
- Point to resources: Dribbble, Awwwards, Behance, design blogs
- Help them think about minimalism: What can we remove? What's essential?
- Animation planning: Where would smooth transitions enhance the experience?

**Files to reference:**
- Wireframes/mockups (user-created, not in repo yet)
- Design inspiration doc (user-created)

**Next Milestone:** Mockups + animation strategy document

---

### Phase 1: Architecture & Planning
**Status:** 🔵 PENDING  
**Learning Goal:** Data flow, component organization, scalable structure

**Objectives:**
- [ ] Decide: JSON files or Supabase for content?
- [ ] Design data schema (projects, blog posts, experience, skills)
- [ ] Create folder structure in `src/`
- [ ] Define TypeScript interfaces

**Guidance for Agents:**
- Explain tradeoffs: JSON = simpler, Supabase = scalable + queryable
- Ask: "What data do your projects need?" (title, description, images, links, tech stack, etc.)
- Show existing TypeScript patterns in the codebase
- Help them think about reusability: Can this schema support future sections?

**Critical Files (to create):**
- `src/data/projects.json` or Supabase setup
- `src/types/index.ts` (TypeScript interfaces)
- `src/lib/` (utilities for data fetching)

**Current State of Codebase:**
- Tech stack: Next.js 14, React 18, TypeScript, Tailwind, (unused Supabase)
- Components: Header, Hero, Footer, Card (unused)
- Pages: Home, planned but unbuilt: About, Projects, Contact
- Note: Components folder is misspelled as "componenets"

**Next Milestone:** Schema defined + folder structure created

---

### Phase 2: Visual Components & Animations
**Status:** 🔵 PENDING  
**Learning Goal:** React + Tailwind + Framer Motion animations

**Objectives:**
- [ ] Install Framer Motion: `npm install framer-motion`
- [ ] Build `ProjectCard` with hover animations + smooth reveal
- [ ] Build `ExperienceTimeline` with scroll-triggered animations
- [ ] Create `AnimatedSection` wrapper for scroll triggers
- [ ] Create animation presets library (`src/lib/animations.ts`)
- [ ] Implement smooth page transitions

**Guidance for Agents:**
- Introduce Framer Motion: `animate`, `transition`, `variants`, gesture props
- Show: How to make components respond to scroll (useViewportScroll, AnimatePresence)
- Teach: Micro-interactions (hover scales, color shifts, smooth transitions)
- Ask: "What should happen when this card enters the viewport?"
- Help debug animation performance (GPU acceleration, when to use `will-change`)

**Libraries to use:**
- Framer Motion (animations, gestures)
- Tailwind CSS (styling)

**Critical Files (to create):**
- `src/components/ProjectCard.tsx` (animated card)
- `src/components/ExperienceTimeline.tsx` (timeline with animations)
- `src/components/AnimatedSection.tsx` (scroll-trigger wrapper)
- `src/lib/animations.ts` (animation variants/presets)

**Design Reference:** Minimalist + elegant, smooth animations, hover interactions

**Next Milestone:** Animated components built + used in pages

---

### Phase 3: Advanced Interactivity & Effects
**Status:** 🔵 PENDING  
**Learning Goal:** Gestures, parallax, advanced animations

**Objectives:**
- [ ] Add parallax to Hero section
- [ ] Add scroll progress indicator
- [ ] Implement smooth page transitions between routes
- [ ] (Optional) Canvas-based animated background
- [ ] (Optional) Gesture animations on mobile

**Guidance for Agents:**
- Teach: Scroll-linked animations (useScroll, useMotionTemplate)
- Parallax tutorial: Offset elements based on scroll position
- Performance note: Use `transform: translateZ(0)` for GPU acceleration
- Gesture detection: How to make interactions feel natural on mobile

**Libraries:**
- Framer Motion (scrolling, gestures)
- (Optional) three.js or Babylon.js for 3D effects

**Critical Files (to create/modify):**
- `src/components/Hero.tsx` (add parallax)
- `src/components/ScrollProgress.tsx` (new)
- `src/app/layout.tsx` (page transitions)

**Next Milestone:** Advanced effects implemented + tested

---

### Phase 4: Next.js Features & Dynamic Routes
**Status:** 🔵 PENDING  
**Learning Goal:** SSG, ISR, metadata, SEO

**Objectives:**
- [ ] Convert projects to dynamic routes (`/projects/[slug]`)
- [ ] Set up blog with SSG or ISR
- [ ] Implement proper `metadata` in each page
- [ ] Generate sitemap + robots.txt

**Guidance for Agents:**
- Explain: When to use SSG vs ISR vs server components
- Show: How to structure dynamic routes in Next.js 14
- SEO fundamentals: Metadata, Open Graph, structured data
- Performance: Pre-rendering benefits, when ISR makes sense

**Critical Files (to create/modify):**
- `src/app/projects/[slug]/page.tsx`
- `src/app/blog/[slug]/page.tsx`
- `src/app/robots.ts`
- `src/app/sitemap.ts`

**Next Milestone:** Dynamic routes working + metadata set

---

### Phase 5: Backend & API Work
**Status:** 🔵 PENDING  
**Learning Goal:** Building APIs, form handling, validation

**Objectives:**
- [ ] Design API endpoints (GET /api/projects, POST /api/contact, etc.)
- [ ] Build `/api/contact` endpoint with validation
- [ ] Create contact form component with animations
- [ ] Add error handling and user feedback

**Guidance for Agents:**
- API design: RESTful conventions, status codes, error responses
- Validation: Zod schemas, server-side vs client-side
- Form state: Best practices for form handling in React
- Error UX: Show friendly messages, handle edge cases

**Libraries:**
- Zod (schema validation)
- React Hook Form (form state, optional)

**Critical Files (to create):**
- `src/app/api/contact/route.ts`
- `src/lib/validation.ts`
- `src/components/ContactForm.tsx` (with animations)

**Next Milestone:** Contact form works end-to-end

---

### Phase 6: Quality & Optimization
**Status:** 🔵 PENDING  
**Learning Goal:** Testing, performance, code quality

**Objectives:**
- [ ] Set up Jest + React Testing Library
- [ ] Write tests for key components
- [ ] Run Lighthouse audit + fix issues
- [ ] Enable TypeScript strict mode
- [ ] Code cleanup + refactoring

**Guidance for Agents:**
- Testing: Unit vs integration, what to test, how to test animations
- Performance: Image optimization, lazy loading, bundle analysis
- TypeScript: Benefits of strict mode, catching bugs early
- Code quality: Linting, code organization, DRY principles

**Tools:**
- Jest, React Testing Library
- Lighthouse (Chrome DevTools)
- TypeScript strict: `true`

**Next Milestone:** Tests passing, Lighthouse score > 90

---

## Tech Stack

- **Next.js 14** (app router, SSG/ISR)
- **React 18** (hooks, server components)
- **TypeScript** (strict mode)
- **Tailwind CSS** (utility-first styling + design tokens)
- **Framer Motion** (animations, gestures, scroll effects)
- **Zod** (validation)
- **Jest + React Testing Library** (testing)

---

## Design Direction

**Aesthetic:** Minimalist + elegant  
**Interactions:** Scroll animations, hover effects, micro-interactions, advanced effects  
**Feel:** Smooth, sophisticated, interactive

---

## How to Use This File

- **For agents:** Read this file first. It's the source of truth for project direction and progress.
- **For ongoing work:** Update this file as phases complete. Mark status, note blockers, update next steps.
- **For teaching:** Reference the "Guidance for Agents" section when helping the user.

---

## Current Blockers / Notes

(None yet—Phase 0 just started)

---

## Quick Links

- **Plan file:** See `.claude/plans/i-want-to-remake-ticklish-cat.md` for detailed implementation plan
- **Repo structure:** `src/app/`, `src/components/`, `src/data/`, `src/lib/`, `src/types/`
- **Current misspelling note:** Folder is `src/componenets/` (should be `components`—fix in Phase 1)

---

Last updated: 2026-06-03  
Next review: After Phase 0 design mockups complete
