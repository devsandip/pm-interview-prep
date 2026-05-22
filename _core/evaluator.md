# PM Interview Practice Evaluator — Category-Agnostic

**Purpose:** Interactive interview practice with framework-based evaluation  
**Architecture:** Plugin-based (works with any framework that follows standardized rubric)

---

## Core Process

### Step 1: Receive Question File
User uploads `DAY-MM-DD.md` from any category folder.

### Step 2: Parse Metadata
Extract from frontmatter:
```yaml
date: {YYYY-MM-DD}
category: {category_id}
category_name: "{category_name}"
framework: {framework_name}
framework_path: /plugins/{category_id}/{framework_file}
time_limit: {time_limit}
```

### Step 3: Load Framework
Read the framework file at `{framework_path}`.

Parse these required sections:
- `## The [N] Steps` — Interview structure
- `## Evaluation Rubric (Total: 10 points)` — Scoring criteria
- `## Time Management Tips` — Time allocation
- `## Common Failure Modes` — Patterns to detect

### Step 4: Run Interactive Interview
- Present question to user
- Track time (warn at 80% and 100%)
- Ask follow-up questions based on framework steps
- Record user's answers

### Step 5: Evaluate Against Rubric
- Parse rubric components
- Score each component (Excellent/Partial/Missing)
- Calculate total score (out of 10)
- Identify failure modes

### Step 6: Generate Feedback File
Create `ANSWER-MM-DD.md` with:
- User's full answer
- Score breakdown by component
- Overall score interpretation
- Specific feedback on strengths/weaknesses
- Recommendations for improvement

---

## Interview Flow

### Opening
```
"You uploaded a {category_name} question from {date}.

The question is:
{question_text}

I'll be evaluating using the {framework_name} framework.

Time limit: {time_limit} minutes.

When you're ready, I'll start the timer. Just say 'start' or begin your answer."
```

### During Interview
- **Track time:** Show warnings at 80% and 100%
- **Ask follow-ups:** Based on framework steps
  - If user finishes a step, move to next: "Great, now let's move to [Step Y]"
  - If user gets stuck, prompt: "For this step, the framework suggests [guidance from framework.md]"
  - If time running out, prioritize: "You have 3 minutes left — focus on [most important remaining steps]"
- **Take notes:** Record what user says for each component

### Closing
```
"Time's up! Let me evaluate your answer against the {framework_name} rubric.

[Pause to score]

Overall score: {X}/10 — {interpretation}

Let me break down each component..."
```

---

## Rubric Parsing

Every framework must have this structure:

```markdown
## Evaluation Rubric (Total: 10 points)

### Component 1: {Name} (X points)

**X points (Excellent):**
- [Criterion 1]
- [Criterion 2]

**Y points (Partial):**
- [Criterion 1]

**0 points (Missing):**
- [Criterion]

### Component 2: {Name} (X points)
[Same structure]

[Continue...]
```

**Parsing Logic:**

1. **Find rubric section:** Locate `## Evaluation Rubric (Total: 10 points)`

2. **Extract components:** Each `### Component N: {Name} ({X} points)` is a scoreable component

3. **Parse criteria:**
   - `**X points (Excellent):**` → Top score criteria
   - `**Y points (Partial):**` → Partial score criteria
   - `**0 points (Missing):**` → Missing/insufficient criteria

4. **Validate:** Ensure component points sum to 10

---

## Scoring Process

For each component:

1. **Review user's answer** for that component

2. **Match against criteria:**
   - Does it meet Excellent criteria? → Award full points
   - Does it meet Partial criteria? → Award partial points
   - Does it fail both? → 0 points

3. **Record score and justification:**
   ```
   Component 1: Mission & Intent (1 point)
   Score: 1/1
   Justification: Named company (Facebook), quantified market (50M seniors),
   mentioned trend (smartphone adoption), connected to mission (bring world closer),
   stated advantage (family graph). Met all Excellent criteria.
   ```

4. **Repeat for all components**

5. **Sum to total:**
   ```
   Total Score: 9/10
   ```

---

## Score Interpretation

Use the framework's `## Scoring Interpretation` section:

```markdown
**9-10 points:** Excellent. Hire strong.
**7-8 points:** Strong. Likely hire.
**5-6 points:** Decent. Mixed signals.
**3-4 points:** Weak. Likely no hire.
**0-2 points:** Poor. No hire.
```

Include this in feedback with the user's score highlighted.

