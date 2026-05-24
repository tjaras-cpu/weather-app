# LeanPath — Business Strategy Report

_Generated: May 2026_

---

## 1. Product Summary

**LeanPath** is a zero-friction, mobile-first weight-loss companion delivered as a single HTML file with no backend, no account, and no dependencies. Users track three things: daily calorie intake against a configurable TDEE-minus-deficit budget, sweets resistance (with a streak counter), and body weight over time (with a trend chart and goal weight). All data lives in the user's browser via localStorage.

**Built for:** People who want a lightweight, private alternative to heavyweight calorie trackers — no sign-up, no ads, just the numbers that matter.

---

## 2. Target Market

| Dimension | Detail |
|-----------|--------|
| **Primary users** | Adults actively trying to lose weight via calorie deficit (CICO — Calories In, Calories Out) |
| **Secondary users** | People reducing sugar intake, habit-building enthusiasts, fitness coaches recommending tools to clients |
| **Market segment** | B2C consumer health & wellness — prosumer sub-segment (users who want control without complexity) |
| **Market size** | Large and growing: ~45% of adults in developed markets are actively trying to lose weight at any given time; the global weight management market exceeds $200B. The "simple / privacy-first" niche within digital tools is underserved. |

---

## 3. Competitive Positioning

| Competitor | Their Differentiator | LeanPath Wins / Loses |
|------------|---------------------|----------------------|
| **MyFitnessPal** | Massive food database (14M+ items), social features, macro tracking | LeanPath wins on privacy and zero friction; loses on food search and macros |
| **Lose It!** | Barcode scanner, meal plans, premium coaching | LeanPath wins on simplicity and cost; loses on guided experience |
| **Cronometer** | Micronutrient detail, research-grade accuracy | LeanPath wins for casual dieters who don't need vitamin breakdowns |
| **Noom / Simple** | AI coaching, psychology-based curriculum | LeanPath wins on privacy and one-time simplicity; loses on accountability and support |
| **Apple Health / Samsung Health** | Built-in, integrates with wearables | LeanPath wins on calorie deficit focus and sweets streak; loses on ecosystem integration |

**Positioning statement:**
> "For people who just want to eat less and weigh less, LeanPath is the calorie tracker that starts in seconds with no account or data sharing, unlike MyFitnessPal which requires registration and monetises your health data."

---

## 4. Monetization Options

### ⭐ Recommendation: Option 1 — Freemium PWA (SaaS-lite)

**Option 1 — Freemium PWA / One-Time Unlock** _(Top pick)_
- **Why it fits:** The app's core value is simplicity and privacy; a paywall or subscription would undermine both. A one-time "Pro" unlock preserves the frictionless feel while generating revenue.
- **Key risk:** Low conversion rate on web; users may not perceive enough premium value to pay.
- **Pricing sketch:**
  - Free: Core tracking (calories, sweets, weight), 7-day history
  - Pro — $4.99 one-time: Unlimited history, data export (CSV/JSON), custom food presets, Apple Health sync, no "upgrade" prompts

**Option 2 — App Store (iOS/Android) Paid Download**
- **Why it fits:** Converts the existing PWA into a native wrapper (Capacitor/Cordova). Mobile users are accustomed to paying $0.99–$2.99 for utility apps.
- **Key risk:** App Store fees (30%), curation delays, maintenance overhead across OS versions.
- **Pricing sketch:** $1.99 one-time on App Store / Google Play; free web version remains as marketing funnel.

**Option 3 — Affiliate / Sponsorship**
- **Why it fits:** Health product affiliates (protein powders, meal kits, fitness gear) align naturally with the audience. No paywall preserves reach.
- **Key risk:** Revenue is unpredictable; affiliate links can erode trust if not disclosed carefully. Only viable at meaningful traffic scale (>50k MAU).
- **Pricing sketch:** $0.10–$0.50 EPC (earnings per click) on affiliate links; sponsored "Tip of the Day" placement at ~$500–2k/month at scale.

---

## 5. Feature Prioritization (MoSCoW)

