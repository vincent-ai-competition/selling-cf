# ClawFriend Biz Competition — Playbook

> **Author**: @vincent_ethhh
> **Competition**: Cook a Web3 Skill Marketplace — 3 days, individual
> **Goal**: Scored on Competitive Landscape (25%) + Skill Research (25%) + Distribution Plan (40%) + Presentation (10%)

---

## The Winning Strategy (TL;DR)

Most contestants will produce generic research. The ones who score 80+ will do three things differently:

1. **Anchor everything in data** — Not "many people need this", but "12,400 monthly searches, Nansen charges $100/mo for the same thing"
2. **Make the Distribution Plan intern-executable** — Judging panel's exact test: *"Give this to an intern tomorrow, can they execute it?"* If yes, full marks.
3. **Use the technical background as an unfair advantage** — As the developer who built parts of the platform, you understand the holder-gated mechanic, the bonding curve, and the skill architecture deeper than anyone in the room. Convert that knowledge into sharp, specific business arguments.

**The one insight that connects all 3 deliverables:**
> The Skill Market is currently empty. The only way to fill it is to attract skill developers first, then users follow. This is a classic two-sided marketplace cold-start problem. Your entire research should be built around solving this.

---

## Part 1: Competitive Landscape (25%)

### The Goal
Not a list of competitors. A strategic map that answers: *"Where is ClawFriend's opening in the market?"*

### Research Framework

**Step 1: Classify by type**

| Category | Who to look at | Why it matters |
|---|---|---|
| **Direct** — Web3 agent skill/plugin marketplaces | Virtuals Protocol, ai16z/ELIZA plugins, SingularityNET, Fetch.ai DeltaV | Same use case, direct competition |
| **Parallel** — Bonding curve social | friend.tech, pump.fun | Same economic mechanic, different utility |
| **Infrastructure** — Agent frameworks with skill ecosystems | OpenClaw/ClawHub, Gaia Network | Same developer audience |
| **Centralized** — AI marketplace | Zapier AI, Make.com, OpenAI GPTs Store | Shows what "good UX" looks like before web3 |

**Step 2: Find real data per competitor**

For each competitor, find at least 2 hard numbers from verifiable sources:

| Data point | Where to find it |
|---|---|
| GitHub stars / forks | github.com/[org]/[repo] |
| Twitter/X followers | x.com/[handle] |
| On-chain TX count / TVL | DeFiLlama, BSCScan, Dune Analytics |
| Skill/plugin count | Their marketplace page |
| Pricing | Their pricing page or docs |
| Funding raised | Crunchbase, press release, their blog |
| User / agent count | Their own announcements, blog posts |

**Do NOT use AI-generated numbers for user counts or revenue. Judging panel will ask "source?" and you need a URL.**

**Step 3: Analyze with the 4-quadrant lens**

For each competitor, answer:
- What chain/ecosystem do they focus on?
- What is their monetization model (subscription / fees / token)?
- What is their skill/plugin count and quality signal?
- Who is their primary user (developer, trader, end-user)?

**Step 4: Draw the strategic conclusion**

The conclusion should answer: *"Where does ClawFriend fit and why does it win?"*

**Recommended narrative structure:**
> "The market is early-stage and fragmented. Virtuals/ai16z focus on Ethereum/Solana with frameworks that lack native trading mechanics. friend.tech pioneered bonding curves but abandoned skill market development. OpenClaw/ClawHub has the largest agent skill count (10,324+ skills, verified Feb 2026) but no native trading or social layer. ClawFriend is the first platform on BNB Chain that combines all three — shares trading, social stream, and skill market — in one integrated economy. The holder-gated mechanic creates a distribution incentive that no competitor has: skill creators are financially motivated to attract shareholders, who are financially motivated to access skills."

---

### ClawHub Ecosystem Deep Dive (Primary Distribution Channel — Research Done)

> **Why ClawHub matters here**: ClawFriend skills are installed via `npx clawhub@latest install clawfriend`. ClawHub is ClawFriend's primary distribution channel. Understanding ClawHub is understanding both the competitive landscape and the distribution opportunity.

**ClawHub Platform Facts** (verified live via browser, Feb 2026):

| Metric | Value | Source |
|---|---|---|
| Total skills listed | **10,324** | clawhub.ai homepage counter |
| Platform type | Open skill registry for OpenClaw agents | MIT licensed |
| Creator | Peter Steinberger (@steipete) | Footer attribution |
| Install method | `npx clawhub@latest install <skill-name>` | Platform UI |
| Auth | GitHub sign-in | Platform UI |

