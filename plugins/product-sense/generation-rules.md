# Product Sense Question Generator Module

## Category Overview

**Category:** Product Sense (Type E)  
**Question Format:** "Design a product for [User/Use Case]" OR "How would you improve [Product]?"  
**Time Limit:** 20-25 minutes  
**Recommended Frameworks:** MILEJPSR or CIRCLES

---

## What This Category Tests

### Core Skills Being Evaluated:
- **Product intuition**: Can you identify real user problems?
- **User empathy**: Do you understand user needs deeply?
- **Design thinking**: Can you structure ambiguous problems?
- **Solution creativity**: Can you generate diverse solutions?
- **Prioritization**: Can you choose the best option with clear reasoning?
- **Business sense**: Do you consider feasibility, metrics, and trade-offs?

### What Interviewers Listen For:
- Do you clarify before solving?
- Do you segment users and pick ONE?
- Do you identify needs (not features)?
- Do you generate multiple solutions (not just one)?
- Do you evaluate trade-offs honestly?
- Do you show conviction in your recommendation?

### Common Failure Modes:
- Jumping to solution without understanding the problem
- Designing for "all users" instead of picking one segment
- Listing features instead of identifying needs
- Generating only one solution (no alternatives considered)
- Ignoring trade-offs or feasibility
- Weak recommendation (no conviction)

---

## Question Generation Rules

### Question Type Distribution

**60% Design from Scratch:**
- "Design a product for [User Segment]"
- "Design a [Product Category] for [Company]"
- "How would you help [Users] with [Problem]?"

**40% Improve Existing:**
- "How would you improve [Product]?"
- "What feature would you add to [Product]?"
- "If you were PM for [Product], what would you build?"

---

### Question Type 1: Design from Scratch

**Format:** "Design a [Product/Feature] for [User Segment/Use Case]"

**User Segment Examples:**
- **Demographic-based**: Elderly, teenagers, parents, professionals
- **Behavior-based**: Commuters, travelers, remote workers, content creators
- **Context-based**: People moving to a new city, first-time home buyers, students preparing for exams

**Use Case Examples:**
- Help [users] stay connected
- Help [users] stay productive
- Help [users] make better decisions
- Help [users] save time/money
- Help [users] learn/improve skills

**Company Context (optional):**
- "Design a product for Google to help..."
- "Design a feature for Facebook to..."
- "What would you build for Amazon to..."

**Required Elements:**
- Clear user segment OR use case
- Enough ambiguity to require clarification
- Not too constrained (room for creativity)
- Not too broad (can be scoped in 20 min)

---

### Question Type 2: Improve Existing Product

**Format:** "How would you improve [Product]?" OR "What feature would you add to [Product]?"

**Product Selection Pool:**

**Consumer Apps (50%):**
- Social: Instagram, LinkedIn, Twitter/X, Reddit, Discord
- Video: YouTube, TikTok, Netflix, Twitch
- Audio: Spotify, Podcasts, Clubhouse
- Productivity: Notion, Evernote, Todoist, Google Calendar
- Communication: WhatsApp, Telegram, Slack, Zoom
- Marketplace: Airbnb, Uber, DoorDash, Etsy
- Finance: Venmo, Cash App, Robinhood, Mint

**B2B Products (30%):**
- Collaboration: Slack, Miro, Figma, Notion
- Sales/CRM: Salesforce, HubSpot, Gong
- Dev Tools: GitHub, Linear, Jira
- Analytics: Mixpanel, Amplitude, Tableau

**Indian Products (20%):**
- PhonePe, Paytm, Swiggy, Zomato, Cred, Meesho

**Specificity Variations:**
- **Broad**: "How would you improve Instagram?"
- **Focused**: "How would you improve Instagram Stories?"
- **Goal-oriented**: "How would you improve retention for Netflix?"
- **User-focused**: "How would you improve Spotify for podcast listeners?"

---

## Question Template

### Template 1: Design from Scratch

```markdown
## Question [1 or 2]

**Question:**  
Design a product to help [User Segment] with [Use Case/Problem]

**Context:**  
[Optional: Company context, constraints, strategic priority]

**Time Limit:** 20-25 minutes

**Recommended Framework:** MILEJPSR or CIRCLES

**Framework Locations:**
- MILEJPSR: `plugins/product-sense/framework-milejpsr.md`
- CIRCLES: `plugins/product-sense/framework-circles.md`

**Evaluation Criteria:**
- Did you clarify the situation (company, goal, constraints)?
- Did you segment users and pick ONE?
- Did you identify needs (not features)?
- Did you generate 3+ diverse solutions?
- Did you evaluate trade-offs?
- Did you define success metrics?
- Did you show conviction in your recommendation?
```

---

### Template 2: Improve Existing Product

```markdown
## Question [1 or 2]

**Question:**  
How would you improve [Product] [optional: for User Segment / to achieve Goal]?

**Product Context:**
- **What it does**: [Brief description]
- **Current state**: [Users, revenue, key metrics if known]
- **Known challenges**: [Optional: mention 1-2 challenges if relevant]

**Time Limit:** 20-25 minutes

**Recommended Framework:** MILEJPSR or CIRCLES

**Framework Locations:**
- MILEJPSR: `plugins/product-sense/framework-milejpsr.md`
- CIRCLES: `plugins/product-sense/framework-circles.md`

**Evaluation Criteria:**
- Did you clarify the goal (improve engagement? retention? monetization?)?
- Did you segment users and pick ONE?
- Did you map the current experience and identify pain points?
- Did you prioritize ONE pain to solve?
- Did you generate 3+ diverse solutions?
- Did you evaluate trade-offs?
- Did you define success metrics?
```

