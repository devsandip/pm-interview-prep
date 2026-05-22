# Trade-off Question Generation Rules

## Category Overview

**Category:** Trade-offs  
**Question Format:** "Should we prioritize [X] or [Y]?" OR "Trade-off between [A] and [B]"  
**Time Limit:** 15-20 minutes  
**Recommended Framework:** T.R.A.D.E Framework

---

## What This Category Tests

### Core Skills Being Evaluated:
- **Multi-dimensional thinking**: Do you evaluate multiple factors, not just one?
- **Quantitative analysis**: Can you put numbers on trade-offs?
- **Decision-making**: Can you make clear recommendations under uncertainty?
- **Strategic thinking**: Do you connect to business strategy and competitive dynamics?
- **Experimental mindset**: Do you design tests to validate decisions?

### What Interviewers Listen For:
- Do you frame the type of trade-off?
- Do you quantify both sides with metrics?
- Do you analyze multiple dimensions (reversibility, time horizon, user impact)?
- Do you make a clear recommendation with rationale?
- Do you design experiments to validate?

### Common Failure Modes:
- Picked a side immediately without analysis
- No quantification (vague "better for users")
- One-dimensional analysis (only revenue OR only users)
- No clear recommendation ("it depends")
- Ignored alternatives (binary thinking)
- No experiment plan

---

## Question Generation Rules

### Trade-off Type Selection Pool

**Short vs Long Term (30%):**
- Revenue now vs user growth later
- Quick win vs sustainable solution
- Short-term engagement vs long-term retention

**User Segments (25%):**
- Power users vs casual users
- New users vs existing users
- Paying users vs free users
- Creators vs consumers

**Stakeholders (20%):**
- Users vs advertisers
- Users vs creators
- Shareholders vs customers
- Platform vs ecosystem partners

**Product Attributes (15%):**
- Feature richness vs performance
- Quality vs quantity
- Simplicity vs power
- Speed vs accuracy

**Business Objectives (10%):**
- Growth vs monetization
- Engagement vs privacy
- Innovation vs stability

---

### Product/Feature Selection Pool

**Social Media (30%):**
- Instagram/Facebook: Feed algorithm, ad load, creator monetization
- TikTok: Content moderation, recommendation system
- LinkedIn: Content quality vs engagement
- Twitter/X: Verification, algorithm changes

**Marketplace (25%):**
- Airbnb: Host protection vs guest experience
- Uber: Driver pay vs rider prices
- Amazon: Selection vs delivery speed
- DoorDash: Restaurant commissions vs dasher pay

**Content Platforms (20%):**
- YouTube: Ad load vs watch time
- Spotify: Free tier vs premium conversion
- Netflix: Content spend vs pricing
- Twitch: Streamer revenue vs platform take rate

**B2B/SaaS (15%):**
- Slack: Features vs simplicity
- Notion: Performance vs functionality
- Salesforce: Customization vs usability
- Zoom: Quality vs accessibility

**Emerging (10%):**
- AI products: Accuracy vs speed
- Crypto: Decentralization vs user experience
- Health tech: Privacy vs personalization

---

### Required Context Components

**Every question MUST include:**

1. **The Trade-off:**
   - Option A: [What it is]
   - Option B: [What it is]
   - Why they're in tension

2. **Product Context:**
   - Product description
   - User base / scale
   - Current state / challenges

3. **Business Context:**
   - Company mission
   - Strategic priority
   - Competitive landscape
   - Product phase (growth / scaling / mature)

4. **Constraints:**
   - Time pressure (if any)
   - Resource limits (if any)
   - Technical constraints (if any)

5. **Ambiguity:**
   - Both options have merit
   - No obvious right answer
   - Depends on priorities/values

---

## Question Template

```markdown
## Question [1 or 2]

**Question:**  
Should [Company/Product] prioritize [Option A] or [Option B]?

**The Trade-off:**

**Option A: [Name]**
- What it is: [Description]
- Key benefit: [What it optimizes for]
- Key cost: [What it sacrifices]

**Option B: [Name]**
- What it is: [Description]
- Key benefit: [What it optimizes for]
- Key cost: [What it sacrifices]

**Why they're in tension:**
[Explain the fundamental conflict]

**Product Context:**
[Product] is [description]. It has [user base size] and [key metrics/state].

Current challenge: [What problem this trade-off addresses]

**Business Context:**
- Mission: [Company mission statement]
- Strategic priority: [What company cares about most right now]
- Competitive landscape: [Key competitors, what they're doing]
- Product phase: [Early growth / Scaling / Mature / Turnaround]

**Additional Context:**
[Any constraints, recent events, or relevant data]

**Your Task:**
Use the T.R.A.D.E framework to analyze the trade-off and recommend a decision.

**Time Limit:** 15-20 minutes

**Recommended Framework:** T.R.A.D.E Framework
- **T**ype of Trade-off & Context
- **R**eframe with Metrics
- **A**nalyze Dimensions
- **D**eep Dive & Decision Framework
- **E**xperiment & Evaluate

**Framework Location:** `/plugins/tradeoffs/framework.md`
```

