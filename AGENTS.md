<!-- BEGIN:nextjs-agent-rules -->

## This is NOT the Next.js you know

This version has breaking changes — APIs, conventions, and file structure may all differ from your training data. Read the relevant guide in `node_modules/next/dist/docs/` (resolved from this file's directory; in monorepos the `next` package may not be visible from the repo root) before writing any code. Heed deprecation notices.

This block is written and re-added by `next dev` — verify at `node_modules/next/dist/server/lib/generate-agent-files.js`. Removing it from a diff only re-creates the uncommitted change; committing it with your work keeps the tree clean.

<!-- END:nextjs-agent-rules -->
# Otaku Central — Agent Instructions

## Product
Build Otaku Central: an anime-first discovery and personal tracking platform.
Core features: discovery, anime detail pages, watch statuses, episode progress,
personal ratings, custom lists, profiles, and Otaku AI.

## Stack
- Next.js App Router, React, TypeScript
- Tailwind CSS
- Supabase for PostgreSQL and authentication
- GSAP for deliberate motion; Lenis only where it improves navigation
- Server-side API routes/actions for private integrations and AI calls

## Design
- Premium cinematic anime-inspired interface.
- Deep black / midnight-purple base, restrained crimson and violet accents.
- Strong typography, clear hierarchy, high-quality licensed/approved artwork.
- Responsive layouts, accessible contrast, keyboard support.
- Avoid generic dashboards, excessive gradients, clutter, and unnecessary animation.

## Engineering
- Use small reusable components and typed data models.
- Keep server-only secrets out of client components.
- Validate user input on the server.
- Add loading, empty, error, and success states.
- Do not invent API endpoints or scrape services without permission.
- Do not change unrelated files or add dependencies without explaining why.
- Preserve existing functionality and run lint/type checks after changes.

## Data and privacy
- Separate shared anime metadata from each user's private tracking records.
- Enforce Supabase Row Level Security for user-owned data.
- Never expose service-role keys or LLM keys in browser code.
- Respect provider terms, rate limits, attribution, and deletion requests.

## Workflow
1. Inspect existing files before editing.
2. Explain a short plan and identify files to change.
3. Implement the smallest coherent change.
4. Run available checks and report exact results.
5. Summarise changed files, setup steps, and known limitations.