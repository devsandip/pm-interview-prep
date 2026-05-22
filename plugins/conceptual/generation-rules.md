# Conceptual Question Generator Module

## Category Overview

**Category:** Conceptual (Type D)  
**Question Format:** "What's the difference between [Concept A] and [Concept B]?" OR "Explain [Concept]"  
**Time Limit:** 5 minutes  
**Recommended Framework:** Definition-Example Framework

---

## What This Category Tests

### Core Skills Being Evaluated:
- **Conceptual clarity**: Do you understand core PM concepts deeply?
- **Communication**: Can you explain complex ideas simply?
- **Practical application**: Can you give concrete examples, not just definitions?
- **Structured thinking**: Can you break down the distinction systematically?

### What Interviewers Listen For:
- Do you define both terms clearly before comparing?
- Can you articulate the key distinction (not just say they're "different")?
- Do you give a concrete example that illustrates the difference?
- Can you explain when to use one vs. the other?

### Common Failure Modes:
- Definitions are too abstract (textbook definitions without understanding)
- No clear distinction (they're "kind of similar but different")
- No examples (all theory, no application)
- Over-complicating (using jargon to hide lack of understanding)

---

## Question Generation Rules

### Concept Pairs Selection Pool

**Strategic Concepts (25% of questions):**
- Strategy vs. Roadmap vs. Vision
- Mission vs. Vision vs. Values
- Objectives vs. Key Results (in OKRs)
- Goals vs. Metrics vs. KPIs
- Strategic Planning vs. Tactical Execution
- Product Strategy vs. Go-to-Market Strategy

**Product Metrics (25% of questions):**
- North Star Metric vs. OKRs vs. KPIs
- Leading Indicators vs. Lagging Indicators
- Vanity Metrics vs. Actionable Metrics
- Engagement vs. Retention vs. Growth
- Active Users vs. Registered Users vs. Power Users
- Conversion Rate vs. Activation Rate vs. Adoption Rate

**Product-Market Fit (15% of questions):**
- Product-Market Fit vs. Product-Channel Fit
- Market Pull vs. Product Push
- Early Adopters vs. Early Majority
- TAM vs. SAM vs. SOM
- Horizontal Market vs. Vertical Market
- Niche vs. Mass Market

**Business Models (20% of questions):**
- Platform vs. Marketplace vs. Network
- B2B vs. B2B2C vs. B2C vs. B2B2B
- Freemium vs. Free Trial vs. Paymium
- Horizontal SaaS vs. Vertical SaaS
- Subscription vs. Usage-Based vs. Transaction-Based
- GMV vs. Revenue vs. Take Rate

**Product Development (15% of questions):**
- MVP vs. MLP vs. MMP
- Feature vs. Product vs. Platform
- 0→1 vs. 1→10 vs. 10→100
- Discovery vs. Delivery vs. Optimization
- Waterfall vs. Agile vs. Lean
- Product-Led Growth vs. Sales-Led Growth

---

### Explanatory Questions (Not Comparisons)

**For single-concept questions** (20% of Type D questions should be explanatory, not comparative):

**Common "Explain" Topics:**
- "Explain network effects"
- "What makes a good North Star metric?"
- "How do you know you've achieved product-market fit?"
- "Explain the difference between user research and user testing"
- "What is a two-sided marketplace?"
- "Explain the concept of technical debt"
- "What are switching costs and why do they matter?"
- "Explain the jobs-to-be-done framework"

---

### Required Components

**Every comparison question MUST:**
1. State both terms clearly
2. Both terms should be commonly used in PM
3. There should be a meaningful distinction (not synonyms)
4. Should be answerable in 3-5 minutes
5. Lend itself to concrete examples

**Every explanatory question MUST:**
1. Be a core PM concept
2. Have practical application
3. Be explainable with examples
4. Be answerable in 3-5 minutes

---

## Question Template

### For Comparison Questions

```markdown
## Question [1 or 2]

**Question:**  
What's the difference between [Concept A] and [Concept B]?

**Follow-up (optional):**  
[Additional clarification or application question]

**Time Limit:** 5 minutes

**Recommended Structure:**
1. **Define Each Term** (60 sec): What is A? What is B?
2. **State the Key Distinction** (60 sec): What's the core difference?
3. **Give an Example** (90 sec): Concrete example from a real product
4. **When to Use Each** (60 sec): In what situations would you use A vs. B?

**Framework Location:** `plugins/conceptual/framework.md`
```

### For Explanatory Questions

```markdown
## Question [1 or 2]

**Question:**  
Explain [Concept]

**Follow-up (optional):**  
[Give an example from a product you know well]

**Time Limit:** 5 minutes

**Recommended Structure:**
1. **Define** (60 sec): What it is
2. **Why It Matters** (60 sec): Why this concept exists
3. **Example** (90 sec): Concrete illustration
4. **When to Use** (60 sec): Practical application

**Framework Location:** `plugins/conceptual/framework.md`
```

---

## Example Questions

### Example 1: Strategy vs. Roadmap (Comparison)

**Question:**  
What's the difference between a product strategy and a product roadmap?

**Follow-up:**  
Give an example of each for a product you know well.

**Time Limit:** 5 minutes

**Recommended Structure:**
1. Define each term
2. State the key distinction (WHAT/WHY vs. WHEN/HOW)
3. Give an example (e.g., Instagram Commerce)
4. Explain when to use each

**Framework Location:** `plugins/conceptual/framework.md`

---

### Example 2: Network Effects (Explanatory)

**Question:**  
Explain network effects and why they matter for product strategy.

**Follow-up:**  
Give an example of a product with strong network effects and one without.

**Time Limit:** 5 minutes

**Recommended Structure:**
1. Define network effects (product becomes more valuable as more people use it)
2. Why it matters (creates defensibility, hard to replicate)
3. Example (LinkedIn vs. Netflix)
4. When to design for it (social, marketplace, platform products)

**Framework Location:** `plugins/conceptual/framework.md`

---

### Example 3: Leading vs. Lagging Indicators (Comparison)

**Question:**  
What's the difference between leading indicators and lagging indicators?

**Follow-up:**  
For a subscription product, give examples of each.

**Time Limit:** 5 minutes

**Recommended Structure:**
1. Define each:
   - Leading: Predicts future outcome
   - Lagging: Measures past outcome
2. Key distinction: Leading is predictive, lagging is retrospective
3. Example: Spotify
   - Leading: Weekly listening sessions, playlist saves
   - Lagging: Monthly revenue, annual churn rate
4. When to use: Leading for early detection, lagging for performance reporting

**Framework Location:** `plugins/conceptual/framework.md`

---

### Example 4: Product-Market Fit (Explanatory)

**Question:**  
How do you know when you've achieved product-market fit?

**Follow-up:**  
What are the signs, and what should you do differently before vs. after PMF?

**Time Limit:** 5 minutes

**Recommended Structure:**
1. Define PMF (product solves a real problem for a real market)
2. Signs:
   - Organic growth
   - High retention
   - Users would be "very disappointed" if product disappeared
   - Word-of-mouth spreading
3. Example: Slack had 30% week-over-week growth pre-launch from referrals
4. Before PMF: Focus on learning, rapid iteration. After PMF: Focus on scaling, optimization

**Framework Location:** `plugins/conceptual/framework.md`

---

### Example 5: 0→1 vs. 1→10 (Comparison)

**Question:**  
What's the difference between 0→1 product work and 1→10 product work?

**Follow-up:**  
What skills are most important for each?

**Time Limit:** 5 minutes

**Recommended Structure:**
1. Define each:
   - 0→1: Creating something new (searching for PMF)
   - 1→10: Scaling something proven (optimizing for growth)
2. Key distinction: 0→1 is high uncertainty, 1→10 is execution
3. Example:
   - 0→1: Instagram Threads (testing if text-based social works)
   - 1→10: Instagram Reels (scaling a proven format)
4. Skills:
   - 0→1: Comfort with ambiguity, user research, rapid experimentation
   - 1→10: Execution, analytics, operational excellence

**Framework Location:** `plugins/conceptual/framework.md`

---

## Concept Distinction Reference

To help generate quality questions, here are the key distinctions for common concept pairs:

| Concept A | Concept B | Key Distinction |
|-----------|-----------|-----------------|
| Strategy | Roadmap | WHAT/WHY (stable) vs. WHEN/HOW (flexible) |
| Mission | Vision | Purpose (why we exist) vs. Destination (what success looks like) |
| North Star | OKR | THE metric (customer value) vs. Quarterly goals (drive the metric) |
| PMF | Product-Channel Fit | Product solves problem vs. Found right distribution |
| Platform | Marketplace | Enables others to build vs. Matches buyers/sellers |
| Leading | Lagging | Predicts future vs. Measures past |
| B2B | B2B2C | Sell to businesses (they use it) vs. Sell to businesses (they distribute) |
| MVP | MLP | Minimum Viable (test if it works) vs. Minimum Lovable (test if they love it) |
| 0→1 | 1→10 | Create something new vs. Scale something proven |
| Horizontal | Vertical | Serves many industries vs. Serves one industry deeply |

---

## Quality Checklist

Before finalizing each question, verify:

- [ ] Both terms (if comparison) are commonly used in PM
- [ ] Terms are not synonyms (there's a real distinction)
- [ ] Answerable in 5 minutes
- [ ] Lends itself to concrete examples
- [ ] Not too obscure (should be familiar to senior PMs)
- [ ] Has practical application (not just academic)
- [ ] Time limit is 5 minutes
- [ ] Framework recommendation is "Definition-Example Framework"
- [ ] Framework file path is included

---

## Difficulty Calibration

**Medium (70% of questions):**
- Common concept pairs
- Clear distinction
- Easy to find examples

**Hard (25% of questions):**
- Subtle distinctions OR
- Requires deeper PM knowledge OR
- Multiple valid interpretations

**Very Hard (5% of questions):**
- Rarely discussed concepts OR
- Academic/theoretical distinctions OR
- Requires specific domain expertise

---

## Variety Rules

**Weekly:**
- Don't repeat the same concept pair within 2 weeks
- Mix concept categories (strategic, metrics, PMF, business models, development)
- Include 1-2 explanatory questions per week (not just comparisons)

**Distribution:**
- 25% Strategic concepts
- 25% Product metrics
- 20% Business models
- 15% Product-Market Fit
- 15% Product development

---

## Common Misconceptions to Address

**When generating questions, consider including these common misconceptions in the context:**

- "Strategy and roadmap are the same thing" → NO (WHAT/WHY vs. WHEN/HOW)
- "North Star and OKR are interchangeable" → NO (North Star is THE metric, OKRs drive it)
- "MVP means half-baked product" → NO (it's the minimum to TEST, not minimum to ship)
- "Product-market fit is a one-time milestone" → NO (it's a continuous state you maintain)
- "Platform and marketplace are the same" → NO (enable building vs. match supply/demand)
- "All metrics are KPIs" → NO (KPIs are key indicators of business health, not all metrics qualify)
- "Freemium and free trial are the same" → NO (permanent free tier vs. time-limited full access)

---

**Module Version:** 1.0  
**Last Updated:** May 2026  
