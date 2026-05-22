# Tech Application Question Generator Module

## Category Overview

**Category:** Tech Application (Type C)  
**Question Format:** "How would you use [Technology] at/for/in [Company/Domain]?"  
**Time Limit:** 20 minutes  
**Recommended Framework:** Capabilities Matrix Framework

---

## What This Category Tests

### Core Skills Being Evaluated:
- **Technology understanding**: Do you actually know how [AI/blockchain/AR] works?
- **Domain expertise**: Do you understand the company/industry context?
- **Concrete thinking**: Can you go from "use AI" to specific use cases with details?
- **Prioritization**: Can you pick the highest-impact use case vs. listing 10?
- **Feasibility assessment**: Do you understand technical/operational constraints?

### What Interviewers Listen For:
- Do you clarify scope? ("By SDLC, do you mean internal dev or delivery lifecycle?")
- Can you map technology capabilities to business problems systematically?
- Do you explain HOW the technology solves the problem (not just "use AI")?
- Can you prioritize use cases and defend your choice?
- Do you acknowledge constraints (data availability, technical maturity, cost)?

### Common Failure Modes:
- Buzzword bingo ("Use AI for personalization") without details
- Listing 10 use cases without prioritization
- Ignoring constraints (assumes infinite data, mature tech, no cost)
- Not connecting to business outcomes (how does this improve revenue/cost/experience?)
- Misunderstanding the technology (blockchain for everything!)

---

## Question Generation Rules

### Technology Selection Pool

**AI/ML (50% of questions):**
- **LLMs**: GPT-4, Claude, Llama for text generation, chat, summarization
- **Computer Vision**: Image recognition, object detection, OCR
- **NLP**: Sentiment analysis, entity extraction, translation
- **Recommendation Systems**: Collaborative filtering, content-based
- **Predictive Analytics**: Forecasting, anomaly detection, classification

**Emerging Tech (20% of questions):**
- **Blockchain**: Smart contracts, decentralized ledgers, tokenization
- **Web3**: NFTs, DAOs, decentralized identity
- **Crypto**: Payment rails, DeFi primitives

**Spatial Computing (15% of questions):**
- **AR**: Augmented reality overlays, try-before-you-buy
- **VR**: Virtual environments, immersive experiences
- **Mixed Reality**: Physical-digital integration

**Connected Tech (10% of questions):**
- **IoT**: Sensors, connected devices, telemetry
- **Edge Computing**: Processing at the edge vs cloud
- **5G Applications**: Real-time, high-bandwidth use cases

**Interface Tech (5% of questions):**
- **Voice UI**: Voice assistants, voice commands
- **Conversational AI**: Chatbots, dialogue systems
- **Gesture Control**: Motion tracking, spatial interaction

---

### Domain Selection Pool

**Consumer Apps (30% of questions):**
- Spotify, Airbnb, DoorDash, Instagram, LinkedIn
- Netflix, Uber, Pinterest, Reddit, Discord
- TikTok, Snapchat, Duolingo, Peloton

**B2B Products (30% of questions):**
- Slack, Notion, Figma, Salesforce, Zoom
- HubSpot, Asana, Miro, Linear, Loom
- Stripe, Plaid, Twilio, MongoDB

**Vertical Industries (25% of questions):**
- Healthcare: EMRs, telemedicine, diagnostics
- Education: LMS, tutoring, assessment
- Logistics: Routing, warehouse, last-mile
- Manufacturing: Quality control, predictive maintenance
- Agriculture: Precision farming, yield prediction
- Finance: Fraud detection, underwriting, trading

**Internal Functions (15% of questions):**
- SDLC: Development, testing, deployment, monitoring
- Customer Support: Ticketing, chat, knowledge base
- Sales: Lead scoring, pipeline management, forecasting
- Marketing: Personalization, attribution, content generation
- Operations: Inventory, scheduling, workforce planning

---

### Required Context Components

**Every question MUST include:**

1. **What They Do:**
   - Business description
   - Core product/service
   - User/customer segment

2. **Current Tech Stack:**
   - What technology they use today (if known)
   - Level of technical maturity
   - Existing AI/ML/automation

3. **Pain Points:**
   - Specific problems that exist
   - Quantified where possible (cost, time, error rate)
   - Impact on business metrics

