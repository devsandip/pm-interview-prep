# Goals & Metrics Question Generation Rules

## Category Overview

**Category:** Goals & Metrics  
**Question Format:** "Define success metrics for [Product/Feature]" OR "How would you measure [Product]?"  
**Time Limit:** 20-25 minutes  
**Recommended Framework:** G.A.M.E Framework

---

## What This Category Tests

### Core Skills Being Evaluated:
- **Strategic alignment**: Can you connect metrics to company mission?
- **Ecosystem thinking**: Do you see all stakeholders, not just end users?
- **Metrics rigor**: Can you select the right North Star using a framework?
- **Systems thinking**: Do you understand metric relationships and trade-offs?
- **Execution mindset**: Do you consider measurement methodology and edge cases?

### What Interviewers Listen For:
- Do you use VITAL framework to select North Star?
- Do you map supply/demand sides of ecosystem?
- Do you define guardrails, not just optimization metrics?
- Do you think about gaming and edge cases?
- Do you set specific numeric goals?

### Common Failure Modes:
- No North Star selected (just listed 10 metrics)
- Only user metrics (ignored creators, advertisers, platform)
- No guardrails (optimize engagement without safety/quality checks)
- Vanity metrics (look good but don't drive value)
- No edge cases (didn't consider bots, accidental clicks, etc.)

---

## Question Generation Rules

### Product/Feature Selection Pool

**Social Media Features (30%):**
- Instagram Reels, Stories, Live
- Facebook Groups, Marketplace, Dating
- TikTok For You page, Creator Fund
- YouTube Shorts, Community posts
- LinkedIn Feed algorithm, Newsletter platform

**Marketplace/Platform Features (25%):**
- Airbnb Experiences, Flexible dates search
- Uber Pool, Uber Eats subscription
- DoorDash DashPass, Group orders
- Amazon Prime Video, Subscribe & Save

**Creator Economy (20%):**
- YouTube Partner Program, Super Thanks
- Patreon Creator tiers
- Substack paid subscriptions
- Spotify Podcast subscriptions
- TikTok Creator Marketplace

**B2B Products (15%):**
- Slack Huddles, Canvas
- Notion AI, Templates marketplace
- Figma Comments, Dev Mode
- Salesforce Einstein, Slack integration

**Emerging Categories (10%):**
- AR filters (Snapchat Lenses, Instagram Effects)
- Live audio (Twitter Spaces, Spotify Greenroom)
- AI features (ChatGPT plugins, Notion AI)

---

### Required Context Components

**Every question MUST include:**

1. **Product Description:**
   - What it is
   - Who it serves (supply/demand sides if applicable)
   - Current state (users, engagement, revenue if known)

2. **Company Context:**
   - Company mission
   - Strategic priority (growth? monetization? retention?)
   - Competitive landscape

3. **The Challenge:**
   - What problem does this solve?
   - Why metrics matter now?
   - What's at stake?

4. **Ecosystem Hint:**
   - Mention supply AND demand sides (if applicable)
   - Example: "Creators post content, viewers watch, advertisers pay"

---

## Question Template

```markdown
## Question [1 or 2]

**Question:**  
Define success metrics for [Product/Feature at Company]

**Product Description:**
[Product] is [Company]'s [type of product]. It [what it does] for [user segment].

**Current state:**
- [Users/Scale metric]
- [Engagement metric if known]
- [Revenue/Monetization if applicable]

**Company Context:**
- Mission: [Company mission statement]
- Strategic priority: [What company cares about most right now]
- Competitive landscape: [Key competitors, what they're doing]

**The Challenge:**
[Why metrics matter now - is it new? struggling? growing fast? needs monetization?]

**Ecosystem:**
[Quick mention of supply/demand sides or key stakeholders]

**Time Limit:** 20-25 minutes

**Recommended Framework:** G.A.M.E Framework
- **G**oal and Product Rationale
- **A**udience & Actors
- **M**etrics (with VITAL framework for North Star selection)
- **E**xecution and Edge Cases

**Framework Location:** `/plugins/goals-metrics/framework.md`
```

---

## Example Questions

### Example 1: Social Media Feature

**Question:**  
Define success metrics for Instagram Reels

**Product Description:**
Instagram Reels is Meta's short-form video feature launched in 2020 to compete with TikTok. Users create 15-90 second videos with music, effects, and AR filters.

**Current state:**
- 2B Instagram users, 200M create Reels monthly
- Reels makes up 20% of time spent on Instagram (2024)
- Reels ads launched, but monetization lags TikTok

**Company Context:**
- Mission: Meta's mission is to give people the power to build community and bring the world closer together
- Strategic priority: Win short-form video before TikTok dominates Gen Z entirely
- Competitive landscape: TikTok (1.5B users, 52 min/day), YouTube Shorts (2B users, growing fast)

**The Challenge:**
Reels is growing but needs better creator monetization to retain top talent. TikTok pays creators directly (Creator Fund), Instagram only has brand deals. Need metrics framework that balances viewer engagement AND creator economics.

**Ecosystem:**
- Supply: Creators post Reels
- Demand: Viewers watch Reels
- Platform: Meta serves ads, takes revenue share

**Time Limit:** 25 minutes

**Recommended Framework:** G.A.M.E Framework

**Framework Location:** `/plugins/goals-metrics/framework.md`

---

### Example 2: Marketplace Feature

**Question:**  
Define success metrics for Airbnb Experiences

**Product Description:**
Airbnb Experiences are activities hosted by locals (cooking classes, guided tours, workshops). Launched 2016 to expand beyond accommodation into full travel platform.

**Current state:**
- 40K Experiences in 1,000+ cities
- Experiences are <5% of Airbnb revenue ($8.4B total in 2023)
- Hosts earn avg $150/experience

**Company Context:**
- Mission: Create a world where anyone can belong anywhere
- Strategic priority: Diversify beyond accommodation (regulatory risk, competition)
- Competitive landscape: Viator (TripAdvisor), GetYourGuide, local tour operators

**The Challenge:**
Experiences has supply (hosts) but low demand (guest discovery is poor). Only 10% of Airbnb guests book an Experience. Need metrics to drive both supply quality AND demand growth.

**Ecosystem:**
- Supply: Experience hosts create listings
- Demand: Guests book and attend Experiences
- Platform: Airbnb takes 20% commission

**Time Limit:** 20 minutes

**Recommended Framework:** G.A.M.E Framework

**Framework Location:** `/plugins/goals-metrics/framework.md`

---

### Example 3: Creator Economy

**Question:**  
Define success metrics for Spotify Podcast Subscriptions

**Product Description:**
Spotify Podcast Subscriptions let podcasters offer premium content (ad-free, bonus episodes, early access) for $2.99-$9.99/month. Spotify takes 5% commission (vs Apple's 15-30%).

**Current state:**
- 5M podcasts on Spotify, 500M total users
- Subscriptions launched 2021, adoption <1% of podcasters
- YouTube and Patreon dominate creator monetization

**Company Context:**
- Mission: Unlock the potential of human creativity
- Strategic priority: Keep top podcasters from leaving to YouTube/Apple
- Competitive landscape: YouTube (memberships, Super Thanks), Patreon ($300M+ to creators annually)

**The Challenge:**
Joe Rogan, Call Her Daddy exclusive deals expire 2026-27. Need native monetization tools to re-sign creators without $100M+ guarantees. Metrics must show path to creator revenue.

**Ecosystem:**
- Supply: Podcasters create premium content
- Demand: Listeners subscribe for premium access
- Platform: Spotify takes 5% commission + ad revenue on free tier

**Time Limit:** 20 minutes

**Recommended Framework:** G.A.M.E Framework

**Framework Location:** `/plugins/goals-metrics/framework.md`

---

## Quality Checklist

Before finalizing each question, verify:

- [ ] Product/feature is from approved pool
- [ ] Company mission stated
- [ ] Current state includes scale metrics
- [ ] Challenge/strategic priority is clear
- [ ] Ecosystem sides mentioned (supply/demand or key stakeholders)
- [ ] Time limit is 20-25 minutes
- [ ] Framework recommendation is "G.A.M.E Framework"
- [ ] Framework file path is included

---

## Difficulty Calibration

**Medium (60% of questions):**
- Well-known product (Instagram, YouTube, Airbnb)
- Clear two-sided marketplace OR single user group
- Straightforward ecosystem
- Obvious North Star candidates

**Hard (30% of questions):**
- Less common product OR
- Complex ecosystem (3+ stakeholder groups) OR
- Competing metrics (growth vs monetization tension) OR
- New product category (unclear what "success" means)

**Very Hard (10% of questions):**
- B2B product with multiple buyer personas OR
- Platform with 4+ stakeholder groups OR
- Regulatory constraints on metrics OR
- Privacy concerns limit tracking

---

## Variety Rules

**Weekly:**
- Don't repeat the same product 2 days in a row
- Mix social/marketplace/creator economy/B2B
- Vary ecosystem complexity (simple 2-sided vs complex multi-sided)

**Product Type Distribution:**
- 30% Social media features
- 25% Marketplace/platform features
- 20% Creator economy
- 15% B2B products
- 10% Emerging categories

---

## Meta-Specific Guidance

Since these questions are common at Meta, include this note in questions:

**Note:** This question is commonly asked at Meta/Facebook PM interviews. Focus on:
- Connecting to Meta's mission ("bring the world closer together")
- Two-sided ecosystem thinking (creators/viewers, buyers/sellers)
- VITAL framework for North Star selection
- Guardrails (safety, quality, platform health)

---

**Module Version:** 1.0 (Plugin Architecture)  
**Last Updated:** May 2026  
**Category:** goals-metrics  
**Location:** `/plugins/goals-metrics/generation-rules.md`
