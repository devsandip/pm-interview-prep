# S.I.E.V.E Framework for Debugging & Diagnosis Questions

## What This Framework Is

S.I.E.V.E is a structured approach to diagnosing metric drops or anomalies. It's used for "Metric X dropped Y% — what happened?" questions.

**S.I.E.V.E stands for:**
- **S**cope and Clarity
- **I**nitial Hypothesis (MECE)
- **E**xplore & Eliminate
- **V**alidate Root Cause
- **E**valuate and Execute

---

## When to Use This Framework

**Use for questions like:**
- "[Metric] dropped [X%] — diagnose the issue"
- "DAU/MAU/Revenue is down — what happened?"
- "[Product] engagement decreased — investigate"
- "Why did [metric] suddenly change?"

**Core skill being tested:**
Can you think like a detective? Do you use data systematically? Can you separate correlation from causation? Do you avoid jumping to conclusions?

---

## What This Framework Tests

### Structured Thinking
- Do you scope the problem before hypothesizing?
- Do you generate hypotheses in MECE buckets?
- Do you eliminate systematically, not randomly?

### Data Fluency
- Do you segment data to isolate the issue?
- Do you distinguish correlation from causation?
- Do you look for supporting/disconfirming evidence?

### Business Judgment
- Do you consider measurement issues first?
- Do you think about external factors (seasonality, competitors)?
- Do you check for internal product changes?

### Execution Mindset
- Do you recommend action vs. "do nothing"?
- Do you think short-term AND long-term?
- Do you acknowledge uncertainty appropriately?

---

## The 5 Steps (20 minutes total)

### Step 1: Scope and Clarity (3 minutes)

**What to do:**
Clarify exactly what happened before jumping to causes.

**Structure:**
```
"Let me clarify the scope:

Metric Definition:
- How is [metric] measured exactly?
- Has the measurement methodology changed recently?
- Any known logging issues?

Scope of Drop:
- Magnitude: [X%] drop
- Time period: [When did it start? Ongoing or stabilized?]
- Baseline: What was normal before the drop?

Affected Segments:
- Geography: All regions or specific ones?
- Platform: iOS/Android/Web?
- User type: New vs existing? Power users vs casual?
- Other segments: Age, gender, content type?

Surrounding Context:
- Product/feature changes in this timeframe?
- External events (holidays, news, competitor moves)?
- Any other metrics affected?"
```

**Example:**
```
"Let me clarify the scope:

Metric Definition:
- Instagram Stories DAU = unique users who posted or viewed at least 1 Story per day
- Measured via client-side events (story_view, story_post)
- No known changes to logging in past 30 days

Scope of Drop:
- Magnitude: 10% drop (from 500M → 450M DAU)
- Time period: Started 2 weeks ago, still declining
- Baseline: Stories DAU was flat at ~500M for 6 months prior

Affected Segments:
- Geography: Primarily US (-15%), EU (-12%), rest of world (-5%)
- Platform: iOS (-18%), Android (-8%), Web (-3%)
- User type: Existing users (-12%), new users (-5%)
- Age: 18-24 most affected (-20%), 25-34 (-8%), 35+ (-3%)

Surrounding Context:
- Reels algorithm update shipped 3 weeks ago (more Reels in Feed)
- TikTok launched new 'Photo Mode' feature 1 month ago
- No holidays, no major external events"
```

**What evaluator looks for:**
- Clarified metric definition
- Quantified drop magnitude and timeline
- Segmented by geography, platform, user type
- Checked for product changes and external context

---

### Step 2: Initial Hypothesis - MECE (4 minutes)

**What to do:**
Generate hypotheses in mutually exclusive, collectively exhaustive (MECE) buckets.

**MECE Hypothesis Framework:**

**Bucket 1: MEASUREMENT / DATA ISSUES** (Check first!)
- Tracking bug or logging issue
- Change in metric definition
- Data pipeline failure
- Sampling or aggregation error

**Bucket 2: EXTERNAL / MARKET FACTORS**
- Seasonality (holiday, weekend pattern)
- Competitor activity (new feature launch)
- External events (news, disaster, platform changes)
- Device/OS updates (iOS privacy changes)

**Bucket 3: INTERNAL / PRODUCT CHANGES**
- Recent feature launch or A/B test
- Algorithm change (ranking, recommendations)
- UI/UX change
- Competing feature cannibalization

**Bucket 4: USER BEHAVIOR SHIFTS**
- Natural product lifecycle (maturing product)
- Shift to competing feature (Reels vs Stories)
- User segment mix change (more new users)
- Content quality decline

