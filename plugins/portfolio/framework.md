# Business Diagnosis Framework for CEO/Portfolio Questions

## What This Framework Is

The Business Diagnosis Framework is designed for open-ended CEO/portfolio questions where you need to identify THE constraint, pick ONE big bet, and defend it.

**Framework Steps:**
1. **Diagnose** the constraint
2. **Identify Themes** (2-3 strategic bets)
3. **Prioritize** ONE to focus on
4. **Build** specific products for that bet
5. **Impact** - tie to business outcomes

---

## When to Use This Framework

**Use for questions like:**
- "If you were CEO of [Company], what would you build?"
- "You're the new CPO at [Company] — what's your 100-day plan?"
- "[Company] raised $200M — how do you allocate it?"
- "[Company]'s growth has stalled — what's your strategy?"

**Core skill being tested:**
Can you diagnose a business problem (not just user problem), pick the right bet, and explain why that matters more than alternatives?

---

## What This Framework Tests

### Business Judgment
- Can you identify the biggest constraint/opportunity?
- Do you start with diagnosis before jumping to solutions?
- Do you understand the business model (how they make money)?

### Holistic Thinking
- Do you see the full portfolio, not just one product?
- Can you articulate multiple strategic options?
- Do you understand trade-offs?

### Prioritization Under Ambiguity
- When given no guardrails, can you define the problem AND solve it?
- Can you pick ONE big bet instead of trying to do everything?
- Can you defend your choice against alternatives?

### Strategic Trade-offs
- Can you explain what you're NOT doing and why?
- Do you acknowledge the downside of your choice?
- Do you show you considered alternatives?

### Exec Communication
- Can you think like a GM/CEO (not just a feature PM)?
- Do you tie to business metrics (revenue, margins, market share)?
- Do you speak in terms of business impact, not just user value?

---

## The Five Steps (18-20 minutes total)

### Step 1: Diagnose (2 minutes)

**What to do:**
Identify the core constraint. Not symptoms, but the underlying problem.

**Structure:**
```
"Let me start by diagnosing the business.

[Company] is a [business model] serving [customer segment].
Current state: [Revenue/scale/growth rate]
Business model: [How they make money]

The core constraint is: [THE constraint]

Evidence:
- [Data point 1]
- [Data point 2]
- [Data point 3]

This is different from [symptom], which is just a symptom of [root cause]."
```

**Example for Delhivery (Indian logistics):**
```
"Let me start by diagnosing the business.

Delhivery is a 3PL logistics provider serving e-commerce companies in India. Current state: $1.2B revenue, but operating at 3-5% margins vs. FedEx at 8-10%.

Business model: They charge per shipment (₹40-60/package) but costs are high due to fragmented last-mile.

The core constraint is: Unit economics. Low margins mean they can't invest in tech or expand profitably.

Evidence:
- Last-mile represents 40% of costs
- Manual route planning adds 15% inefficiency
- Tier 2/3 penetration is <20% (not profitable to serve)

This is different from 'we need more customers', which is a symptom. Root cause: can't serve customers profitably."
```

**What evaluator looks for:**
- Started with business context (not just "users want X")
- Named ONE constraint (not 5)
- Explained why this is the root cause (not just a symptom)
- Provided evidence (numbers, not just intuition)

---

### Step 2: Identify Themes (3 minutes)

**What to do:**
Brainstorm 2-3 strategic bets that could address the constraint.

**Structure:**
```
"Given this constraint, I see 3 strategic directions:

Theme 1: [Name]
- [What it is]
- [How it addresses the constraint]
- [Example product]

Theme 2: [Name]
- [What it is]
- [How it addresses the constraint]
- [Example product]

Theme 3: [Name]
- [What it is]
- [How it addresses the constraint]
- [Example product]

All 3 address the constraint, but through different mechanisms."
```

**Example:**
```
"Given this margin constraint, I see 3 strategic directions:

Theme 1: Operational Efficiency
- Use AI/automation to reduce last-mile costs
- How it helps: Cuts costs by 15-20%, improves margins
- Example: AI route optimization, automated warehouse sorting

Theme 2: Market Expansion
- Enter Tier 2/3 cities with lower cost model
- How it helps: Increases volume, spreads fixed costs
- Example: Hub-and-spoke model for smaller cities

Theme 3: Platform Play
- Open logistics API, become the 'Stripe for logistics'
- How it helps: Asset-light scale, 30%+ margins on API layer
- Example: Let small logistics players use our routing/tracking tech

All 3 improve margins, but #1 is cost reduction, #2 is scale, #3 is business model shift."
```

**What evaluator looks for:**
- 2-3 themes (not 1, not 5)
- Each addresses the constraint
- Different mechanisms (not all the same approach)
- Each has at least one example product

---

### Step 3: Prioritize (2 minutes)

**What to do:**
Pick ONE theme to focus on. Defend why this over the others.

