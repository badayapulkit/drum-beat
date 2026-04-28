# Phase 0 — Concierge MVP setup

How to deploy the Drumbeat workflow as a Claude.ai Project so you can
run real launches manually for design partners. ~10 minutes of setup.

## 1. Create the Claude Project

1. Go to https://claude.ai
2. In the left sidebar, click **Projects** → **New project**
3. Name it: **Drumbeat — Concierge MVP**
4. Description: "Launch workflow assistant for product marketers."

## 2. Set the project instructions

1. Open the project, click **Set custom instructions**
2. Open [`templates/prompts/system-instructions.md`](../templates/prompts/system-instructions.md)
3. Copy everything *below* the line `---` (skip the title and intro
   note — Claude only needs the instruction body)
4. Paste into the custom instructions field
5. Save

## 3. Upload project knowledge

Upload these files to the project's knowledge:

**Workflow prompts:**
- [`templates/prompts/brief-intake.md`](../templates/prompts/brief-intake.md)
- [`templates/prompts/tier-classification/tier-classification.md`](../templates/prompts/tier-classification/tier-classification.md)
- [`templates/prompts/messaging-matrix/messaging-matrix.md`](../templates/prompts/messaging-matrix/messaging-matrix.md)

**Asset prompts (all 6):**
- [`templates/prompts/assets/internal-announcement.md`](../templates/prompts/assets/internal-announcement.md)
- [`templates/prompts/assets/sales-one-pager.md`](../templates/prompts/assets/sales-one-pager.md)
- [`templates/prompts/assets/blog-draft.md`](../templates/prompts/assets/blog-draft.md)
- [`templates/prompts/assets/sales-script.md`](../templates/prompts/assets/sales-script.md)
- [`templates/prompts/assets/customer-email.md`](../templates/prompts/assets/customer-email.md)
- [`templates/prompts/assets/social-variants.md`](../templates/prompts/assets/social-variants.md)

**Framework references:**
- [`templates/frameworks/launch-tiering.md`](../templates/frameworks/launch-tiering.md)
- [`templates/frameworks/positioning.md`](../templates/frameworks/positioning.md)
- [`templates/frameworks/messaging-framework.md`](../templates/frameworks/messaging-framework.md)
- [`templates/frameworks/story-toolkit.md`](../templates/frameworks/story-toolkit.md)

## 4. Smoke-test it

Start a new conversation in the project. The first message should be
Drumbeat greeting you in 2 sentences and asking for the brief.

Try this test brief to verify the workflow:

```
Launching: Mira, a Slack-native standup bot for engineering teams.
Audience: Engineering managers at 50–500 person SaaS companies.
Problem: Async standups in Slack are unstructured, low-signal, and
ignored by half the team within 2 weeks of launch.
Differentiation: Mira asks each person 3 questions tailored to their
last week's PRs and Linear tickets — not the same generic prompts.
Proof: 8 design partners, average daily participation 87% (vs 40%
industry average for async standup tools).
Launch date: 4 weeks from today.
Strategic context: Top company OKR is "land 100 paying eng teams in Q3."
Channels: founder LinkedIn, product blog, sales-led email to free-tier
users, Hacker News, eng-leader Slack communities.
Risks: Geekbot incumbent has 30k customers; positioning must
differentiate on the personalized-question wedge, not feature parity.
```

You should get back: a Tier 2 classification, a 4-row messaging matrix,
and the first asset (internal announcement) with the rest waiting.
Walk through generating the remaining 5 assets one at a time.

## 5. Run your first design-partner session

When a design partner says yes:

1. Schedule 30 minutes (Zoom + screen share)
2. Open the Drumbeat project, start a new conversation, share screen
3. Ask them to walk you through their upcoming launch verbally
4. You type the brief into Drumbeat as they talk (or paste their own
   brief if they have one)
5. Walk through tier classification together — ask if it matches their
   intuition
6. Generate messaging matrix; ask which rows feel right and which feel
   off
7. Generate 2–3 assets they care most about (often: blog post + sales
   one-pager + customer email)
8. Export everything to a Google Doc and share with them
9. Run the [feedback questions](outreach/dm-variants.md#questions-to-ask-in-every-session)

## 6. Track sessions

Create a Google Sheet with columns:

| Date | Name | Company | Role | Tier of their launch | Assets we generated | What they loved | What they edited heavily | What was missing | Would pay (Y/N) | Price they named | Notes |

Update after every session. By session 5–10 you'll see clear patterns
in what to build for v1.

## Exit criteria

≥5 sessions complete. ≥3 design partners say "I'd pay $X/mo if this
were self-serve." If <3, **stop and re-examine the wedge** before
moving to Phase 1.