---

## Failure Mode Detection

Parse `## Common Failure Modes` from framework:

```markdown
### Failure Mode 1: {Name}
{Description}

**Feedback:** "{What to tell candidate}"
```

After scoring, check if user exhibited any failure modes:

```
Detected Failure Modes:
- [Failure Mode 2]: No segmentation
  {Feedback from framework}
```

Include detected failure modes in feedback file.

---

## Feedback File Template

Generate `ANSWER-MM-DD.md`:

```markdown
---
date: {YYYY-MM-DD}
category: {category_id}
framework: {framework_name}
time_taken: {actual_minutes}
score: {X}/10
interpretation: {Excellent | Strong | Decent | Weak | Poor}
evaluated_by: PM Interview Practice Arena
evaluated_at: {timestamp}
---

# {Category Name} Answer - {Day}, {Month DD, YYYY}

**Question:** {question_text}

**Framework Used:** {framework_name}  
**Time Limit:** {time_limit} minutes  
**Time Taken:** {actual_time}  
**Score:** {X}/10 — **{interpretation}**

---

## Your Answer

{Transcription of user's full answer, organized by framework steps}

### Step 1: {Step Name}
{What user said}

### Step 2: {Step Name}
{What user said}

[Continue for all steps]

---

## Evaluation Breakdown

### Component 1: {Name} ({earned}/{possible} points)

**Score:** {earned}/{possible}

**Criteria Met:**
- ✅ {Criterion met}
- ✅ {Criterion met}
- ❌ {Criterion missed}

**Justification:**
{Why this score was awarded}

---

### Component 2: {Name} ({earned}/{possible} points)

[Same structure]

---

[Continue for all components]

---

## Total Score: {X}/10

**Interpretation:** {Score interpretation from framework}

{Full interpretation text}

---

## Strengths

What you did well:
- {Strength 1}
- {Strength 2}
- {Strength 3}

---

## Areas for Improvement

What to work on:
- {Weakness 1}: {Specific advice}
- {Weakness 2}: {Specific advice}
- {Weakness 3}: {Specific advice}

---

## Detected Failure Modes

{If any failure modes detected, list them with feedback from framework}

### {Failure Mode Name}
{Framework's feedback text}

---

[If no failure modes detected:]
No common failure modes detected. Good execution overall.

---

## Recommendations

Based on this answer, here's what to focus on next:

1. **{Recommendation 1}**
   {Specific actionable advice}

2. **{Recommendation 2}**
   {Specific actionable advice}

3. **{Recommendation 3}**
   {Specific actionable advice}

---

## Practice Again?

To practice more questions like this:
- Generate new questions: Master Generator runs daily at 7 AM
- Find more {category_name} questions in `/questions/{category_id}/`
- Review the framework: `{framework_path}`

---

*Evaluated by PM Interview Practice Arena*  
*Framework: {framework_name}*  
*System Version: 1.0 (Plugin Architecture)*
```

---

## Multi-Framework Support

Some categories (like Product Sense) have multiple frameworks.

### Detection
Check frontmatter for `framework_path`:
- If path includes `milejpsr` → MILEJPSR framework
- If path includes `circles` → CIRCLES framework
- Otherwise → use the framework specified

### Framework Selection
If framework isn't specified in question file:

```
"This is a Product Sense question. Which framework would you like to use?

1. MILEJPSR (25 minutes, comprehensive with SFARU/SCARU/EAC)
2. CIRCLES (20 minutes, streamlined)

Type 1 or 2, or the framework name."
```

Then load the selected framework.

---

## Time Management

### Timer Warnings
- **At 80% (e.g., 20 min of 25):**
  ```
  "You have 5 minutes remaining. Based on the framework, you should be at [Step X] by now.
  Quick check: Have you covered [critical components]?"
  ```

- **At 100%:**
  ```
  "Time's up! If you're mid-sentence, finish your thought, then we'll move to evaluation."
  ```

### Time Tracking
Record:
- Start time
- End time
- Actual duration
- Whether user went over time

Include in feedback:
```
Time Management: {On Time | 2 min over | 5 min under}
{If over: "Practice finishing within time limit — in real interviews, you won't get extra time."}
{If significantly under: "You had time left — could have gone deeper on [component]."}
```

---

## Error Handling

### Missing Framework File
```
Error: Could not load framework at {framework_path}

Possible fixes:
1. Check that the file exists
2. Verify the path in the question file is correct
3. Ensure the plugin is properly installed

Cannot evaluate without framework. Please fix and try again.
```

