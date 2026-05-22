# Capabilities Matrix Framework for Tech Application Questions

## What This Framework Is

The Capabilities Matrix Framework is designed for "How would you use [Technology] at [Company/Domain]?" questions where you need to be concrete about technology application, not just buzzwords.

**Framework Steps:**
1. **Clarify** scope (if ambiguous)
2. **Map** technology capabilities × business problems
3. **Prioritize** use cases
4. **Deep Dive** on #1 use case
5. **Rollout** plan

---

## When to Use This Framework

**Use for questions like:**
- "How would you use AI in SDLC at [Company]?"
- "How should [Company] use LLMs?"
- "What role should blockchain play in [Domain]?"
- "How would you integrate AR/VR into [Product]?"

**Core skill being tested:**
Do you understand the technology AND the domain? Can you be concrete, not just "use AI for personalization"?

---

## What This Framework Tests

### Technology Understanding
- Do you actually know how [AI/blockchain/AR] works?
- Can you explain the capabilities (not just buzzwords)?
- Do you understand limitations/constraints?

### Domain Expertise
- Do you understand the company/industry context?
- Do you know the specific pain points?
- Do you know the current tech stack?

### Concrete Thinking
- Can you go from "use AI" to specific use cases?
- Can you explain HOW the technology solves the problem?
- Do you provide technical details, not hand-waving?

### Prioritization
- Can you pick the highest-impact use case?
- Can you defend your choice?
- Do you avoid listing 10 use cases without prioritization?

### Feasibility Assessment
- Do you acknowledge constraints (data, cost, maturity)?
- Do you consider technical/operational risks?
- Do you have a realistic rollout plan?

---

## The Five Steps (18-20 minutes total)

### Step 1: Clarify (30 seconds)

**What to do:**
If the question is ambiguous, ask a clarifying question.

**Common ambiguities:**
- "SDLC" = internal software development OR delivery lifecycle?
- "Customer support" = B2B support OR consumer support?
- "AI" = LLMs, computer vision, predictive ML?

**Structure:**
```
"Quick clarification: By [ambiguous term], do you mean [interpretation A] or [interpretation B]?

I'll assume [interpretation] for this answer."
```

**Example:**
```
"Quick clarification: By 'SDLC at Delhivery', do you mean their internal software development process, or the logistics delivery lifecycle?

I'll assume internal software development for this answer."
```

**What evaluator looks for:**
- Did they catch the ambiguity?
- Did they state their assumption clearly?
- (If no ambiguity, skip this step)

---

### Step 2: Map Capabilities (3 minutes)

**What to do:**
Draw a matrix: Technology capabilities (rows) × Business problems/phases (columns).

Fill in 5-8 key cells with specific use cases.

**Structure:**
```
"Let me map [Technology] capabilities across [Domain/Phase]:

[Draw matrix]

Technology       Phase 1      Phase 2       Phase 3       Phase 4
────────────────────────────────────────────────────────────────
Capability A     Use case 1   Use case 2    —             —
Capability B     —            Use case 3    Use case 4    —
Capability C     Use case 5   Use case 6    Use case 7    —
```

**Example for "AI in SDLC":**
```
"Let me map AI capabilities across the SDLC phases:

AI Capability       Planning    Development    Testing       Deployment    Monitoring
──────────────────────────────────────────────────────────────────────────────────────
Code generation     Story gen   Autocomplete   Test gen      —             —
Analysis/Review     Estimate    Code review    Bug find      Rollback rec  —
Prediction          Velocity    Build time     Flake rate    Rollout risk  Incident
Pattern recog       Similar      Copy-paste    Regression    —             Anomaly
                    tickets      detection     detection
```

**What evaluator looks for:**
- Drew a matrix (visual organization)
- Technology capabilities are specific (not just "AI")
- Business problems/phases are domain-relevant
- 5-8 cells filled (not 2, not 20)

---

### Step 3: Prioritize Use Cases (2 minutes)

**What to do:**
From the matrix, pick top 3 use cases. Rank them. Explain why.

**Structure:**
```
"From this matrix, top 3 use cases:

#1: [Use case]
Why: [Impact] + [Feasibility]

#2: [Use case]
Why: [Impact] + [Feasibility]

#3: [Use case]
Why: [Impact] + [Feasibility]

I'd focus on #1 because [core argument]."
```

**Example:**
```
"From this matrix, top 3 use cases:

#1: AI Code Review
Why: High impact (catches 40% of bugs pre-production) + High feasibility (we have 5 years of code history to train on)

#2: Test Generation
Why: Medium-high impact (increases coverage 20-30%) + Medium feasibility (need integration with test framework)

#3: Incident Prediction
Why: High impact (reduces downtime 30%) + Lower feasibility (need production telemetry data, we don't collect enough)

I'd focus on #1 (Code Review) because it has both highest impact AND highest feasibility. #3 has higher impact potential but would take 18 months to get data infra ready."
```

