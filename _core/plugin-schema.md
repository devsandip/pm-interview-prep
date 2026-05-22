# Plugin Schema — How to Create a New Question Category

## Overview

Each question category is a **self-contained plugin**. Adding a new category requires:
1. Creating a plugin folder with 3 required files
2. Adding the category to `config.yaml`
3. **No changes to core files needed**

---

## Plugin Folder Structure

```
plugins/
└── {category-id}/
    ├── framework.md           # How to answer and evaluate
    ├── generation-rules.md    # How to generate questions
    └── examples.md            # 3-6 example questions
```

**Example:** To add RCU (execution) questions:
```
plugins/
└── execution/
    ├── framework.md
    ├── generation-rules.md
    └── examples.md
```

---

## Required File 1: `framework.md`

**Purpose:** Defines how to answer AND how to evaluate answers.

**Required Sections:**

```markdown
# [Framework Name] for [Category] Questions

## What This Framework Is
[1-2 paragraph description of the framework]

## When to Use This Framework
**Use for questions like:**
- [Question type 1]
- [Question type 2]
- [Question type 3]

## What This Framework Tests
### [Skill 1]
[What this measures]

### [Skill 2]
[What this measures]

---

## The [N] Steps ([X] minutes total)

### Step 1: [Step Name] ([X] minutes)

**What to do:**
[Instructions for candidate]

**Structure:**
```
[Template showing how to structure the answer]
```

**Example:**
```
[Concrete example]
```

**What evaluator looks for:**
- [Criterion 1]
- [Criterion 2]
- [Criterion 3]

---

### Step 2: [Step Name] ([X] minutes)
[Same structure as Step 1]

---

[Continue for all steps]

---

## Evaluation Rubric (Total: 10 points)

### Component 1: [Name] (X points)

**X points (Excellent):**
- [Criterion 1]
- [Criterion 2]
- [Criterion 3]

**Y points (Partial):**
- [Criterion 1]
- [Criterion 2]

**0 points (Missing):**
- [Criterion]

---

### Component 2: [Name] (X points)
[Same structure]

---

[Continue until total = 10 points]

---

## Scoring Interpretation

**9-10 points:** [What this means - hire/no hire]
**7-8 points:** [What this means]
**5-6 points:** [What this means]
**3-4 points:** [What this means]
**0-2 points:** [What this means]

---

## Time Management Tips

**Total time: [X] minutes**

- **Step 1**: [X] min
- **Step 2**: [X] min
- **Step 3**: [X] min
[etc.]

**If running out of time:**
- [Which steps to compress]
- [Which steps to keep]

---

## Common Failure Modes

### Failure Mode 1: [Name]
[Description of failure]

**Feedback:** "[What to tell candidate]"

---

### Failure Mode 2: [Name]
[Description]

**Feedback:** "[What to tell candidate]"

---

[Continue for 4-6 failure modes]
```

**Critical Requirements:**
- ✅ Total rubric must equal **10 points**
- ✅ Each component must have Excellent/Partial/Missing criteria
- ✅ Time management must sum to stated total time
- ✅ Must include at least 4 failure modes

---

## Required File 2: `generation-rules.md`

**Purpose:** Defines how to generate questions for this category.

**Required Sections:**

```markdown
# [Category] Question Generation Rules

## Category Overview

**Category:** [Name]
**Question Format:** [Template showing structure]
**Time Limit:** [X] minutes
**Recommended Framework:** [Framework name]

---

## What This Category Tests

### Core Skills Being Evaluated:
- [Skill 1]: [Description]
- [Skill 2]: [Description]
- [Skill 3]: [Description]

### What Interviewers Listen For:
- [Signal 1]
- [Signal 2]
- [Signal 3]

### Common Failure Modes:
- [Failure 1]
- [Failure 2]
- [Failure 3]

---

## Question Generation Rules

### Selection Pools

[Define the pools to pull from - companies, products, concepts, etc.]

**Pool 1 (X% of questions):**
- [Item 1]
- [Item 2]
- [Item 3]

**Pool 2 (Y% of questions):**
- [Item 1]
- [Item 2]
- [Item 3]

---

### Required Context Components

**Every question MUST include:**

1. **[Component 1]:**
   - [What to include]
   - [Why it matters]

2. **[Component 2]:**
   - [What to include]
   - [Why it matters]

[Continue for all required components]

---

## Question Template

```markdown
## Question [1 or 2]

