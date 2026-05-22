# MATRIX Framework for Product Roadmap Questions

## What This Framework Is

The MATRIX Framework is designed for 2-3 year product strategy questions where you need to show both portfolio thinking (breadth) and execution depth.

**MATRIX stands for:**
- **M**ap the Portfolio
- **A**nchor Sequence  
- **T**ie Dependencies
- **R**esolve Year 1 Deeply
- **I**dentify Risks
- **X**ecute (buffer for Q&A)

---

## When to Use This Framework

**Use for questions like:**
- "Build a 3-year strategy for [Product]"
- "How would you grow [Product] revenue over 3 years?"
- "Create a roadmap for [Product] to compete with [Competitor]"

**Core skill being tested:**
Can you think strategically (multi-year, portfolio view) AND tactically (Year 1 execution details)?

---

## What This Framework Tests

### Strategic Thinking
- Do you see themes, not just features?
- Can you organize opportunities across surfaces/segments?
- Do you understand the full opportunity space?

### Sequencing Logic
- Can you explain why Year 1 → 2 → 3 in that order?
- Do you show what unlocks what?
- Is your sequence defensible or arbitrary?

### Prioritization
- Can you choose what NOT to do?
- Can you defend your choices against alternatives?
- Do you pick anchor products, not just themes?

### Execution Depth
- Can you go from strategy (high-level) to tactics (Year 1 details)?
- Do you cover problem, solution, metrics, GTM?
- Do you quantify impact?

### Business Acumen
- Do you tie products to revenue/metrics?
- Do you understand the business model?
- Do you show how this makes money?

---

## The Six Steps (20-25 minutes total)

### Step 1: Map the Portfolio (2 minutes)

**What to do:**
Draw a matrix with:
- **Columns** = Product surfaces (where users interact)
- **Rows** = Strategic themes (the big bets)

Fill in 5-8 key cells with SHORT product names (not full descriptions).

**Example for Instagram Monetization:**
```
                Classic    Reels       Messages    Live
Commerce        Storefront Shoppable   AI agent    Live shopping
                Cart       tags
AI/LLM          AI content Sora clone  Chat        —
                           "Add me"    assistant
VR/AR           —          —           —           Glasses live
```

**What evaluator looks for:**
- Did they draw a matrix? (visual organization)
- Are surfaces product-specific? (not generic "mobile app")
- Are themes strategic? (not just "features")
- Did they fill 5-8 cells? (not 2, not 20)

---

### Step 2: Anchor Sequence (2 minutes)

**What to do:**
Extract a 3-year roadmap from the matrix:

```
Year 1: [Theme] 
• [Anchor product 1] ([Surface])
• [Anchor product 2] ([Surface])

Year 2: [Theme]
• [Anchor product] ([Surface])
• [Supporting products]

Year 3: [Theme]
• [Anchor product] ([Surface])
```

**State the theme AND specific products for each year.**

**Example:**
```
Year 1: Social Commerce foundation
• InstaBuy checkout (Classic)
• Shoppable tags (Reels)

Year 2: AI + Commerce scale
• Sora clone (Reels)
• AI support agent (Messages)

Year 3: Transformation
• AI shopping chatbot (Messages)
• Meta glasses live (Live)
```

**What evaluator looks for:**
- Clear Year 1, 2, 3 labels
- Theme name for each year
- Specific anchor products (not vague "improve commerce")
- Surface specified for each product

---

### Step 3: Tie Dependencies (2 minutes)

**What to do:**
Explain why this sequence. For each Year 2/3 product, state what it needs from prior years.

**Structure:**
```
"Why this sequence?

Year 2 requires Year 1's [infrastructure/data/scale].
[Specific example of dependency]

Year 3 requires Years 1-2's [specific thing].
[Specific example of dependency]

Could we reverse it? No, because [reason]."
```

**Example:**
```
"Why this sequence?

Year 2 needs Year 1's payment infrastructure. The AI support agent can't help with order issues if we're not processing orders yet. Order tracking needs checkout built first.

Year 3 needs Years 1-2's purchase data. The AI shopping chatbot needs transaction history to make recommendations—can't cold-start without knowing what users buy.

Could we reverse it? No. Can't do Messages commerce before Classic commerce (no infrastructure). Can't do AI shopping before we have purchase data."
```

**What evaluator looks for:**
- Explicit dependency statements ("Year 2 needs Year 1's X")
- Concrete examples (not just "they're related")
- Reversibility test ("Could we do Year 2 first? No, because...")
- Infrastructure, data, or scale dependencies mentioned

---

### Step 4: Resolve Year 1 Deeply (10 minutes)

**What to do:**
Pick ONE anchor product from Year 1 and go deep:

