# CEO/Portfolio Question Generator Module

## Category Overview

**Category:** CEO/Portfolio (Type B)  
**Question Format:** "If you were [CEO/CPO] at [Company], what would you [build/prioritize/focus on]?"  
**Time Limit:** 20 minutes  
**Recommended Framework:** Business Diagnosis Framework

---

## What This Category Tests

### Core Skills Being Evaluated:
- **Business judgment**: Can you identify the biggest constraint/opportunity?
- **Holistic thinking**: Do you see the full portfolio, not just one product?
- **Prioritization under ambiguity**: When given no guardrails, can you define the problem AND solve it?
- **Strategic trade-offs**: Can you explain what you're NOT doing and why?
- **Exec communication**: Can you think and communicate like a GM/CEO?

### What Interviewers Listen For:
- Do you start with "What's the constraint?" (diagnosis before solution)
- Can you pick ONE big bet instead of trying to do everything?
- Do you explain the business context (margins, unit economics, competitive position)?
- Do you tie your answer to the company's core business model?
- Can you articulate WHY this matters more than alternatives?

### Common Failure Modes:
- Trying to solve 5 problems at once (no focus)
- Jumping to solutions without diagnosing the constraint
- Ignoring the business model (Delhivery has 3% margins → this matters!)
- Listing features without explaining the strategic impact
- Not differentiating from what the company already does

---

## Question Generation Rules

### Company Selection Pool

**High-Growth Startups (30% of questions):**
- Notion, Figma, Linear, Loom, Superhuman
- Coda, Airtable, Miro, Canva, Webflow
- Vercel, Supabase, Replit, Cal.com

**Established But Challenged (25% of questions):**
- Dropbox, Evernote, Box, SurveyMonkey
- Yelp, TripAdvisor, Eventbrite, OpenTable
- Glassdoor, Grubhub, Etsy, Shopify (specific challenges)

**Indian Companies (30% of questions):**
- Razorpay, Dunzo, Urban Company, Meesho, Delhivery
- Cred, Groww, Zerodha, Ola, Swiggy
- Nykaa, OfBusiness, Udaan, BlackBuck

**Challenger Brands (15% of questions):**
- DuckDuckGo, Brave, ProtonMail, Signal
- Bluesky, Mastodon, Substack, Beehiiv
- Arc Browser, Raycast, Warp Terminal

---

### Framing Variations

**Distribution:**
- 40% "What would you build as CEO of X?"
- 25% "You're the new CPO at X — what's your 100-day plan?"
- 20% "X raised $200M — how do you allocate it?"
- 15% Other ("X's growth stalled", "If you ran X differently")

**Variation Examples:**

**Standard CEO:**
- "What would you build if you were CEO of [Company]?"
- "If you ran [Company], what would you prioritize?"

**New Leadership:**
- "You're the new CPO at [Company] — what's your 100-day plan?"
- "You just joined [Company] as Head of Product — what's your strategy?"

**Funding Scenario:**
- "[Company] just raised $200M Series C — how would you allocate it?"
- "[Company] has $500M cash — where would you invest?"

**Turnaround:**
- "[Company]'s growth has stalled — what's your strategy?"
- "[Company] is losing market share to [Competitor] — what do you do?"

**Strategic Choice:**
- "If you ran [Company], what would you do differently than the current CEO?"
- "Should [Company] focus on [Option A] or [Option B]?"

---

### Required Context Components

**Every question MUST include:**

1. **Business Description:**
   - What they do
   - Who they serve (B2B, B2C, marketplace)
   - Business model (how they make money)

2. **Current State:**
   - Revenue (if known) or scale metrics
   - Key business metrics (margins, unit economics, retention)
   - Company stage (seed, Series B, mature, declining)

3. **The Constraint:**
   - What's holding them back?
   - Examples: low margins, high churn, competition, product-market fit issues, operational complexity

