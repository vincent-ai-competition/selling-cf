# Distribution Plan — ClawFriend Skill Market

> **Deliverable 3 of 3** | Weight: 40% | Competition Day 2–3
> This plan is intern-executable. Every channel has a specific action, target, and measurement criteria.

---

## Executive Summary

**Goal**: 500–700 qualified signups in Month 1 (users who install ≥1 skill, not just register)
**Budget**: $10,000 (plus unlimited time for organic channels)
**Primary insight**: The Skill Market has 0 skills today. We are solving a cold-start problem, not a growth problem. The distribution strategy must bring *both* skill developers and end users simultaneously — you cannot grow one without the other.

**Strategic sequence** (do not skip steps):
```
Step 1: Fix the blocking issue (VirusTotal flag on ClawHub)
Step 2: Seed the skill market (publish Skills 1, 3, 6 as first installs)
Step 3: Activate organic community channels
Step 4: Launch paid amplification
Step 5: Measure and reallocate
```

**Why this order matters**: Running KOL campaigns or paid ads pointing to a platform with 0 skills and a VirusTotal "suspicious" warning on the install page will burn budget with near-zero conversion. Fix the funnel first.

---

## The Blocking Issue: VirusTotal Flag on ClawHub

**Status** (verified Feb 2026): ClawFriend's skill on [clawhub.ai/leeknowsai/clawfriend](https://clawhub.ai/leeknowsai/clawfriend) displays a prominent security warning: *"Skill flagged — suspicious patterns detected."* The skill has 1 current install out of 1,100 page views — a 0.09% conversion rate. The flag is the primary reason.