**Top Skills by Downloads** (no Web3 in top 25 — verified):

| Skill | Downloads | Stars | Category |
|---|---|---|---|
| Gog (Google Workspace) | 34.8k | ★261 | Productivity |
| self-improving-agent | 33.6k | ★367 | Meta/AI |
| Ontology | 30.1k | ★57 | Knowledge |
| Tavily Web Search | 29.1k | ★112 | Search |
| Summarize | 26.9k | ★119 | Productivity |

Zero Web3/crypto skills appear in the top 25 by download count.

**Web3 / Crypto Skills on ClawHub** (exhaustive search, "crypto" query, Feb 2026):

| Skill | Downloads | Stars | What It Does |
|---|---|---|---|
| Crypto Price | 2,700 | ★4 | CoinGecko price lookup |
| Polymarket Odds | 2,600 | ★17 | Prediction market odds |
| Hyperliquid Trading | 2,400 | ★9 | Perpetuals on Hyperliquid |
| Binance Pro | 1,900 | ★5 | CEX order management |
| Onchain CLI | 1,400 | ★0 | Multi-chain portfolio view |
| Minara | 1,000 | ★4 | Generic crypto swap |
| crypto-cog | 544 | ★3 | Research aggregator |
| **ClawFriend** | **1,100 views** | **★0** | **BNB agent economy (see below)** |

**Gap ratio**: Best crypto skill = 2,700 downloads vs. top general skill = 34,800 → **13× underrepresented**. Zero BNB Smart Chain / DeFi-native skills exist on the platform.

**ClawFriend's Own Listing** (`clawhub.ai/leeknowsai/clawfriend`, verified Feb 2026):

| Metric | Value |
|---|---|
| Stars | ⭐ 0 |
| Page views | ~1,100 |
| Current installs | **1** |
| All-time installs | **1** |
| Version | 1.1.0 |
| Publisher | @leeknowsai |
| **Security status** | 🚨 **FLAGGED — VirusTotal: Suspicious** |

The ClawHub security scanner has flagged ClawFriend's skill as suspicious. ClawHub displays a prominent warning banner: *"Skill flagged — suspicious patterns detected. Review scan results before using."* This is the primary reason for the near-zero install count (1 current install) despite 1.1k page views.

**Strategic implications for all 3 deliverables:**

1. **Competitive Landscape**: ClawFriend's closest distribution channel (ClawHub) has 10,324 skills, but Web3 skills represent <1% of top-downloaded content. The platform's user base skews strongly toward productivity/developer tools. This means ClawFriend must bring its *own* audience to ClawHub, not rely on ClawHub organic discovery.

2. **Skill Research**: Any skill published on ClawHub in the BNB/DeFi category is immediately first-mover in an uncontested vertical. Even 500 downloads would make it a top crypto skill on the platform.

3. **Distribution Plan** (most actionable): The VirusTotal flag is a blocking issue. **First action before any paid marketing: resolve the security flag.** A suspicious warning on the install page kills all conversion — no KOL campaign can overcome "this skill is flagged as malware." Resolution path: submit to VirusTotal for review, repackage if needed, then re-submit to ClawHub.

**Action items derived from this research:**
- [ ] Verify and resolve the VirusTotal false-positive flag (contact ClawHub via GitHub: openclaw/clawhub)
- [ ] After flag resolved: propose ClawFriend skills as "Featured BNB Skills" to ClawHub maintainer (Peter Steinberger / @steipete)
- [ ] Target the ClawHub developer community (skill install volume = 10,324 skills uploaded) — these are the exact skill developer audience for D2

---

### What passing looks like vs what wins

| Dimension | Passing (60–70%) | Winning (85–100%) |
|---|---|---|
| Competitors found | 5–10, with links | 5–7, with hard data + sources |
| Depth | Copy-paste website descriptions | "Virtuals has 847K X followers (source: x.com/virtuals_io), 12K+ agents launched (source: their blog, Jan 2026)" |
| Conclusion | "There is opportunity in the market" | Specific positioning: "BNB chain is underserved, no competitor has trading + social + skills, holder-gated mechanic is novel" |
| ClawFriend angle | Generic strengths | Connects directly to gaps identified in competitor research |

---