---

## Example Questions

### Example 1: Design from Scratch (Demographic)

**Question:**  
Design a product to help elderly people (65+) stay connected with their family

**Context:**  
Assume you're designing for a major tech company (Google, Facebook, or Apple). No specific constraints on technology or budget. Success = daily active usage and sustained family connections.

**Time Limit:** 25 minutes

**Recommended Framework:** MILEJPSR (allows for Mission/strategic context)

**Framework Location:** `plugins/product-sense/framework-milejpsr.md`

---

### Example 2: Design from Scratch (Behavior-based)

**Question:**  
Design a product for commuters to make better use of their commute time

**Context:**  
Focus on public transit commuters (subway, bus, train) in major US cities. Commute times range from 30-90 minutes each way. Assume mobile-first environment with intermittent connectivity.

**Time Limit:** 20 minutes

**Recommended Framework:** CIRCLES (good for clarifying ambiguous "better use" goal)

**Framework Location:** `plugins/product-sense/framework-circles.md`

---

### Example 3: Design from Scratch (Use Case)

**Question:**  
Design a feature to help remote workers build stronger connections with their team

**Context:**  
Post-pandemic, 40% of knowledge workers are fully remote. Companies report declining "team cohesion" and "spontaneous collaboration." Design a feature that could be added to any collaboration platform (Slack, Zoom, Teams, etc.).

**Time Limit:** 20 minutes

**Recommended Framework:** CIRCLES

**Framework Location:** `plugins/product-sense/framework-circles.md`

---

### Example 4: Improve Existing (Broad)

**Question:**  
How would you improve Spotify?

**Product Context:**
- **What it does**: Music and podcast streaming platform
- **Current state**: 500M users, 200M premium subscribers, $13B revenue
- **Known challenges**: Podcast monetization lagging, competition from Apple/YouTube

**Time Limit:** 25 minutes

**Recommended Framework:** MILEJPSR (broad question benefits from strategic context)

**Framework Location:** `plugins/product-sense/framework-milejpsr.md`

---

### Example 5: Improve Existing (Focused)

**Question:**  
How would you improve LinkedIn's messaging experience?

**Product Context:**
- **What it does**: Professional networking platform with messaging feature
- **Current state**: 950M users, messaging used primarily for recruiting/sales outreach
- **Known challenges**: High spam rate, low engagement (most messages go unanswered)

**Time Limit:** 20 minutes

**Recommended Framework:** CIRCLES (focused scope fits 20 min)

**Framework Location:** `plugins/product-sense/framework-circles.md`

---

### Example 6: Improve Existing (Goal-oriented)

**Question:**  
How would you improve retention for Netflix?

**Product Context:**
- **What it does**: Streaming platform for movies and TV shows
- **Current state**: 250M subscribers, but churn increasing (11% annual in 2024 vs 8% in 2020)
- **Known challenges**: Content costs rising, password sharing crackdown causing churn, competition from Disney+/Prime

**Time Limit:** 25 minutes

**Recommended Framework:** MILEJPSR (retention requires strategic thinking)

**Framework Location:** `plugins/product-sense/framework-milejpsr.md`

---

## Quality Checklist

Before finalizing each question, verify:

- [ ] Question is clear (not too vague, not too constrained)
- [ ] User segment OR use case is specified
- [ ] For "improve" questions: product context is provided
- [ ] Time limit is appropriate (20 min for focused, 25 min for broad)
- [ ] Framework recommendation matches question type
- [ ] Framework file path is included
- [ ] Evaluation criteria are listed

---

## Difficulty Calibration

**Medium (60% of questions):**
- Clear user segment
- Familiar product (if "improve" question)
- Reasonable scope (can be completed in time limit)

**Hard (30% of questions):**
- Ambiguous user segment (requires heavy clarification) OR
- Less familiar product OR
- Broad scope (requires aggressive prioritization)

**Very Hard (10% of questions):**
- Multiple competing user segments OR
- Niche product with complex ecosystem OR
- Requires deep domain knowledge

---

## Variety Rules

**Weekly:**
- Don't repeat the same product 2 days in a row
- Mix design/improve (60/40 split)
- Mix consumer/B2B/Indian products

**Question Source Variety:**
- 50% Consumer apps
- 30% B2B products
- 20% Indian products

**User Segment Variety:**
- Rotate demographics (elderly, students, parents, etc.)
- Rotate behaviors (commuters, travelers, remote workers, etc.)
- Rotate contexts (new city, buying home, learning skill, etc.)

---

## Framework Guidance for Candidates

**Include this guidance in every question file:**

### When to Use MILEJPSR:
- Question has strategic context (company, market, competition)
- You have 25 minutes
- You want to show prioritization frameworks (SFARU, SCARU, EAC)
- Question is "build for [Company]" or "improve [Product]"

### When to Use CIRCLES:
- Question is more ambiguous (needs heavy clarification)
- You have 20 minutes
- Question is "design a product for [use case]"
- You want a simpler, more linear structure

### Both frameworks work for most questions
- MILEJPSR is more comprehensive (longer)
- CIRCLES is more streamlined (shorter)
- Pick based on time available and question type

---

**Module Version:** 1.0  
**Last Updated:** May 2026  
