# Tier classification — Launch Tiering applied

Classify every launch as Tier 1, Tier 2, or Tier 3 using the dimensions
below. Output a tier, a 2–3 sentence rationale citing the dimensions
that drove the call, and the resourcing implications.

## Dimensions to weigh

| Dimension | Tier 1 signal | Tier 2 signal | Tier 3 signal |
|---|---|---|---|
| **Revenue impact** | Material to annual revenue / opens new revenue line | Meaningful to a segment / quarterly KPI | Marginal — improvement to existing | 
| **Audience reach** | Most or all customers + new prospects | A clear segment | Subset / niche |
| **Strategic priority** | Named on company OKRs at the top level | Supports a top-level OKR | Departmental / quality-of-life |
| **Novelty** | New product, new market, or category-defining | New feature, expansion to adjacent market | Iteration on existing |
| **Cross-functional dependencies** | All-hands: PMM, sales, CS, support, partner, exec | PMM-led + sales/CS + 1 exec | PMM-only or PMM + one team |
| **Competitive stakes** | Defines or defends a market position | Affects competitive narrative | Below the noise floor |
| **Prep window needed** | Multi-quarter | Weeks | Days |

## Classification logic

- If 4+ dimensions are Tier 1: **Tier 1**.
- If 4+ dimensions are Tier 3: **Tier 3**.
- Otherwise: **Tier 2** (the most common case).

If the brief is missing a dimension, name the assumption you're making
and recommend the user confirm with their leadership before locking in.

## Output format

```
**Tier {1|2|3}**

**Rationale.** {2–3 sentences citing the dimensions that drove the call.
Be specific: name the dimension and the signal in this brief that
maps to it.}

**Implications.**
- Resourcing: {who needs to be involved}
- Asset depth: {how comprehensive each asset should be}
- Exec involvement: {what level of exec sponsorship}
- Prep timeline: {realistic window for this tier}
- Skipped assets: {if any assets in the standard 6-pack are unnecessary
  at this tier, name them and why}
```

## Asset coverage by tier (default)

| Asset | Tier 1 | Tier 2 | Tier 3 |
|---|---|---|---|
| Internal launch announcement | ✅ deep | ✅ standard | ✅ short |
| Sales one-pager / FAQ | ✅ deep | ✅ standard | ⚠️ skip unless sales-relevant |
| Blog post draft | ✅ launch-day post + thought leadership | ✅ standard | ⚠️ short release note instead |
| Sales script talking points | ✅ full discovery + objections | ✅ standard | ❌ skip |
| Customer email | ✅ segmented (existing + prospects) | ✅ existing customers | ✅ short product update |
| Social variants | ✅ multi-day campaign | ✅ launch day + 1 follow-up | ✅ single post |

Use this as a default; adjust based on the brief's specifics. If you
deviate, say why.

## Anti-patterns to call out

- **"Everything is Tier 1."** If a user insists their small feature
  release is Tier 1, push back. Misclassification at the top burns
  political capital and exec attention.
- **"It's Tier 3, just write something fast."** If the brief shows
  meaningful revenue or competitive stakes, name the mismatch — they
  may be under-investing in a launch that deserves more.
- **No proof points + Tier 1 ambition.** A Tier 1 launch without
  customer proof is fragile. Flag this; recommend collecting at least
  one design-partner case study before launch.
