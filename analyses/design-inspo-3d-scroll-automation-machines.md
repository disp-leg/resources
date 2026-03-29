# Design Inspiration Analysis #2
## Source: Viktor Oddy (@viktoroddy) — Scroll-Based 3D Landing Page

**Post URL:** https://x.com/viktoroddy/status/2037839395638899136
**Posted:** March 28, 2026
**Views:** 25.2K | Likes: 373 | Bookmarks: 436

---

## What the Post Shows

Viktor Oddy (@viktoroddy) is a designer/entrepreneur and founder of **MotionSites.ai** who specializes in building "premium cinematic websites using AI in minutes." This post demonstrates a **scroll-based 3D landing page** built for a fictional company called **"AUTOMATION MACHINES"** — and crucially, shows that anyone can recreate it using an AI prompt.

The post shows a side-by-side screen recording:
- **Left panel:** An AI builder interface (appears to be Bolt.new or a similar AI coding tool) with a chat conversation guiding the construction
- **Right panel:** The live preview of the resulting "AUTOMATION MACHINES" landing page

The key message: a production-grade, cinematic 3D website was generated almost entirely through AI prompting — no traditional hand-coding required.

---

## The Website Being Highlighted

**Name:** AUTOMATION MACHINES
**Type:** Hero Section / Landing Page (for an industrial automation company concept)
**Source/Template Library:** [MotionSites.ai](https://motionsites.ai) — listed as a Premium "Hero Section" template

The Automation Machines design is one of Viktor Oddy's template prompts on MotionSites.ai — a prompt library for generating high-quality landing pages via AI tools (Bolt.new, Lovable, Gemini, etc.).

---

## Design Elements

### Color Palette
- **Primary:** Near-black (#0a0a0a or equivalent) — deep, pure dark background
- **Accent:** Neutral metallics — chrome, gunmetal silver, steel gray on the robotic arm 3D model
- **Text:** Bright white for the headline ("AUTOMATION MACHINES"), sharp contrast against the black background
- **Subtle secondary text:** Low-opacity white/gray for supporting copy
- No neon or bright accent colors — this is deliberately industrial/premium, not cyberpunk

### Typography
- **Headline:** Large, bold, extended-width sans-serif all-caps — "AUTOMATION MACHINES" set in a wide tracking, high-impact display weight
- Reminiscent of industrial/manufacturing brand language — mechanical, authoritative
- The dot or bullet after "MACHINES·" suggests animated punctuation or a typewriter-style trailing character
- Supporting body copy is small, tight, and low-contrast — kept out of the way of the 3D hero

### Layout
- **Full-viewport hero:** No above-the-fold clutter — the entire first screen is consumed by the 3D scene and the headline
- **Two-column visual weight:** The headline dominates the left, the 3D robotic arm anchors the right — classic hero composition
- **Minimal navbar:** Thin, light-colored navigation links along the top (HOME, FEATURES, PRICING, etc.) with a CTA button — does not compete with the hero
- Generous whitespace around all elements — the 3D model breathes

### 3D Elements
- **Hero Object:** A high-fidelity industrial robotic arm — chrome/steel finish, detailed joint geometry, sitting on a circular base
- The arm is rendered with realistic material shading: specular highlights, ambient occlusion shadows, metallic reflections
- **Probable tooling:** Spline — Viktor Oddy's templates consistently use Spline for browser-native 3D, and the Spline community has specific robot arm assets/templates. The model quality and render style match Spline's PBR (physically-based rendering) engine
- The arm appears to be embedded as a Spline scene via `<spline-viewer>` web component or the Spline React package, rendering in WebGL

### Scroll-Based Animation (The Core Innovation)
This is the distinguishing feature of the post:

- As the user scrolls, the **3D scene transforms** — the camera angle shifts, the robotic arm moves or assembles, and content sections animate into view
- This is the "Apple product page" model applied to industrial/B2B — the 3D object is the star, and scrolling is the narrative driver
- Scroll events are bound to Spline's animation timeline, controlling which keyframe of the arm's motion is displayed at any given scroll position
- The effect: scrolling down feels like operating the machine, not reading a page

### Animations and Interactions
- Entry animation: The robotic arm likely fades/scales in on page load
- Hover states: The Spline scene probably responds to mouse position — the arm tracking or tilting slightly with cursor movement (common in Spline interactive exports)
- Section transitions: Content blocks slide or fade in as they enter the viewport
- The scroll progress is mapped to a Spline animation timeline — this is Spline's "scroll event" feature or a custom GSAP ScrollTrigger integration

---

## Technical Implementation

### Stack
- **3D Engine:** Spline (browser-native WebGL, not Three.js from scratch)
- **Framework:** React (via Bolt.new or similar AI full-stack builder)
- **Animation:** Either Spline's built-in scroll events, or Spline + GSAP ScrollTrigger for precise scroll-to-timeline scrubbing
- **Styling:** Tailwind CSS (standard for AI-generated React sites)
- **Deployment:** Likely Netlify or Vercel (Bolt.new deploys to both)

### How Spline Is Used Here
Spline is not Three.js — it is a no-code 3D design tool with a direct browser export. The workflow:
1. Designer (or AI prompt) builds/selects a 3D scene in Spline editor
2. Spline exports a `scene.splinecode` file
3. The React component imports `@splinetool/react-spline` and passes the scene URL
4. Scroll position is fed into Spline's `spline.emitEvent()` or via Spline's built-in scroll trigger
5. The entire 3D experience runs in WebGL, embedded natively in the page

### Why This Implementation Stands Out
1. **Zero Three.js complexity:** Spline abstracts away the shader code, lighting rigs, and camera control that would take weeks to build from scratch
2. **AI-generated in minutes:** The prompt Viktor Oddy uses (shared on MotionSites.ai) instructs the AI builder to set up the Spline embed, configure scroll behavior, and build the surrounding layout — this is a complete production page from a single prompt
3. **Photorealistic materials in WebGL:** The chrome/steel robotic arm uses PBR materials that look like a product render, not a game asset — this elevates the perceived brand value dramatically
4. **Scroll-as-storytelling:** Rather than static product screenshots, the 3D object IS the content — it moves, assembles, or reveals itself as the user reads, which keeps engagement extremely high

---

## What Makes the 3D Implementation Stand Out

1. **Industrial realism:** Most 3D web scenes use abstract blobs, particles, or stylized geometry. A photorealistic industrial robot arm is rare — it communicates competence and precision, not just aesthetic flair.

2. **Narrative scroll:** The scroll doesn't just reveal content below the fold — it controls what the 3D model is doing. This creates an interactive feel without requiring the user to click anything.

3. **AI-buildable:** The entire scene was constructed through prompting (shared publicly on MotionSites.ai as a premium prompt). This means the pattern is replicable and scalable — teams can now ship 3D scroll sites without a dedicated 3D artist or WebGL engineer.

4. **Brand-appropriate 3D:** The 3D object is directly relevant to the product (automation/robotics) — not decorative. This is better practice than using generic abstract 3D because it communicates function.

---

## What MotionSites.ai Is

Viktor Oddy's product behind this post. It is a **prompt library for AI-generated landing pages**, with 40+ hero section prompts covering SaaS, Web3, Agency, Portfolio, Automotive, and 3D/Creative categories.

- Pricing: $59 lifetime (unlimited access) or $99 "Power" tier
- Templates include: Space Voyage, NeoVision, Orbit Web3, NOVA Space Systems, Framelix 3D Studios, Planet Orbit, Nexus IT Solutions, Automation Machines, and more
- Free prompts available for many templates; 3D/premium ones like Automation Machines require payment
- The associated learning platform is **Design Rocket** (designrocket.io)
- Viktor Oddy has 23.5K YouTube subscribers and documents the full AI design process publicly

---

## Relevance to a Movie Recommendation App

### Direct Applications

**1. 3D Hero Section with Scroll-Driven Camera**
A movie rec app could feature a 3D cinema environment — seats, a screen, film reels, or a projector — that animates as the user scrolls into the app. Spline makes this buildable without a Three.js engineer.

**2. Scroll-Triggered Genre Exploration**
Instead of tabs or filters, genres could be revealed as the user scrolls through a 3D scene — different environments rotating or assembling to represent Horror (dark dungeon), Sci-Fi (space station), Romance (warm interior), etc.

**3. Featured Film "Object" Hero**
A specific film's iconic prop or setting could be a 3D hero — a spinning planet for a space movie, a spinning vinyl for a music documentary. The Automation Machines prompt shows how to pair a 3D product with dark-background typography effectively.

**4. Rating/Interaction with 3D Response**
When a user rates a film, a 3D element (a star, a film clapboard, a popcorn bucket) could animate in response — micro-interaction design elevated by Spline.

**5. Dark-Premium Aesthetic**
The Automation Machines color language (pure black + white text + silver 3D) translates extremely well to cinema — theaters are dark, premium movie streaming platforms (Apple TV+, A24's aesthetic) embrace the same palette. This is the right design language for a premium movie rec experience.

### Specific Spline Patterns to Steal
- **Material:** PBR metallic/specular shaders for any mechanical or premium object
- **Scroll binding:** Map scroll position to Spline animation timeline for cinematic reveals
- **Mouse tracking:** Spline's pointer events make the 3D scene respond to cursor, adding interactivity without custom code
- **Embed method:** `@splinetool/react-spline` — the standard React integration

### Key Caution
Spline scenes add significant JavaScript and WebGL overhead. For a movie rec app where page performance affects user retention (especially on mobile), the 3D should be:
- Hero-only (one Spline scene max per page)
- Lazy-loaded below the fold if not the primary hero
- Replaced with a video fallback on mobile or low-power devices

---

## Files Captured

- `/tmp/x-link-design-inspo-2.png` — Screenshot of the X/Twitter post showing the AI-build session + Automation Machines preview
- `/tmp/automation-machines-card.png` — Close-up of the Automation Machines hero section card from MotionSites.ai
- `/tmp/motionsites-homepage.png` — MotionSites.ai homepage showing the full template library
- `/tmp/motionsites-guide.png` — MotionSites.ai guide page with Viktor Oddy's YouTube workflow video

---

## Summary

This post is really about two things: (1) the **Automation Machines 3D scroll-based landing page** as a design artifact, and (2) **MotionSites.ai** as the platform where anyone can access the prompt to build it themselves. The 3D implementation is Spline-based, scroll-driven, and photorealistic — using a robotic arm as the hero object on a pure black background with a bold white headline. The pattern is directly applicable to a premium movie recommendation app's hero design, genre browsing experience, and film-focused micro-interactions.