4. **Recent Context:**
   - Recent funding, leadership changes, competitive moves
   - Market shifts, regulatory changes
   - Product launches, acquisitions

5. **Resources Available:**
   - Budget (if funding scenario)
   - Team size
   - Time horizon

---

## Question Template

```markdown
## Question [1 or 2]

**Question:**  
[Framing variation with Company]

**Company Context:**

**Business:** [What they do, who they serve, business model]

**Current State:**
- Revenue/Scale: [Numbers]
- Key metrics: [Margins, unit economics, churn, etc.]
- Stage: [Seed/Growth/Mature/Declining]

**The Constraint:**
[What's limiting them - be specific]
- [Evidence 1]
- [Evidence 2]
- [Evidence 3]

**Recent Context:**
[Recent news, funding, competitive moves, market shifts]

**Resources Available:**
- [Budget if applicable]
- [Team size if known]
- [Time horizon: 100 days, 1 year, 3 years]

**Time Limit:** 20 minutes

**Recommended Framework:** Business Diagnosis Framework
1. **Diagnose** the core constraint
2. **Identify Themes** (2-3 strategic bets)
3. **Prioritize** ONE to focus on
4. **Build** specific products/initiatives
5. **Impact** - tie to business outcomes

**Framework Location:** `plugins/portfolio/framework.md`
```

---

## Example Questions

### Example 1: Standard CEO Question

**Question:**  
What would you build if you were CEO of Delhivery?

**Company Context:**

**Business:** Delhivery is India's largest 3PL (third-party logistics) provider, serving e-commerce companies with warehousing, transportation, and last-mile delivery.

**Current State:**
- Revenue: $1.2B (FY2024), growing 25% YoY
- Margins: 3-5% operating margins vs. FedEx at 8-10%
- Scale: 50K delivery personnel, 28 cities, 30M packages/month
- Business model: Per-package fee (₹40-60/package depending on weight, distance)

**The Constraint:**
Unit economics. Low margins mean they can't invest in technology or expand profitably to Tier 2/3 cities. Root causes:
- Last-mile costs represent 40% of revenue (vs. 25-30% for mature logistics)
- Manual route planning adds 15% inefficiency
- Tier 2/3 cities have <50 packages/km² density (vs. 200+ in metros)

**Recent Context:**
- Went public in May 2022, stock down 30% since IPO
- Amazon and Flipkart building in-house logistics (threatening volume)
- Raised ₹5,000 crores ($600M) pre-IPO, need to show path to profitability

**Resources Available:**
- $300M cash available for investment
- 2,000 engineers (mostly in operations, not product/tech)
- 18-month runway to demonstrate margin improvement

**Time Limit:** 20 minutes

**Recommended Framework:** Business Diagnosis Framework

**Framework Location:** `plugins/portfolio/framework.md`

---

### Example 2: New CPO Question

**Question:**  
You're the new CPO at Razorpay — what's your 100-day plan?

**Company Context:**

**Business:** Razorpay is India's leading payment gateway and neobanking platform for businesses. Services include payment processing, banking (RazorpayX), lending (Capital), and payroll.

**Current State:**
- Revenue: $300M (FY2024), growing 80% YoY
- TPV: $150B processed annually, 10M merchants
- Take rate: 2% on payments, higher on banking/lending
- Stage: Series F, $750M raised, valued at $7.5B (2023)

**The Constraint:**
Portfolio complexity. Four product lines (Payments, Banking, Capital, Payroll) with different GTM motions, customer segments, and unit economics. Product org is siloed — each product has its own PM team, little cross-sell. Customer retention suffering because products don't integrate well.

Recent churn analysis:
- Merchants using 1 product: 25% annual churn
- Merchants using 2+ products: 8% annual churn
- Cross-sell rate is only 15% (vs. 40% target)

**Recent Context:**
- Previous CPO left after 18 months (product complexity cited)
- Stripe entered India in Jan 2024 (taking SMB share)
- Paytm's regulatory issues create opportunity to grab their merchant base