**Structure:**
```
"I'd focus on Theme [X]: [Name]

Why this over the others?

1. [Reason 1 - usually impact or urgency]
2. [Reason 2 - usually feasibility or risk]
3. [Reason 3 - usually strategic fit]

Theme Y is attractive because [upside], but [downside/risk].
Theme Z could work long-term, but [reason it's not priority now].

Theme X is the right bet because [core argument]."
```

**Example:**
```
"I'd focus on Theme 1: Operational Efficiency.

Why this over the others?

1. **Fastest impact**: AI route optimization can deploy in 6 months, improve margins immediately
2. **Lowest risk**: We control it (vs. market expansion which depends on Tier 2/3 demand)
3. **Unlocks others**: Better margins enable us to then invest in Tier 2/3 expansion

Theme 2 (Market Expansion) is attractive because it increases scale, but we can't serve Tier 2/3 profitably at current costs. Need to fix unit economics first.

Theme 3 (Platform Play) could work long-term, but it's a 3-year bet. Need to stabilize core business before platform pivot.

Theme 1 is the right bet because margins are existential. Can't scale if every new customer loses money."
```

**What evaluator looks for:**
- Picked ONE (not "we'd do all 3")
- Explained why (impact, feasibility, strategic fit)
- Acknowledged trade-offs (what you're giving up)
- Addressed why NOT the others

---

### Step 4: Build (10 minutes)

**What to do:**
Describe 2-3 specific products/initiatives for your chosen theme. Go deep on #1.

**Structure:**
```
"For [Theme], I'd build:

Product 1: [Name]
[Go deep - 6 minutes]
- Problem
- Solution
- Why us
- Business impact
- Metrics
- Timeline

Product 2: [Name]
[Light - 2 minutes]
- What it is
- Why it matters
- How it ties to Product 1

Product 3: [Name] [optional]
[Very light - 1 minute]
```

**Example (abbreviated):**
```
"For Operational Efficiency, I'd build:

Product 1: DeliverAI Route Optimizer

Problem: Manual route planning is inefficient. Drivers make 30 stops/day vs. optimal 45. That's 15 stops x $8 margin = $120/day lost x 50K drivers = $2B/year leaked.

Solution: AI-powered route optimization. Inputs: real-time traffic, package dimensions, delivery windows. Outputs: optimal routes. Updates every 15 minutes.

Why Delhivery: We have 5 years of delivery data (30M packages/month). FedEx/DHL don't have India road network data at this granularity.

Business Impact: 15-20% improvement in stops/driver = 7-9 stops/day = $60-70/driver/day = $1.1B/year margin improvement at scale.

Metrics: Stops per driver per day (30 → 45 target). Cost per delivery (₹50 → ₹42 target).

Timeline: 6-month build, 3-month pilot with 5K drivers, 6-month rollout to all 50K.

Product 2: Automated Warehouse Sorting
[2 min of details]

Product 3: Predictive Demand Allocation
[1 min of details]"
```

**What evaluator looks for:**
- 2-3 products named
- Deep dive on Product 1 (problem, solution, impact, metrics, timeline)
- Business impact quantified ($X saved, Y% margin improvement)
- Products connect to each other (not random)

---

### Step 5: Impact (3 minutes)

**What to do:**
Tie back to the constraint and business outcomes.

**Structure:**
```
"How this solves the constraint:

[Chosen theme] addresses [constraint] by [mechanism].

Business outcomes over 18-24 months:
- [Metric 1]: [Current] → [Target] 
- [Metric 2]: [Current] → [Target]
- [Metric 3]: [Current] → [Target]

This creates a flywheel:
[Better margins] → [more investment] → [better service] → [more customers] → [scale] → [even better margins]

Why this wins:
[Strategic advantage / defensibility]"
```

**Example:**
```
"How this solves the constraint:

Operational Efficiency addresses margin pressure by reducing cost per delivery 15-20%.

Business outcomes over 18-24 months:
- Margins: 3-5% → 6-8% (competitive with global 3PLs)
- Cost per delivery: ₹50 → ₹42 (16% reduction)
- Revenue: $1.2B → $1.8B (can now compete on price for Tier 2/3)

This creates a flywheel:
Better margins → invest in tech → faster/cheaper delivery → win more enterprise contracts → more volume → better margins from scale

Why this wins:
Once we have the India road network data advantage, competitors (FedEx, Blue Dart) can't catch up without 3-5 years of local data collection."
```

**What evaluator looks for:**
- Tied back to original constraint
- Quantified business outcomes (not just "we'd do better")
- Showed flywheel/compounding effect
- Explained defensibility (why this advantage is sustainable)

---

## Evaluation Rubric (Total: 10 points)

### Component 1: Diagnose (2 points)

**2 points (Excellent):**
- Named ONE core constraint (not 5)
- Explained why this is root cause (not symptom)
- Provided evidence (numbers, data points)
- Showed business understanding (revenue, margins, business model)

**1 point (Partial):**
- Named constraint but too vague ("we need growth")
- OR listed symptoms, not root cause
- OR no evidence (just intuition)

**0 points (Missing):**
- Jumped to solutions without diagnosis
- No business context

---

### Component 2: Identify Themes (2 points)

**2 points (Excellent):**
- Named 2-3 themes
- Each addresses the constraint
- Different mechanisms (not all the same)
- Each has example products

**1 point (Partial):**
- Only 1 theme identified
- OR themes are too similar
- OR didn't explain how they address constraint

**0 points (Missing):**
- No themes, just jumped to one solution

---

### Component 3: Prioritize (2 points)

**2 points (Excellent):**
- Picked ONE theme clearly
- Explained why (impact, feasibility, strategic fit)
- Acknowledged trade-offs
- Addressed why NOT the others

**1 point (Partial):**
- Picked one but weak reasoning ("it's better")
- OR didn't address alternatives
- OR tried to do multiple things ("we'd do all 3")

**0 points (Missing):**
- No prioritization
- Everything is equal priority

---

### Component 4: Build (3 points)

**3 points (Excellent):**
- 2-3 products described
- Deep dive on Product 1 (problem, solution, impact, metrics, timeline)
- Business impact quantified
- Products connect to each other

**2 points (Good):**
- 2 products described
- Some depth but missing elements (e.g., no metrics)
- Business impact mentioned but not quantified

**1 point (Partial):**
- Only 1 product described
- OR stayed high-level (no details)

**0 points (Missing):**
- No specific products
- Just said "we'd improve X"

---

### Component 5: Impact (1 point)

**1 point (Excellent):**
- Tied back to constraint
- Quantified business outcomes
- Showed flywheel/compounding
- Explained defensibility

**0.5 points (Partial):**
- Mentioned impact but didn't quantify
- OR no flywheel shown

**0 points (Missing):**
- Didn't tie back to business outcomes

---

## Scoring Interpretation

**9-10 points:** Excellent. Strong GM/CEO thinking.
- Diagnosed correctly, picked right bet, quantified impact
- Ready for leadership role

**7-8 points:** Strong. Good business judgment.
- Minor gaps (e.g., weak on trade-offs)
- Would succeed with coaching

**5-6 points:** Decent. Some business sense.
- Either good diagnosis but weak execution, OR vice versa
- Needs practice on holistic thinking

**3-4 points:** Weak. Limited business judgment.
- Jumped to solutions without diagnosis
- OR couldn't prioritize

**0-2 points:** Poor. Not ready.
- No business context
- Feature PM, not strategic PM

---

## Common Failure Modes to Watch For

### Failure Mode 1: Jumped to Solutions
Immediately said "I'd build X" without diagnosing the business.

**Feedback:** "You jumped straight to solutions. A CEO must first understand the constraint. Next time: spend 2 minutes diagnosing the business before proposing anything."

---

### Failure Mode 2: Listed Everything
Tried to solve 5 problems at once. No focus.

**Feedback:** "You tried to do too much. CEOs must prioritize ruthlessly. Next time: pick ONE big bet and defend it."

---

### Failure Mode 3: No Business Model
Described products but never explained how they improve revenue/margins/market share.

**Feedback:** "I don't know how this improves the business. Next time: tie every product to business outcomes (margins, revenue, retention)."

---

### Failure Mode 4: Ignored Alternatives
Picked a direction but didn't explain why not the others.

**Feedback:** "You picked a direction but didn't show me you considered alternatives. Next time: name 2-3 options, then defend why this one."

---

### Failure Mode 5: Stayed Abstract
Said "we'd improve efficiency" but never got concrete.

**Feedback:** "Too high-level. CEOs need to see you can execute. Next time: name specific products with metrics and timelines."

---

## Time Management Tips

**If running out of time:**
- **Have done Diagnose + Themes (5 min)?** → Skip to Prioritize + Build (focus on Product 1 only)
- **Have done Prioritize?** → Skip Products 2-3, just do Product 1 deep
- **Not done Prioritize yet?** → This is critical. Compress Diagnose (1 min) to get to Prioritize

**If ahead of schedule:**
- Add more detail to Product 2-3
- Extend Impact section (show 3-year flywheel)

---

## Framework Adaptation

**For fundraising questions** ("You raised $200M"):
Add allocation section after Prioritize:
- $X for Product 1 (build team, deploy)
- $Y for Product 2 (pilot)
- $Z for Product 3 (R&D)

**For turnaround questions** ("Growth has stalled"):
Start with diagnosis of WHY it stalled:
- Market saturation?
- Competitive pressure?
- Product-market fit decay?

Then proceed with framework.

---

**Framework File Version:** 1.0  
**Last Updated:** May 2026  
**Location:** `plugins/portfolio/framework.md`
