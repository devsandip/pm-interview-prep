# G.A.M.E Framework for Goals & Metrics Questions

## What This Framework Is

G.A.M.E is a comprehensive framework for defining product goals, identifying stakeholders, establishing metrics, and planning execution. It's used for "How would you measure success for X?" questions.

**G.A.M.E stands for:**
- **G**oal and Product Rationale
- **A**udience & Actors
- **M**etrics
- **E**xecution and Edge Cases

---

## When to Use This Framework

**Use for questions like:**
- "Define success metrics for [Product/Feature]"
- "How would you measure success for [Product]?"
- "What metrics would you track for [Feature]?"
- "If you were PM for [Product], what's your metrics framework?"

**Core skill being tested:**
Can you think holistically about product success? Do you understand ecosystem dynamics? Can you define the right North Star? Do you consider edge cases?

---

## What This Framework Tests

### Strategic Thinking
- Do you connect product goals to company mission?
- Do you understand market context and competitive dynamics?
- Do you see the broader ecosystem, not just end users?

### Metrics Rigor
- Can you select the right North Star metric?
- Do you define comprehensive metrics (not just one)?
- Do you balance leading/lagging, input/output metrics?

### Systems Thinking
- Do you map the full ecosystem (supply/demand)?
- Do you identify metric relationships and trade-offs?
- Do you think about guardrails, not just optimization?

### Execution Mindset
- Do you consider measurement methodology?
- Do you think about edge cases and gaming?
- Can you translate metrics to actionable goals?

---

## The 4 Steps (20-25 minutes total)

### Step 1: Goal and Product Rationale (3 minutes)

**What to do:**
Establish why this product exists and how it fits the company's strategy.

**Structure:**
```
"Let me start with strategic context:

Company Mission Alignment:
[Product] advances [Company]'s mission of [mission] by [specific connection].
It enables [type of value] through [capability].

Market Context:
- Trends: [What's changing in the market]
- Competitors: [Who else is here, what they're doing]
- Our USP: [What makes our approach unique]

This matters because [strategic importance]."
```

**Example:**
```
"Let me start with strategic context:

Company Mission Alignment:
Instagram Reels advances Meta's mission of bringing the world closer together by enabling creative expression through short-form video. It allows anyone to become a creator, not just consume content.

Market Context:
- Trends: Short-form video consumption up 300% since 2020 (TikTok effect)
- Competitors: TikTok dominates (1B+ users), YouTube Shorts growing fast (2B users)
- Our USP: Instagram's social graph + creator monetization tools + cross-posting to Feed/Stories

This matters because short-form video is THE growth lever for social platforms right now. Without Reels, Instagram loses Gen Z to TikTok."
```

**What evaluator looks for:**
- Named the company mission explicitly
- Connected product to mission (not generic)
- Mentioned market trends with data
- Named competitors and their strengths
- Stated what makes this product different

---

### Step 2: Audience & Actors (4 minutes)

**What to do:**
Map the full ecosystem — all players, not just end users.

**Structure:**
```
"Ecosystem map:

Supply Side:
- [Actor 1]: [What they provide, what they want]
- [Actor 2]: [What they provide, what they want]

Demand Side:
- [Actor 1]: [What they consume, what they want]
- [Actor 2]: [What they consume, what they want]

Platform:
- [What platform needs]

Prioritization:
The most critical actor is [Actor X] because [reason].
The flywheel starts with [Actor Y]: when they [action], it drives [Actor Z] to [action]."
```

**Example:**
```
"Ecosystem map:

Supply Side:
- Creators: Provide content (Reels videos). Want: reach, monetization, tools
- Brands/Advertisers: Provide ad spend. Want: engagement, conversions

Demand Side:
- Viewers: Consume Reels. Want: entertainment, discovery, connection
- Casual Posters: Create occasionally. Want: easy creation, friends seeing their content

Platform:
- Instagram/Meta: Wants engagement, time on platform, ad revenue

Prioritization:
The most critical actor is Creators because without high-quality content, viewers leave.
The flywheel starts with Creators: when they post great Reels, it drives Viewers to watch more, which drives more ad revenue, which funds creator monetization, which attracts more creators."
```

**What evaluator looks for:**
- Mapped supply AND demand sides (not just users)
- Identified platform as a stakeholder
- For each actor, stated what they provide/consume AND what they want
- Picked one critical actor with reasoning
- Explained the flywheel logic

---

### Step 3: Metrics (10 minutes)

**What to do:**
Define comprehensive metrics framework with North Star selection.

**Structure:**
```
"Metrics framework:

[Build AARRR/Pirate Metrics table]

North Star Metric Selection (VITAL framework):
- Candidate 1: [Metric]
  - Value Focused: [H/M/L] — [Why]
  - Intelligible: [Y/N] — [Why]
  - Trackable: [H/M/L] — [Why]
  - Actionable: [Y/N] — [Why]
  - Legitimate: [Y/N] — [Why]
  - Score: [X/5]

- Candidate 2: [Metric]
  [Same scoring]

Chosen North Star: [Metric] with score [X/5]

Primary Metrics (support North Star):
- [Metric 1]: [Why it matters]
- [Metric 2]: [Why it matters]

Ecosystem Metrics (health of stakeholders):
- Creators: [Metric]
- Viewers: [Metric]
- Advertisers: [Metric]

Guardrail Metrics (don't break things):
- User safety: [Metric]
- Content quality: [Metric]
- Platform health: [Metric]

Metric Trade-offs:
Watch time ↑ might → session count ↓ (longer sessions, fewer visits)
How to balance: Track both, optimize for daily time spent (captures both)"
```