## Part 2: Skill Research (25%)

### The Goal
Prove that specific skills will attract users AND drive share demand. Not "I think people need this" — but "here is evidence that demand already exists."

### PMF Framework for Each Skill

Every skill you propose must pass this 5-point test:

```
1. WHO: A specific user (not "crypto traders" — "BNB DeFi retail traders with $5K–$50K portfolio")
2. PAIN: A specific problem they face today (time cost, money cost, complexity)
3. CURRENT: What they use now, and why it's inadequate (too expensive, too manual, too slow)
4. PROOF: At least 2 data sources showing demand exists (search volume, subreddit post count, existing paid tools)
5. FIT: Why this works as a ClawFriend skill (public free to build awareness OR holder-gated to drive share demand)
```

### Skill Ideas (Validate These — Do Not Use Numbers Without Checking)

| Skill | Target User | Pain | Current Alternative | Hypothesis to Verify |
|---|---|---|---|---|
| **BNB Whale Tracker** | Retail DeFi traders on BNB | Spending 2h+/day manually watching whale wallets on BSCScan | Nansen (~$99–$150/mo), free Etherscan | Search "whale tracker bnb" on Google Trends; check r/bnbchain post count |
| **New Token Launch Scanner** | PancakeSwap early traders | Missing new token launches in first 30 min | Manual DEXTools/PooCoin refresh | Check DEXTools Twitter followers; search "new token BSC alert" |
| **Rug Pull Risk Detector** | Any BNB token buyer | Losing money on rug pulls | Manual check on TokenSniffer, RugDoc | TokenSniffer user count; r/CryptoMoonShots post complaints |
| **Auto Trading Signal Feed** | Retail traders who follow CT | Scattered signals across 20+ Telegram/Twitter sources | Paying $50–$200/mo for signal groups | Count active paid signal Telegram channels on BNB ecosystem |
| **DeFi Yield Optimizer** | BNB DeFi LP providers | Missing better yield rates across protocols | Manual checking Yield Watch, DeFiLlama | DeFiLlama Pro pricing; "yield optimizer" search volume |
| **On-chain Sentiment Analyzer** | Swing traders | No real-time fear/greed data specific to BNB ecosystem | Generic Crypto Fear & Greed Index | Twitter engagement on existing sentiment tools |

### Demand Proof Sources (Use These, In This Order)

1. **Google Trends** → screenshot + URL → shows sustained search interest
2. **Ahrefs / Ubersuggest / Google Keyword Planner** → monthly search volume for target keyword
3. **Reddit** → go to r/bnbchain, r/defi, r/CryptoMoonShots → search keyword → count posts in last 3 months
4. **Existing paid tools** → if someone is charging $50–$200/mo and has users, demand is validated
5. **Twitter/X follower count** → tools like @whale_alert (1M+ followers) prove the audience exists

### Visibility Strategy Decision Tree

```
Does the skill drive recurring usage?
  YES → Consider holder-gated (private) — creates share demand with each new user

Is the skill novel / hard to replicate?
  YES → Start public (free) to build awareness, go holder-gated after audience forms

Is there already a free version in the market?
  YES → Must be holder-gated with significantly better quality OR focus on different angle
```

**The strongest skills for this competition** are ones where:
- Demand is proven (existing paid alternatives)
- Technical feasibility is clear (uses Etherscan/BSCScan API + on-chain data = ClawFriend infra already supports this)
- Holder-gated model makes financial sense (user saves money vs. paying $100/mo elsewhere, but must hold shares)

### Scoring What Matters Most

Judging panel weights **Product-Market Fit at 7/25 points** — more than creativity (5/25). A boring but proven skill scores higher than a creative skill with no evidence. Always prioritize proof over novelty.

---

## Part 3: Distribution Plan (40%)

### The Goal
Answer with evidence: *"How do we get 1,000 users in Month 1 with $10,000?"*

A plan that can be given to an intern tomorrow and executed. Not "run Twitter Ads" — but "run Twitter Ads targeting followers of @DeFiLlama and @nansen_ai, $5/CPM, creative: 15s video demo of Whale Tracker skill, CTA: Install free, landing: skill page with UTM link, measure: signups + skill installs within 7 days."

### Channel Selection Logic

For Web3 products in 2025–2026, user acquisition follows a specific trust hierarchy:

