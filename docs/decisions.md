# Decision log

A living record of every meaningful decision on Drumbeat — what we picked,
what we considered, why we picked it, and the tradeoff we accepted. New
decisions go at the top.

---

## 2026-04-28 — Wedge: Launch Workflows (not battlecards, not win/loss)

**Decision.** The first product Drumbeat ships is a launch-workflow tool.
Battlecards, win/loss, and persona builders are deferred to later modules.

**Considered.**
- *Battlecards.* Clear market, but dense competition (Klue, Crayon — both
  well-funded category leaders). Low ARPU per seat ($30–50). Thin AI story
  for an interview portfolio.
- *Win/loss programs.* Genuinely underserved. High contract value. But
  services-heavy (real customer interviews) and slow to sell.
- *Launch workflows.* Adjacent competition only (Productboard, LaunchNotes,
  Airfocus) — nobody owns the PMM launch workflow end-to-end. Highest AI
  surface area (tier classification + messaging + 6 assets + sales
  enablement + retro). Uses 12+ frameworks from the PMA library. Strongest
  interview-portfolio story.

**Why launches won.**
1. Less consolidated competition → real wedge available.
2. Higher ARPU potential ($200–1500/team/mo) → plausible $10M ARR path.
3. Multi-step orchestration → demonstrates deeper PM + engineering work
   than a single-shot generator.
4. Maps to most of the PMA template library, so the catalog becomes a moat
   instead of dead weight.

**Tradeoff accepted.** Bigger MVP than battlecards (6–8 weeks vs ~4).
Willing to pay this cost for a real wedge instead of a knife fight.

---

## 2026-04-28 — MVP scope: brief → 6 assets → hub

**Decision.** v0 ships exactly: structured brief intake, tier
classification, positioning + messaging matrix, generation of 6 launch
assets (internal announcement, blog draft, sales one-pager / FAQ, sales
script talking points, social variants, customer email), and a hub view
where each asset can be edited and regenerated.

**Out of scope for v0.** Project management, real-time multi-user collab,
integrations beyond Notion/Google Docs export, win/loss, battlecards,
personas, approval workflows, custom branding, SSO, public API.

**Why.** Smallest unit that delivers a "wow" demo — brief in, launch
package out — and the smallest thing that justifies a paid tier. Every
feature outside this critical path is cut.

**Tradeoff accepted.** Won't impress enterprise buyers on day one. That's
fine — enterprise is phase 3.

---

## 2026-04-28 — Stack: Next.js 15 + Drizzle + Clerk + Inngest + Sonnet 4.6

**Decision.** See README.md "Tech stack" table.

**Why each choice.**
- *Next.js 15 over Remix/Astro/SvelteKit.* Largest hiring pool, RSC for
  streaming AI output (matters for asset generation UX), Vercel-native
  deploy, biggest ecosystem of templates and SaaS starters.
- *Drizzle over Prisma.* Lighter, faster cold-start, no codegen step, full
  type safety without magic. Tradeoff: younger ecosystem.
- *Clerk over Auth.js / Lucia.* Built-in organizations & team membership —
  required for B2B SaaS pricing tiers. Setup in a day vs a week. Tradeoff:
  ~$25/mo at scale and vendor lock-in.
- *Inngest over raw queue (BullMQ, SQS).* Asset-pack generation is a
  multi-step durable workflow. Inngest gives retries, step caching, and
  observability for free. Tradeoff: another vendor.
- *Sonnet 4.6 default, Opus 4.7 for Pro tier.* Sonnet has the best
  $/quality ratio for marketing copy. Opus becomes a paid-tier
  differentiator ("Pro mode generates with our largest model"). Tradeoff:
  single-vendor dependency, acceptable for MVP.
- *Stripe over Lemon Squeezy / Paddle.* B2B-grade billing, complex pricing,
  enterprise invoicing. Heavier setup but no migration later.

---

## 2026-04-28 — Repo: public, source-available (not OSS)

**Decision.** GitHub repo `drum-beat` is public, with a proprietary
"All Rights Reserved" license. Code is readable for portfolio and hiring
purposes; not licensed for use or modification.

**Why.** Public visibility serves the interview-portfolio goal. Proprietary
license keeps commercialization options open and prevents AGPL/MIT
ambiguity that could harm a future commercial offering or acquisition.

**Tradeoff accepted.** No external contributions. Acceptable — this is a
solo-founder commercial project, not a community OSS project.

---

## 2026-04-28 — PMA template handling: derivative only, never verbatim

**Decision.** PMA course templates are copyrighted. The repo includes
framework *names* (factual references) and original AI prompts that *apply*
the methodologies, but never the verbatim template text. Verbatim PMA
content stays out of the public repo (and out of the product as content
served to users).

**Why.** Avoid copyright infringement and keep the commercial product on
defensible legal ground.