**Structure:**
```
"MECE hypothesis buckets:

1. Measurement Issues:
   - [Hypothesis 1]
   - [Hypothesis 2]

2. External Factors:
   - [Hypothesis 1]
   - [Hypothesis 2]

3. Internal Changes:
   - [Hypothesis 1]
   - [Hypothesis 2]

4. User Behavior:
   - [Hypothesis 1]
   - [Hypothesis 2]

Most likely: [Which bucket] because [pattern in data]"
```

**Example:**
```
"MECE hypothesis buckets:

1. Measurement Issues:
   - iOS logging bug (iOS drop is -18% vs Android -8%)
   - Client-side event tracking broken on iOS

2. External Factors:
   - TikTok Photo Mode pulling Gen Z away (18-24 most affected)
   - iOS 17 privacy changes affecting tracking
   - Seasonality (back to school → less social media time)

3. Internal Changes:
   - Reels algorithm update 3 weeks ago → more Reels in Feed → less Stories discovery
   - Stories posting flow changed → harder to create Stories
   - Stories tab moved in navigation

4. User Behavior:
   - Gen Z shifting from Stories to Reels (more public, less ephemeral)
   - Content quality declining → less engagement → fewer viewers → fewer posters

Most likely: Bucket 3 (Internal Changes) because:
- Timing aligns: Reels algorithm update 3 weeks ago, drop started 2 weeks ago
- Pattern matches: Reels time up 15% in same period
- Segment pattern: iOS users see more Reels (algorithm is stronger there)"
```

**What evaluator looks for:**
- Used all 4 MECE buckets
- Generated 2+ hypotheses per bucket
- Checked measurement issues FIRST
- Selected most likely bucket with data-driven reasoning

---

### Step 3: Explore & Eliminate (5 minutes)

**What to do:**
Use data segmentation to narrow down hypotheses.

**Structure:**
```
"Data exploration to eliminate hypotheses:

Test 1: [Hypothesis] → [Data check] → [Result: Eliminated or Supported]
Test 2: [Hypothesis] → [Data check] → [Result: Eliminated or Supported]
Test 3: [Hypothesis] → [Data check] → [Result: Eliminated or Supported]

Key segments to check:
- Geography: [Finding]
- Platform: [Finding]
- User cohort: [Finding]
- Time of day: [Finding]
- Content type: [Finding]

Eliminated: [List]
Still possible: [List]"
```

**Example:**
```
"Data exploration to eliminate hypotheses:

Test 1: iOS logging bug?
→ Check: Compare iOS event volume to Android (normalized by DAU)
→ Result: iOS events per DAU are normal. ELIMINATED.

Test 2: TikTok Photo Mode competition?
→ Check: Did TikTok DAU increase by 50M? Did Instagram overall DAU drop?
→ Result: TikTok DAU flat. Instagram overall DAU stable. Stories drop is isolated. ELIMINATED.

Test 3: Reels algorithm update cannibalization?
→ Check: Is Reels time spent up? Are users posting fewer Stories but more Reels?
→ Result: Reels time +15%, Stories posts per user -20%, Reels posts per user +30%. SUPPORTED.

Test 4: Stories posting flow change?
→ Check: Is Stories post creation funnel drop-off higher?
→ Result: Stories post creation funnel unchanged. ELIMINATED.

Key segments:
- Geography: US/EU hit harder (Reels algorithm more aggressive there)
- Platform: iOS hit harder (Reels video quality better on iOS)
- User cohort: 18-24 hit hardest (Gen Z prefers public Reels over ephemeral Stories)
- Time of day: Evening drop most severe (prime Reels viewing time)
- Content type: Stories with music/effects down most (same features now in Reels)

Eliminated:
- iOS logging bug (events normal)
- TikTok competition (no TikTok surge)
- Seasonality (no historical pattern)
- Stories posting flow (funnel unchanged)

Still possible:
- Reels algorithm update → Reels cannibalized Stories (STRONGEST)
- Gen Z behavior shift → prefer Reels over Stories"
```

**What evaluator looks for:**
- Tested 3+ hypotheses with data
- Used segmentation (geography, platform, user type, time)
- Explicitly eliminated weak hypotheses
- Showed supporting evidence for remaining hypotheses

---

### Step 4: Validate Root Cause (4 minutes)

**What to do:**
Distinguish correlation from causation. Find evidence that validates the root cause.

