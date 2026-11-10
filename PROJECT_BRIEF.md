# VEYRA — AI Voice Assistant Concept (Project Brief)

## 1. Project Overview
**Product:** VEYRA — AI Voice Assistant Concept Website  
**Slogan:** "Voice That Understands You."  
**Tagline:** "The next-generation voice interface designed to process ideas, automate workflows, and create content in real time. Zero latency, total privacy."  
**Purpose:** Landing page / concept presentation for an AI voice assistant product  
**Language:** Strictly English (all copy, UI, code comments)

## 2. Design System
### Visual Style
- **Theme:** Dark futurism, high-tech, AI
- **Background:** Deep dark `#030308` / `#08070B`
- **Accent 1 (Electric Blue):** `#2563EB`
- **Accent 2 (Neon Purple):** `#7C3AED`
- **UI Language:** Glassmorphism (semi-transparent dark bg, backdrop-filter blur, thin neon borders), neon glow effects, micro-animations on hover
- **Typography:** Clean sans-serif (system font stack: -apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial), high-contrast white text on dark background

### Key Visual Elements
- VEYRA logo: purple sound-wave icon in rounded square + bold white "VEYRA" text
- Concentric Tides background effect (CSS approximation of React Bits Pro component)
- Glassmorphic cards with neon-purple/blue hover glows
- Animated sound waves, node graphs, lock icons, audio spectrums
- Gradient text effects (blue→purple) with neon drop-shadow

## 3. Tech Stack
- **HTML5** (semantic markup)
- **CSS3** (custom properties, CSS Grid, Flexbox, CSS animations/keyframes, backdrop-filter)
- **Vanilla JavaScript** (tab switching, Play/Pause toggle, typing simulation, form validation)
- **No build step** — single `index.html` + `style.css`, opens directly in browser
- **Git repo:** `https://github.com/gL1337-bro/veyra`

## 4. File Structure
```
D:\ai-assistant-presentation\
├── index.html          # Main HTML file (all sections + inline JS)
├── style.css           # All styles (responsive, animations, theme variables)
├── PROJECT_BRIEF.md    # This file
└── .git/               # Git history
```

## 5. Sections (Top to Bottom)

### Header (Absolute, sticky over Hero)
- Position: `absolute; top: 0; left: 0; width: 100%; z-index: 50; background: transparent`
- Left: VEYRA Logo (clickable → `/`)
- Center: Nav links — About, Features, Technology, Contact (muted gray → white glow on hover)
- Right: Capsule neon-purple button "Explore VEYRA ↗" with arrow shift on hover

### Hero (`#hero`)
- Badge: "AI Voice Assistant Concept" (semi-transparent pill, neon border)
- H1: "Voice That <span class="highlight">Understands You.</span>" (gradient blue→purple + neon glow)
- Subtitle: "The next-generation voice interface designed to process ideas, automate workflows, and create content in real time. Zero latency, total privacy."
- CTAs: "Join Waitlist" (gradient + shimmer hover), "Watch Demo" (transparent + neon border)
- Background: Concentric Tides approximation (radial gradients + mask), deep black with electric blue/neon purple glows

### Capabilities / Bento Grid (`#features`)
- Badge: "Capabilities"
- H2: "Engineered for Complete Control"
- Subtitle: "Discover how VEYRA integrates into your workflow with zero friction."
- 4 glassmorphic cards in responsive grid (3-col desktop, 1-col mobile):
  1. **Real-Time Response** (large 2×2 card) — animated sound wave bars, description: "Sub-200ms latency ensures conversations feel entirely natural and fluid, matching human reaction speed."
  2. **Contextual Memory** — node-graph icon, description: "Remembers previous sessions, ongoing tasks, and preferences without needing reminders."
  3. **Private & Secure** — lock icon with glowing aura, description: "End-to-end encryption with local execution options to keep your sensitive data entirely yours."
  4. **Natural Expression** — audio spectrum bars, description: "Choose from hyper-realistic voices equipped with adaptive emotional intonation."

### Workflows / Interactive Tabs (`#workflows`)
- Badge: "Workflows"
- H2: "Speak It Into Existence"
- Subtitle: "See how VEYRA transforms simple spoken prompts into complex completed tasks."
- 3 tabs: "Automate Schedule", "Summarize & Draft", "Creative Generation"
- Each tab shows: Spoken Input → arrow → VEYRA Action output with custom visuals
- Tab switching via JS with smooth fade animation
- Visuals: calendar with moving slots + green checkmark, document with bullets + email draft, canvas with glow nodes + loading bars

