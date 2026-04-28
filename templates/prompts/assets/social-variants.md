# Asset — Social post variants

Launch-day social posts. Generate platform-specific variants — never one
generic post copy-pasted everywhere.

## Inputs
- Brief
- Tier (drives volume — Tier 1 gets a multi-day campaign; Tier 3 gets
  a single post)
- Messaging matrix (anchor message + tagline candidates)
- Blog post (link to drive traffic to)

## Output — generate these by tier

### Tier 1 — multi-day campaign
- LinkedIn: founder/exec post (long-form, 1500–2200 chars)
- LinkedIn: PMM post (medium, 800–1200 chars)
- LinkedIn: company page post (short, 400–600 chars)
- Twitter/X: announcement thread (5–7 tweets)
- Twitter/X: standalone tweet (single, quotable)
- 3-day follow-up plan: 1 post per day with a different angle
  (problem, customer story, behind-the-scenes)

### Tier 2 — launch day + one follow-up
- LinkedIn: PMM/founder post (medium, 800–1200 chars)
- LinkedIn: company page post (short)
- Twitter/X: announcement (single tweet or short thread)
- Day-3 follow-up: one post on customer reaction or a deeper dive

### Tier 3 — single post
- LinkedIn: short company page post (200–400 chars)
- Twitter/X: single tweet

## Output structure (per variant)

```
**Platform:** {LinkedIn / Twitter}
**Variant:** {Founder | PMM | Company | Thread}
**Length target:** {char count}

---

{Post copy — written in the voice of the variant. Hook in the first
line. Specific. Quotable. Ends on a clear CTA — usually a link to the
blog post.}

---

**CTA:** {What we want the reader to do — read blog, book demo, reply,
share}
**Hashtags (if any — use sparingly):** {#PMM, #ProductLaunch, etc.}
```

## Voice rules per platform

### LinkedIn
- Lead with a problem statement or a sharp observation, not "I'm
  excited to announce."
- Personal voice for founder/PMM variants. First-person.
- No hashtags except for community ones (e.g., #PMM, #ProductMarketing
  for visibility in those communities).
- Line breaks every 1–2 sentences for scannability on mobile.
- End on a clear CTA or question.

### Twitter/X
- First tweet is the hook — it must stand alone if the rest gets
  truncated.
- Threads: each tweet is self-contained. Reader should be able to land
  on tweet 4 and still understand.
- Avoid emoji-spam. 1–2 max per thread.
- Numbers in tweets get higher engagement than abstract claims.

## Quality criteria

- [ ] Each variant is genuinely platform-native (not LinkedIn copy
      cross-posted to Twitter)
- [ ] First line of every post passes the "would I keep reading"
      test on mobile
- [ ] No banned generic phrases
- [ ] CTA is specific (not "check it out")
- [ ] Tier-appropriate volume (don't generate 6 variants for a Tier 3
      launch)

## Common failure modes

- **One post, copy-pasted.** Defeats the purpose. Each platform has
  different attention patterns.
- **"Excited to announce."** First-line death. Open on the problem,
  the customer, the data point, or a sharp claim.
- **Hashtag soup.** #productlaunch #saas #b2b #ai #innovation = looks
  like marketing automation, not a human.
- **No CTA.** Even thought-leadership posts should have one — "What's
  your team's launch process?" is a CTA.

## Examples of strong opening lines

- "We just shipped {thing}. Here's what we learned building it." 
  (founder voice)
- "Most {audience} spend {N} weeks on {task}. Here's how to do it in
  {fraction}." (problem framing)
- "Three months ago, {customer} was {painful state}. Today: {good
  state}." (customer story)
- "{N} {audience members} ran their {task} through {product} this
  month. Top three things they did differently:" (data + curiosity)

Avoid:
- "I'm thrilled to share..."
- "Big news from the {Company} team..."
- "We are honored to announce..."
- "🚀🎉 LAUNCH DAY 🎉🚀"
