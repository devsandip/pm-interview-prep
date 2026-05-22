# Debugging & Diagnosis Example Questions

## Example 1: Social Media Cannibalization

**Question:**  
Instagram Stories DAU dropped 10% over the past 2 weeks. Diagnose the issue and recommend action.

**Metric Definition:**
Stories DAU = unique users who posted or viewed at least 1 Story per day. Measured via client-side events (story_view, story_post). Normal baseline is 480-520M DAU.

**The Drop:**
- Magnitude: 10% drop (500M → 450M DAU)
- Timeline: Started 2 weeks ago, declining -1%/week
- Pattern: Gradual, not sudden

**Product Context:**
Instagram Stories are ephemeral 24-hour photo/video posts. 2B Instagram users total, 500M were daily Stories users before the drop. Stories drives DMs and social connection.

**Recent Changes:**
- Reels algorithm update 3 weeks ago: Increased Reels in Feed by 40%
- iOS 17 privacy update 1 month ago
- TikTok launched "Photo Mode" 1 month ago

**Initial Data Points:**

1. **Platform:**
   - iOS: -18%
   - Android: -8%
   - Web: -3%

2. **Age:**
   - 18-24: -20%
   - 25-34: -8%
   - 35+: -3%

3. **Geography:**
   - US: -15%
   - EU: -12%
   - Asia: -5%

4. **Related metrics:**
   - Reels time: +15%
   - Stories tab opens: -12%
   - Instagram DAU: +0.5% (stable)

**Time Limit:** 20 minutes

**Recommended Framework:** S.I.E.V.E Framework

**Framework Location:** `/plugins/debugging/framework.md`

---

## Example 2: Marketplace Conversion

**Question:**  
Airbnb booking conversion rate dropped 15% over the past week. Diagnose the issue and recommend action.

**Metric Definition:**
Booking conversion rate = (Bookings / Search sessions) × 100%. Measured from search initiation to confirmed booking. Normal baseline is 3.5-4.0%.

**The Drop:**
- Magnitude: 15% drop (3.8% → 3.2%)
- Timeline: Started 7 days ago, sudden drop on Monday
- Pattern: Sudden drop, then stable at new lower level

**Product Context:**
Airbnb connects travelers with hosts offering accommodations. 150M users, 7M listings globally. Booking conversion is critical revenue driver (20% commission).

**Recent Changes:**
- Payment page redesign shipped last Monday (new checkout flow)
- Google updated search algorithm last week (organic traffic down 5%)
- Summer travel season starting (seasonally high demand)
- Competitor Vrbo launched price-match guarantee

**Initial Data Points:**

1. **Funnel stage:**
   - Search → Listing view: No change
   - Listing view → Request booking: -20%
   - Request booking → Payment: -10%
   - Payment → Confirmed: -5%

2. **Device:**
   - Mobile web: -25%
   - Desktop: -8%
   - iOS app: -5%
   - Android app: -3%

3. **Geography:**
   - US: -18%
   - EU: -12%
   - Asia: -10%

4. **Related metrics:**
   - Payment errors: +200% on mobile web
   - Cart abandonment: +15%
   - Customer support tickets: +40% ("can't complete booking")

**Time Limit:** 20 minutes

**Recommended Framework:** S.I.E.V.E Framework

**Framework Location:** `/plugins/debugging/framework.md`

---

## Example 3: B2B Product Engagement

**Question:**  
Slack daily active teams dropped 8% over the past month. Diagnose the issue and recommend action.

**Metric Definition:**
Daily active teams = teams with at least 1 message sent or read per day. Measured via server-side events. Normal baseline is 650K-680K teams.

**The Drop:**
- Magnitude: 8% drop (670K → 616K teams)
- Timeline: Started 4 weeks ago, gradual decline
- Pattern: Steady -2%/week decline

**Product Context:**
Slack is a team messaging platform. 18M DAU across 750K paid teams. Daily active teams is key engagement metric tied to retention.

**Recent Changes:**
- Microsoft Teams added AI co-pilot 6 weeks ago (free for Enterprise customers)
- Slack Canvas feature launched 8 weeks ago (new document collaboration)
- Zoom added persistent team chat 3 months ago
- Economic downturn causing layoffs (20% of tech companies reducing headcount)

**Initial Data Points:**

1. **Team size:**
   - Small teams (5-20): -12%
   - Medium teams (20-100): -8%
   - Large teams (100+): -3%

2. **Industry:**
   - Tech: -15%
   - Finance: -5%
   - Healthcare: -3%
   - Other: -6%

3. **Geography:**
   - US: -10%
   - EU: -6%
   - Asia: -5%

4. **Related metrics:**
   - Messages per team: -5%
   - Churned teams: +40%
   - New team signups: -20%
   - Microsoft Teams adoption in tech sector: +25%

**Time Limit:** 20 minutes

**Recommended Framework:** S.I.E.V.E Framework

**Framework Location:** `/plugins/debugging/framework.md`

---

**Examples Version:** 1.0 (Plugin Architecture)  
**Last Updated:** May 2026  
**Category:** debugging  
**Location:** `/plugins/debugging/examples.md`