**Structure:**
```
"Root cause validation:

Primary hypothesis: [Hypothesis]

Correlation:
- [Metric 1] and [Metric 2] moved together
- Timeline aligns: [Event] → [Metric change]

Causation checks:
1. Mechanism: How does [cause] lead to [effect]?
   → [Explanation]

2. Dose-response: Does bigger change → bigger effect?
   → [Check]

3. Supporting signals: What else should we see if this is true?
   → [Check 1]: [Result]
   → [Check 2]: [Result]

4. Disconfirming evidence: What would prove this wrong?
   → [Check]: [Result]

Confidence: [High/Medium/Low] that [hypothesis] is root cause"
```

**Example:**
```
"Root cause validation:

Primary hypothesis: Reels algorithm update caused Stories cannibalization

Correlation:
- Reels time +15%, Stories DAU -10%
- Timeline: Reels update 3 weeks ago → Stories drop started 2 weeks ago (1-week lag makes sense)

Causation checks:

1. Mechanism: How does more Reels → fewer Stories?
   → Users have finite time. More Reels in Feed → less Stories tab discovery → fewer Story views → fewer Story posts (network effect).

2. Dose-response: Users who see MORE Reels → bigger Stories drop?
   → YES: Heavy Reels users (top quartile): Stories usage -25%
   → Light Reels users (bottom quartile): Stories usage -3%

3. Supporting signals:
   → Stories tab opens: -12% (less discovery)
   → Stories replies: -15% (less engagement drives less posting)
   → Reels shares to Stories: +40% (Reels replacing Stories as communication medium)

4. Disconfirming evidence: If Reels algorithm, we should see:
   → Reels impressions UP: ✅ +20%
   → Stories impressions DOWN: ✅ -18%
   → Overall Instagram time FLAT or UP (time shifts, not lost): ✅ Total time +2%

Confidence: HIGH (90%) that Reels algorithm update caused Stories cannibalization via attention shift"
```

**What evaluator looks for:**
- Explained mechanism (cause → effect)
- Checked dose-response relationship
- Found supporting signals (2+ additional data points)
- Looked for disconfirming evidence
- Stated confidence level

---

### Step 5: Evaluate and Execute (4 minutes)

**What to do:**
Decide if this is a problem, then recommend action.

**Structure:**
```
"Evaluation and recommendation:

Is this actually a problem?
- [Perspective 1]: [Why yes or no]
- [Perspective 2]: [Why yes or no]
- Decision: [Problem or not]

Recommendations:

Immediate (this week):
- [Action 1]

Short-term (next month):
- [Action 2]

Medium-term (next quarter):
- [Action 3]

Long-term (6+ months):
- [Action 4]

Trade-offs:
[What we give up if we reverse course]"
```

**Example:**
```
"Evaluation and recommendation:

Is this actually a problem?

Against (it's fine):
- Overall Instagram time is UP +2% (good for ads)
- Reels engagement is UP +15% (strategic priority)
- Stories was declining anyway (mature product)
- Gen Z prefers public content (Reels) over ephemeral (Stories)

For (it's a problem):
- Stories is core to Instagram identity (differentiation from TikTok)
- Stories drives DMs and social connection (mission-critical)
- Creators use Stories for authentic, behind-the-scenes content (losing this hurts creator retention)
- Advertisers buy Stories ads separately (revenue stream at risk)

Decision: YES, this is a PROBLEM. We're cannibalizing a differentiated, high-value product.

Recommendations:

Immediate (this week):
- Rollback: Reduce Reels impressions in Feed by 20% for users in bottom quartile of Stories usage
- Notify ads team of potential Stories revenue impact

Short-term (next month):
- Algorithm balance: Train ranking model to optimize for BOTH Reels and Stories engagement (multi-objective)
- UI change: Add Stories tab to bottom nav on iOS (increase discovery)
- Creator incentive: Launch Stories monetization pilot (retain creator content)

Medium-term (next quarter):
- Product differentiation: Stories = close friends, Reels = public audience (make them non-competing)
- Cross-posting: Make it easier to turn Reels into Stories (reduce creation friction)
- Quality scoring: Weight Stories by reply rate (not just views) to promote authentic content

Long-term (6+ months):
- Strategic reposition: Stories as messaging layer, Reels as entertainment layer
- Merge: Consider unified "Instagram Video" that adapts to audience size (close friends vs public)

Trade-offs:
- Reducing Reels impressions → Reels growth slows (but Stories recovers)
- Keeping both products → duplicate content, user confusion
- Kill Stories → lose differentiation from TikTok, lose DM driver"
```

**What evaluator looks for:**
- Evaluated whether it's actually a problem (considered both sides)
- Recommended actions at multiple time horizons (immediate, short, medium, long)
- Acknowledged trade-offs
- Showed business judgment (not just "fix it")