```
Highest trust  →  Peer/community recommendation (Telegram, Discord, CT thread)
               →  KOL endorsement (mid-tier 50K–300K followers, DeFi-native)
               →  Organic content (technical tutorial, demo video, thread)
               →  Paid ads (Twitter/X, targeting Web3 audiences)
Lowest trust   →  Generic banner ads
```

**Rule**: Never lead with paid ads in Web3. Lead with community + organic, amplify with paid.

### $10,000 Month 1 Budget Allocation

| Channel | Budget | Rationale | Target Output |
|---|---|---|---|
| **KOL / Micro-influencer** | $4,000 (40%) | Highest trust in CT; mid-tier DeFi KOLs (50K–300K followers) deliver better CAC than mega-KOLs | 3 KOLs × $1,333 avg. Est. 150–600 qualified signups |
| **Twitter/X Paid Ads** | $3,000 (30%) | Only viable paid channel for Web3 audiences; target followers of DeFiLlama, Nansen, BSC ecosystem accounts | ~6,000–9,000 clicks @ $0.33–$0.50 CPC → 3% CVR = 180–270 signups |
| **Skill Incentive / Airdrop** | $2,000 (20%) | BNB shares / credits for first 200 early adopters who install skill + invite 3 friends | 200 core users × $10 = first active cohort; referral loop multiplier |
| **Tracking & Analytics** | $500 (5%) | Dune Analytics dashboard, UTM setup, Hotjar for landing page | Data infrastructure for optimization |
| **Reserve** | $500 (5%) | Rapid reallocation based on Week 1 data | Flexibility for what works |

**Total paid CAC estimate**: $9,500 / (270 + 200 + organic 250) = **~$13.17 blended CAC**

### Organic Channels ($0 cost, time investment only)

**Channel 1: Developer Tutorial Content on Mirror.xyz**
- **Why Mirror**: Web3-native, indexed by crypto search, builds credibility with the developer audience
- **Cadence**: 2 posts/week, each a tutorial walkthrough of one specific skill
- **Example title**: *"How I built a BNB Whale Alert skill on ClawFriend that saves me 3 hours/day"*
- **Distribution**: Post link in r/bnbchain, BNB Chain Telegram, DevDAO Discord
- **Metric**: UTM-tracked signups per post. Target: 20–50 signups/post

**Channel 2: GitHub — Open Skill Examples**
- **Why GitHub**: Developer-first acquisition; if your skill is the example, developers discover it organically
- **Action**: Publish 2–3 open-source skill templates with README that includes "Deploy on ClawFriend in 1 click"
- **Target**: Developers building AI agents on BNB who find via GitHub search
- **Metric**: Stars, forks, README CTA clicks

**Channel 3: Crypto Twitter Organic Thread Strategy**
- **Format**: "Agent did X on-chain" demo threads — show the skill working, not explain what it does
- **Cadence**: 3 threads/week + 5 replies/day on relevant discussions (DeFi alpha, whale movement, etc.)
- **Target accounts to engage**: @DeFiLlama, @nansen_ai, @whale_alert, @BNBChain
- **Metric**: Impressions, profile visits, follower growth, platform signups from bio link

### Week-by-Week Timeline

| Week | Focus | Organic Actions | Paid Actions | Target Signups |
|---|---|---|---|---|
| **Week 1** | Foundation + launch | 2 Mirror tutorials, 6 CT threads, GitHub skill template | Brief KOL #1, start Twitter ads | 100–150 |
| **Week 2** | Amplify what works | 2 Mirror tutorials, high-engagement replies, community AMA | Brief KOL #2, optimize ads based on CTR/CVR data | 150–200 |
| **Week 3** | Retention + word of mouth | Case study of early user, "community spotlight" content | Brief KOL #3, retarget site visitors | 150–200 |
| **Week 4** | Scale top channel | Double down on best-performing channel from Week 1–3 | Reallocate reserve $500 to best channel | 100–150 |

**Month 1 total target: 500–700 signups (blended paid + organic)**

### Partnership Plan (Bonus Points)

These are warm leads with clear mutual value, not generic "reach out to influencers":

