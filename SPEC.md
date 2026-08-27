# SPEC: SEO Audit Dashboard (with De-AI Pass)

**Author:** Mina Ashraf
**Track:** Frontend AI Engineering
**Date:** August 27, 2026

---

## Problem Statement
Website owners and content creators often publish AI-assisted content without checking two things: (1) whether the page follows basic on-page SEO best practices, and (2) whether the writing still reads as noticeably AI-generated in a way that hurts trust and engagement. This tool audits any public URL and returns both an SEO score and a "de-AI" rewrite pass on flagged content.

## Target User
Solo content creators, small business owners, or freelance marketers who publish their own web content and don't have access to an SEO specialist or professional editor.

## Core Features (MVP)
1. **URL input** — user pastes any public webpage URL.
2. **SEO audit engine** — fetches the page and checks: title tag length, meta description presence, heading hierarchy (H1/H2 structure), image alt-text coverage, and word count.
3. **SEO score** — a 0–100 score with a breakdown of what passed/failed and why.
4. **De-AI pass** — sends flagged paragraphs (repetitive phrasing, generic AI-sounding language) to an AI model, which rewrites them in a more natural, human tone, shown as a before/after diff.
5. **Dashboard view** — results displayed as a clean, single-page report with score, checklist, and rewrite suggestions.

## Tech Stack
- **Frontend:** Next.js (App Router) + React + Tailwind CSS
- **Backend:** Next.js API routes for fetching/parsing pages and calling the AI model
- **AI:** Claude API (or equivalent) for the de-AI rewrite pass
- **Deployment:** Vercel (free tier)

## Success Criteria
- A user can paste any public URL and get a working SEO score within ~10 seconds.
- The de-AI pass produces a genuinely different, more natural rewrite (not just synonym-swapping).
- The dashboard is usable and readable on both desktop and mobile.
- Deployed live with a shareable URL by FE-05.

## Out of Scope (for now)
- User accounts / saved audit history
- Competitor comparison or keyword-ranking data
- Auditing pages behind login walls
- Multi-language support (English content only for MVP)

## Milestones
| Assignment | Deliverable |
|---|---|
| FE-04 | Skeleton scaffolded (routes, layout, placeholder screens) |
| FE-05 | Capstone skeleton deployed live |
| FE-06 | Core SEO audit engine working end-to-end |
| FE-07 | De-AI rewrite pass integrated + tests |
| FE-08 | Accessibility pass + polish |
| Week 8 | Final capstone submission |
