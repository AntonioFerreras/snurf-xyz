# PROJECT.md

# Vibecoded Personal Portfolio

## Overview
This document outlines the technical stack and design philosophy for a modern, expressive personal portfolio website. The goal is to create a site that feels unique, interactive, and intentionally crafted—avoiding generic templates while still maintaining fast iteration and low friction during development ("vibecoding").

---

## Core Principles

### 1. Fast Iteration
The stack should allow rapid experimentation without heavy setup or friction.
- Minimal configuration
- Instant feedback loops
- Easy deployment

### 2. Expressive UI
The website should feel alive and intentional.
- Smooth animations
- Responsive interactions
- Thoughtful spacing and typography

### 3. Focused Complexity
Avoid overengineering.
- Start simple
- Add complexity only where it adds impact
- One standout interactive element > many mediocre effects

### 4. Performance by Default
The site should feel fast without constant optimization effort.

---

## Engineering Principles

### 1. Fail Hard, Not Silently
- If something is misconfigured, crash. Do not fall back to defaults that hide broken state.
- No silent retries, no quiet fallbacks, no “safe” defaults that mask issues.
- A predictable crash is better than unpredictable behavior.

### 2. No Defensive Programming for Its Own Sake
- Don’t guard against things that can’t happen.
- Trust internal code and framework guarantees.
- Only validate at system boundaries: user input, external APIs, config.
- If bad data comes from our own code, fix the caller.

### 3. Lines of Code: Golf, Not Bowling
- Prefer fewer lines.
- Avoid premature abstractions.
- Don’t introduce helpers or utilities for one-off use.
- Don’t add unused extensibility or config.

### 4. Simple Beats Clever
- The smallest clear solution that fully solves the problem wins.
- Fewer moving parts over dense abstractions.
- If you can’t explain it in one sentence, simplify it.

---

## Tech Stack

### Framework — Next.js
**Role:** Application structure and runtime

Handles:
- Routing (pages like `/`, `/projects`, `/about`)
- Build system and bundling
- Performance optimizations
- Deployment compatibility with Vercel

---

### Language — TypeScript
**Role:** Code safety and maintainability

---

### Styling — Tailwind CSS
**Role:** Visual design and layout

Handles:
- Layout (flex, grid)
- Spacing
- Typography
- Colors
- Responsiveness

---

### Animation — Motion (Framer Motion)
**Role:** Movement and interaction

Handles:
- Page transitions
- Hover effects
- Scroll animations
- Micro-interactions

---

### Interactive Visuals (Optional) — React Three Fiber
**Role:** 3D and advanced visual elements

Use for:
- Hero section centerpiece
- Interactive backgrounds
- Shader-based effects

Guideline:
- Use sparingly (one or two sections max)

---

### Hosting — Vercel
**Role:** Deployment platform

---

### Domain & DNS — Cloudflare
**Role:** Domain management and DNS

---

## Architecture

```
User → Cloudflare DNS → Vercel → Next.js App
```

---

## Design Philosophy

### Minimal Structure, Maximum Personality
- Clean layout
- Strong typography
- Intentional whitespace

Personality comes from:
- Motion
- Timing
- Interaction details

---

### Motion as a First-Class Element
Animation defines the experience, not decorates it.

---

### One Memorable Moment
Focus on a single standout feature:
- Interactive hero
- Mouse-reactive element
- Subtle 3D scene

---

### Cohesive Visual System
Consistency across:
- Spacing
- Typography
- Animation timing

---

### Content Simplicity
- Hardcoded or local content
- No CMS initially

---

## Site Structure

- Home
- Projects
- About
- Contact

---

## Workflow

1. Build locally (Next.js)
2. Style (Tailwind)
3. Add motion (Motion)
4. Push to GitHub
5. Deploy (Vercel)
6. Connect domain (Cloudflare)

---

## Future Enhancements

- Custom shaders
- Advanced transitions
- Custom cursor
- Subtle sound design

---

## Summary

Build something that is:
- Fast to iterate
- Visually intentional
- Memorable through interaction, not complexity