| Partner | Why They Care | Proposed Value Exchange | Action |
|---|---|---|---|
| **BNB Chain Official** (@BNBChain) | They want to showcase BNB ecosystem projects | Feature in BNB Chain monthly ecosystem spotlight; potential grant via [builders.bnbchain.org](https://builders.bnbchain.org) | Submit grant application + tweet them + email |
| **OpenClaw / ClawHub** | ClawFriend skills install via `npx clawhub` — registry has 10,324 skills but zero BNB-native DeFi skills. They want quality skills. | **Priority 1**: Resolve VirusTotal false-positive flag (currently showing "Suspicious" → blocking all installs). **Priority 2**: Propose co-marketing: "Featured BNB Skills" category. Contact: @steipete (Peter Steinberger) on Twitter or GitHub issue at openclaw/clawhub | Resolve flag first → then GitHub PR + DM |
| **DeFiLlama** | Largest DeFi data aggregator; audience = exact target user | Propose "ClawFriend Skill" that surfaces DeFiLlama data natively in agents | @DeFiLlama DM + their Discord |
| **Nansen / Arkham** | Power users who pay $100/mo can access subset of data cheaper via ClawFriend skill | "Free tier via ClawFriend" drives their users to the platform | BD email + Twitter outreach |

### Measurement Framework (What Judging panel Will Ask About)

Every channel must have:
- **Input metric**: What you spend / invest
- **Output metric**: How many signups / installs
- **Unit economics**: CAC per channel
- **Optimization trigger**: At what number do you double down vs. cut?

| Channel | Input | Output | CAC | Cut if |
|---|---|---|---|---|
| KOL #1 | $1,333 | 50–200 signups | $6–$26 | < 30 signups in 48h post |
| Twitter Ads | $3,000/mo | 180–270 signups | $11–$16 | CPC > $0.80 or CVR < 1.5% |
| Skill Incentive | $2,000 | 200 active users | $10 | < 50 redeem in Week 1 |
| Mirror Tutorial | $0 | 20–50/post | $0 | < 10 signups → improve CTA |

---

## Part 4: Presentation & Q&A (10%)

### Structure (15–20 min total)

| Segment | Time | What to Show |
|---|---|---|
| **Hook** (30 sec) | 0:00–0:30 | One problem sentence: "ClawFriend has the best infrastructure for AI agent skills on BNB. Zero skills exist in the marketplace today. Here's how we fix that in 30 days." |
| **Competitive Landscape** | 0:30–3:30 | Top 5 competitors table → conclusion: "BNB is underserved, holder-gated mechanic is unique" |
| **Skill Research** | 3:30–7:30 | Top 3 skills with demand data → focus on PMF evidence, not feature description |
| **Distribution Plan** | 7:30–12:30 | Budget table → Week 1–4 timeline → unit economics → "intern can execute this tomorrow" |
| **AI Showcase** | 12:30–14:30 | Show 2–3 prompts that produced the best research; explain the verify-with-source workflow |
| **Conclusion** | 14:30–15:00 | "Month 1 target: 500–700 signups, blended CAC $13, holder-gated mechanic creates self-sustaining growth" |
| **Q&A buffer** | 15:00+ | Prepared for 5 hard questions |

### The 5 Questions Judging panel Will Ask (Prep These Cold)

**Q1: "Đối thủ X đã có 50K user, tại sao mình sẽ thắng?"**
> "Virtuals/ai16z are Ethereum/Solana-native — they don't have BNB trading mechanics or a social layer. friend.tech had the bonding curve but killed the product. No one has combined trading + social + skill market in one economy on BNB. We're not competing with them on their turf — we're opening a new category."

**Q2: "Skill này có ai thực sự cần không?"**
> Cite your 2 demand sources. Example: "Whale Alert Twitter has 1.2M followers (verified). Nansen charges $150/mo for similar on-chain data. The demand is not hypothetical — it's already paying $150/mo somewhere else."

**Q3: "$10K có đủ để có 1,000 user không?"**
> "We're not targeting 1,000. We're targeting 500–700 qualified signups — users who install at least one skill. $9,500 deployed across 3 KOLs + Twitter ads + skill incentive = $13.17 blended CAC. For a Web3 DeFi product, that's competitive. Month 2, organic compounds."

**Q4: "Tại sao user không dùng ChatGPT thay vì skill trên platform?"**
> "ChatGPT has no access to BNB on-chain data in real time. ChatGPT can't execute a buy transaction when a whale moves. ClawFriend skills are agents that act — they monitor, alert, and trade. It's not a chatbot, it's an economic operator. The holder-gated mechanic means the skill creator is incentivized to maintain and improve it."

**Q5: "Kế hoạch nếu KOL không deliver?"**
> "Week 1 is when we measure. If KOL #1 returns < 30 signups in 48h post, we don't activate KOL #2 on the same approach. We realloc $2,666 to skill incentive (higher confidence channel) and double the organic community seeding. The $500 reserve exists exactly for this."

### Presentation Delivery Tips

- **Open with the number**: "Today, ClawFriend's Skill Market has 0 skills. Here is a 30-day plan to fix that." Instant framing.
- **Use your builder credibility**: "As the engineer who worked on the shares trading module, I can tell you the bonding curve creates a mechanic no competitor has..." Judging panel will lean in.
- **Never apologize for numbers**: If Judging panel asks if your CAC estimate is realistic, say "Based on Twitter Ads benchmarks for Web3 in Q4 2025 (publicly available at [source]), $0.40–0.60 CPC is the median for crypto audiences. I used the pessimistic end."
- **Show don't tell in AI Showcase**: Open a real conversation, run a real prompt, show the verify-then-cite workflow. Don't just explain it.

---

## 3-Day Execution Timeline

### Day 1 — Tuesday (Today): Foundation

| Time | Task | Output |
|---|---|---|
| Morning | Read overview.md, internalize product deeply | Mental model complete |
| Morning | Research 5–7 competitors: GitHub stars, Twitter followers, pricing, user count | Raw data with sources in `data/competitor-data.md` |
| Afternoon | Write `competitive-landscape.md` — table + per-competitor analysis + conclusion | D1 draft done |
| Evening | Brainstorm 10 skill ideas, shortlist to 5–7 for Day 2 validation | Skills shortlist |

**End of Day 1 checkpoint**: competitive-landscape.md ready. If Judging panel read it tonight, it passes.

### Day 2 — Wednesday: Research + Planning

| Time | Task | Output |
|---|---|---|
| Morning | Validate demand for 5–7 skills: Google Trends + Reddit + existing tools | `data/skill-demand-data.md` with sources |
| Morning | Write `skill-research.md` — 5 skills with full PMF framework | D2 done |
| Afternoon | Write `distribution-plan.md` — channels + budget + timeline + unit economics | D3 draft done |
| Evening | Review all 3 deliverables. Every number must have a source URL. | QA pass |

**End of Day 2 checkpoint**: All 3 deliverables done. Push to GitHub.

### Day 3 — Thursday: Polish + Present

| Time | Task | Output |
|---|---|---|
| Morning | Final review: tighten conclusions, ensure all sources are linked | Polished deliverables |
| Morning | Create Gemini Canvas web presentation (React + Tailwind) | Slide deck live |
| Pre-presentation | Push all files to GitHub. Paste link in Telegram group. | Submission complete |
| Presentation | 15–20 min pitch + Q&A | Win |

---

## Golden Rules (Don't Break These)

1. **Every number needs a source** — Format: `"X.ai has 50K X followers (source: x.com/x_ai, checked Feb 2026)"`. Judging panel will ask.
2. **Distribution Plan is intern-executable** — After writing each channel, ask: "Could a 22-year-old intern execute this tomorrow with no additional instructions?" If no, add more detail.
3. **Holder-gated mechanic appears in all 3 deliverables** — It's the unique differentiator. D1: no competitor has it. D2: it's the visibility strategy for premium skills. D3: it's the growth mechanic.
4. **Quality > quantity everywhere** — 5 skills with full PMF > 10 skills with 2 lines each. 5 competitors with data > 10 with descriptions.
5. **Show AI workflow, don't hide it** — The AI Showcase is +points. Document prompts as you go. Screenshot interesting outputs.
6. **Use your tech knowledge as a weapon** — Mention the bonding curve formula, the `launch()` function, the skill registry architecture. Judging panel (especially Lucas) will respect technical depth in business context.

---

## Repo Structure

```
selling-cf/
├── README.md                    ← This file (master playbook)
├── overview.md                  ← ClawFriend product deep-dive
├── competitive-landscape.md     ← Deliverable 1 (25%)
├── skill-research.md            ← Deliverable 2 (25%)
├── distribution-plan.md         ← Deliverable 3 (40%)
├── ai-showcase/
│   └── prompts.md               ← AI prompts used + screenshots
└── data/
    ├── competitor-data.md       ← Raw competitor research + sources
    └── skill-demand-data.md     ← Search volumes, Reddit counts, tool pricing
```

---

*Built with Claude + verified by hand. All data in deliverables sourced from public records.*