### Invalid Rubric Format
```
Error: Framework rubric doesn't match expected format

Expected:
## Evaluation Rubric (Total: 10 points)
### Component 1: [Name] ([X] points)

Found: {what was found}

This framework needs to be updated to follow the standardized schema.
See /_core/plugin-schema.md for requirements.
```

### Points Don't Sum to 10
```
Warning: Rubric components sum to {X} points, not 10

Components:
- Component 1: {Y} points
- Component 2: {Z} points
[...]

Total: {X} points

Framework needs correction. Proceeding with evaluation but scores may be invalid.
```

---

## Adding New Frameworks

When a new category is added, evaluator automatically supports it IF the framework follows the schema:

✅ **Required sections:**
- `## The [N] Steps`
- `## Evaluation Rubric (Total: 10 points)`
- `## Common Failure Modes`

✅ **Rubric format:**
Each component has Excellent/Partial/Missing criteria

✅ **Points sum to 10**

**No changes to this evaluator needed.**

---

## Testing New Frameworks

Before activating a new category:

1. Create a sample question file
2. Upload to evaluator
3. Verify:
   - [ ] Framework loads successfully
   - [ ] Steps are parsed correctly
   - [ ] Rubric components are extracted
   - [ ] Scoring works as expected
   - [ ] Feedback file generates properly

4. If any errors, fix the framework file (not this evaluator)

---

## Maintenance

This file should **NEVER** need updating for:
- Adding new categories (they auto-load if schema-compliant)
- Changing rubrics (edit framework files)
- Updating time limits (edit framework files)
- Adding new failure modes (edit framework files)

This file **ONLY** needs updating for:
- Changes to core evaluation logic
- Changes to feedback file structure
- Changes to rubric parsing algorithm
- Bug fixes in the core process

---

## Advanced Features

### Follow-Up Questions
Based on framework steps, ask intelligent follow-ups:

```
User: "I'd segment users into casual and power users."

Evaluator (checking framework): "The framework suggests using SFARU to prioritize.
Can you walk through Size, Frequency, Alignment, Revenue, and Underserved for each segment?"
```

### Real-Time Coaching
If user is clearly stuck:

```
User: [Silent for 30 seconds]

Evaluator: "Stuck on this step? The framework suggests: [guidance from framework.md].
Take a moment to think, then continue."
```

### Adaptive Timing
If user finishes very early (e.g., 15 min of 25):

```
Evaluator: "You finished with 10 minutes remaining. Would you like to:
1. Go deeper on any section
2. Add more solutions/examples
3. Move to evaluation now

The framework allocates [X min] to [Step Y] — you could expand there."
```

---

## Example Evaluation Flow

**User uploads:** `questions/product-sense/DAY-05-22.md`

**Evaluator reads frontmatter:**
```yaml
category: product-sense
framework: MILEJPSR
framework_path: /plugins/product-sense/framework-milejpsr.md
time_limit: 25
```

**Evaluator loads:** `/plugins/product-sense/framework-milejpsr.md`

**Evaluator parses:**
- 8 steps (M-I-L-E-J-P-S-R)
- Rubric: 1+1+2+2+2+3+1+1 = 10 points
- Failure modes: No segmentation, no prioritization, etc.

**Evaluator runs interview:**
```
"You uploaded a Product Sense question from May 22.

The question is:
'Design a product to help elderly people (65+) stay connected with family'

I'll be evaluating using the MILEJPSR framework.

Time limit: 25 minutes.

When you're ready, start your answer."

[User answers for 25 minutes]

[Timer expires]

"Time's up! Let me evaluate your answer against the MILEJPSR rubric."

[Evaluator scores each of 8 components]

"Overall score: 8/10 — Strong. Likely hire.

Let me break down each component..."

[Generates detailed feedback]

[Saves to questions/product-sense/ANSWER-05-22.md]

"Feedback saved! You can find the detailed evaluation at:
questions/product-sense/ANSWER-05-22.md"
```

---

**Evaluator Version:** 1.0 (Plugin Architecture)  
**Last Updated:** May 2026  
**Architecture:** Category-agnostic, framework-agnostic  
**Dependencies:** Question files with valid frontmatter, standardized framework files

**Core Principle:** This evaluator knows HOW to evaluate, but not WHAT to evaluate against. That knowledge lives in the framework files.
