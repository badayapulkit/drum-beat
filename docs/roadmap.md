# Roadmap

## Phase 0 — Validate (weeks 1–2)

**Goal.** Confirm the wedge resonates with real PMMs before writing app code.

- Set up Claude Project with PMA-derivative templates and brief-intake
  prompts.
- Recruit 5–10 PMM design partners (LinkedIn, PMA Slack/community, Reforge,
  founder network).
- Run their real launches through the concierge MVP — *operator-driven*,
  not self-serve yet.
- Track: which assets they reuse, where they edit heavily, what they ask
  for that doesn't exist.
- Decide: confirm asset pack, drop or replace anything weak.

**Exit criteria.** ≥5 design partners say "I'd pay for this if it were
self-serve."

## Phase 1 — Wedge MVP (weeks 3–8)

**Goal.** Self-serve product that takes a brief and ships a launch package.

- Next.js 15 + Tailwind + shadcn scaffold
- Clerk auth with organizations
- Neon Postgres + Drizzle schema (users, orgs, launches, briefs, assets,
  versions)
- Brief intake form (structured)
- Tier classification AI step (Sonnet)
- Messaging matrix generation (Sonnet, structured output)
- Asset-pack generation orchestrated via Inngest (6 parallel asset jobs)
- Launch hub view: read all assets, inline edit, regenerate single asset
- Export to Notion + Google Docs (one-shot)
- Stripe billing wired with Free / Pro / Team tiers
- Resend for transactional email
- PostHog analytics on every meaningful event

**Exit criteria.** Design partners can self-serve a complete launch end to
end, including export, without operator help.

## Phase 2 — Closed beta (weeks 9–12)

- Design partners flip to paying beta users (50% off Pro, 12 months)
- Add: launch templates library (start a launch from a template)
- Add: regenerate-with-feedback ("make it more bold," "shorter," "add
  proof point X")
- Add: simple comments per asset (async collab, not real-time)
- Add: Slack notifications when teammates edit
- Iterate based on telemetry + interviews

**Exit criteria.** ≥10 paying customers, ≥80% week-4 retention.

## Phase 3 — Public launch (weeks 13–16)

- ProductHunt launch
- PMA community marketing (sponsored newsletter / Slack drops)
- Content engine: weekly blog post on launch methodology
- Founder-led sales motion for Team tier
- First enterprise pilot conversations

**Exit criteria.** $20k MRR, 50+ paying teams.

## Phase 4 — Expand (weeks 17+)

- **Battlecards module** — competitive intel asset type, integrates into
  launch flow (battlecard auto-generated from launch brief)
- **Win/loss module** — interview transcript ingestion, theme extraction,
  feedback loop into next launch
- **Persona builder** — B2B/B2C persona generation from interviews
- **Integrations** — Linear / Asana (sync launch milestones), Salesforce
  (push assets to sales enablement)
- **Enterprise tier** — SSO, audit log, custom branding, API
- **API + Zapier** — third-party automation

**$10M ARR target.** Years 3–5, requires sustained execution and the
expansion modules landing.