**Question:**
[Question text following the format]

**Context:**
[Context structure]

**Time Limit:** [X] minutes

**Recommended Framework:** [Framework name]

**Framework Location:** `/plugins/{category}/framework.md`
```

---

## Quality Checklist

Before finalizing each question, verify:

- [ ] [Criterion 1]
- [ ] [Criterion 2]
- [ ] [Criterion 3]
- [ ] [Criterion 4]
- [ ] Time limit is [X] minutes
- [ ] Framework recommendation is correct
- [ ] Framework file path is included

---

## Difficulty Calibration

**Medium (60% of questions):**
- [Description of medium difficulty]
- [Examples]

**Hard (30% of questions):**
- [Description of hard]
- [Examples]

**Very Hard (10% of questions):**
- [Description of very hard]
- [Examples]

---

## Variety Rules

**Weekly:**
- [Rule 1]
- [Rule 2]
- [Rule 3]

**Monthly:**
- [Rule 1]
- [Rule 2]
```

**Critical Requirements:**
- ✅ Must define selection pools with percentages
- ✅ Must specify required context components
- ✅ Must include question template
- ✅ Must define difficulty calibration (60/30/10 split)
- ✅ Must include variety rules

---

## Required File 3: `examples.md`

**Purpose:** Provides concrete examples of well-formed questions.

**Required Sections:**

```markdown
# [Category] Example Questions

## Example 1: [Type/Variation]

**Question:**
[Full question text]

**Context:**
[All required context]

**Time Limit:** [X] minutes

**Recommended Framework:** [Framework name]

**Framework Location:** `/plugins/{category}/framework.md`

---

## Example 2: [Type/Variation]
[Same structure]

---

## Example 3: [Type/Variation]
[Same structure]

---

[Continue for 3-6 examples covering different variations]
```

**Critical Requirements:**
- ✅ Minimum **3 examples**, maximum **6 examples**
- ✅ Each example must be complete (not truncated)
- ✅ Examples should cover different variations/difficulty levels
- ✅ All examples must follow the question template from `generation-rules.md`

---

## Registering Your Plugin

After creating the 3 files, add your category to `config.yaml`:

```yaml
categories:
  - id: {category-id}
    name: "{Category Display Name}"
    active: true
    questions_per_day: 2
    time_limit: 25
    folder: "plugins/{category-id}"
```

**Fields:**
- `id`: Folder name (lowercase, hyphenated)
- `name`: Human-readable name
- `active`: `true` to generate questions, `false` to disable
- `questions_per_day`: How many to generate (1-3)
- `time_limit`: Default time in minutes
- `folder`: Path to plugin folder (always `plugins/{id}`)

---

## Testing Your Plugin

Before activating, verify:

1. **All 3 files exist**
   ```bash
   ls plugins/{category-id}/
   # Should show: framework.md  generation-rules.md  examples.md
   ```

2. **Framework follows schema**
   - Has "## Evaluation Rubric (Total: 10 points)" section
   - Each component has Excellent/Partial/Missing
   - Time management adds up

3. **Generation rules are complete**
   - Selection pools defined
   - Required context specified
   - Question template included

4. **Examples are valid**
   - At least 3 examples
   - Follow question template
   - Include all required context

5. **Config entry added**
   ```yaml
   - id: {category-id}
     active: true
     questions_per_day: 2
   ```

6. **Test generation**
   - Run master generator
   - Verify question file created in `questions/{category-id}/`
   - Check that question includes framework path

7. **Test evaluation**
   - Upload generated question to evaluator
   - Verify framework loads correctly
   - Check that rubric is parsed and applied

---

## Complete Example: Adding RCU (Execution) Questions

### Step 1: Create plugin folder

```bash
mkdir -p plugins/execution
```

### Step 2: Create `framework.md`

