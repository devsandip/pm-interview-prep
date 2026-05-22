# Debugging & Diagnosis Question Generation Rules

## Category Overview

**Category:** Debugging  
**Question Format:** "[Metric] dropped [X%] — diagnose" OR "[Product] engagement decreased — investigate"  
**Time Limit:** 20 minutes  
**Recommended Framework:** S.I.E.V.E Framework

---

## What This Category Tests

### Core Skills Being Evaluated:
- **Structured thinking**: Do you scope before hypothesizing?
- **MECE hypothesis generation**: Do you cover all possible causes systematically?
- **Data fluency**: Can you segment data to isolate issues?
- **Causal reasoning**: Can you distinguish correlation from causation?
- **Business judgment**: Do you recommend appropriate action?

### What Interviewers Listen For:
- Do you check measurement issues FIRST?
- Do you use MECE buckets (Measurement, External, Internal, User Behavior)?
- Do you segment by geography, platform, user type?
- Do you validate root cause with supporting evidence?
- Do you evaluate trade-offs before recommending action?

### Common Failure Modes:
- Jumped to conclusion without scoping
- Ignored measurement/data issues
- Assumed correlation = causation
- No data segmentation
- Listed hypotheses but didn't test them
- No business judgment on whether it's a problem

---

## Question Generation Rules

### Metric Selection Pool

**Engagement Metrics (40%):**
- DAU/MAU/WAU
- Time spent (daily, per session)
- Session frequency
- Content creation rate (posts, uploads, shares)
- Content consumption (views, reads, watches)

**Retention Metrics (25%):**
- D7/D30 retention
- Churn rate
- Resurrection rate
- Stickiness (DAU/MAU ratio)

**Monetization Metrics (20%):**
- Revenue (total, per user, per transaction)
- Conversion rate
- ARPU (Average Revenue Per User)
- Purchase frequency
- Cart abandonment

**Product-Specific Metrics (15%):**
- Stories DAU (Instagram/Snapchat)
- Reels watch time (Instagram/Facebook)
- Match rate (dating apps)
- Booking conversion (travel/marketplace)
- Ad click-through rate

---

### Drop Magnitude Pool

**Medium (60%):**
- 5-15% drop
- Clear signal, not noise
- Large enough to investigate

**Hard (30%):**
- 15-30% drop
- Severe, urgent
- Multiple stakeholders affected

**Very Hard (10%):**
- 3-5% drop (hard to distinguish from noise) OR
- 30%+ drop (catastrophic, many possible causes)

---

### Product Selection Pool

**Social Media (30%):**
- Instagram, Facebook, TikTok, Snapchat, Twitter/X, LinkedIn
- Features: Stories, Reels, Feed, Messages, Groups

**Marketplace (25%):**
- Airbnb, Uber, DoorDash, Amazon, eBay, Etsy
- Features: Search, booking, payments, reviews

**Content Platforms (20%):**
- YouTube, Spotify, Netflix, Twitch
- Features: Recommendations, subscriptions, live streams

**B2B/Productivity (15%):**
- Slack, Notion, Figma, Salesforce, Zoom
- Features: Collaboration, integrations, admin tools

**Emerging (10%):**
- Dating apps (Tinder, Hinge, Bumble)
- Fintech (PayPal, Venmo, Cash App)
- Health/Fitness (Peloton, Strava, MyFitnessPal)

---

### Required Context Components

**Every question MUST include:**

1. **Metric Definition:**
   - Exact metric name
   - How it's measured
   - Typical range/baseline

2. **Drop Magnitude:**
   - Percentage drop
   - Absolute numbers (before → after)
   - Timeframe (when it started, duration)

3. **Product Context:**
   - What the product/feature does
   - User base size
   - Recent changes or events

4. **Initial Data Points (3-5):**
   - Segment breakdowns (e.g., iOS vs Android)
   - Related metric movements
   - Temporal pattern (sudden vs gradual)

5. **Ambiguity:**
   - At least 2 plausible root causes
   - Some red herrings
   - Requires data exploration to solve

---

## Question Template

```markdown
## Question [1 or 2]

**Question:**  
[Product]'s [Metric] dropped [X%] over the past [timeframe]. Diagnose the issue and recommend action.

**Metric Definition:**
[Metric] is defined as [exact definition]. It's measured by [methodology]. Normal baseline is [range].

**The Drop:**
- Magnitude: [X%] drop ([absolute numbers]: [before] → [after])
- Timeline: Started [when], [ongoing/stabilized]
- Pattern: [Sudden/gradual] [one-time/continuing]

**Product Context:**
[Product] is [description]. It has [user base size]. [Key feature/value prop].

**Recent Changes:**
- [Change 1]: [What happened, when]
- [Change 2]: [What happened, when]
- [External event if any]

**Initial Data Points:**
You have access to the following data:

1. **Segment breakdown:**
   - [Dimension 1]: [Segment A] -X%, [Segment B] -Y%
   - [Dimension 2]: [Segment C] -Z%, [Segment D] -W%

2. **Related metrics:**
   - [Metric 2]: [Changed by X%]
   - [Metric 3]: [Changed by Y%]

3. **Temporal pattern:**
   - [Pattern description]

4. **Other context:**
   - [Additional clue or red herring]

**Your Task:**
Use the S.I.E.V.E framework to diagnose root cause and recommend action.

**Time Limit:** 20 minutes

**Recommended Framework:** S.I.E.V.E Framework
- **S**cope and Clarity
- **I**nitial Hypothesis (MECE)
- **E**xplore & Eliminate
- **V**alidate Root Cause
- **E**valuate and Execute

**Framework Location:** `/plugins/debugging/framework.md`
```

---

## Quality Checklist

Before finalizing each question, verify:

- [ ] Metric is clearly defined
- [ ] Drop magnitude is realistic (5-30%)
- [ ] Timeline is specified
- [ ] 3-5 initial data points provided
- [ ] At least 2 plausible root causes exist
- [ ] Product context is sufficient
- [ ] Recent changes are mentioned
- [ ] Question is ambiguous enough to require S.I.E.V.E process

---

## Difficulty Calibration

**Medium (60%):**
- Clear metric definition
- 10-15% drop
- 3-4 data points hint at root cause
- 2-3 plausible hypotheses

**Hard (30%):**
- Complex product (multi-sided marketplace) OR
- Many recent changes (4-5) OR
- Conflicting data points OR
- Drop affects multiple metrics

**Very Hard (10%):**
- Small drop (5-7%) hard to distinguish from noise OR
- Catastrophic drop (30%+) with many possible causes OR
- Measurement methodology changed recently (is it real?) OR
- Multiple concurrent A/B tests running

---

## Variety Rules

**Weekly:**
- Mix engagement, retention, monetization metrics
- Don't repeat same product 2 days in a row
- Vary drop magnitude (avoid always 10%)
- Alternate obvious vs. subtle root causes

**Product Type Distribution:**
- 30% Social media
- 25% Marketplace
- 20% Content platforms
- 15% B2B/Productivity
- 10% Emerging categories

---

## Root Cause Categories (For Variety)

**Rotate these root causes:**
- Measurement/logging bug (20%)
- Internal feature cannibalization (25%)
- External competitor move (15%)
- Algorithm change side effect (20%)
- Seasonal/temporal pattern (10%)
- User segment mix shift (10%)

---

**Module Version:** 1.0 (Plugin Architecture)  
**Last Updated:** May 2026  
**Category:** debugging  
**Location:** `/plugins/debugging/generation-rules.md`