**Resources Available:**
- 120 PMs across 4 product lines
- $100M budget for product development (18 months)
- CEO wants cross-sell rate to hit 30% within 12 months

**Time Limit:** 20 minutes

**Recommended Framework:** Business Diagnosis Framework

**Framework Location:** `plugins/portfolio/framework.md`

---

### Example 3: Funding Allocation Question

**Question:**  
Meesho just raised $500M — how would you allocate it across the product portfolio?

**Company Context:**

**Business:** Meesho is India's social commerce platform connecting small sellers (often women entrepreneurs) with buyers. GMV-focused model with zero commission for sellers.

**Current State:**
- Revenue: $500M (FY2024), loss-making (burning $200M/year)
- GMV: $8B, 150M users, 1.2M sellers
- Business model: Takes commission on logistics (Meesho Mall), ads (future)
- Stage: Series F, $1.5B raised total, valued at $5B

**The Constraint:**
Business model tension. Zero-commission promise attracts sellers but limits monetization. Meanwhile, Flipkart and Amazon have better discovery, faster delivery, and trust (returns/refunds). Meesho's differentiation (low prices, C2C sellers) is also its weakness (quality issues, slow delivery).

Key metrics:
- Repeat purchase rate: 30% (vs. 55% for Amazon India)
- NPS: 25 (vs. 50+ for Flipkart)
- Seller churn: 40% annual (sellers go multi-platform)

**Recent Context:**
- Just raised $500M (Jan 2026) with mandate to reach profitability in 24 months
- Flipkart launched "Shopsy" (zero-commission marketplace) in direct competition
- Regulatory pressure on social commerce (WhatsApp commerce rules tightening)

**Resources Available:**
- $500M to allocate
- 800 person product+eng team
- 24 months to profitability target

**Time Limit:** 20 minutes

**Recommended Framework:** Business Diagnosis Framework

**Framework Location:** `plugins/portfolio/framework.md`

---

## Quality Checklist

Before finalizing each question, verify:

- [ ] Company is from the approved pool (or justified if not)
- [ ] Framing variation matches distribution (40% CEO, 25% CPO, 20% funding, 15% other)
- [ ] All 5 context components included (business, state, constraint, recent, resources)
- [ ] Constraint is specific and non-obvious (not just "they need growth")
- [ ] Business model is clearly stated
- [ ] Numbers are realistic (verify with public data if available)
- [ ] Time limit is 20 minutes
- [ ] Framework recommendation is "Business Diagnosis Framework"
- [ ] Framework file path is included

---

## Difficulty Calibration

**Medium (60% of questions):**
- Well-known company
- Clear constraint
- Obvious strategic options
- Sufficient context provided

**Hard (30% of questions):**
- Less familiar company OR
- Multiple competing constraints OR
- Ambiguous trade-offs OR
- Limited public information (need to make assumptions)

**Very Hard (10% of questions):**
- Niche company AND
- Complex multi-sided business model OR
- Multiple stakeholders with conflicting interests OR
- Regulatory/cultural constraints

---

## Variety Rules

**Weekly:**
- Don't repeat the same company 2 days in a row
- Mix startup/established/Indian/challenger across the week
- Vary framing (CEO, CPO, funding, turnaround)

**Daily Focus (4-day cycle, `(day_of_month - 1) % 4`):**
- Index 0 (days 1, 5, 9, 13, 17, 21, 25, 29): Margin/profitability focus (70% questions about improving unit economics)
- Index 1 (days 2, 6, 10, 14, 18, 22, 26, 30): Growth focus (70% questions about scaling, market expansion)
- Index 2 (days 3, 7, 11, 15, 19, 23, 27, 31): Competitive focus (70% questions about competitive threats)
- Index 3 (days 4, 8, 12, 16, 20, 24, 28): Mixed (balanced)

---

**Module Version:** 1.0  
**Last Updated:** May 2026  
