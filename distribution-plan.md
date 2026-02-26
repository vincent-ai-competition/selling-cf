# Distribution Plan — ClawFriend

> **Deliverable 3 of 3** | Weight: 40% | Status: Draft
> Budget: $10,000 for Month 1. Companion to competitive-landscape.md and skill-research.md.

---

## Executive Summary

ClawFriend's distribution challenge is not a brand problem — it is a **supply + conversion problem**. The platform has real infrastructure, a working contract, and 6 validated skills ready to ship. What is missing:

1. **Supply**: Zero community skills published. The skill market looks empty to any new visitor.
2. **Conversion**: ClawFriend's ClawHub listing has 1,100 page views but only 1 install — a 0.09% conversion rate caused by a VirusTotal "Suspicious" flag. Every dollar spent on paid acquisition before fixing this is wasted.
3. **Awareness**: Zero BNB-native AI agent platform has established itself. The window is open but not permanent.

**Strategy for Month 1**: Fix the conversion blocker first. Then activate KOL seeding to seed the supply side. Then drive paid acquisition to amplify what already works. Run a skill creator contest in parallel to solve the cold-start supply problem.

---

## Budget Allocation — $10,000 Month 1

| Channel | Type | Budget | % | Priority |
|---|---|---|---|---|
| Channel 1: ClawHub Fix | Organic | $0 | — | 🚨 DAY 1 — blocker |
| Channel 2: KOL Agent Launch Program | Paid | $4,500 | 45% | Week 2 |
| Channel 3: Twitter/X Ads | Paid | $4,000 | 40% | Week 2 |
| Channel 4: Skill Creator Contest | Paid | $1,500 | 15% | Week 2 |
| Channel 5: BNB Community Seeding | Organic | $0 | — | Week 1 |
| **TOTAL** | | **$10,000** | **100%** | |

---

## Channel 1: ClawHub Fix + Optimization

**Type**: Organic | **Cost**: $0 | **Priority**: 🚨 Must complete before ANY paid spend

### Why this channel

ClawHub is ClawFriend's primary install channel. The listing already has 1,100 page views — the audience is arriving. But the VirusTotal "Suspicious" flag is killing every install. Current conversion rate: **0.09%** (1 install from 1,100 views). A clean listing at even a 5% conversion rate would deliver 55 installs from the same traffic, for $0.

This is the highest-ROI action in the entire plan.

### The problem

| Metric | Value |
|---|---|
| ClawHub page views (all-time) | 1,100 |
| Installs | 1 |
| Conversion rate | 0.09% |
| VirusTotal status | 🚨 Suspicious |
| Root cause | File hash flagged — likely false positive from unsigned binary |

### Action plan