**What evaluator looks for:**
- Named 3 use cases (not 1, not 10)
- Ranked them (1, 2, 3)
- Explained why (impact + feasibility logic)
- Picked one to focus on

---

### Step 4: Deep Dive (10 minutes)

**What to do:**
Go deep on your #1 use case:

1. **Problem** (90 sec): What's broken? How bad?
2. **Solution** (3 min): How does the technology solve it? Be technical.
3. **Why This Company** (90 sec): What's their unique advantage?
4. **Metrics** (2 min): How do you measure success? What could go wrong?
5. **Risks** (2 min): Technical, operational, cost risks

**Example (abbreviated):**
```
Deep Dive: AI Code Review

Problem: Manual code review is slow and inconsistent. Average PR sits for 2 days before human review. When humans review, they catch syntax/style issues but miss subtle bugs (race conditions, memory leaks). 20% of production bugs trace back to missed code review issues.

Solution: AI-powered code review as pre-merge gate.

Technical approach:
- Train transformer model on 5 years of Delhivery code (2M commits, 500K PRs)
- Model learns: code style, common bug patterns, security vulnerabilities
- On each new PR: model analyzes diff, flags issues with severity (critical/major/minor)
- Integration: GitHub Actions workflow runs AI review before human review
- Human reviewers see AI flags, focus on architecture/business logic

Technology fit:
- LLMs (like Codex) excel at code understanding
- Pattern recognition catches repetitive bugs humans miss
- Context window (100K tokens) handles large PRs

Why Delhivery:
- 200 engineers, high PR volume (500/week)
- Legacy codebase (lots of technical debt)
- High cost of bugs (downtime = lost revenue)
- Already use GitHub (easy integration)

Metrics:
- **North Star**: Bug escape rate (bugs found in production)
  - Current: 20/week
  - Target: 12/week (40% reduction)
  
- **Input metrics**:
  - PR turnaround time: 48hrs → 6hrs (AI review instant, humans focus on critical path)
  - Code review coverage: 60% → 85% (AI reviews ALL PRs, humans are selective)
  
- **Guardrails**:
  - False positive rate <15% (if higher, devs ignore it)
  - Critical bug catch rate >80% (must catch real issues)

Risks:
1. **False positives**: AI flags non-issues, devs lose trust
   - Mitigation: Tune model, allow devs to mark false positives (feedback loop)

2. **Missed novel bugs**: AI only knows patterns it's seen
   - Mitigation: Hybrid approach (AI + human review, not replacement)

3. **Cost**: LLM inference is expensive at scale
   - Mitigation: Start with critical paths only (payments, orders), expand later
   
4. **Data privacy**: Code contains business logic, can't use external LLMs
   - Mitigation: Self-hosted model (Hugging Face, not OpenAI API)
```

**What evaluator looks for:**
- All 5 sections covered (problem, solution, why them, metrics, risks)
- Technical details (not just "use AI")
- Quantified (numbers for impact, timelines)
- Acknowledged constraints (data, cost, false positives)
- Realistic rollout (phased approach)

---

### Step 5: Rollout Plan (3 minutes)

**What to do:**
Describe Phase 1 → 2 → 3 rollout.

**Structure:**
```
"Rollout in 3 phases:

Phase 1: [Timeframe]
- [What we build/deploy]
- [Success criteria]
- [Go/no-go decision]

Phase 2: [Timeframe]
- [What we expand]
- [Based on Phase 1 learnings]

Phase 3: [Timeframe]
- [Full rollout]
- [When we hit scale]
```

**Example:**
```
"Rollout in 3 phases:

Phase 1: Pilot (3 months)
- Deploy AI code review on 2 teams (Payments + Orders - 30 engineers)
- Non-blocking mode (suggestions only, doesn't block PRs)
- Success criteria: <15% false positive rate, >60% of suggestions accepted
- Go/no-go: If devs ignore >50% of suggestions, pause and retrain

Phase 2: Expand (3 months)
- Roll out to all backend teams (150 engineers)
- Blocking mode for critical paths (payments, orders)
- Non-blocking for other code
- Tune model based on Phase 1 feedback

Phase 3: Full rollout (6 months)
- All 200 engineers
- Blocking on all PRs for critical severity issues
- Integrate with CI/CD (auto-fail builds on critical bugs)
- Add auto-fix for simple issues (formatting, import cleanup)

Timeline: 12 months pilot → full rollout"
```

**What evaluator looks for:**
- 3 phases described (pilot, expand, full)
- Each phase has timeline
- Success criteria for each phase
- Acknowledged learning/iteration (not just "we'd launch it")

---

## Evaluation Rubric (Total: 10 points)