---

## Evaluation Rubric (Total: 10 points)

### Component 1: Scope and Clarity (2 points)

**2 points (Excellent):**
- Clarified metric definition
- Quantified drop (magnitude, timeline)
- Segmented by 3+ dimensions (geo, platform, user type)
- Checked for product changes and external context

**1 point (Partial):**
- Clarified metric but no segmentation OR
- Segmented but didn't check context

**0 points (Missing):**
- Jumped straight to hypotheses without scoping

---

### Component 2: Initial Hypothesis - MECE (2 points)

**2 points (Excellent):**
- Used all 4 MECE buckets (Measurement, External, Internal, User Behavior)
- Generated 2+ hypotheses per bucket
- Checked measurement issues FIRST
- Selected most likely bucket with reasoning

**1 point (Partial):**
- Used some buckets but incomplete (<4) OR
- No prioritization/selection

**0 points (Missing):**
- Random list of hypotheses, not MECE

---

### Component 3: Explore & Eliminate (2 points)

**2 points (Excellent):**
- Tested 3+ hypotheses with data checks
- Used segmentation to narrow down
- Explicitly eliminated weak hypotheses
- Showed supporting evidence for remaining

**1 point (Partial):**
- Tested some hypotheses but weak data checks OR
- No explicit elimination

**0 points (Missing):**
- No data exploration

---

### Component 4: Validate Root Cause (2 points)

**2 points (Excellent):**
- Explained mechanism (cause → effect)
- Checked dose-response or supporting signals
- Looked for disconfirming evidence
- Stated confidence level

**1 point (Partial):**
- Explained mechanism but no validation OR
- Found correlation but didn't test causation

**0 points (Missing):**
- Assumed causation without evidence

---

### Component 5: Evaluate and Execute (2 points)

**2 points (Excellent):**
- Evaluated if it's a problem (considered both sides)
- Recommended actions at multiple time horizons
- Acknowledged trade-offs
- Showed business judgment

**1 point (Partial):**
- Recommended action but only one time horizon OR
- No trade-off consideration

**0 points (Missing):**
- No recommendation

---

## Scoring Interpretation

**9-10 points:** Excellent. Hire strong. Structured, data-driven, business judgment.
**7-8 points:** Strong. Likely hire. Minor gaps (e.g., weak on validation).
**5-6 points:** Decent. Mixed signals. Found cause but weak on execution.
**3-4 points:** Weak. Likely no hire. Poor structure or no data usage.
**0-2 points:** Poor. No hire. Jumped to conclusions without evidence.

---

## Time Management Tips

**Total time: 20 minutes**

- **Scope**: 3 min
- **Hypothesis**: 4 min (1 min per bucket)
- **Explore**: 5 min (1 min per hypothesis test)
- **Validate**: 4 min
- **Execute**: 4 min

**If running out of time:**
- Compress Hypothesis (2 min)
- Keep Explore and Validate (this is the core)
- Give quick recommendation in Execute

---

## Common Failure Modes

### Failure Mode 1: Jumped to Conclusion
Immediately said "It's because of [X]" without scoping or exploring alternatives.

**Feedback:** "Don't jump to conclusions. Use S.I.E.V.E: Scope first, generate MECE hypotheses, then explore with data."

---

### Failure Mode 2: Ignored Measurement Issues
Didn't check if it's a logging bug or data issue before investigating product causes.

**Feedback:** "Always check measurement issues FIRST. 50% of metric drops are data bugs, not real drops."

---

### Failure Mode 3: Correlation = Causation
Found two metrics moving together and assumed one caused the other without testing mechanism.

**Feedback:** "Correlation ≠ causation. Explain the mechanism, check dose-response, and look for disconfirming evidence."

---

### Failure Mode 4: No Segmentation
Looked at aggregate metric without breaking down by geography, platform, user type.

**Feedback:** "Always segment. The drop might be isolated to one platform or user group — that's a huge clue about root cause."

---

### Failure Mode 5: Listed Hypotheses But Didn't Test
Generated 10 hypotheses but didn't use data to eliminate any.

**Feedback:** "Hypotheses are useless without data checks. Test each one explicitly, then eliminate or support with evidence."

---

### Failure Mode 6: No Business Judgment
Found root cause but didn't evaluate if it's actually a problem or recommend action.

**Feedback:** "As a PM, you need business judgment. Is this drop acceptable? What are the trade-offs of fixing it?"

---

**Framework File Version:** 1.0 (Plugin Architecture)  
**Last Updated:** May 2026  
**Category:** debugging  
**Location:** `/plugins/debugging/framework.md`