---

## Example Question Structure

**Question:**  
Should Instagram Reels prioritize increasing ad load (for revenue) or reducing ad load (for user experience)?

**The Trade-off:**

**Option A: Increase ad load**
- What it is: Increase from 4 ads/hour → 6 ads/hour in Reels
- Key benefit: +50% ad revenue ($500M → $750M/year)
- Key cost: User session time likely drops 10-15%

**Option B: Reduce ad load**
- What it is: Decrease from 4 ads/hour → 2 ads/hour in Reels
- Key benefit: User session time likely increases 8-10%
- Key cost: Ad revenue drops 40% ($500M → $300M/year)

**Why they're in tension:**
Reels is losing Gen Z users to TikTok (which has 2-3 ads/hour). Higher ad load funds creator monetization but hurts user experience. Lower ad load improves engagement but reduces creator earnings and platform revenue.

**Product Context:**
Instagram Reels is Meta's short-form video feature competing with TikTok. 2B Instagram users, 200M create Reels monthly, Reels is 20% of Instagram time spent.

Current challenge: TikTok has 50% higher daily time spent among 18-24 year olds. Reels needs to improve engagement to win Gen Z.

**Business Context:**
- Mission: Bring the world closer together (connection > monetization)
- Strategic priority: Beat TikTok in short-form video before they dominate Gen Z completely
- Competitive landscape: TikTok has 1.5B users, 52 min/day. YouTube Shorts has 2B users, growing fast.
- Product phase: Scaling (launched 2020, now 200M creators)

**Additional Context:**
- Meta's Q2 earnings call: CFO said Reels needs to "improve monetization efficiency"
- Recent creator survey: 60% of top creators considering leaving for TikTok (better Creator Fund payouts)
- User research: Gen Z says "too many ads" is #2 reason for preferring TikTok

---

## Quality Checklist

Before finalizing each question, verify:

- [ ] Trade-off type is clear (short/long, segments, stakeholders, attributes, objectives)
- [ ] Both options have merit (not obvious choice)
- [ ] Product context is sufficient
- [ ] Business context includes mission, strategy, competitive landscape
- [ ] Question creates genuine tension (not "obviously pick X")
- [ ] Both sides are quantifiable with metrics
- [ ] Time limit is 15-20 minutes
- [ ] Framework recommendation is "T.R.A.D.E"

---

## Difficulty Calibration

**Medium (60%):**
- Two clear options
- Obvious metrics for both sides
- Clear business context
- 2-dimensional trade-off (e.g., revenue vs users)

**Hard (30%):**
- Three options (A, B, or hybrid) OR
- Multi-stakeholder (users, creators, advertisers) OR
- Unclear which metrics to use OR
- Time pressure / urgency

**Very Hard (10%):**
- Four+ stakeholders affected differently OR
- Irreversible decision OR
- Major strategic inflection point OR
- Conflicting company values

---

## Variety Rules

**Weekly:**
- Mix trade-off types (short/long, segments, stakeholders, attributes, objectives)
- Don't repeat same product 2 days in a row
- Vary industries (social, marketplace, content, B2B)
- Alternate obvious vs subtle trade-offs

**Trade-off Type Distribution:**
- 30% Short vs Long term
- 25% User Segments
- 20% Stakeholders
- 15% Product Attributes
- 10% Business Objectives

---

## Recommended Decisions (For Variety)

**Rotate these patterns:**
- Pick Option A (30%)
- Pick Option B (30%)
- Hybrid/Dynamic approach (25%)
- Experiment first, then decide (15%)

**Avoid always recommending the same pattern.**

---

**Module Version:** 1.0 (Plugin Architecture)  
**Last Updated:** May 2026  
**Category:** tradeoffs  
**Location:** `/plugins/tradeoffs/generation-rules.md`
