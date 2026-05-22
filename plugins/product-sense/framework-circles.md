# CIRCLES Framework for Product Design Questions

## What This Framework Is

CIRCLES is Lewis Lin's framework for product design interview questions. It provides a structured approach to design or improve products by focusing on comprehension, users, problems, and solutions.

**CIRCLES stands for:**
- **C**omprehend the Situation
- **I**dentify the Customer
- **R**eport the Customer's Needs
- **C**ut Through Prioritization
- **L**ist Solutions
- **E**valuate Trade-offs
- **S**ummarize Your Recommendation

---

## When to Use This Framework

**Use for questions like:**
- "Design a product for [User Segment]"
- "How would you improve [Product]?"
- "Design [Feature] for [Company]"
- "What would you build for [Use Case]?"

**Core skill being tested:**
Can you structure ambiguous problems? Do you clarify before solving? Can you prioritize users and needs? Can you generate and evaluate multiple solutions?

---

## What This Framework Tests

### Clarification & Comprehension
- Do you ask clarifying questions before jumping to solutions?
- Do you understand the business context and constraints?
- Do you define scope appropriately?

### User-Centric Thinking
- Can you identify and segment users?
- Do you prioritize one user segment?
- Do you understand user needs deeply?

### Prioritization
- Can you choose ONE customer segment from many?
- Can you choose ONE need from many?
- Do you defend your choices with reasoning?

### Solution Design
- Can you generate multiple diverse solutions?
- Do you evaluate trade-offs systematically?
- Do you choose the best solution with clear logic?

### Business Acumen
- Do you consider feasibility, cost, and impact?
- Do you tie solutions to business goals?
- Do you show conviction in your recommendation?

---

## The Seven Steps (20 minutes total)

### Step 1: Comprehend the Situation (2 minutes)

**What to do:**
Ask clarifying questions. Define scope and constraints.

**Questions to ask:**
- "What's the goal? Are we designing from scratch or improving existing?"
- "Who is the company? What's their mission and core business?"
- "Are there technical constraints? Budget? Timeline?"
- "What does success look like for this product?"
- "Any specific user segments we should focus on?"

**Structure:**
```
"Before I dive in, let me clarify:

Goal: [Design new product OR improve existing OR add feature]
Company: [Who we're building for, their mission]
Constraints: [Technical, budget, timeline]
Success criteria: [What does winning look like]
Scope: [What's in vs out of scope]

Based on this, I'll [approach the problem as...]"
```

**Example for "Design a product for commuters":**
```
"Before I dive in, let me clarify:

Goal: Design a new product (not improve existing)
Company: Let's assume Google (mission: organize world's information)
Constraints: Mobile-first (commuters on phones), must work offline
Success criteria: Daily active usage during commute, user retention
Scope: Focus on US urban commuters (subway, bus, train), not drivers

Based on this, I'll design a mobile app for public transit commuters that helps them make the most of their commute time."
```

