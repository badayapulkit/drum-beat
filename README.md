# Drumbeat

**AI-native launch workflow platform for product marketers.**
Turn a product brief into a tier-classified, on-message launch package in under 30 minutes.

---

## The problem

Every product launch is a fire drill. PMMs juggle a dozen artifacts (positioning, messaging matrix, sales script, FAQ, blog draft, internal comms, social variants, customer email) under deadline pressure, with no single tool that understands launch *methodology*. Existing options:

- **Project tools** (Asana, Linear) track tasks but don't write copy.
- **AI writers** (Jasper, Copy.ai) write copy but don't know what a Tier 1 launch is.
- **PMM frameworks** (Product Marketing Alliance, Reforge) teach the right approach but live in PDFs and Notion templates.

The gap: an opinionated, AI-native workflow that takes a product brief and produces a launch-ready package, grounded in proven PMM methodology.

## The solution

Drumbeat is the launch workflow PMMs actually want:

1. **Brief in** — structured intake (what's launching, audience, problem, differentiation, timeline).
2. **Tier classification** — applies Launch Tiering framework, recommends Tier 1/2/3 with reasoning.
3. **Positioning + messaging matrix** — generated from the brief, framework-aware.
4. **Asset pack** — 6 launch assets generated together (internal announcement, blog draft, sales one-pager, sales script talking points, social variants, customer email).
5. **Launch hub** — one shareable URL where the team reviews, edits inline per asset, exports to Notion / Google Docs.

## Wedge & strategy

Drumbeat enters the market through **launch workflows** specifically — not "the everything tool for PMMs." Once we own launches, adjacent modules (battlecards, win/loss programs, persona builders) become natural expansions.

See [`docs/decisions.md`](docs/decisions.md) for the full reasoning behind the wedge choice and every other major decision.

## Status

🚧 Pre-MVP. Concierge validation phase.

| Phase | Window | Goal |
|---|---|---|
| 0 — Validate | Weeks 1–2 | Concierge MVP with 5–10 PMM design partners |
| 1 — Wedge MVP | Weeks 3–8 | Brief → 6 assets → hub, end-to-end |
| 2 — Closed beta | Weeks 9–12 | Design partners onboarded as paying beta users |
| 3 — Public launch | Weeks 13–16 | ProductHunt + PMA community + content engine |
| 4 — Expand | Weeks 17+ | Win/loss + battlecards + personas as add-on modules |

Full roadmap: [`docs/roadmap.md`](docs/roadmap.md).

## Tech stack

| Layer | Choice | Rationale |
|---|---|---|
| Framework | Next.js 15 (App Router) + TypeScript | RSC for streaming AI output, largest hiring pool, Vercel-native |
| UI | Tailwind + shadcn/ui | Ship fast, fully owned components |
| DB | Neon Postgres + Drizzle ORM | Serverless Postgres with branching; type-safe ORM with no magic |
| Auth | Clerk | Built-in orgs/teams (B2B SaaS need); 1-day setup |
| AI | Claude Sonnet 4.6 (default), Opus 4.7 (Pro tier) | Sonnet = best $/quality for asset gen; Opus = premium differentiator |
| Async | Inngest | Durable steps for multi-asset generation; built-in retries & observability |
| Billing | Stripe | B2B-grade, complex pricing, dispute handling |
| Email | Resend | Transactional + product emails |
| Analytics | PostHog | Product analytics + feature flags |
| Hosting | Vercel | Zero-config Next.js, edge functions, preview envs |

Detailed reasoning per choice: [`docs/decisions.md`](docs/decisions.md).

## Pricing model (planned)

| Tier | Price | Limits | Target |
|---|---|---|---|
| Free | $0 | 1 launch / month, basic templates | Discovery, SEO, community |
| Pro | $49 / PMM / mo | Unlimited launches, all assets, exports | Solo PMMs, founders |
| Team | $199 / 3 seats / mo | + collaboration, shared library, branded exports | PMM teams |
| Enterprise | Custom | + SSO, audit log, custom assets, API | 50+ person companies |

## Local dev

(To be added in Phase 1.)

## Author

Built by [@badayapulkit](https://github.com/badayapulkit) as part of a PM/PMM portfolio + commercial SaaS effort.

## License

Source-available for portfolio and reference. **Not open source.** See [`LICENSE.md`](LICENSE.md).