### Component 1: Clarify (1 point)

**1 point (Excellent):**
- Caught ambiguity
- Asked clarifying question
- Stated assumption

**0.5 points (Partial):**
- No ambiguity but acknowledged the scope anyway

**0 points:**
- (If no ambiguity, automatically give 1 point)
- (If ambiguity existed and they missed it, give 0)

---

### Component 2: Map Capabilities (2 points)

**2 points (Excellent):**
- Drew a matrix
- Technology capabilities are specific
- Business problems/phases are relevant
- 5-8 cells filled

**1 point (Partial):**
- Matrix attempted but incomplete (2-3 cells)
- OR didn't organize as matrix (just listed use cases)

**0 points (Missing):**
- No matrix
- Just said "we'd use AI for X, Y, Z"

---

### Component 3: Prioritize (2 points)

**2 points (Excellent):**
- Named 3 use cases
- Ranked them (1, 2, 3)
- Explained why (impact + feasibility)
- Picked one to focus on

**1 point (Partial):**
- Named use cases but didn't rank
- OR ranking logic weak ("this one is better")

**0 points (Missing):**
- No prioritization
- Just listed everything

---

### Component 4: Deep Dive (4 points)

**4 points (Excellent):**
- All 5 sections (problem, solution, why them, metrics, risks)
- Technical details (not hand-waving)
- Quantified impact
- Acknowledged constraints
- Realistic approach

**3 points (Good):**
- 4 sections covered
- Some technical details
- Quantified but not deeply

**2 points (Partial):**
- 2-3 sections only
- Stayed high-level ("use AI to review code")
- No technical details

**1 point (Weak):**
- 1 section or less
- Just buzzwords

**0 points (Missing):**
- No deep dive

---

### Component 5: Rollout (1 point)

**1 point (Excellent):**
- 3 phases (pilot, expand, full)
- Timelines for each
- Success criteria
- Learning/iteration

**0.5 points (Partial):**
- 1-2 phases only
- OR no success criteria

**0 points (Missing):**
- Just said "we'd build it"
- No rollout plan

---

## Scoring Interpretation

**9-10 points:** Excellent. Strong technical depth + business sense.
- Concrete, feasible, well-prioritized
- Ready for technical PM role

**7-8 points:** Strong. Good understanding.
- Minor gaps (e.g., weak on constraints)
- Would succeed with coaching

**5-6 points:** Decent. Some understanding.
- Either good tech understanding but weak prioritization, OR vice versa
- Needs more depth

**3-4 points:** Weak. Limited technical depth.
- Buzzword bingo ("use AI for everything")
- No concrete use cases

**0-2 points:** Poor. Not ready.
- No technical understanding
- No domain knowledge

---

## Common Failure Modes to Watch For

### Failure Mode 1: Buzzword Bingo
Said "use AI for personalization" without explaining HOW.

**Feedback:** "Too vague. What does 'use AI for personalization' mean technically? What model? What data? How does it work?"

---

### Failure Mode 2: Listed Everything
Named 10 use cases without prioritization.

**Feedback:** "You listed many use cases but didn't prioritize. A PM must choose. Next time: pick top 3, rank them, defend your choice."

---

### Failure Mode 3: Ignored Constraints
Assumed infinite data, mature technology, zero cost.

**Feedback:** "You didn't acknowledge constraints. AI needs data (do we have it?), costs money (what's the ROI?), and has limitations (false positives?). Next time: discuss feasibility."

---

### Failure Mode 4: No Technical Depth
Stayed abstract, never got specific about how the technology works.

**Feedback:** "I don't understand HOW this works. What model? What inputs/outputs? How does it integrate? Next time: be technical."

---

### Failure Mode 5: Skipped Business Case
Described cool technology but didn't tie to business outcomes.

**Feedback:** "Why does this matter for the business? How does it improve revenue/cost/experience? Next time: quantify impact."

---

## Time Management Tips

**If running out of time:**
- **Have done Map + Prioritize (5 min)?** → Skip to Deep Dive (focus just on Problem + Solution)
- **Have done Deep Dive?** → Compress Rollout (1 min)
- **Not done Deep Dive yet?** → This is most important. Compress Map (1 min) to get to Deep Dive

**If ahead of schedule:**
- Add more detail to use cases #2 and #3
- Discuss alternative technologies considered

---

## Framework Adaptation

**For "compare technologies" questions** ("LLMs vs traditional ML"):
Add comparison section after Map:
- Use case A: LLMs better because [reason]
- Use case B: Traditional ML better because [reason]

**For "emerging tech" questions** (blockchain, Web3):
Add maturity assessment:
- What's ready today vs. 3 years out?
- What are we betting on?

---

**Framework File Version:** 1.0  
**Last Updated:** May 2026  
**Location:** `plugins/tech-application/framework.md`