**What evaluator looks for:**
- Asked clarifying questions (didn't assume)
- Defined scope explicitly
- Stated constraints
- Established success criteria

**Note:** In a real interview, the interviewer will answer your questions. For practice, YOU make reasonable assumptions and state them clearly.

---

### Step 2: Identify the Customer (3 minutes)

**What to do:**
Segment users into distinct groups. Pick ONE to design for.

**Structure:**
```
"Let me segment users:

Segment 1: [Name] — [Key characteristic]
Segment 2: [Name] — [Key characteristic]  
Segment 3: [Name] — [Key characteristic]

I'll focus on [Segment X] because:
- [Size/importance]
- [Pain severity]
- [Strategic fit]
- [Underserved by current solutions]
```

**Example:**
```
"Let me segment commuters:

Segment 1: Short Commuters (15-30 min)
- Quick trips, want bite-sized content
- Often browse social media, check emails

Segment 2: Long Commuters (45-90 min)
- Substantial time, want deep engagement
- Read articles, watch videos, do work

Segment 3: Inconsistent Commuters (varies by day)
- Mix of short and long, unpredictable
- Want flexibility in content consumption

I'll focus on Long Commuters (45-90 min) because:
- Size: 35% of US public transit commuters (15M people)
- Pain: They struggle to stay productive or entertained for full duration
- Strategic fit: Google's strength is information + productivity
- Underserved: Current apps (Pocket, podcasts) solve parts but not holistically"
```

**What evaluator looks for:**
- 3 segments identified
- Segments are meaningfully different (not just demographics)
- Picked ONE with clear reasoning
- Didn't try to design for "all commuters"

---

### Step 3: Report the Customer's Needs (3 minutes)

**What to do:**
List the customer's needs, pain points, and goals. Prioritize.

**Structure:**
```
"For [Segment], here are their needs:

Need 1: [Description]
- Why: [Context]
- Pain: [Current friction]

Need 2: [Description]
- Why: [Context]
- Pain: [Current friction]

Need 3: [Description]
- Why: [Context]
- Pain: [Current friction]

Top priority: Need [X] because [reasoning]"
```

**Example:**
```
"For Long Commuters (45-90 min), here are their needs:

Need 1: Stay productive
- Why: They feel guilty "wasting" 90 min/day
- Pain: Hard to do real work on phone (small screen, distractions, no keyboard)

Need 2: Be entertained
- Why: Commute is boring, want to unwind
- Pain: Too many choices (Netflix, YouTube, podcasts) leads to decision fatigue

Need 3: Learn something new
- Why: Commute time could be "self-improvement time"
- Pain: Educational content (courses, articles) feels like work, not engaging

Need 4: Arrive informed
- Why: Need to know when to get off, if there are delays
- Pain: Current transit apps only show routes, not real-time updates with context

Top priority: Need 1 (Stay productive) because:
- Highest pain: 70% of long commuters report feeling guilty about "wasted time"
- Biggest gap: Entertainment is solved (Netflix, Spotify), productivity is not
- Google's strength: Workspace products (Docs, Sheets, Gmail) already exist
- Business value: Hooks users into Google ecosystem, increases Workspace adoption"
```

**What evaluator looks for:**
- 3-4 needs listed
- Each need has context (why it matters)
- Prioritized ONE need with reasoning
- Didn't just list features ("they need offline mode"), listed outcomes ("they need to stay productive")

---

### Step 4: Cut Through Prioritization (1 minute)

**What to do:**
Make the hard call. Pick ONE need to solve. State it clearly.

**Structure:**
```
"I'm prioritizing [Need X]: [Restate the need]

Why this over others:
- [Impact]
- [Alignment]
- [Feasibility]

I'll design a solution that helps [Segment] [achieve need]."
```

**Example:**
```
"I'm prioritizing Need 1: Help long commuters stay productive during their 45-90 minute commute.

Why this over others:
- Impact: Productivity is the #1 pain (70% report guilt about wasted time)
- Alignment: Google's core strength is productivity (Workspace)
- Feasibility: We can adapt existing products (Docs, Sheets, Gmail) for commute context

I'll design a solution that helps long commuters stay productive on small screens with intermittent connectivity."
```

**What evaluator looks for:**
- ONE need chosen (not "I'll solve needs 1, 2, and 3")
- Clear reasoning
- Stated as a problem to solve, not a solution yet

---

### Step 5: List Solutions (4 minutes)

**What to do:**
Generate 3 different solutions. Describe each. Pick one to elaborate.

**Structure:**
```
"Three solutions to help [Segment] [achieve need]:

Solution 1: [Name]
- What: [1-2 sentence description]
- How: [Key mechanism]

Solution 2: [Name]
- What: [1-2 sentence description]
- How: [Key mechanism]

Solution 3: [Name]
- What: [1-2 sentence description]
- How: [Key mechanism]

I'll go deep on Solution [X]."
```

**Example:**
```
"Three solutions to help long commuters stay productive:

Solution 1: Commute Mode for Google Workspace
- What: One-tap mode in Gmail/Docs that optimizes UI for phone + offline
- How: Bigger touch targets, voice dictation, auto-save offline, sync when back online

Solution 2: Micro-Tasks App
- What: Breaks work into 5-10 min chunks (review emails, approve docs, brainstorm ideas)
- How: AI suggests tasks based on calendar, priority, and time available

Solution 3: Commute Co-Working
- What: Live video co-working sessions for remote workers commuting to co-working spaces
- How: Match commuters on same route, video call, accountability/focus together

I'll go deep on Solution 2 (Micro-Tasks App).

**Micro-Tasks App:**

Core features:
- Smart task suggestions: AI scans Gmail, Calendar, Docs for pending work
- Time-boxed: Each task estimated at 5-15 min (fits commute context)
- Offline-first: All tasks work offline, sync when connected
- Progress tracking: Shows what you accomplished during commute

User flow:
1. Open app at start of commute
2. See suggested tasks: "Review Q3 budget" (8 min), "Reply to 5 emails" (10 min), "Brainstorm ideas for product launch" (12 min)
3. Pick a task, complete it
4. App auto-syncs when back online, marks items as done in Gmail/Docs
5. End-of-commute summary: "You completed 3 tasks, saved 30 min later"

Why this works:
- Addresses productivity guilt (see tangible progress)
- Fits commute constraints (short tasks, offline, mobile-optimized)
- Leverages Google data (knows your work from Gmail, Calendar, Drive)"
```

**What evaluator looks for:**
- 3 distinct solutions (not variations of same idea)
- Picked one to elaborate
- Went deep on chosen solution (features, flow, why it works)
- Spent ~2 minutes on the other two, ~2 minutes going deep on winner

---

### Step 6: Evaluate Trade-offs (3 minutes)

**What to do:**
Discuss pros/cons of your chosen solution. Compare to alternatives.

**Structure:**
```
"Trade-offs of Solution [X]:

Pros:
- [Benefit 1]
- [Benefit 2]
- [Benefit 3]

Cons:
- [Downside 1]
- [Downside 2]
- [Downside 3]

Comparison to alternatives:
- Solution 1: [Why not this one]
- Solution 2: [Why not this one]

Despite the cons, Solution [X] is the right choice because [conviction]."
```

**Example:**
```
"Trade-offs of Micro-Tasks App:

Pros:
- Addresses core pain (productivity guilt)
- Fits commute constraints (short tasks, offline)
- Leverages existing Google ecosystem (no new data needed)
- Low switching cost (uses existing Gmail/Docs, just adds smart layer)

Cons:
- Requires AI to accurately estimate task time (might over/under estimate)
- Only useful if user has pending work (doesn't help on weekends/vacation)
- Could add stress (commute becomes "work time" instead of "me time")

Comparison to alternatives:
- Solution 1 (Commute Mode for Workspace): Better long-term, but requires redesigning Gmail/Docs UI for mobile—big engineering lift, 12-18 month timeline. Micro-Tasks is faster (6 months).
- Solution 3 (Commute Co-Working): Novel but niche. Only works for remote workers commuting to co-working spaces (~10% of commuters). Micro-Tasks works for anyone with knowledge work.

Despite the cons, Micro-Tasks is the right choice because:
1. Fastest to ship (6 months vs 12-18 for Commute Mode)
2. Broadest applicability (anyone with Gmail/Calendar)
3. Lowest risk (if AI messes up, users just ignore suggestions—no harm done)"
```

**What evaluator looks for:**
- Listed 3 pros and 3 cons
- Compared to alternatives (not in vacuum)
- Acknowledged cons honestly (not just cheerleading)
- Defended choice despite cons

---

### Step 7: Summarize Your Recommendation (2 minutes)

**What to do:**
Recap the full logic. State metrics. Show conviction.

**Structure:**
```
"Summary:

Problem: [Segment] struggles with [Need]
Solution: [Your chosen solution]
Why: [Key reasons this is the right bet]

Success metrics:
- North Star: [Primary metric]
- Input metrics: [2-3 drivers]
- Target: [Specific goal]

Risks:
- [Biggest risk]
- Mitigation: [How we de-risk]

This is the right product to build because [conviction statement]."
```

**Example:**
```
"Summary:

Problem: Long commuters (45-90 min, 15M in US) feel guilty about "wasted" commute time and want to stay productive.

Solution: Micro-Tasks App breaks work into 5-15 min chunks, suggests tasks from Gmail/Calendar, works offline, syncs when back online.

Why: 
- Addresses #1 pain (productivity guilt)
- Fast to build (6 months, leverages existing Google data)
- Low risk (if AI fails, users ignore—no harm)
- Strategic: Hooks users into Google Workspace ecosystem

Success metrics:
- North Star: Weekly active commuters completing 2+ tasks
- Input metrics: Task completion rate (60% target), time saved per commute (20 min target)
- Target: 1M active users in first year (7% of long commuters)

Risks:
- AI estimates task time wrong → users lose trust
- Mitigation: Start with simple tasks (email triage, doc reviews), improve AI over time

This is the right product because commute time is the largest untapped "found time" for knowledge workers—2 hours/day they already have but aren't using well. Google can uniquely solve this by connecting Gmail, Calendar, and Docs in a mobile-first, offline-first experience. No competitor has this data or ecosystem advantage."
```

**What evaluator looks for:**
- Concise summary of full logic (problem → solution → why)
- Metrics defined (North Star + inputs)
- Risk acknowledged + mitigation
- Showed conviction (not hedging)

---

## Evaluation Rubric (Total: 10 points)

### Component 1: Comprehend (1 point)

**1 point (Excellent):**
- Asked clarifying questions (or stated assumptions)
- Defined scope explicitly
- Stated constraints
- Established success criteria

**0.5 points (Partial):**
- Some clarification but incomplete

**0 points (Missing):**
- Jumped to solution without clarifying

---

### Component 2: Identify Customer (2 points)

**2 points (Excellent):**
- 3 segments identified
- Segments are meaningfully different
- Picked ONE with clear reasoning
- Stated why not the others

**1 point (Partial):**
- Segments identified but picked weakly OR
- Only 2 segments

**0 points (Missing):**
- No segmentation
- Tried to design for "all users"

---

### Component 3: Report Needs (2 points)

**2 points (Excellent):**
- 3-4 needs listed with context
- Each need has "why" and "pain"
- Prioritized ONE need with reasoning

**1 point (Partial):**
- Needs listed but no prioritization OR
- Needs are features, not outcomes

**0 points (Missing):**
- No needs identified
- Jumped to solutions

---

### Component 4: Cut (1 point)

**1 point (Excellent):**
- ONE need chosen clearly
- Reasoning stated (impact, alignment, feasibility)

**0.5 points (Partial):**
- Chose one but weak reasoning

**0 points (Missing):**
- Didn't prioritize (tried to solve multiple needs)

---

### Component 5: List Solutions (2 points)

**2 points (Excellent):**
- 3 distinct solutions
- Picked one to elaborate
- Went deep (features, flow, why it works)

**1 point (Partial):**
- 2-3 solutions but similar (not diverse) OR
- Picked one but stayed shallow

**0 points (Missing):**
- Only 1 solution
- No elaboration

---

### Component 6: Evaluate Trade-offs (1 point)

**1 point (Excellent):**
- 3 pros, 3 cons listed
- Compared to alternatives
- Defended choice despite cons

**0.5 points (Partial):**
- Pros/cons listed but no comparison OR
- Only listed pros (no cons)

**0 points (Missing):**
- No trade-offs discussed

---

### Component 7: Summarize (1 point)

**1 point (Excellent):**
- Concise summary of logic
- Metrics defined (North Star + inputs)
- Risk + mitigation
- Showed conviction

**0.5 points (Partial):**
- Summary present but missing metrics OR risk

**0 points (Missing):**
- No summary
- Just said "so we should build this"

---

## Scoring Interpretation

**9-10 points:** Excellent. Hire strong.
- Structured thinking, user-centric, prioritization strong, business sense evident

**7-8 points:** Strong. Likely hire.
- Good product sense, minor gaps

**5-6 points:** Decent. Mixed signals.
- Some good elements but missing key components

**3-4 points:** Weak. Likely no hire.
- Skipped segmentation or prioritization
- Shallow solutions

**0-2 points:** Poor. No hire.
- No structure, jumped to solution

---

## Time Management Tips

**Total time: 20 minutes**

- **Comprehend**: 2 min
- **Identify**: 3 min
- **Report**: 3 min
- **Cut**: 1 min
- **List**: 4 min (2 min for all 3 solutions, 2 min deep dive on winner)
- **Evaluate**: 3 min
- **Summarize**: 2 min
- **Buffer**: 2 min

**If running out of time:**
- Compress Report (2 min instead of 3)
- Compress Evaluate (2 min instead of 3)
- Keep List and Summarize (these are most critical)

---

## CIRCLES vs MILEJPSR: When to Use Each

### **Use CIRCLES when:**
- Question is more ambiguous ("design a product for X")
- Need to clarify scope heavily
- 20-minute time constraint
- Interviewer expects Lewis Lin's framework

### **Use MILEJPSR when:**
- Question has clear business context already
- Need to show strategic thinking (Mission, Industry)
- 25-minute time available
- Want to show prioritization frameworks (SFARU, SCARU, EAC)

### **Key Differences:**

| Aspect | CIRCLES | MILEJPSR |
|--------|---------|----------|
| **Focus** | Clarity → Users → Solutions | Strategy → Users → Prioritization → Solutions |
| **Time** | 20 min | 25 min |
| **Prioritization** | Simpler (pick one) | Deeper (SFARU, SCARU, EAC frameworks) |
| **Strategic Context** | Light (Comprehend) | Heavy (Mission, Industry) |
| **Best For** | "Design a product" | "Build for [Company]" |

---

## Common Failure Modes

### Failure Mode 1: Skipped Comprehend
Jumped to solution without clarifying.

**Feedback:** "You assumed too much. Always clarify: goal, company, constraints, success criteria."

---

### Failure Mode 2: No Customer Segmentation
Designed for "all commuters" instead of picking one.

**Feedback:** "Can't design for everyone. Segment users, pick ONE, design specifically for them."

---

### Failure Mode 3: Listed Features, Not Needs
Said "they need offline mode" instead of "they need to stay productive."

**Feedback:** "Needs are outcomes (stay productive), features are solutions (offline mode). Always separate needs from solutions."

---

### Failure Mode 4: Only One Solution
Generated one solution, didn't consider alternatives.

**Feedback:** "One solution shows lack of creativity. Generate 3, pick the best one."

---

### Failure Mode 5: No Trade-offs
Only listed pros, ignored cons.

**Feedback:** "Every solution has trade-offs. Be honest about cons, then defend why it's still the right choice."

---

### Failure Mode 6: Weak Summary
Just said "so we should build this" without recap.

**Feedback:** "Summary should tie everything together: problem → solution → metrics → conviction."

---

**Framework File Version:** 1.0  
**Based on:** Lewis Lin's CIRCLES Method  
**Last Updated:** May 2026  
**Location:** `plugins/product-sense/framework-circles.md`