**Example:**
```
"Metrics framework:

Pirate Metrics Table:
| Stage | Metric Examples |
|-------|----------------|
| Acquisition | New Reels viewers, Reels tab opens |
| Activation | First Reel watched to completion, First Reel created |
| Retention | D7/D30 Reels viewers, Weekly Reels creators |
| Revenue | Ad impressions in Reels, Reels ad revenue |
| Referral | Reels shared to Stories/DMs, Reels cross-posted |

North Star Metric Selection (VITAL):

Candidate 1: Daily Time Spent in Reels (minutes)
- Value: High — captures engagement, correlates with ad revenue
- Intelligible: Yes — everyone understands "time spent"
- Trackable: High — robust logging, hard to game
- Actionable: Yes — can A/B test content ranking, creation tools
- Legitimate: Medium — can be gamed with auto-play
- Score: 4.5/5

Candidate 2: Weekly Active Reels Creators
- Value: Medium — creator supply matters, but viewer engagement is end goal
- Intelligible: Yes
- Trackable: High
- Actionable: Yes
- Legitimate: High — hard to fake creator activity
- Score: 4/5

Chosen North Star: Daily Time Spent in Reels (4.5/5)

Primary Metrics:
- Reels completion rate: Shows content quality, predicts retention
- Creator post frequency: Leading indicator of content supply health

Ecosystem Metrics:
- Creators: Monthly active creators, avg posts/creator/week
- Viewers: D7 retention, avg sessions/day
- Advertisers: Reels ad CTR, Reels ad revenue per user

Guardrail Metrics:
- User safety: Violation rate in Reels content
- Content quality: Time Well Spent score (user surveys)
- Platform health: Feed cannibalization (Reels views → Feed views down)

Metric Trade-offs:
Watch time ↑ but session count ↓ (fewer, longer sessions)
Balance: Track daily time spent (captures both length × frequency)"
```

**What evaluator looks for:**
- Used VITAL framework to score North Star candidates
- Selected North Star with clear reasoning
- Defined primary metrics that SUPPORT North Star (not random)
- Ecosystem metrics cover all stakeholder groups
- Guardrails include safety, quality, platform health
- Identified at least one metric trade-off with mitigation

---

### Step 4: Execution and Edge Cases (5 minutes)

**What to do:**
Show how you'd actually measure metrics and handle edge cases.

**Structure:**
```
"Execution details:

Measurement Methodology for [Key Metric]:
- Definition: [Exactly how it's measured]
- Edge cases to remove:
  - Bot activity: Filter users with <5 friends
  - Accidental clicks: Require 3+ seconds of watch time
  - Background playback: Only count active screen time
- Cadence: Track daily, report 7-day moving average
- Segmentation: Break down by user cohort, geography, content type

Gaming & Pitfalls:
- Risk: Auto-play inflates watch time without real engagement
  Mitigation: Weight by completion rate (finished videos count more)
- Risk: Algorithm could optimize for clickbait
  Mitigation: Track Time Well Spent score as guardrail

Goal Setting:
- 6-month goal: Increase daily time spent from 10 min → 15 min (+50%)
- Leading indicators: Creator posts +30%, completion rate +10%"
```

**Example:**
```
"Execution details:

Measurement Methodology for Daily Time Spent in Reels:
- Definition: Sum of all seconds spent actively viewing Reels per user per day
- Edge cases to remove:
  - Bot activity: Filter accounts with <5 friends or suspicious patterns
  - Accidental clicks: Require 3+ seconds watch time to count
  - Background playback: Only count time when app is in foreground
- Cadence: Track daily, report 7-day moving average (smooth weekend dips)
- Segmentation: Break down by new vs existing users, age group, geography

Gaming & Pitfalls:
- Risk: Auto-play inflates watch time without real engagement
  Mitigation: Weight by completion rate — 30-sec video watched 10 sec = 33% engagement score
- Risk: Watch time up but session count down (cannibalization)
  Detection: Track both, segment by user cohort
- Risk: Algorithm optimizes for watch time → shows only viral content
  Mitigation: Cap single-creator exposure at 20% of feed

Goal Setting:
- 6-month goal: Daily time spent in Reels 10 min → 15 min (+50%)
- Leading indicators: Creator post frequency +30%, Reels completion rate 60% → 70%
- Lagging indicators: D30 retention +5%, Reels ad revenue +40%"
```

**What evaluator looks for:**
- Defined measurement methodology precisely
- Removed 3+ edge cases (bot, accidental, background, etc.)
- Specified cadence and segmentation approach
- Identified 2+ gaming risks with mitigations
- Set specific numeric goals with timeline

