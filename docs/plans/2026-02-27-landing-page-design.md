# Landing Page Design

Date: 2026-02-27
Owner: Miroslav Rehounek

## Goals
- Deliver a dead simple, formal personal professional landing page.
- Keep the site single-page and GH Pages friendly.
- Preserve fast load, minimal dependencies, and easy editability.

## Non-Goals
- No blog, portfolio, or case study subpages.
- No build tooling, frameworks, or external runtime dependencies.

## Information Architecture
- Hero: Name, title, positioning line, primary CTA to contact.
- Experience Highlights: 4-6 concise bullets (inferred, editable).
- Services: 4 cards (cloud, AI/ML, DevOps, technical strategy) with crisp copy.
- Contact: email and LinkedIn.

## Copy (Initial Draft)
Hero positioning line:
- "Solution Architect focused on cloud, platform engineering, and security-conscious systems."

Experience highlights (draft, inferred):
- Cloud architecture across AWS and Azure with security-first design.
- Platform engineering and CI/CD modernization for faster delivery.
- Data and distributed systems design for reliability at scale.
- Architecture leadership in presales and solution design.
- Tradeoff analysis aligned to business outcomes.

## Visual Direction
- Formal tone with deliberate typography and spacing.
- Keep the existing dark theme but increase contrast and clarity.
- Background uses a subtle gradient and low-contrast decorative shape.
- Add gentle, meaningful motion (page load fade, staggered card reveal).
- Maintain strong focus states and reduced-motion support.

## Accessibility
- Maintain readable contrast for text and links.
- Provide visible focus styles for keyboard navigation.
- Respect prefers-reduced-motion.

## Deployment
- GitHub Pages served from repository root.
- Keep `CNAME` for custom domain.