```markdown
# RCU Framework for Execution Questions

## What This Framework Is
RCU (Resource, Cost, User) framework for execution questions.

## When to Use This Framework
**Use for questions like:**
- "How would you execute X?"
- "You've decided to build Y — how do you execute?"

## What This Framework Tests
### Resource Planning
Can you identify team, tools, budget needed?

### Cost Analysis
Do you understand engineering time, infrastructure, opportunity cost?

### User Rollout
Can you design phased rollout with metrics?

---

## The 3 Steps (15 minutes total)

### Step 1: Resources (5 minutes)

**What to do:**
Identify all resources needed to execute.

**Structure:**
```
"Resources needed:

Team:
- [Size]: [X] engineers, [Y] designers, [Z] PMs
- [Skills]: [Required expertise]

Tools:
- [Infrastructure needed]
- [Third-party services]

Budget:
- [Engineering cost]
- [Infrastructure cost]
- [Total]"
```

**What evaluator looks for:**
- Named team size and skills
- Listed required tools/infrastructure
- Estimated budget

### Step 2: Costs (5 minutes)

**What to do:**
Break down all costs (not just financial).

**Structure:**
```
"Cost breakdown:

Engineering Time:
- [X] engineer-months for [feature Y]
- [Timeline]

Infrastructure:
- [Servers, databases, CDN, etc.]
- [Monthly cost]