4. **Scale:**
   - Users, transactions, data volume
   - Team size (if internal function)
   - Geographic footprint

5. **Constraints:**
   - Data availability (do they have the data to train models?)
   - Technical maturity (is the technology ready?)
   - Cost (what's the budget/ROI threshold?)
   - Regulatory (GDPR, HIPAA, financial regulations)

---

## Question Template

```markdown
## Question [1 or 2]

**Question:**  
How would you use [Technology] at/for/in [Company/Domain]?

**Domain/Company Context:**

**What they do:**  
[Business description]

**Current tech:**  
[What technology they use today, level of maturity]

**Pain points:**  
[Specific problems with numbers]
- [Pain point 1]: [Cost/time/error rate]
- [Pain point 2]: [Impact on metrics]
- [Pain point 3]: [User friction]

**Scale:**  
- [Metric 1]: [Number] (e.g., 10M users, 50K transactions/day)
- [Metric 2]: [Number] (e.g., 500 support agents, 100K tickets/month)
- [Metric 3]: [Number] (e.g., 20 warehouses, 5M packages/month)

**Constraints:**  
- **Data**: [What data is available? What's missing?]
- **Technical maturity**: [Is the tech ready? Proven? Experimental?]
- **Cost**: [Budget constraints? ROI expectations?]
- **Regulatory**: [Compliance requirements? Privacy concerns?]

**Time Limit:** 20 minutes

**Recommended Framework:** Capabilities Matrix Framework
1. **Clarify** scope (if ambiguous)
2. **Map** technology capabilities × business problems
3. **Prioritize** use cases (top 3, ranked)
4. **Deep Dive** on #1 use case
5. **Rollout** plan (Phase 1 → 2 → 3)

**Framework Location:** `plugins/tech-application/framework.md`
```

---

## Example Questions

### Example 1: LLMs in Customer Support

**Question:**  
How would you use LLMs in customer support at Razorpay?

**Domain/Company Context:**

**What they do:**  
Razorpay is India's payment gateway and neobanking platform. 10M merchants use Razorpay for payment processing, business banking, and capital.

**Current tech:**  
Traditional ticket-based support system (Zendesk), rule-based chatbot (catches 20% of queries), human agents for complex cases.

**Pain points:**  
- **Volume**: 500K tickets/month, growing 30% YoY
- **Resolution time**: 24 hours average (Tier 1), 48 hours (Tier 2)
- **Cost**: $8M/year support cost (1,500 agents @ $5.3K/agent/year)
- **Repeat tickets**: 60% are repetitive (payment status, settlement delays, API docs)
- **Agent churn**: 40% annual turnover (support burnout)

**Scale:**  
- 10M merchants (1M active monthly)
- 500K support tickets/month
- 1,500 support agents (800 Tier 1, 500 Tier 2, 200 Tier 3)
- 150B rupees processed monthly

**Constraints:**  
- **Data**: 5 years of ticket history (3M tickets), resolution notes, customer satisfaction scores
- **Technical maturity**: LLMs proven for support (Stripe, Intercom use them), but Hindi/regional language support needed (40% of merchants prefer Hindi)
- **Cost**: LLM inference costs ~$0.02/query, need <$2M/year budget to stay profitable
- **Regulatory**: PCI-DSS compliance (can't expose payment card data to LLM)

**Time Limit:** 20 minutes

**Recommended Framework:** Capabilities Matrix Framework

**Framework Location:** `plugins/tech-application/framework.md`

---

### Example 2: Computer Vision in Logistics

**Question:**  
How would you use computer vision for quality control at Delhivery warehouses?

**Domain/Company Context:**

**What they do:**  
Delhivery is India's largest 3PL logistics provider with warehousing, sorting, and last-mile delivery. Processes 30M packages/month across 20 fulfillment centers.

**Current tech:**  
Manual inspection at warehouse intake (workers check package condition, weight, dimensions). Barcode scanners for tracking. No automation in quality control.

**Pain points:**  
- **Damage rate**: 3% of packages arrive damaged (merchants blame Delhivery)
- **Mis-sorts**: 2% of packages routed to wrong destinations (adds 1-2 day delay)
- **Throughput**: Manual inspection bottleneck (60 packages/hour/worker vs. 120 theoretical)
- **Liability**: ₹400M/year in damage claims, refunds, re-shipping costs
- **Fraud**: Merchants sometimes claim "damage" on undamaged goods (5% false claims, hard to dispute)

**Scale:**  
- 30M packages/month across 20 warehouses
- 5,000 warehouse workers (200-300 per facility)
- Peak: 100M packages in Q4 (festive season)
- 10K inbound trucks/day

**Constraints:**  
- **Data**: Can collect package images (don't have historical dataset yet), need to build
- **Technical maturity**: Computer vision for defect detection is mature (Amazon uses it), but Indian warehouse lighting/conditions vary
- **Cost**: Camera infrastructure ₹5 crores/warehouse (₹100 crores total), need 2-year ROI
- **Operational**: Workers are skeptical of automation (union resistance), need change management

**Time Limit:** 20 minutes

**Recommended Framework:** Capabilities Matrix Framework

**Framework Location:** `plugins/tech-application/framework.md`

---

### Example 3: AR in E-commerce

**Question:**  
How would you integrate AR into Nykaa's beauty shopping experience?

**Domain/Company Context:**

**What they do:**  
Nykaa is India's leading beauty e-commerce platform (makeup, skincare, haircare). Mix of marketplace (brands sell on Nykaa) and owned brands (Nykaa Cosmetics).

**Current tech:**  
Standard e-commerce (product images, reviews, filters). No AR/try-on features yet. Mobile-first (80% traffic from app).

**Pain points:**  
- **Return rate**: 25% for makeup (wrong shade, looks different in person)
- **Conversion**: Browse-to-purchase 8% (vs. 12-15% for Sephora in US)
- **Uncertainty**: 60% of users in surveys say "wish I could see how it looks on me"
- **Category-specific**: Lipstick, foundation have 30-35% return rates (highest)
- **Competition**: Sephora India launched AR try-on in 2025 (taking market share)

**Scale:**  
- 20M users (5M monthly active)
- 2M SKUs (makeup, skincare, fragrance, personal care)
- 2,000 brands, 50 owned-brand SKUs
- $500M GMV, $100M revenue (20% take rate)

**Constraints:**  
- **Data**: Need 3D models of products (lipsticks, foundations), skin tone datasets (Indian skin tones underrepresented in training data)
- **Technical maturity**: AR try-on is proven (L'Oréal, Sephora, ModiFace), but needs mobile compute power (older Android phones struggle)
- **Cost**: Licensing ModiFace costs $2M/year, building in-house costs $5M (18 months), need to choose
- **UX**: AR features can feel gimmicky if not done well (need real product value, not just marketing)

**Time Limit:** 20 minutes

**Recommended Framework:** Capabilities Matrix Framework

**Framework Location:** `plugins/tech-application/framework.md`

---

## Quality Checklist

Before finalizing each question, verify:

- [ ] Technology is from the approved pool (or justified if not)
- [ ] Domain/company matches distribution (30% consumer, 30% B2B, 25% vertical, 15% internal)
- [ ] All 5 context components included (what they do, current tech, pain points, scale, constraints)
- [ ] Pain points are quantified (cost, time, error rate)
- [ ] Constraints are realistic and specific
- [ ] Time limit is 20 minutes
- [ ] Framework recommendation is "Capabilities Matrix Framework"
- [ ] Framework file path is included

---

## Difficulty Calibration

**Medium (60% of questions):**
- Proven technology (LLMs, computer vision)
- Clear use cases
- Sufficient data available
- Straightforward constraints

**Hard (30% of questions):**
- Emerging technology (Web3, mixed reality) OR
- Complex domain (regulated industries) OR
- Data scarcity OR
- Multiple competing constraints

**Very Hard (10% of questions):**
- Experimental technology (quantum, brain-computer interface) AND
- Novel domain OR
- Regulatory minefield OR
- Requires deep technical + domain expertise

---

## Variety Rules

**Weekly:**
- Don't repeat the same technology 2 days in a row
- Mix AI/emerging/spatial/connected across the week
- Vary domains (consumer, B2B, vertical, internal)

**Technology Distribution (monthly):**
- 50% AI/ML (the hot topic)
- 20% Emerging (blockchain, Web3)
- 15% Spatial (AR, VR)
- 10% Connected (IoT, edge)
- 5% Interface (voice, gesture)

---

**Module Version:** 1.0  
**Last Updated:** May 2026  
