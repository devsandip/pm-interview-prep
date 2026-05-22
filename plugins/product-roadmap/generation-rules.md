# Product Roadmap Question Generation Rules

## Category Overview

**Category:** Product Roadmap  
**Question Format:** "Build a [2-3] year [strategy/roadmap] for [Product] [optional: specific goal]"  
**Time Limit:** 25 minutes  
**Recommended Framework:** MATRIX Framework

---

## What This Category Tests

### Core Skills Being Evaluated:
- **Strategic thinking**: Can you think multi-year? Do you see themes, not just features?
- **Sequencing logic**: Can you explain why Year 1 → 2 → 3 in that order? What unlocks what?
- **Prioritization**: Can you choose what NOT to do? Can you defend your choices?
- **Execution depth**: Can you go from strategy (high-level) to tactics (Year 1 details)?
- **Business acumen**: Do you tie products to revenue/metrics? Do you understand the business model?

### What Interviewers Listen For:
- Do you start with the business problem, not just user problems?
- Can you name anchor products (not just themes like "improve commerce")?
- Do you show dependencies? ("Year 2 needs Year 1's infrastructure")
- Can you go deep on Year 1 without losing the 3-year arc?
- Do you quantify impact? ($X revenue, Y% growth)

### Common Failure Modes:
- Listing 10 products per year (no prioritization)
- No sequencing logic (could do them in any order)
- Staying too high-level ("We'll focus on AI") without concrete products
- Going deep on all 3 years equally (run out of time, no depth anywhere)
- Ignoring business model (how does this make money?)

---

## Question Generation Rules

### Selection Pools

**Consumer Apps (40% of questions):**
- Spotify, YouTube, WhatsApp, LinkedIn, Notion
- Airbnb, Uber, DoorDash, Instagram, TikTok
- Snapchat, Pinterest, Reddit, Discord, Twitch

**B2B Tools (30% of questions):**
- Slack, Zoom, Figma, Salesforce, HubSpot
- Notion, Linear, Loom, Miro, Airtable
- Asana, Monday.com, ClickUp, Coda

**Fintech (15% of questions):**
- Stripe, PayPal, Robinhood, Cash App, Revolut
- Plaid, Square, Coinbase, Chime

**Indian Companies (30% of questions - can overlap with above):**
- Swiggy, Zomato, PhonePe, Paytm, Razorpay
- Meesho, Delhivery, Dunzo, Cred, Groww
- Ola, Flipkart, Myntra, Nykaa

---

### Goal Specification

**Distribution:**
- 50% Monetization-focused
- 30% Growth-focused
- 20% Competitive/Defensive

**Monetization Goals (examples):**
- "Build a 3-year monetization strategy for [Product]"
- "How would you grow [Product] revenue to $XB over 3 years?"
- "Create a roadmap to add $XM in new revenue streams"

**Growth Goals (examples):**
- "Build a 3-year strategy to grow [Product] MAU"
- "How would you increase [Product] retention over 3 years?"
- "Create a roadmap to expand [Product] to new markets"

**Competitive Goals (examples):**
- "Build a 3-year roadmap for [Product] to compete with [Competitor]"
- "How would [Product] defend against [Competitor] threat?"
- "Create a strategy for [Product] to catch up to [Competitor]"

---

### Required Context Components

**Every question MUST include:**

1. **Current State:**
   - Revenue (if public) or scale metrics
   - User count (MAU/DAU)
   - Growth rate (YoY)
   - Current business model

2. **The Constraint:**
   - What's limiting growth?
   - Examples: ad saturation, low margins, creator churn, competition, regulatory

3. **Competitive Landscape:**
   - Who are the key competitors?
   - What are they doing well?
   - Where is the opportunity gap?

4. **Strategic Opportunity:**
   - Why now?
   - What's the unlock?
   - What's changed in the market?

---

## Question Template

```markdown
## Question [1 or 2]

**Question:**  
Build a [X]-year [strategy/roadmap] for [Product] [goal]

**Context:**  
[Product] is a [type] serving [user segment]. 

**Current state:**
- [Metric 1]: [Number] (e.g., Revenue: $2.5B, growing 15% YoY)
- [Metric 2]: [Number] (e.g., MAU: 150M, DAU: 45M)
- [Metric 3]: [Number] (e.g., Current monetization: $X per user/year)

**The constraint:**
[What's limiting growth/revenue/scale]
- [Evidence point 1]
- [Evidence point 2]

**Competitive landscape:**
- [Competitor 1]: [What they're doing well]
- [Competitor 2]: [Threat or opportunity]

**Strategic opportunity:**
[Why this matters now, what's the unlock]

**Time Limit:** 25 minutes

**Recommended Framework:** MATRIX Framework

**Framework Location:** `/plugins/product-roadmap/framework.md`
```

---

## Quality Checklist

Before finalizing each question, verify:

- [ ] Product is from the approved pool (or justified if not)
- [ ] Goal type matches distribution (50% monetization, 30% growth, 20% competitive)
- [ ] All 4 context components included (current state, constraint, competitive, opportunity)
- [ ] Numbers are realistic (check public data if available)
- [ ] Constraint is specific (not just "they need growth")
- [ ] Time limit is 25 minutes
- [ ] Framework recommendation is "MATRIX Framework"
- [ ] Framework file path is included
- [ ] Question is neither too easy nor impossibly hard

---

## Difficulty Calibration

**Medium (60% of questions):**
- Well-known product
- Clear constraint
- 1-2 obvious competitors
- Straightforward goal

**Hard (30% of questions):**
- Less common product OR
- Ambiguous constraint OR
- Multiple competing priorities OR
- Requires deep domain knowledge

**Very Hard (10% of questions):**
- Niche product AND
- Complex multi-sided marketplace OR
- Regulatory constraints OR
- Multiple goals in tension (monetization vs growth)

---

## Variety Rules

**Weekly:**
- Don't repeat the same product 2 days in a row
- Mix consumer/B2B/Indian across the week
- Vary goal types (monetization, growth, competitive)

**Daily Focus (4-day cycle, `(day_of_month - 1) % 4`):**
- Index 0 (days 1, 5, 9, 13, 17, 21, 25, 29): 70% monetization questions
- Index 1 (days 2, 6, 10, 14, 18, 22, 26, 30): 70% growth questions
- Index 2 (days 3, 7, 11, 15, 19, 23, 27, 31): 70% competitive questions
- Index 3 (days 4, 8, 12, 16, 20, 24, 28): Mixed (balanced)

---

**Module Version:** 1.0 (Plugin Architecture)  
**Last Updated:** May 2026  
**Category:** product-roadmap  
**Location:** `/plugins/product-roadmap/generation-rules.md`
