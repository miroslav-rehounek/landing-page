# Landing Page Implementation Plan

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** Update the existing single-page site to a formal, minimal personal landing page with experience highlights and refined visual polish.

**Architecture:** Keep a single static HTML file and one CSS file, no build tools, and GH Pages compatibility. Update structure in `index.html` and styles in `style.css` only.

**Tech Stack:** HTML, CSS (no JS)

---

### Task 1: Update page structure and copy

**Files:**
- Modify: `index.html`

**Step 1: Update hero copy and CTA**

```html
<p class="tagline">Solution Architect focused on cloud, platform engineering, and security-conscious systems.</p>
```

**Step 2: Add Experience Highlights section after hero**

```html
<section class="highlights" id="highlights">
  <div class="container">
    <h2>Experience Highlights</h2>
    <ul class="highlights-list">
      <li>Cloud architecture across AWS and Azure with security-first design.</li>
      <li>Platform engineering and CI/CD modernization for faster delivery.</li>
      <li>Data and distributed systems design for reliability at scale.</li>
      <li>Architecture leadership in presales and solution design.</li>
      <li>Tradeoff analysis aligned to business outcomes.</li>
    </ul>
  </div>
</section>
```

**Step 3: Tighten service card copy (shorter, formal)**

```html
<p>Scalable, secure cloud foundations on AWS and Azure with clear cost controls.</p>
```

**Step 4: Update LinkedIn URL**

```html
<a href="https://www.linkedin.com/in/miroslav-rehounek-aaa01a173/" class="contact-link" target="_blank" rel="noopener noreferrer">LinkedIn</a>
```

**Step 5: Manual check**

Open `index.html` in a browser and confirm section order, copy, and links.

---

### Task 2: Refine visual system and layout

**Files:**
- Modify: `style.css`

**Step 1: Update typography and colors**

```css
:root {
  --color-bg: #0b111c;
  --color-surface: #121a29;
  --color-border: #1f2a3d;
  --color-text: #eef2f7;
  --color-text-muted: #a7b1c2;
  --color-accent: #d5a25f;
  --color-accent-hover: #e0b677;
  --font-stack: "Iowan Old Style", "Palatino Linotype", "Book Antiqua", Palatino, serif;
  --font-stack-sans: "IBM Plex Sans", "Segoe UI", Helvetica, Arial, sans-serif;
  --max-width: 68rem;
}
```

**Step 2: Add background gradient and subtle shape**

```css
body {
  background: radial-gradient(1200px 600px at 80% -10%, rgba(213, 162, 95, 0.15), transparent 60%),
    linear-gradient(180deg, #0b111c 0%, #0e1626 100%);
}

.hero::after {
  content: "";
  position: absolute;
  inset: auto -10% -30% auto;
  width: 40rem;
  height: 40rem;
  background: radial-gradient(circle, rgba(255, 255, 255, 0.06), transparent 70%);
  pointer-events: none;
}
```

**Step 3: Style highlights section**

```css
.highlights {
  padding: 4.5rem 1.5rem;
}

.highlights-list {
  display: grid;
  gap: 0.75rem;
  list-style: none;
  color: var(--color-text-muted);
}
```

**Step 4: Add subtle motion and reduced-motion handling**

```css
.hero,
.service-card,
.highlights-list li {
  animation: fadeUp 700ms ease both;
}

@keyframes fadeUp {
  from { opacity: 0; transform: translateY(12px); }
  to { opacity: 1; transform: translateY(0); }
}

@media (prefers-reduced-motion: reduce) {
  * {
    animation: none !important;
    transition: none !important;
  }
}
```

**Step 5: Manual check**

Open `index.html` on desktop and a narrow mobile viewport to verify readability and spacing.

---

### Task 3: Validate and polish

**Files:**
- Modify: `style.css`

**Step 1: Verify focus styles**

```css
.cta-button:focus-visible,
.contact-link:focus-visible {
  outline: 2px solid var(--color-accent);
  outline-offset: 3px;
}
```

**Step 2: Final manual check**

Confirm keyboard focus, contrast, and that all links work.

**Step 3: Commit**

```bash
git add index.html style.css docs/plans/2026-02-27-landing-page-implementation-plan.md
git commit -m "refactor: refresh landing page layout and styling"
```