Opportunity Cost:
- [What we're NOT building by doing this]
- [Impact]"
```

**What evaluator looks for:**
- Calculated engineering time
- Estimated infrastructure costs
- Named opportunity cost

### Step 3: Users (5 minutes)

**What to do:**
Design rollout plan with phases and metrics.

**Structure:**
```
"Rollout plan:

Phase 1 (2 weeks): Internal beta
- [Who tests]
- [Metrics to track]

Phase 2 (4 weeks): 10% users
- [Which segment]
- [Success criteria]

Phase 3 (4 weeks): 100% rollout
- [Metrics]
- [Kill criteria]"
```

**What evaluator looks for:**
- Phased rollout (not big bang)
- Metrics for each phase
- Kill criteria defined

---

## Evaluation Rubric (Total: 10 points)

### Component 1: Resources (4 points)

**4 points (Excellent):**
- Team size and skills specified
- Tools and infrastructure listed
- Budget estimated

**2 points (Partial):**
- Some resources listed but incomplete
- Missing budget OR missing tools

**0 points (Missing):**
- No resource planning

### Component 2: Costs (3 points)

**3 points (Excellent):**
- Engineering time calculated
- Infrastructure costs estimated
- Opportunity cost named

**1 point (Partial):**
- Only one cost type identified

**0 points (Missing):**
- No cost analysis

### Component 3: Users (3 points)

**3 points (Excellent):**
- Phased rollout with 2-3 phases
- Metrics for each phase
- Kill criteria defined

**1 point (Partial):**
- Mentioned rollout but no metrics OR no kill criteria

**0 points (Missing):**
- No rollout plan

---

## Scoring Interpretation

**9-10 points:** Excellent. Hire strong.
**7-8 points:** Strong. Likely hire.
**5-6 points:** Decent. Mixed signals.
**3-4 points:** Weak. Likely no hire.
**0-2 points:** Poor. No hire.

---

## Time Management Tips

**Total time: 15 minutes**

- **Resources**: 5 min
- **Costs**: 5 min
- **Users**: 5 min

**If running out of time:**
- Keep all 3 sections (they're equally weighted)
- Compress by listing fewer details
- Don't skip opportunity cost or kill criteria

---

## Common Failure Modes

### Failure Mode 1: No Team Sizing
Just said "need engineers" without specifying how many.

**Feedback:** "How many engineers? What skills? Be specific about resource needs."

### Failure Mode 2: Only Financial Costs
Listed infrastructure cost but ignored engineering time and opportunity cost.

**Feedback:** "Cost isn't just money. What's the engineering time? What are we NOT building?"

### Failure Mode 3: Big Bang Launch
Proposed 100% rollout immediately.

**Feedback:** "Always phase rollout. Internal → 10% → 100% gives you chances to course-correct."

### Failure Mode 4: No Kill Criteria
Didn't say what would make you abort the launch.

**Feedback:** "What metrics would make you pull the plug? Define kill criteria upfront."
```

### Step 3: Create `generation-rules.md`

```markdown
# Execution Question Generation Rules

## Category Overview

**Category:** Execution (RCU)
**Question Format:** "You've decided to build [Feature]. How would you execute it?"
**Time Limit:** 15 minutes
**Recommended Framework:** RCU Framework

---

## What This Category Tests

### Core Skills Being Evaluated:
- **Resource planning**: Can you identify team, tools, budget?
- **Cost awareness**: Do you understand engineering time, infrastructure, opportunity cost?
- **Rollout discipline**: Can you design phased rollout with metrics?

### What Interviewers Listen For:
- Do you specify team size and skills (not just "need engineers")?
- Do you calculate costs beyond money (engineering time, opportunity cost)?
- Do you phase the rollout (not big bang)?
- Do you define kill criteria?

### Common Failure Modes:
- Vague resource planning ("need some engineers")
- Only considering financial costs
- Proposing immediate 100% rollout
- No kill criteria defined

---

## Question Generation Rules

### Selection Pools

**Feature Types (distribute evenly):**

**Infrastructure Features (25%):**
- Notification system
- Search functionality
- Recommendation engine
- Analytics platform

**User-Facing Features (40%):**
- Messaging feature
- Video calling
- Stories/ephemeral content
- Live streaming
- Dark mode

**Monetization Features (20%):**
- Subscription tier
- Ads platform
- In-app purchases
- Premium features

**Platform Features (15%):**
- API for third-party developers
- Plugin marketplace
- Webhooks
- OAuth integration

---

### Required Context Components

**Every question MUST include:**

1. **Feature Description:**
   - What the feature does
   - Who it's for
   - Why it was chosen (tie to strategy)

2. **Constraints:**
   - Timeline (3-6 months typical)
   - Team size (6-15 people typical)
   - Budget ($1M-$5M typical)

3. **Scale:**
   - Current users
   - Expected usage of new feature
   - Growth projections

4. **Risk:**
   - What could go wrong
   - Why this is hard

---

## Question Template

```markdown
## Question [1 or 2]

**Question:**
You've decided to build [Feature] for [Product]. How would you execute it?

**Feature Description:**
[What it does, who it's for, why now]

**Constraints:**
- Timeline: [X months]
- Team: [N engineers, M designers, 1 PM]
- Budget: $[X]M

**Scale:**
- Current users: [X]M
- Expected adoption: [Y]% of users will use this feature
- Growth: [Z]% user growth expected from this

**Risk:**
[What could go wrong, why this is hard]

**Time Limit:** 15 minutes

**Recommended Framework:** RCU Framework

**Framework Location:** `/plugins/execution/framework.md`
```

---

## Quality Checklist

Before finalizing each question, verify:

- [ ] Feature is clear and specific
- [ ] Constraints include timeline, team, budget
- [ ] Scale metrics provided (current users, expected adoption)
- [ ] Risk is stated
- [ ] Time limit is 15 minutes
- [ ] Framework recommendation is "RCU Framework"
- [ ] Framework file path is included

---

## Difficulty Calibration

**Medium (60% of questions):**
- Common feature type (messaging, notifications)
- Clear constraints
- 3-6 month timeline
- Moderate scale (10M-100M users)

**Hard (30% of questions):**
- Complex feature (recommendation engine, ML-based) OR
- Tight timeline (2-3 months) OR
- Large scale (100M+ users) OR
- Multiple dependencies

**Very Hard (10% of questions):**
- Novel feature (no prior art) AND
- Very tight timeline (6-8 weeks) OR
- Massive scale (500M+ users) OR
- Significant technical risk

---

## Variety Rules

**Weekly:**
- Don't repeat the same feature type 2 days in a row
- Mix infrastructure/user-facing/monetization/platform features
- Vary difficulty

**Monthly:**
- 25% infrastructure
- 40% user-facing
- 20% monetization
- 15% platform
```

### Step 4: Create `examples.md`

```markdown
# Execution Example Questions

## Example 1: User-Facing Feature

**Question:**
You've decided to build Stories for LinkedIn. How would you execute it?

**Feature Description:**
Stories are ephemeral content (disappears after 24 hours) where professionals can share quick updates, behind-the-scenes content, or career highlights. Target: professionals who want to show personality beyond formal posts.

**Constraints:**
- Timeline: 6 months to launch
- Team: 8 engineers (4 backend, 3 mobile, 1 web), 2 designers, 1 PM (you)
- Budget: $2M (team salaries + infrastructure)

**Scale:**
- Current users: 950M LinkedIn users
- Expected adoption: 15% of users will post Stories (based on Instagram Stories adoption)
- Growth: Could increase DAU by 20% (more frequent checking)

**Risk:**
Stories might feel too casual for LinkedIn's professional brand. Risk of low adoption if users don't see value in ephemeral professional content.

**Time Limit:** 15 minutes

**Recommended Framework:** RCU Framework

**Framework Location:** `/plugins/execution/framework.md`

---

## Example 2: Infrastructure Feature

**Question:**
You've decided to build a recommendation engine for Spotify to improve music discovery. How would you execute it?

**Feature Description:**
ML-based recommendation engine that suggests songs/playlists based on listening history, time of day, mood, and social listening patterns. Replaces current random shuffle.

**Constraints:**
- Timeline: 9 months (3 months for MVP, 6 months to scale)
- Team: 12 engineers (6 ML engineers, 4 backend, 2 mobile), 1 designer, 1 PM (you)
- Budget: $5M (team + compute costs for training models)

**Scale:**
- Current users: 500M Spotify users, 200M premium
- Expected usage: Every user gets recommendations, 80% will interact with them
- Impact: Goal is to increase listening time by 15% (better discovery = more engagement)

**Risk:**
Cold start problem (new users have no history). Models might reinforce existing preferences instead of true discovery. High compute costs for real-time recommendations.

**Time Limit:** 15 minutes

**Recommended Framework:** RCU Framework

**Framework Location:** `/plugins/execution/framework.md`

---

## Example 3: Monetization Feature

**Question:**
You've decided to build a premium subscription tier for Discord. How would you execute it?

**Feature Description:**
Discord Nitro Premium ($15/month) with HD video, screen share at 4K, custom emojis across servers, larger upload limits (100MB), and server boosts. Target: power users and server admins.

**Constraints:**
- Timeline: 4 months to launch
- Team: 6 engineers (3 backend, 2 web, 1 mobile), 1 designer, 1 PM (you)
- Budget: $1.5M

**Scale:**
- Current users: 150M MAU
- Target: 5% conversion to premium (7.5M subscribers)
- Revenue: $1.3B annually at full conversion

**Risk:**
Existing Nitro users might not upgrade (need compelling value prop). Free users might churn if features feel paywalled. Payment processing and subscription management complexity.

**Time Limit:** 15 minutes

**Recommended Framework:** RCU Framework

**Framework Location:** `/plugins/execution/framework.md`
```

### Step 5: Add to `config.yaml`

```yaml
categories:
  # ... existing categories ...
  
  - id: execution
    name: "Execution (RCU)"
    active: true
    questions_per_day: 1
    time_limit: 15
    folder: "plugins/execution"
```

### Step 6: Done!

Master generator will now:
- Detect the `execution` category
- Load `plugins/execution/generation-rules.md`
- Generate 1 question per day
- Save to `questions/execution/DAY-MM-DD.md`

Evaluator will:
- Load `plugins/execution/framework.md`
- Parse the RCU rubric (4+3+3 = 10 points)
- Evaluate answers automatically

---

## Validation Checklist

Before declaring your plugin complete:

- [ ] All 3 files exist (`framework.md`, `generation-rules.md`, `examples.md`)
- [ ] Framework has standardized rubric (Total: 10 points)
- [ ] Framework has time management section
- [ ] Framework has 4+ failure modes
- [ ] Generation rules define selection pools
- [ ] Generation rules specify required context
- [ ] Generation rules include question template
- [ ] Examples file has 3-6 complete examples
- [ ] Config entry added with `active: true`
- [ ] Category folder created: `questions/{category-id}/`

---

**Plugin Schema Version:** 1.0  
**Last Updated:** May 2026  
**Location:** `/_core/plugin-schema.md`
