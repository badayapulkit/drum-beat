# Asset — Customer-facing launch email

Email that goes to existing customers (and optionally a separate version
for prospects). Sent from product / PMM, not marketing automation.

## Inputs
- Brief
- Tier
- Messaging matrix (audience rows for "existing customer" and "prospect"
  if both exist)

## Output structure

Generate **one email per audience row** that warrants its own send. For
most launches that's 1–2 emails (existing customers + prospects).

```
**Subject:** {6–10 words. Specific. Avoid clickbait. Aim for >25% open
rate.}

**Preheader:** {50–80 chars. Extends the subject — don't repeat it.}

---

Hi {first name},

{Opening — 1 sentence. Tie to something the recipient already cares
about. For existing customers: a workflow they already use. For
prospects: a problem they probably have.}

{Body — 3–5 short paragraphs:}

- Para 1: What's launching today, in one sentence. Link to the blog
  post for depth.
- Para 2: The most relevant value for *this* audience. Concrete,
  specific. If you wouldn't say it out loud to a customer, cut it.
- Para 3: Proof — one customer / metric, or honest beta framing if
  none yet.
- Para 4 (optional, for existing customers): What changes for them.
  Anything they need to do? Anything they should NOT worry about
  (pricing, breaking changes, account access)?
- Para 5: Single, specific CTA. Match to audience.
  - Existing customers: "Try it in your dashboard" (link to feature)
  - Prospects: "Book a 20-minute walkthrough" (link to calendar)

{Sign-off — from a real human, with their title. PMM, founder, or
product lead. Not "The {Company} Team."}

P.S. {Optional. One sentence. Use for: a soft second CTA, a personal
note, or a heads-up about an upcoming related thing.}
```

## Length
150–250 words for the body. Anything longer gets skimmed or deleted.

## Tone
- **Existing customers**: warm, operational, respectful of their time.
  They've already bought; don't sell them again.
- **Prospects**: direct, specific, confident. They need a reason to
  click; the body must earn the click in the first paragraph.

## Quality criteria

- [ ] Subject line is specific and not clickbait
- [ ] Preheader extends the subject, doesn't repeat it
- [ ] First sentence of body is *not* "I'm excited to announce"
- [ ] Single, specific CTA — not 3 links competing for attention
- [ ] Sign-off is a named human with a title
- [ ] Body could not be confused with a marketing automation send
- [ ] Length stays under 250 words

## Common failure modes

- **Bullet-heavy.** Customer emails read like emails, not landing pages.
  Prose paragraphs.
- **Multiple CTAs.** "Read the blog OR book a demo OR try it free" =
  no one does anything. Pick one.
- **Generic sign-off.** "The {Company} Team" feels lazy. Sign as a
  human.
- **Selling to existing customers.** They already pay you. Tell them
  what changes for them.

## Subject line variants — generate 3

Always offer the user 3 subject lines to A/B or pick from. Examples
of strong patterns:

- **Direct value**: "{Outcome} in {timeframe}"
  e.g., "Ship your launch in 3 days, not 3 weeks"
- **Curiosity (sparingly)**: "{Specific noun} we just shipped"
  e.g., "The launch workflow we just shipped"
- **Customer language**: "{Quote-shaped phrase}"
  e.g., "'I cut my launch prep by 60%'"

Avoid: emoji-heavy, all-caps, "Re:" or "Fwd:" fakery, "Don't open
this email" patterns.