### About / Mission (`#about`)
- Badge: "Our Philosophy"
- H2: "The Future of Human-AI Interaction"
- Subtitle: "We believe screens create unnecessary friction. Voice is the most direct path from thought to execution."
- Left column: narrative paragraph + 3 feature bullets (glowing purple dots):
  1. Zero-latency stream processing.
  2. Privacy-first architecture with on-device capabilities.
  3. Emotionally intelligent voice synthesis.
- Right column: glassmorphic card with neon orb core + stats (<200ms Latency, 100% On-Device Privacy)

### Interactive Demo (`#demo`)
- Badge: "Live Interactive Demo"
- H2: "Experience the Latency-Free Voice"
- Subtitle: "Click to simulate a real-time interaction with VEYRA's neural core."
- Glassmorphic panel with:
  - Top: glowing orb + horizontal frequency bars (pulse when playing)
  - Controls: Play/Pause button (neon-purple glow, SVG icons only), Voice Selector chips (Standard Voice / Expressive Tone / Technical Assistant)
  - Simulation area: User prompt bubble → VEYRA response bubble with typing animation
- JS logic: Play/Pause toggles spectrum bars (orb hidden when active), typing effect reveals response text character by character

### Waitlist / CTA (`#waitlist`)
- Badge: "Early Access"
- H2: "Be the First to Experience VEYRA"
- Subtitle: "Join the exclusive waitlist and get priority access to the next-generation voice interface."
- Form: email input (glassmorphic, neon focus ring, placeholder "Enter your email address...") + "Request Access" button (gradient + shimmer + SVG arrow)
- Validation: requires "@" in email, red shake animation on invalid
- Success state: "You're on the list!" message with checkmark icon + "Submit another" reset button
- Trust text: "Limited spots available for Alpha release. No spam ever."

### Footer
- Background: `#08070B`
- Top: multi-column grid (4 cols desktop):
  - Navigation: Home, About, Capabilities, Workflow, Demo, Waitlist
  - Join Us: "View open positions" + Hiring badge
  - Address: Neural Lab 04, Silicon Valley, CA
  - Follow Us: X (Twitter), GitHub, Discord
  - Top-right: circular badge "100% On-Device"
- Divider: thin horizontal neon gradient line
- Bottom bar: "© 2026 VEYRA AI Inc. All rights reserved." (left) | "Privacy Policy" & "Terms of Service" links (right)
- Wordmark: massive "VEYRA" text (blue→purple gradient), wide letter-spacing, centered, edge-to-edge width

## 6. Responsive Breakpoints
- **Desktop:** > 900px (4-col footer grid, 3-col bento grid, side-by-side About columns)
- **Tablet:** ≤ 900px (2-col footer grid, 1-col bento, stacked About columns)
- **Mobile:** ≤ 480px (1-col everything, stacked bottom bar, reduced padding, hidden mobile nav)

## 7. Key Implementation Details
- All animations are pure CSS (`@keyframes`): wave pulse, node pulse/ring, spectrum grow, orb float, typing dots, shimmer on buttons
- Tab switching: JS toggles `.active` class, ARIA attributes for accessibility
- Waitlist form: `event.preventDefault()`, email `@` validation, success/error UI states
- Demo player: SVG icons only (no emojis), Play/Pause state synced with spectrum visibility
- `scroll-behavior: smooth` for anchor navigation

## 8. Known Limitations / Next Steps
- No React/Next.js port yet (Node.js not available in current environment)
- `<Concentric Tides />` React component from React Bits Pro not installed — CSS approximation used instead
- No backend — waitlist form is frontend-only simulation
- No actual voice/audio integration — demo is visual simulation only
- To deploy: upload `index.html` + `style.css` to any static hosting (GitHub Pages, Vercel, Netlify, etc.)

## 9. How to Handoff to New Chat
Pass this file + the two source files (`index.html`, `style.css`) to continue development. Recommended next steps:
1. Initialize React/Next.js project
2. Install `@reactbits-starter/concentric-tides-tw` for true animated background
3. Port sections one by one as React components
4. Add real backend for waitlist subscriptions
5. Add actual Web Speech API integration for Demo section