---

## Evaluation Rubric (Total: 10 points)

### Component 1: Goal & Product Rationale (2 points)

**2 points (Excellent):**
- Named company mission explicitly
- Connected product to mission (specific, not generic)
- Mentioned market trends with data
- Named competitors and their approaches
- Stated unique value proposition

**1 point (Partial):**
- Mentioned mission but weak connection OR
- Named competitors but no USP OR
- Missing market context

**0 points (Missing):**
- No strategic context
- Generic "helps users" statements

---

### Component 2: Audience & Actors (2 points)

**2 points (Excellent):**
- Mapped supply AND demand sides
- Identified platform as stakeholder
- For each actor, stated what they provide/want
- Prioritized one critical actor with reasoning
- Explained flywheel logic

**1 point (Partial):**
- Mapped ecosystem but incomplete (only demand OR supply) OR
- No prioritization OR
- No flywheel explanation

**0 points (Missing):**
- Only mentioned "users"
- No ecosystem thinking

---

### Component 3: Metrics (4 points)

**4 points (Excellent):**
- Used VITAL framework to select North Star (scored 2+ candidates)
- Chosen North Star has clear reasoning
- Defined 2+ primary metrics supporting North Star
- Ecosystem metrics for all stakeholder groups
- Guardrails include safety, quality, platform
- Identified metric trade-off with mitigation

**3 points (Good):**
- Selected North Star with some reasoning (but no VITAL) OR
- Missing ecosystem metrics OR
- Missing guardrails OR
- No trade-offs identified

**2 points (Partial):**
- Picked North Star but weak reasoning OR
- Only North Star, no supporting metrics OR
- Metrics list but no categorization

**0 points (Missing):**
- No North Star selected
- Just listed random metrics

---

### Component 4: Execution & Edge Cases (2 points)

**2 points (Excellent):**
- Defined measurement methodology precisely
- Removed 3+ edge cases
- Specified cadence and segmentation
- Identified 2+ gaming risks with mitigations
- Set specific numeric goals

**1 point (Partial):**
- Some measurement details but incomplete OR
- Mentioned edge cases but no mitigations OR
- No goal setting

**0 points (Missing):**
- No execution details
- Just said "we'll track it"

---

## Scoring Interpretation

**9-10 points:** Excellent. Hire strong.
- Strategic thinking + metrics rigor + execution mindset
- Ready for senior PM role

**7-8 points:** Strong. Likely hire.
- Good metrics framework, minor gaps (e.g., weak on edge cases)
- Would succeed with coaching

**5-6 points:** Decent. Mixed signals.
- Selected North Star but weak ecosystem thinking OR
- Good metrics but no execution details

**3-4 points:** Weak. Likely no hire.
- No North Star OR
- Listed metrics without framework

**0-2 points:** Poor. No hire.
- Fundamental gaps in metrics thinking

---

## Time Management Tips

**Total time: 20-25 minutes**

- **Goal & Rationale**: 3 min
- **Audience & Actors**: 4 min
- **Metrics**: 10 min (most important section)
  - Pirate table: 2 min
  - North Star selection: 4 min
  - Primary/Ecosystem/Guardrails: 3 min
  - Trade-offs: 1 min
- **Execution**: 5 min
- **Buffer**: 3 min

**If running out of time:**
- Compress Goal & Actors (2 min each)
- Keep Metrics section (this is the core)
- Skip detailed goal-setting in Execution

---

## Common Failure Modes

### Failure Mode 1: No North Star Selection
Listed 10 metrics but didn't pick THE one that matters most.

**Feedback:** "Metrics frameworks need a North Star. Use VITAL to score candidates and pick one. Everything else should support it."

---

### Failure Mode 2: Only User Metrics
Ignored creators, advertisers, platform — only focused on viewer metrics.

**Feedback:** "Think ecosystem. Reels has supply (creators), demand (viewers), AND platform needs. Metrics must cover all."

---

### Failure Mode 3: No Guardrails
Optimized for engagement without considering safety, quality, or cannibalization.

**Feedback:** "Always define guardrails. Watch time optimization without guardrails → clickbait, unsafe content, Feed cannibalization."

---

### Failure Mode 4: Vanity Metrics
Picked metrics that look good but don't drive business value (e.g., "Reels created" without engagement).

**Feedback:** "Test metrics against VITAL framework. 'Reels created' isn't valuable if no one watches them. North Star must capture real value."

---

### Failure Mode 5: No Edge Cases
Said "track watch time" but didn't consider bots, accidental clicks, background playback.

**Feedback:** "Real-world measurement has noise. Always define edge cases to remove — otherwise your metric is meaningless."

---

### Failure Mode 6: Ignored Trade-offs
Optimized one metric without considering impact on others.

**Feedback:** "Metrics interact. Watch time ↑ but session frequency ↓ might signal cannibalization. Always identify trade-offs."

---

**Framework File Version:** 1.0 (Plugin Architecture)  
**Last Updated:** May 2026  
**Category:** goals-metrics  
**Location:** `/plugins/goals-metrics/framework.md`