1. **Problem** (90 sec): Who has it? What's the pain? How big?
2. **Solution** (3 min): What is it? Why this approach? Key features
3. **Why Us** (90 sec): What's our unique advantage?
4. **Business Model** (60 sec): How do we make money? Unit economics
5. **Metrics** (60 sec): North Star, input metrics, guardrails
6. **GTM** (90 sec): Launch plan, timeline, phases

**Example (abbreviated):**
```
Problem: 800M Instagram shoppers browse but 70% leave when they hit "View on website." We influence $100B in purchases but capture <5% of transaction value.

Solution: InstaBuy is native checkout. Shopping cart holds items from multiple sellers, one-tap payment, order tracking in-app. Why this vs better affiliate links? We need first-party transaction data to fix Apple ATT damage.

Why Instagram: We have creator trust (users believe recommendations), social graph (friend social proof), engagement (53 min/day). Just need to close the loop.

Business Model: 5% take rate on GMV. At $5B Year 1 GMV, that's $250M direct. Plus retargeting ads for purchasers = $500M. Total: $750M.

Metrics: North Star = Monthly shoppers who complete purchase in-app (target 50M). Inputs = Checkout conversion (8%), repeat purchase (15%). Guardrails = Merchant NPS, shipping time.

GTM: Q1-Q2 beta with 1K DTC brands, zero take rate. Q3 expand to 10K, introduce 5% fee. Q4 open to all verified sellers, launch retargeting.
```

**What evaluator looks for:**
- All 6 sections covered (problem, solution, why us, business model, metrics, GTM)
- Quantified (numbers for TAM, revenue, conversion, etc.)
- Specific (not "users want this" but "800M users, 70% drop-off")
- Business model explicit (how we make money)
- GTM has phases (not just "we'd launch it")

---

### Step 5: Identify Risks (2 minutes)

**What to do:**
Name top 3 risks with likelihood and mitigation:

```
Risk 1: [What could go wrong]
Likelihood: [High/Medium/Low]
Mitigation: [How we de-risk]

Risk 2: [What could go wrong]
Likelihood: [High/Medium/Low]
Mitigation: [How we de-risk]

Risk 3: [What could go wrong]
Likelihood: [High/Medium/Low]
Mitigation: [How we de-risk]

Alternative considered: [What else did you think about?] Chose [your approach] because [reason].
```

**Example:**
```
Risk 1: Merchant adoption. Brands don't want 5% take rate when Shopify charges 2-3%.
Likelihood: High
Mitigation: Zero take rate for first 10K merchants (Year 1 only) to prove 30%+ conversion lift justifies 5%.

Risk 2: Fulfillment failures. Orders lost, late delivery—customers blame Instagram.
Likelihood: Medium
Mitigation: Partner with Shopify/Shippo. Instagram handles payments only in Year 1.

Risk 3: Regulatory (antitrust). FTC says we're anti-competitive.
Likelihood: Medium
Mitigation: Checkout is opt-in. No ranking penalty for external checkout brands.

Alternative: Shoppable Reels ads (easier, faster revenue). Chose InstaBuy because it's foundational—unlocks creator commerce and AI shopping later. Reels ads are incremental, can run in parallel.
```

**What evaluator looks for:**
- 3 risks named (not 1, not 5)
- Likelihood stated
- Mitigation specific (not "we'd monitor it")
- Alternative mentioned (shows considered trade-offs)

---

### Step 6: eXecute (Buffer, 2-3 minutes)

**What this is:**
Time left for Q&A, probing, follow-ups.

**Candidate should be ready for:**
- "Why not [Surface] you didn't cover?"
- "Why not Year 2 before Year 1?"
- "What if Year 1 fails?"
- "Can you go deeper on Year 2?"

---

## Evaluation Rubric (Total: 10 points)

### Component 1: Map Portfolio (2 points)

**2 points (Excellent):**
- Drew a clear matrix (themes × surfaces)
- 5-8 cells filled with specific products
- Themes are strategic (not just feature buckets)
- Surfaces are product-specific (not generic)

**1 point (Partial):**
- Matrix drawn but incomplete (only 2-3 cells)
- OR themes are too vague ("growth", "AI")
- OR didn't organize as matrix (just listed products)

**0 points (Missing):**
- No matrix
- Just listed 10 random products without organization

---

### Component 2: Anchor Sequence (2 points)

**2 points (Excellent):**
- Clear Year 1, 2, 3 stated
- Each year has a theme name
- Each year has 1-2 specific anchor products
- Surface specified for each product

**1 point (Partial):**
- Years stated but vague ("focus on commerce")
- OR no anchor products (just themes)
- OR no surfaces specified

**0 points (Missing):**
- No temporal sequence
- All products in one bucket