**Day 1 — Submit VirusTotal false-positive review**
- Go to [virustotal.com/gui/file-analysis](https://www.virustotal.com/)
- Find the specific file hash flagged for the ClawFriend skill
- Submit false-positive dispute: provide GitHub repo link, package description, no obfuscation confirmation
- Expected resolution time: 3–7 days

**Day 1 — Contact @steipete (ClawHub creator)**
- DM on Twitter: `@steipete Hi, our ClawFriend skill (clawhub.ai/leeknowsai/clawfriend) is flagged Suspicious by VirusTotal — we believe it's a false positive. Can you manually whitelist or review? We have 1,100 views and 1 install. Happy to share the source code for review.`
- Goal: Manual whitelist or expedited review

**Day 1–3 — Repackage if needed**
- If VirusTotal review takes > 3 days: rebuild the skill package with a clean binary
- Ensure: no bundled executables, pure Node.js if possible, full source available on GitHub
- New package = new file hash = VirusTotal starts fresh

**Day 3 — Update ClawHub listing**
- Add full README with: what the skill does, how to install, screenshots, demo GIF
- Add GitHub link to source code (builds trust, reduces Suspicious perception)
- Add demo video (Loom or MP4) showing skill working end-to-end
- Rewrite description: focus on the use case ("Real-time BNB whale alerts, rug detection, and share portfolio tracking — right inside your OpenClaw agent")

**Ongoing — Track daily**
- Check [clawhub.ai/leeknowsai/clawfriend](https://clawhub.ai/leeknowsai/clawfriend) every morning
- Log: page views, install count, VirusTotal status
- Alert threshold: if installs don't increase within 7 days after fix → escalate to @steipete again

### Expected results

| Metric | Before Fix | After Fix (Target) |
|---|---|---|
| VirusTotal status | Suspicious | Clean |
| Conversion rate | 0.09% | 5%+ |
| Monthly installs (at 1,100 views/mo) | 1 | 55+ |

---

## Channel 2: KOL Agent Launch Program

**Type**: Paid | **Budget**: $4,500 (3 KOLs × $1,500) | **Timeline**: Week 2–4

### Why this channel

Standard sponsored posts (KOL posts a tweet about your platform) have 2 problems: (1) no skin in the game — the KOL doesn't use the product, (2) audience knows it's an ad. This program is different. KOLs **actually launch their own agent on ClawFriend**, use the platform, and report their experience. When a KOL with 15K followers launches their agent and says "my holders get my alpha calls first," that creates real FOMO for their audience.

Each KOL launch also creates a new tradeable share subject — directly expanding the supply side of the share market.

### KOL selection criteria

| Criteria | Requirement | Why |
|---|---|---|
| Twitter followers | 5,000–50,000 | Big enough for reach, small enough to be authentic |
| BNB/DeFi native | Yes — posts about BNB, PancakeSwap, BSC | Ensures audience overlap with ClawFriend target users |
| Engagement rate | ≥ 2% (likes + replies / followers) | Low engagement = bot followers = wasted spend |
| Paid promo history | Max 2 paid posts in last 30 days | Prevents "shiller" profile — audience trust matters |
| Category | Trader, analyst, or AI agent builder | Direct fit with ClawFriend's use case |

### How to find KOLs

**Step 1**: Search Twitter for: `BNB DeFi`, `PancakeSwap alpha`, `BSC trading`, `AI agent BNB`

**Step 2**: Filter by followers 5K–50K. Check last 20 tweets: are they actually trading? Do they post on-chain data?

**Step 3**: Check engagement: total likes on last 10 posts ÷ followers = engagement rate. Target ≥ 2%.

**Step 4**: DM list of 20 candidates in Week 2. Expect 25–30% response rate → confirm 3 from 20 outreach.

### KOL deliverables (per $1,500)

| Deliverable | Description | When |
|---|---|---|
| Agent launch | Use Agent Launch Kit to launch their ClawFriend agent | Week 3 or 4 |
| Launch tweet | "I just launched my agent on @ClawFriend [link]. My holders get my exclusive alpha first. Buy a share here: [link]" | Day of launch |
| Experience thread | 3–5 tweets about their experience: what skills they installed, what they shared with holders, what they found interesting | 3–5 days after launch |
| Stories/short video | Optional: 60s walkthrough of their agent profile (strong bonus) | Within 1 week of launch |

### KOL outreach script (DM)

```
Hey [name], saw your BNB alpha calls — really solid.

We built ClawFriend, the first AI agent economy on BNB. You can launch your own agent,
and your followers can hold your shares to get exclusive alpha from you (like a
holder-gated Telegram but on-chain).

We're inviting 3 BNB traders to be founding agents this month.
$1,500 to cover your time + setup support.

The catch: you actually have to use it and post honestly about your experience.
No scripted shill.

Interested?
```

### Timeline

| Day | Action |
|---|---|
| Day 8–10 | DM 20 KOL candidates |
| Day 12 | Follow up with non-replies. Confirm 3 paid partners. |
| Day 13 | Brief confirmed KOLs: walk through Agent Launch Kit, answer questions, set launch date |
| Day 15–17 | KOL 1 + KOL 2 launch agents. Tweet goes out same day. |
| Day 22–24 | KOL 3 launches agent. |
| Day 28 | Collect results: share buyers, subjectFee earned, follower count of each agent |

### Metrics

| Metric | Target per KOL | Total (3 KOLs) |
|---|---|---|
| Tweet impressions | 5,000–15,000 | 15,000–45,000 |
| Clicks to ClawFriend | 150–500 | 450–1,500 |
| New share buyers | 20–50 | 60–150 |
| SubjectFee earned by KOL | > $50 (validates the model) | > $150 |
| New skill installs from traffic | 30–80 | 90–240 |

---

## Channel 3: Twitter/X Ads

**Type**: Paid | **Budget**: $4,000 ($1,000/week, Weeks 2–4 + Week 1 setup) | **Timeline**: Launch Day 8

### Why this channel

BNB DeFi users live on Twitter/X. The followers of @BNBChain, @PancakeSwap, @whale_alert are exactly the people who would install a rug detector or whale alert skill. Twitter/X Ads allows precise follower targeting — we can reach the audience of competitors and complementary tools directly.

This channel amplifies what is already working (ClawHub organic traffic, KOL launches). It is NOT the first thing to launch — it waits until the VirusTotal flag is fixed and Phase 1 skills are live.

### Campaign structure

**Campaign 1: Rug Detector Awareness** (Week 2–4, $1,500 budget)

| Element | Detail |
|---|---|
| Objective | Website traffic → clawfriend.ai/skills/rug-detector |
| Creative | 15s video: screen recording of pasting a contract address → DANGER verdict appears in 3 seconds. Caption: "Check before you ape. Free." |
| CTA | "Try Free" |
| Targeting | Followers of: @BNBChain @PancakeSwap @BSCScan @coinmarketcap |
| Interest keywords | BSC, DeFi, rug pull, token safety |

**Campaign 2: Whale Alert** (Week 2–4, $1,500 budget)

| Element | Detail |
|---|---|
| Objective | Website traffic → clawfriend.ai/skills/whale-whisper |
| Creative | Static image: mock whale alert notification ("Smart Wallet #7 just moved $180K into [TOKEN] on PancakeSwap — 347% ROI in last 90 days"). Caption: "Know before they dump." |
| CTA | "Get Alerts" |
| Targeting | Followers of: @whale_alert @Nansen_ai @lookonchain @DefiLlama |
| Interest keywords | whale tracker, smart money, DeFi trading |

**Campaign 3: KOL Social Proof** (Week 3–4, $1,000 budget — starts after KOL launches)

| Element | Detail |
|---|---|
| Objective | Followers + website traffic |
| Creative | Screenshot of KOL launch tweet + "Join [KOL name]'s holders. Get their exclusive alpha." |
| CTA | "Buy a Share" |
| Targeting | Followers of the specific KOL who launched |
| Note | Only runs after KOL 1 launches (Week 3). Uses authentic KOL content as creative. |

### Targeting setup (step-by-step for intern)

1. Go to ads.twitter.com → Create campaign → Website Traffic
2. Ad group targeting:
   - **Follower look-alike**: Enter @BNBChain, @PancakeSwap, @whale_alert, @cz_binance, @Nansen_ai
   - **Keywords**: "BSC", "BNB DeFi", "rug pull", "whale wallet", "PancakeSwap"
   - **Geography**: Worldwide (crypto audience is global)
   - **Language**: English
3. Budget: $50/day per campaign
4. Bid type: Automatic (optimize for clicks)

### UTM tracking setup

All ad landing pages must have UTM parameters:
- `?utm_source=twitter&utm_medium=paid&utm_campaign=rug-detector`
- `?utm_source=twitter&utm_medium=paid&utm_campaign=whale-alert`
- `?utm_source=twitter&utm_medium=paid&utm_campaign=kol-social-proof`

Track in Google Analytics or equivalent: sessions, skill installs, share purchases per campaign.

### Target metrics

| Metric | Target | Calculation |
|---|---|---|
| CPC (cost per click) | ≤ $0.50 | $4,000 budget ÷ 8,000 clicks |
| CTR | ≥ 1% | Benchmark for DeFi ad creative |
| Conversion rate (click → install) | ≥ 3% | After VirusTotal fix |
| CAC (cost to acquire user) | ≤ $17 | $4,000 ÷ 240 conversions |
| Total new users from ads | 200–300 | Conservative estimate |

### Optimization rules

- **Day 14 check**: If CPC > $0.80 → pause worst-performing ad, reallocate budget to best performer
- **Day 21 check**: If Campaign 1 (Rug Detector) outperforms Campaign 2 → move $500 from Campaign 2 to Campaign 1
- **Kill signal**: If CTR < 0.3% after 3 days → creative is not working → create new creative before spending more

---

## Channel 4: Skill Creator Contest

**Type**: Paid (prize pool) | **Budget**: $1,500 | **Timeline**: Announce Day 8, judging Day 30

### Why this channel

The skill market cold-start problem: ClawFriend team can ship 6 skills, but a marketplace with 6 skills is still sparse. The only way to seed community skills quickly is to make it financially attractive. A $1,500 prize pool, announced in developer communities, targets exactly the people who already build agent skills (elizaOS devs, OpenClaw devs) and gives them a concrete reason to target ClawFriend's marketplace.

### Contest rules

**Name**: ClawFriend Skill Challenge — Month 1

**Prizes**: 1st place $750 | 2nd place $500 | 3rd place $250

**Eligibility**:
- Publish a new skill to ClawHub AND link it in ClawFriend's marketplace
- Skill must be functional (installs without errors)
- One entry per developer

**Judging criteria (equal weight)**:
1. Install count by Day 30
2. Share demand generated (new buyers of the skill creator's ClawFriend shares)
3. Technical quality (code review by ClawFriend team)

**How to submit**: Open a GitHub Issue at github.com/leeknowsai/clawfriend with title "Skill Challenge: [skill name]"

### Where to announce

| Channel | Post format | Day |
|---|---|---|
| OpenClaw GitHub Discussions | Issue titled "ClawFriend Skill Challenge — $1,500 prize pool for Month 1" | Day 8 |
| ClawHub Discord (if exists) | Same message | Day 8 |
| BNB Chain Discord #developers | Introduce platform + contest in one post | Day 8 |
| Twitter (@ClawFriend) | Thread: "We're launching a Skill Challenge. 3 winners share $1,500..." | Day 8 |
| r/bnbchain | Post: "Building on BNB? ClawFriend is offering $1,500 for the best AI agent skill this month" | Day 9 |

### Expected results

| Metric | Target |
|---|---|
| Contest submissions | 10–20 skills |
| New developers onboarded | 10–15 |
| Community skills in marketplace | 10+ |
| Organic reach from contest announcements | 5,000–10,000 impressions |

---

## Channel 5: BNB Community Organic Seeding

**Type**: Organic | **Cost**: $0 | **Timeline**: Start Day 7, ongoing throughout Month 1

### Why this channel

BNB's DeFi community is large (130M+ wallets, active Telegram/Discord/Reddit communities) and completely untouched by any AI agent economy platform. Organic presence in these communities is zero-cost and builds genuine credibility — paid ads alone without community presence look hollow.

**Rule**: Never post promotional content without providing value first. Every post must answer a question or share genuinely useful information.

### Target communities and schedule

| Community | Size | Platform | What to post |
|---|---|---|---|
| BNB Chain official Discord | Large | Discord | Introduce ClawFriend in #dapps-showcase. Post rug detector demo. |
| r/bnbchain | Active subreddit | Reddit | "We built the first AI agent economy on BNB — here's the rug pull detector" |
| BSCMoonShots Telegram | 100K+ | Telegram | Post when a rug pull would have been caught by Skill 3 |
| PancakeSwap community Discord | Active | Discord | Post in #tools: "Free rug detector for new PancakeSwap pairs" |
| OpenClaw GitHub Discussions | Developers | GitHub | Post about ClawFriend as economic layer for OpenClaw agents |

### Weekly posting schedule

| Week | Content | Channels |
|---|---|---|
| Week 1 (Day 7) | "Introducing ClawFriend — first AI agent skill economy on BNB Chain. 6 skills live. Here's how it works: [thread]" | Twitter, BNB Discord, r/bnbchain |
| Week 2 (Day 12) | "We just shipped BSC Rug Detector — free for all traders. Paste any contract address, get a verdict in 3 seconds." Demo GIF included. | All 5 communities |
| Week 3 (Day 19) | Showcase KOL 1 launch story: "[@KOL] just launched their agent on ClawFriend. Their holders got this alpha 2 hours before Twitter." Screenshot of Holder Broadcast. | Twitter, BNB Discord, r/bnbchain |
| Week 4 (Day 26) | "Month 1 results: X agents launched, X skills installed, X shares traded. Contest closes in 4 days — 3 winners share $1,500." | All channels |

### Metrics

| Metric | Target |
|---|---|
| Total organic posts | 16 (4 weeks × 4 channels) |
| Average engagement per post | 10+ reactions/upvotes |
| Click-throughs to ClawFriend | 200–400 total |
| New users from organic community | 50–100 |

---

## Partnership Plan (Bonus)

Three specific partnerships with named contacts, clear value propositions, and concrete first actions.

---

### Partner 1: OpenClaw Community

**Contact**: @openclaw on Twitter | github.com/openclaw

**Why**: ClawFriend is built on the OpenClaw framework. Every developer currently building an OpenClaw agent is the exact profile of a ClawFriend skill creator. This is not an external partnership — this is the developer community ClawFriend already belongs to.

**Value for OpenClaw**: Their agents gain access to a monetizable skill economy. Developers can now earn revenue from skills they build instead of giving them away free.

**Value for ClawFriend**: Access to OpenClaw's active developer community (10,000+ GitHub stars) as a ready-made skill creator pipeline.

**First action (Day 7)**:
1. Open a GitHub Discussion on github.com/openclaw titled: "ClawFriend — economic layer for OpenClaw skills: monetize your agent's capabilities"
2. Twitter DM to @openclaw: "We built an economic layer on top of OpenClaw — skills can now earn revenue through holder-gated access. Would love to explore a co-announcement. Can we jump on a call?"
3. Offer: List all OpenClaw community skills on ClawFriend marketplace for free. They get distribution; we get supply.

**Proposed outcome**: OpenClaw adds a "Deploy to ClawFriend" section to their documentation → every new OpenClaw developer sees ClawFriend as the monetization path.

---

### Partner 2: BNB Chain Foundation

**Contact**: foundation.bnbchain.org | @BNBChain on Twitter | MVB program: bnbchain.org/en/mvb

**Why**: BNB Chain Foundation actively funds projects building on BNB through the MVB (Most Valuable Builder) program and ecosystem grants. ClawFriend is a strong MVB candidate: live contract, 6 skills, first AI agent economy on BNB. A grant or featured spot on BNB's official channels would provide both capital and credibility that no paid ad can replicate.

**Value for BNB Foundation**: ClawFriend fills the AI agent economy gap on BNB — a segment Virtuals Protocol dominates on Base. Supporting ClawFriend = BNB becomes competitive in the fastest-growing Web3 sector.

**Value for ClawFriend**: Potential grant (MVB grants range from $10K–$50K+), featured on @BNBChain (3M+ followers), credibility with BNB DeFi community.

**First action (Day 14)**:
1. Apply to BNB MVB Program at bnbchain.org/en/mvb — one-page application describing ClawFriend, live contract address, 6 skills, distribution plan
2. Twitter: Tag @BNBChain in the KOL launch tweet ("First AI agent economy launches on @BNBChain — [KOL]'s agent is now live")
3. Reach out to BNB ecosystem team on Telegram (t.me/BNBchain_Ecosystem)

---

### Partner 3: Virtuals Protocol

**Contact**: @virtuals_io on Twitter | virtuals.io

**Why**: Virtuals has 281K Twitter followers, 18,000+ agents, and $39.5M in protocol revenue — the largest AI agent economy in Web3. They are on Base/Solana, not BNB. This is not competition; it is **complementary validation**. A Virtuals acknowledgment ("ClawFriend is doing for BNB what we do on Base") carries enormous social proof.

**Value for Virtuals**: Content and narrative — the AI agent economy is growing beyond their chains. Associating with BNB's entry validates the category expansion.

**Value for ClawFriend**: Social proof from the category leader. Instant credibility with their 281K followers. Potential cross-promotion to developers who want to launch on multiple chains.

**First action (Day 20 — after KOL launches)**:
1. Twitter DM to @virtuals_io: "Huge fan of what you've built on Base. We launched the first AI agent economy on BNB — same holder-gated mechanic, different chain, different audience. Would love to do a 'ecosystem spotlight' collab — you mention us to BNB-curious developers, we spotlight your platform to our BNB community. Mutual win?"
2. Reference the competitive analysis: "We cited Virtuals as the benchmark in our pitch deck — your $39.5M revenue is the north star we're building toward on BNB."
3. Offer: co-authored blog post "The AI Agent Economy Goes Multi-Chain"

---

## Week-by-Week Timeline

| Week | Days | Actions | Budget Deployed |
|---|---|---|---|
| **Week 1** | Day 1–7 | 🚨 Fix ClawHub VirusTotal (Day 1). DM @steipete (Day 1). Set up Twitter Ads account + create 3 ad creatives. Research 20 KOL candidates. Launch Phase 1 skills (Holder Broadcast, Agent Launch Kit, Portfolio Dashboard). First community post: BNB Discord + r/bnbchain. | $0 |
| **Week 2** | Day 8–14 | Launch Twitter/X Ads Campaign 1 + 2 ($1,000). Cold DM 20 KOL candidates. Confirm 3 paid KOL partners (Day 12). Brief KOLs, schedule launch dates. Announce Skill Creator Contest across all channels. Post Rug Detector demo in BNB communities. | $1,000 |
| **Week 3** | Day 15–21 | KOL 1 + KOL 2 launch their agents (Day 15–17). Their launch tweets go live. Activate Twitter/X Ad Campaign 3 (KOL social proof, $500). Continue Campaigns 1+2 ($500). Start OpenClaw GitHub Discussion. Apply to BNB MVB Program. Community post: share KOL launch story. | $2,000 |
| **Week 4** | Day 22–30 | KOL 3 launches agent. Optimize Twitter/X ads based on CTR data. Contest closes Day 30 — announce winners. DM @virtuals_io. Collect all Month 1 metrics. Draft Month 2 plan with learnings. | $1,000 |
| **Total** | | | **$4,000** (Twitter/X Ads) + **$4,500** (KOL) + **$1,500** (Contest) = **$10,000** |

---

## Success Metrics Dashboard — Month 1

| Metric | Baseline (Day 0) | Target (Day 30) | How to measure |
|---|---|---|---|
| ClawHub installs | 1 | 100+ | clawhub.ai/leeknowsai/clawfriend |
| VirusTotal status | Suspicious | Clean | virustotal.com |
| Total agents launched | ~5 | 15+ | ClawFriend platform |
| Share trades | Unknown | 500+ | ClawFriendV1 contract events |
| Twitter/X followers | Minimal | 1,000+ | Twitter Analytics |
| Community skills published | 0 | 10+ | ClawHub + marketplace |
| Paid CAC | N/A | ≤ $20 | UTM tracking |
| KOL subjectFee earned | $0 | > $150 total | Contract `Trade` events |
| BNB community organic reach | 0 | 500+ clicks | UTM links in community posts |

---

## Month 2 Preview (What Success Unlocks)

If Month 1 metrics are hit:
- **KOL program expands**: Reinvest subjectFee earnings + new budget into 5–7 more KOL launches
- **Twitter/X Ads**: Scale winning campaigns to $2,000/week. Kill underperformers.
- **BNB MVB grant**: If application approved → additional $10K–$50K for Month 2–3
- **Virtuals collab**: Announce cross-chain partnership for broader Web3 press coverage
- **Skill market**: 10+ community skills from contest → skill discovery becomes a viable acquisition channel itself

The Month 1 plan is not optimized for maximum users. It is optimized for **proof of flywheel**: one KOL whose holders are engaged, one viral skill install story, one rug pull saved and shared on CT. That proof of concept is what unlocks Month 2 confidence and budget.

---

*Distribution plan compiled based on competitive landscape analysis, skill research, and ClawFriend smart contract capabilities. Cost benchmarks from public advertising data. Data snapshot: February 2026.*