**Action required BEFORE any paid marketing**:
1. Submit ClawFriend skill zip to [VirusTotal.com](https://www.virustotal.com) for manual review (false positive appeal)
2. Identify which scanner triggered the flag (likely behavioral heuristic from the WebSocket code)
3. Repackage if needed: isolate network-connection code, add inline documentation explaining each external call
4. Re-submit to ClawHub via GitHub issue or PR at [github.com/openclaw/clawhub](https://github.com/openclaw/clawhub)
5. Contact maintainer: Peter Steinberger (@steipete on Twitter/GitHub) — brief, professional DM explaining the false positive

**Expected resolution time**: 2–5 business days (VirusTotal false positive review SLA)
**Impact**: Removing the warning is estimated to increase ClawHub conversion rate from 0.09% to 3–5% (industry benchmark for developer tool discovery pages)

---

## $10,000 Budget Allocation

### Overview

| Channel | Budget | % | Rationale |
|---|---|---|---|
| **KOL / Micro-influencer** | $4,000 | 40% | Highest trust in Web3; mid-tier DeFi KOLs (50K–300K followers) outperform mega-KOLs on CAC |
| **Twitter/X Paid Ads** | $3,000 | 30% | Only viable paid channel for Web3 audience; precise targeting by follower overlap |
| **Skill Incentive / Early Adopter Airdrop** | $2,000 | 20% | BNB shares for first 200 users who install + refer 3 friends; Web3-native growth mechanic |
| **Tracking & Analytics Infrastructure** | $500 | 5% | UTM setup, Dune dashboard, Hotjar landing page recording |
| **Reserve (reallocate Week 2)** | $500 | 5% | Based on Week 1 data — go to the channel with best CAC |

---

### Channel 1: KOL / Micro-influencer — $4,000 (40%)

**Why this is the #1 allocation**: Web3 user acquisition follows a trust hierarchy. Community > KOL endorsement > organic content > paid ads. In CT culture, a mid-tier KOL with genuine DeFi credibility delivers 10× better qualified signups per dollar than a banner ad.

**Target KOL profile**:
- Follower count: **50K–300K** (micro-to-mid tier)
- Primary content: DeFi alpha, BSC ecosystem, BNB trading, wallet analytics
- NOT: generic crypto news accounts, Shitcoin promoters, verified paid shill accounts

**Target accounts to approach** (start here):
| Account | Why | Approach |
|---|---|---|
| @lookonchain | On-chain whale/smart money research; verified, credible | DM: "Can your audience get free early access to our BNB whale alert skill?" |
| BNB ecosystem KOLs (50K–200K) | BNB-native audience, DeFi-active | Search Twitter: "BNB" OR "BSC" from accounts with 50K–300K followers |
| DeFi security/alpha accounts | Exact audience for Rug Pull Detector + Smart Wallet skills | Find accounts that regularly discuss rug pulls, token safety |

**Brief structure**:
- $1,000–$1,500 per KOL (3 KOLs total)
- 1 dedicated tweet/thread + 2 follow-up replies (3-post package)
- Content format: "Demo of the skill" — screen recording or screenshot of the tool working, not a generic promo
- Mandatory: UTM link for tracking (e.g., `clawfriend.ai?utm_source=kol1&utm_medium=twitter`)
- KOL brief template (provide to each KOL):
  > "Show your followers how to install the [Skill Name] skill on ClawFriend and how it works. Here's the install link: [UTM link]. We want authentic, hands-on content — not a generic promo tweet."

**KOL measurement criteria**:
| Metric | Target | Cut if |
|---|---|---|
| Signups within 48h post | 50–200 per KOL | < 30 signups in 48h → don't activate KOL #2 with same approach |
| Cost per signup | < $30 | > $50/signup → reallocate budget to skill incentive channel |
| Skill installs / signups | > 50% | < 25% install rate → landing page problem, not KOL problem |

**Contingency**: If KOL #1 underperforms (< 30 signups in 48h), do NOT automatically activate KOL #2. Instead: diagnose landing page, check UTM data, then either adjust brief or reallocate to Skill Incentive channel.

---

### Channel 2: Twitter/X Paid Ads — $3,000 (30%)

**Why Twitter/X over Meta or Google**: Web3 users are concentrated on Twitter/X. Meta and Google prohibit many crypto ads. Twitter/X allows targeting by follower overlap (people who follow @DeFiLlama, @nansen_ai, @BNBChain) — the most precise Web3 targeting available.

**Campaign structure**:

**Campaign A: Awareness (Weeks 1–2) — $1,500**
- Objective: Traffic (link clicks to skill page)
- Creative: 15-second screen recording of Rug Pull Detector in action — "Scan any BSC token in 3 seconds. Free."
- Audience targeting: Followers of @DeFiLlama, @nansen_ai, @whale_alert, @BNBChain, @PancakeSwap
- CTA: "Try it free — no wallet connect required"
- Landing page: ClawFriend skill page (direct, no intermediate marketing page)
- Budget: $500/week × 3 weeks
- **Target CPC**: $0.33–$0.50 (Web3 Twitter benchmark, Q4 2025 data)
- **Target clicks**: 3,000–4,500 per campaign

**Campaign B: Conversion (Weeks 2–4) — $1,500**
- Objective: Conversions (skill installs, tracked via UTM)
- Creative: "Before/After" — "I used to spend 2 hours/day tracking BNB whales. Now my agent does it while I sleep."
- Audience targeting: Retarget users who clicked Campaign A but didn't install + lookalike of existing skill installers
- CTA: "Install free — 1-minute setup"
- Budget: $500/week × 3 weeks

**Ad performance benchmarks** (industry data, Web3 Twitter Ads, Q4 2025):
| Metric | Conservative | Target |
|---|---|---|
| CPC (cost per click) | $0.50 | $0.35 |
| CTR (click-through rate) | 0.5% | 1.2% |
| Landing page CVR (click → signup) | 2% | 4% |
| Signup → Install rate | 40% | 60% |

**Expected Month 1 output from Twitter Ads**:
- Total clicks: ~6,000–8,500
- Signups: 120–340
- Skill installs: 50–200

**Optimization triggers** (check every Monday):
- If CPC > $0.80 → kill the campaign, diagnose creative
- If CTR < 0.3% → change creative immediately (A/B test 2 variants simultaneously)
- If CVR < 1.5% → landing page problem (check Hotjar recordings, add social proof)

---

### Channel 3: Skill Incentive / Early Adopter Airdrop — $2,000 (20%)

**Mechanism**: Web3-native acquisition mechanic. Give the first 200 users $10 worth of BNB shares (or platform credits) for completing a 3-step action:
1. Install any skill via ClawFriend
2. Make 1 trade (buy or sell any agent share)
3. Refer 3 friends via personal referral link

**Why this works in Web3**: Token/share incentives align user motivation with platform economics. Users who complete all 3 steps understand the product deeply and are much more likely to remain active. The referral mechanic (step 3) creates exponential reach with a fixed budget.

**Budget breakdown**:
- $1,600 for first 160 users × $10 in BNB shares
- $400 reserve: extend to additional users if viral coefficient > 1.5 (each user refers > 1.5 additional users)

**Implementation requirements**:
- Referral tracking: custom referral link per user (e.g., `clawfriend.ai?ref=user_abc123`)
- Airdrop fulfillment: manual review + BNB transfer within 48h of action completion
- Anti-Sybil: require Twitter account > 30 days old for referral credit

**Target outcome**:
- 200 core early adopters with high product comprehension
- Referral multiplier: if each refers 2 additional users on average → 400 additional installs (viral)
- Total projected reach: 200 core × (1 + referral) = 400–600 additional installs

**Measurement**: Track referral link clicks and conversion rate. If referral coefficient < 1.0 after Week 2 (users are NOT referring friends), the mechanic is not working. Pivot: double the incentive ($20) for weeks 3–4 to re-activate.

---

### Channel 4: Tracking Infrastructure — $500 (5%)

**This is not optional — it's the foundation for all other channels.**

| Tool | Cost | Purpose |
|---|---|---|
| UTM link builder | Free (Google Campaign URL Builder) | Tag every KOL, ad, and organic link for source attribution |
| Hotjar (or Microsoft Clarity — free) | $0–$39/month | Record landing page behavior — where users drop off |
| Dune Analytics dashboard | Free (public query) | Track on-chain: skill installs, share buys correlated to marketing |
| Google Analytics 4 | Free | Standard event tracking for web app |

**Required UTM parameters for every link**:
```
utm_source=[kol1|twitter_ads|referral|mirror|reddit]
utm_medium=[social|paid|organic|email]
utm_campaign=[whale_alert|rug_detector|smart_wallet|launch]
utm_content=[tweet1|thread|demo_video|static_image]
```

**Key dashboards to build (Day 1)**:
1. Daily signups by source channel (GA4)
2. Signup → Skill Install conversion rate by channel (GA4 + Dune)
3. Share buy events correlated to marketing activity (Dune + BSCScan)
4. Referral link performance (custom tracking)

---

## Organic Channels ($0 Budget, Time Investment Only)

### Organic Channel 1: Developer Tutorial Content on Mirror.xyz

**Why Mirror.xyz**: Web3-native publishing platform. Articles are indexed by Google and DuckDuckGo with high domain authority. Builds permanent SEO value. The DeFi developer audience reads Mirror — it's not generic blog content.

**Cadence**: 2 articles per week during Month 1 (8 total)

**Article format**: Tutorial-first, not marketing.
- ❌ "ClawFriend: The Future of Web3 Skill Markets" (marketing)
- ✅ "How I built a BNB Whale Alert skill on ClawFriend that monitors 200 wallets and alerts me within 60 seconds of a $50K move" (tutorial)
- ✅ "Step-by-step: Setting up the BSC Rug Pull Detector skill and scanning 10 tokens before investing" (tutorial)

**Distribution after each article**:
1. Post in r/bnbchain with title "Tutorial: [specific action]" — Reddit link posts, not self-promotion
2. Share in BNB Chain official Telegram groups (verify group rules first)
3. Post in DevDAO Discord `#resources` channel
4. Tweet the thread version of the tutorial with the Mirror link

**Metric**: UTM-tracked signups per article. Target: 20–50 signups per article. If < 10 → rewrite the CTA, not the content.

**8-article plan**:
| Week | Article Topic | Skill Featured |
|---|---|---|
| 1 | "How to track BNB whale wallets with an AI agent (free)" | Whale Alert |
| 1 | "How I stopped getting rugged — the 8-point scan that caught 3 honeypots last week" | Rug Pull Detector |
| 2 | "Building a PancakeSwap new token alert: from zero to 60-second alerts" | Token Sniper |
| 2 | "I put $5K into the wrong BNB pool. Here's the yield optimizer that would have saved me" | Yield Optimizer |
| 3 | "How to find smart money wallets on BNB that actually perform (on-chain verified)" | Smart Wallet |
| 3 | "My ClawFriend agent earned me $80 in subjectFee this week — here's how" | Agent Analytics |
| 4 | "Month 1 results: my AI agent vs. manual DeFi research" | Combined case study |
| 4 | "How to publish your own BNB skill on ClawFriend and earn passive income" | Developer onboarding |

---

### Organic Channel 2: GitHub — Open Skill Developer Resources

**Target**: Developers building AI agents on BNB Chain. This audience discovers tools via GitHub search, not Twitter.

**Actions**:
1. Create `/examples` directory in ClawFriend's public GitHub with 2–3 commented skill templates
2. Each template README includes: "Deploy this skill on ClawFriend in 5 minutes — [link with UTM]"
3. Submit pull request to ClawHub's curated list with ClawFriend skills (after VirusTotal flag resolved)
4. Star and comment on relevant agent/skill repositories to drive awareness of ClawFriend

**Target metric**: GitHub stars on the example repo (target: 50 in Month 1). Every star represents a developer who saw the repo — a qualified lead for skill developer onboarding.

---

### Organic Channel 3: Crypto Twitter Organic — Demo Thread Strategy

**Format**: "My agent did X on-chain" — show the skill working, not describe what it does.

**Thread structure** (for each skill demo):
```
Tweet 1: "I stopped manually checking BSCScan for whale moves.
My ClawFriend agent now watches 200 wallets 24/7.
Here's what it found last night: [screenshot]

Thread below ↓"

Tweet 2–4: Specific alert example with real data — which wallet, which token, the move
Tweet 5: How to set it up (tutorial condensed to 2-step instructions)
Tweet 6: Call to action — "Install free at [UTM link] — 1 minute setup"
```

**Cadence**: 3 demo threads per week + 5 engagement replies per day

**Engagement reply strategy** (5 per day):
- Search Twitter for: "BSC whale" OR "PancakeSwap new token" OR "rug pull BSC" OR "BNB DeFi yield"
- Reply with a relevant insight (not a link): "The top 10 holder concentration is actually the strongest rug pull signal — I learned that the hard way"
- Follow up if they engage: then share the skill link

**Target accounts to engage under**:
- @DeFiLlama tweet threads
- @BNBChain announcements
- @whale_alert large transaction alerts
- r/bnbchain Reddit posts (engage, don't self-promote immediately)

**Metric**: Impressions per thread (target 5K–20K), profile visits from threads, link clicks to skill page. Check Twitter Analytics weekly.

---

## Partnership Plan

These are warm leads with clear mutual value. Priority order matters — start with the highest leverage, lowest time cost.

### Partnership 1: ClawHub / OpenClaw — PRIORITY 1

**Context**: ClawFriend skills install via `npx clawhub@latest install clawfriend`. ClawHub is the primary distribution channel. The current VirusTotal flag is the blocking issue.

**Mutual value**:
- ClawHub needs quality skills to grow (currently 10,324 skills, zero BNB DeFi native)
- ClawFriend needs ClawHub's 5,700+ developer community as skill developers

**Action steps** (Day 1, before everything else):
1. Open GitHub issue at [github.com/openclaw/clawhub](https://github.com/openclaw/clawhub): "False positive VirusTotal flag on clawfriend skill — requesting review"
2. DM @steipete (Peter Steinberger, ClawHub creator) on Twitter: brief professional message explaining the false positive and proposing a "Featured BNB Skills" category
3. After flag resolved: submit ClawFriend community skills (all 6 from this research) to ClawHub directory

**Expected outcome**: Resolution of the VirusTotal flag + potential ClawHub homepage feature (zero cost; they want quality skills in underserved categories)

---

### Partnership 2: BNB Chain Official — PRIORITY 2

**Contact**: @BNBChain on Twitter, builders.bnbchain.org grant program

**Mutual value**:
- BNB Chain wants to showcase ecosystem projects and drive developer activity
- ClawFriend brings on-chain volume (share trades = BSC transactions = network activity)

**Action steps**:
1. Apply for BNB Chain Builder Grant at [builders.bnbchain.org](https://builders.bnbchain.org) — "AI Agent Skill Market on BNB"
2. Tweet @BNBChain with a demo: "We're building the first AI agent skill economy on BNB Chain — check out what our agents found on-chain this week: [screenshot]"
3. Submit to BNB Chain monthly ecosystem spotlight (apply via their official form)

**Expected outcome**: $5K–$50K ecosystem grant (common for early-stage DeFi projects) + featured mention on BNB Chain's official channels (their account has 2M+ followers)

---

### Partnership 3: DeFiLlama — PRIORITY 3

**Contact**: @DeFiLlama on Twitter, Discord

**Mutual value**:
- DeFiLlama users want actionable alerts when yield changes on BNB protocols
- ClawFriend can deliver DeFiLlama data via the Yield Optimizer skill and Rug Pull Detector

**Proposed exchange**: "Free ClawFriend skill that surfaces DeFiLlama BNB yield data in real-time — we'll credit DeFiLlama in every alert tweet"

**Action steps**:
1. Build a skill that posts "Top 5 BNB yields right now" using DeFiLlama's public API
2. DM @DeFiLlama on Twitter: "We built a skill using your API that drives traffic back to DeFiLlama — can we co-promote it?"
3. If they engage: propose co-authored Mirror article: "The 5 BNB yields our combined data shows you're missing"

---

## Week-by-Week Execution Timeline

| Week | Priority Actions | Organic | Paid | Target Signups |
|---|---|---|---|---|
| **Week 0 (pre-launch)** | Resolve VirusTotal flag; seed skill market with Skills 3 + 1; set up UTM tracking; prepare KOL briefs | — | — | 0 (prep only) |
| **Week 1** | Launch: KOL #1 goes live; Twitter Ads Campaign A launches; skill incentive program opens | 2 Mirror tutorials; 6 demo threads; 35 CT engagement replies | KOL #1 + Twitter Ads Campaign A ($1,500) | 100–150 |
| **Week 2** | Analyze Week 1 data; optimize Twitter Ads based on CTR/CVR; brief KOL #2 if KOL #1 delivered | 2 Mirror tutorials; 6 demo threads; 35 CT replies; Reddit AMA in r/bnbchain | KOL #2 + Twitter Ads Campaign A continues ($1,000) | 150–200 |
| **Week 3** | Retain early users; brief KOL #3; publish early user case study; launch Twitter Ads Campaign B (retargeting) | Case study thread; 6 demo threads; 35 CT replies; DevDAO Discord drop | KOL #3 + Twitter Ads Campaign B ($1,000) | 150–200 |
| **Week 4** | Scale top-performing channel; reallocate $500 reserve; push for referral multiplier | Month 1 wrap-up thread; developer tutorial #7 + #8 | Best channel gets reserve ($500) | 100–150 |

**Month 1 total target: 500–700 qualified signups**

---

## Unit Economics

### Paid Channel Economics

| Channel | Budget | Expected Signups | CAC |
|---|---|---|---|
| KOL #1 | $1,500 | 50–200 | $7.50–$30 |
| KOL #2 | $1,500 | 50–200 | $7.50–$30 |
| KOL #3 | $1,000 | 30–100 | $10–$33 |
| Twitter Ads (Campaign A) | $1,500 | 60–170 | $9–$25 |
| Twitter Ads (Campaign B) | $1,500 | 60–170 | $9–$25 |
| Skill Incentive | $2,000 | 200 core + referral | $10 core (+ free referrals) |
| **Total Paid** | **$9,000** | **450–840** | **$10.71–$20 avg** |

### Organic Channel Economics

| Channel | Time Investment | Expected Signups | Effective CAC |
|---|---|---|---|
| Mirror.xyz (8 articles) | 16 hours total | 160–400 (20–50/article) | $0 |
| GitHub dev resources | 8 hours total | 50–100 | $0 |
| CT organic threads (12) | 12 hours total | 60–120 (5–10/thread) | $0 |
| CT engagement (140 replies) | 14 hours total | 30–70 | $0 |
| **Total Organic** | **50 hours** | **300–690** | **$0** |

### Blended CAC

**Conservative scenario** (paid 450 + organic 300 = 750 total):
> Blended CAC = $9,500 / 750 = **$12.67 per qualified signup**

**Target scenario** (paid 840 + organic 690 = 1,530 total):
> Blended CAC = $9,500 / 1,530 = **$6.21 per qualified signup**

**Comparable Web3 benchmarks** (public data):
- Average DeFi user acquisition via KOL: $15–$50 CAC (CryptoViral report, 2025)
- ClawFriend's model is competitive even at conservative estimates

### LTV Assumption

The ClawFriend business model earns 5% protocol fee on every share trade. A single active agent owner who executes 10 trades/month at $50/trade average = $25/month in share volume = $1.25/month in protocol fee per user. At $12.67 CAC and $1.25/month LTV, payback period = ~10 months.

**However**: The protocol fee compounds because share prices increase on the bonding curve. Every new shareholder buying in raises the price for the next buyer — and generates protocol fee on the sell side too. The LTV grows with user tenure.

---

## Measurement Framework

### North Star Metric
**Qualified signups** = users who install ≥1 skill AND execute ≥1 share trade in Month 1

### Weekly KPIs

| Metric | Target | Source |
|---|---|---|
| New signups (weekly) | 125–175/week | GA4 |
| Skill installs (weekly) | ≥60% of signups | GA4 + Dune |
| Share trade events (weekly) | ≥30% of signups | BSCScan / Dune |
| Top traffic source | KOL or Mirror | GA4 UTM |
| Twitter Ads CPC | < $0.50 | Twitter Ads Manager |
| KOL signup rate | > 50 signups/post within 48h | UTM tracking |
| Referral coefficient | > 1.0 (each user invites ≥1 more) | Referral tracking |

### Channel Cut Criteria

| Channel | Cut if | Action |
|---|---|---|
| KOL | < 30 signups in 48h | Don't activate next KOL; diagnose and adjust brief |
| Twitter Ads | CPC > $0.80 OR CVR < 1.5% | Kill campaign; A/B test new creative |
| Mirror tutorials | < 10 signups per article after 72h | Rewrite CTA; add more specific how-to content |
| Skill Incentive | < 50 redemptions in Week 1 | Increase incentive to $20, simplify qualification steps |
| Referral program | Referral coefficient < 1.0 after Week 2 | Double incentive for referring users |

### Optimization Protocol (Every Monday)

1. Pull GA4 report: signups by source, install rate, drop-off point
2. Pull Twitter Ads Manager: CPC, CTR, CVR by creative
3. Pull Dune: share trade events correlated to marketing activity
4. Pull referral tracking: coefficient and top referrers
5. Make ONE major reallocation decision: which underperforming channel gets cut, which gets more budget
6. Update the KOL brief or Twitter ad creative if metrics underperform

---

## Risk Mitigation

| Risk | Likelihood | Mitigation |
|---|---|---|
| VirusTotal flag not resolved in time | Medium | Delay paid channels until resolved; use organic only in Week 1 |
| KOL underperforms | High (industry average) | Pre-screen KOL with follower quality check; set clear brief; measure at 48h not 7 days |
| Twitter Ads restricted (crypto ban) | Low (Twitter/X generally allows crypto ads) | Pre-verify ad copy against Twitter Ads crypto policy; have backup creative ready |
| Skill market still empty at launch | Eliminated | Seed market with Skills 1, 3, 6 before any marketing begins |
| Referral program exploited (Sybil) | Medium | Require Twitter account age > 30 days; manual review of top referrers |
| Low retention (users don't return) | Medium | Skill 6 (Agent Analytics) is the retention tool; activate for all agent owners on signup |

---

## Summary

The distribution plan works because it:
1. **Fixes the funnel first** — VirusTotal flag resolution before spending a dollar on ads
2. **Seeds supply before demand** — Publish skills before bringing users; without skills, there's nothing to install
3. **Leads with organic trust** — Mirror tutorials and CT demos build credibility before KOL and paid channels amplify
4. **Uses Web3-native mechanics** — Airdrop incentives and referral programs align with user expectations
5. **Measures obsessively** — Every channel has a weekly cut criteria; no budget runs on hope
6. **Scales through the holder-gated mechanic** — The platform's economic design (hold shares → access skills → price rises → creators earn) creates a self-reinforcing loop that compounds after Month 1 without additional spend

**The goal isn't 1,000 users. It's 500–700 users who actually use skills and trade shares — a foundation that generates protocol revenue and creates the referral flywheel for Month 2.**