| Priority | Feature | Business Rationale |
|----------|---------|-------------------|
| **Must-have** | Core calorie logging + TDEE settings | Central value prop; already built |
| **Must-have** | Weight tracking + trend chart | Key retention driver; already built |
| **Must-have** | Sweets streak | Unique differentiator vs. generic trackers; already built |
| **Must-have** | PWA installability (manifest + service worker) | Users need home-screen install for retention; currently missing |
| **Should-have** | Push/local notifications (meal reminders, streak alerts) | Dramatically improves daily active use and streak retention |
| **Should-have** | Data export (CSV / JSON backup) | Removes the #1 objection to localStorage-only apps ("what if I clear my browser?") |
| **Should-have** | Custom quick-add food presets | Reduces logging friction for repeat meals; key retention feature |
| **Should-have** | Onboarding flow (TDEE calculator) | Currently users must know their TDEE; most don't — this blocks activation |
| **Could-have** | iCloud / Google Drive sync | Solves multi-device problem without a backend; complex but high value |
| **Could-have** | Apple Health / Google Fit integration | Passive weight/step import; differentiator for power users |
| **Could-have** | Food database / barcode scanner | Reduces calorie-entry effort; large build investment |
| **Won't-have (now)** | Social features / challenges | Contradicts privacy-first positioning; premature at current scale |
| **Won't-have (now)** | AI coaching / meal plans | High complexity, high cost; not core to the simple-tool positioning |
| **Won't-have (now)** | Server-side accounts / sync | Introduces infrastructure cost, privacy concerns, and GDPR obligations |

---

## 6. Go-to-Market (GTM) Strategy

**Launch channel — Communities first:**
- **Reddit:** r/loseit (2.4M members), r/CICO, r/1200isplenty, r/intermittentfasting — post as a "I built a simple tracker" launch. These communities actively recommend tools and hate upsells.
- **Product Hunt:** Launch on a Tuesday–Thursday for maximum visibility. Emphasise "no account, no data sharing."
- **Hacker News:** "Show HN: A calorie tracker in a single HTML file" — resonates with the privacy and simplicity angle.

**Early traction metric:**
- **Weekly Active Users (WAU)** — specifically, users who log at least one entry 3+ days in a week. This is the leading indicator of habit formation and future monetisation.

**Growth loop:**
- **Content SEO:** Target "simple calorie tracker no account," "CICO tracker no login," "free weight loss app no signup" — low competition, high intent. Each article embeds the app directly.
- **Shareability:** Add a "Share my streak" card (image export of sweet-free streak) — social proof that drives organic discovery.

**90-day action plan:**

1. **Week 1–2:** Add PWA manifest + service worker (offline support, home-screen install). This is table-stakes before any launch.
2. **Week 2–3:** Build a 3-screen onboarding flow with a built-in TDEE calculator. Measure activation rate (users who log ≥1 meal on day 1).
3. **Week 3–4:** Launch on Reddit communities + HN. Collect feedback. Target 500 WAU.
4. **Month 2:** Add push notifications (streak reminders) and data export. Begin SEO content (2 articles/week).
5. **Month 3:** Implement the Pro one-time unlock ($4.99). Announce to existing users via in-app banner. Target 2% conversion of MAU.

---

## 7. Key Risks & Mitigations

| Risk | Mitigation |
|------|-----------|
| **localStorage fragility** — Users lose all data when they clear their browser or switch devices, destroying retention | Ship data export (JSON) in the next sprint; explore iCloud/Google Drive sync as a medium-term solution |
| **Discoverability** — A single HTML file has no SEO surface area; organic growth is near zero without intentional distribution | Invest in a landing page with SEO-optimised content that embeds the app; launch on communities where the audience already exists |
| **Monetisation ceiling** — A one-time $4.99 unlock has a hard ceiling; free users generate no revenue | Validate the one-time model first; if WAU exceeds 10k, evaluate an optional subscription for cloud sync as a second revenue layer |

---

## Summary

**Recommended monetisation:** One-time Pro unlock at $4.99. It respects the privacy-first positioning, requires no backend, and converts the existing "free tool" perception into a sustainable business. At 5,000 MAU with a 2% conversion rate, that's $500/month — enough to fund continued development.

**Single most important next action:** Add a TDEE calculator to the onboarding flow. Right now, users who don't know their TDEE can't set their calorie budget, which means they churn on day one. Fixing activation unlocks every downstream metric.

**Assumptions to validate:**
- That the target user is privacy-sensitive enough to choose LeanPath over MyFitnessPal's convenience. If not, the positioning needs to shift toward simplicity rather than privacy.
- That 2% of free users will pay $4.99. This should be A/B tested early with a soft paywall before building full Pro infrastructure.
- That Reddit communities allow promotional posts — check subreddit rules before launch (r/loseit allows tool posts; r/CICO may require manual approval).