---

### Component 3: Tie Dependencies (2 points)

**2 points (Excellent):**
- Explicit "Year X needs Year Y's [specific thing]"
- Concrete examples given
- Reversibility test performed ("Could we do Year 2 first? No because...")
- Infrastructure, data, or scale dependencies mentioned

**1 point (Partial):**
- Mentioned dependencies but vague ("they're related")
- OR didn't test reversibility
- OR only 1 dependency shown

**0 points (Missing):**
- No dependency logic
- Sequence appears arbitrary

---

### Component 4: Resolve Year 1 Deeply (3 points)

**3 points (Excellent):**
- All 6 sections covered (problem, solution, why us, business model, metrics, GTM)
- Quantified (numbers for TAM, revenue, users, etc.)
- Business model explicit (how we make money)
- GTM has phases (beta, scale, full launch)

**2 points (Good):**
- 4-5 sections covered
- Some quantification
- Business model mentioned but not detailed

**1 point (Partial):**
- 2-3 sections only
- Mostly qualitative (no numbers)
- Skipped business model or GTM

**0 points (Missing):**
- Stayed high-level on Year 1 (no depth)
- No business model mentioned

---

### Component 5: Identify Risks (1 point)

**1 point (Excellent):**
- 3 risks named
- Likelihood stated
- Mitigation specific
- Alternative mentioned

**0.5 points (Partial):**
- 1-2 risks only
- OR no mitigations
- OR no alternatives mentioned

**0 points (Missing):**
- No risks discussed
- Just said "it could fail"

---

## Scoring Interpretation

**9-10 points:** Excellent. Hire.
- Strategic thinking AND execution depth
- Clear sequencing with dependencies
- Business model explicit
- Ready for senior PM role

**7-8 points:** Strong. Likely hire.
- Good strategic thinking
- Minor gaps (e.g., weak on dependencies or risks)
- With coaching, would be excellent

**5-6 points:** Decent. Mixed signals.
- Either strong strategy but weak execution, OR vice versa
- Missing business model or sequencing logic
- Needs more practice

**3-4 points:** Weak. Likely no hire.
- Stayed too high-level throughout
- No clear prioritization
- Missing major components

**0-2 points:** Poor. No hire.
- Incomplete answer
- No structure
- Fundamental gaps

---

## Common Failure Modes to Watch For

### Failure Mode 1: No Portfolio Thinking
Lists products but doesn't organize them. No themes, no surfaces, just "here are 10 things we could do."

**Feedback:** "You listed many products but didn't show how they fit together. Next time, draw a themes × surfaces matrix to organize the opportunity space."

---

### Failure Mode 2: Arbitrary Sequence
Says Year 1/2/3 but could be in any order. No dependency logic.

**Feedback:** "Your sequence isn't defensible. I could reverse Year 1 and 2 without breaking anything. Next time, explain what Year 2 needs from Year 1 (infrastructure, data, scale)."

---

### Failure Mode 3: Equal Time on All Years
Spends 5 minutes each on Years 1, 2, 3. Everything is surface-level.

**Feedback:** "You covered all 3 years but never went deep. Interviewers want to see if you can execute. Next time: 10 minutes on Year 1 depth, 2 minutes each on Years 2-3."

---

### Failure Mode 4: No Business Model
Describes great products but never says how they make money.

**Feedback:** "I don't know how Instagram makes money from this. Next time, explicitly state: 'We make money by [transaction fee/ads/subscription], which generates $X revenue at Y scale.'"

---

### Failure Mode 5: No Risks
Assumes everything will work perfectly.

**Feedback:** "Every strategy has risks. Next time, name 3: What could go wrong? How likely? How do we mitigate?"

---

## Time Management Tips

**If running out of time:**
- **Have done Matrix + Sequence (4 min)?** → Skip to Year 1 depth (10 min)
- **Have done Year 1 depth?** → Skip risks, go straight to wrap
- **Not done Year 1 depth yet?** → This is the most important part. Compress Matrix (1 min) and Sequence (1 min) to get to depth

**If ahead of schedule:**
- Add more detail to Year 2-3 (don't just leave it as 1 sentence)
- Add parallel bets ("While these are anchors, we'd also run quick wins like...")

---

## Framework Adaptation

**For competitive questions** ("Compete with X"):
Add competitive framing to Step 1:
- Map where X is strong vs where you have white space
- Sequence should directly address competitive threat in Year 1

**For growth questions** ("Grow MAU"):
Replace business model with growth model:
- How does this drive acquisition/retention/resurrection?
- What's the growth loop?

---

**Framework File Version:** 1.0  
**Last Updated:** May 2026  
**Location:** `plugins/product-roadmap/framework.md`
