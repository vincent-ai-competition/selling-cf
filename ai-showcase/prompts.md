# AI Showcase — Prompts & Workflow

> Documents the AI workflow used throughout this competition.
> For the Presentation's AI Showcase segment (12:30–14:30 in the 15-min deck).

**Core workflow**: Use AI for structured research → verify every number against real sources → document prompt + output + verification.

---

## Prompt 1: Platform Deep-Dive (Day 1 Morning)

**Context**: First prompt of the competition. Goal: extract maximum product knowledge before any business analysis.

**Prompt used**:
```
I'm competing in a 3-day business competition to build a GTM strategy for ClawFriend — a Web3 AI agent platform on BNB Smart Chain with a Skill Market. I have access to the codebase (claw-whales-skill v1.1.0), the guidebook, and the docs.

Create a comprehensive platform overview covering:
1. What ClawFriend is and its core value proposition
2. The 4 core modules (Shares Trading, Skill Market, Social Stream, Infrastructure)
3. The holder-gated viral mechanic — how it works technically and economically
4. The bonding curve economics (fees, price formula, launch() function)
5. Tech stack and API architecture
6. Target user segments
7. Business model
8. Current state and gaps (especially: community skills directory is empty)

Write it as an internal reference document I'll use throughout the competition. Tone: precise, builder-level.
```

**Output**: `overview.md` — 233 lines covering all modules, API endpoints, and the holder-gated viral loop diagram.

**Key insight extracted**: The community skills directory (`clawfriend-community-skills/`) is empty. This is not just a product gap — it's THE business problem. The entire GTM strategy should be built around solving the cold-start problem of an empty skill marketplace.

**Verification**: Cross-checked API endpoints against live docs at docs.clawfriend.ai. Confirmed `launch()` function, bonding curve fee structure (5% + 5%), and `/v1/skill-version` endpoint.

---

## Prompt 2: Competitive Landscape Framework (Day 1 Afternoon)

**Context**: Before doing any competitor research, establish the analytical framework to avoid generic "here is a list of competitors" output.

**Prompt used**:
```
I'm analyzing competitors for ClawFriend (Web3 AI agent platform on BNB Chain with Skill Market + Bonding Curve + Social Stream).

Before I present you any data, give me:
1. A competitor classification framework (tiers by relevance)
2. The exact data points I should collect per competitor (what makes a number worth citing vs. not)
3. The strategic conclusion framework — what question does my competitive analysis need to answer?
4. Red flags for bad competitive analysis (what judges will penalize)

Then: which 6-7 competitors should I prioritize researching? Include the specific URL and metric I should verify for each.
```

**Output used to structure**: `competitive-landscape.md` Tier 1–5 classification, the 4-quadrant lens, and the strategic conclusion narrative template.

**Why this matters**: Most participants will produce a flat list of competitors with copy-pasted website descriptions. This prompt produced a *strategic map* — the output answers "where is ClawFriend's opening?" not just "who exists in the market?"

---

## Prompt 3: ClawHub Live Research (Day 1 — Browser Search)

**Context**: The plan referenced "ClawHub has 5,700+ skills" from the guidebook. I needed to verify this with live data.

**Action**: Navigated directly to clawhub.ai and searched for:
1. Total skill count (homepage counter)
2. Top skills by download
3. "crypto" keyword search for all web3 skills

**What I found vs. what I expected**:
- Expected: 5,700 skills (guidebook number)
- Actual: **10,324 skills** (clawhub.ai homepage, Feb 2026)
- Expected: ClawFriend is discoverable with some installs
- Actual: **1 install all-time**, VirusTotal "Suspicious" warning displayed prominently

**Impact on strategy**: This single research finding changed the entire distribution plan. The VirusTotal flag is a blocking issue — all paid marketing would be wasted if it's not resolved first. This is the kind of insight that wins competitions.

**Verify yourself**: Visit [clawhub.ai/leeknowsai/clawfriend](https://clawhub.ai/leeknowsai/clawfriend) — the warning is still present as of Feb 2026.

---

## Prompt 4: Skill Research Framework (Day 2 Morning)

**Prompt used**:
```
I need to propose 6 skills for a ClawFriend Skill Market (Web3 AI agent platform on BNB Smart Chain).

Each skill will be judged on: PMF (7pts), Creativity (5pts), Visibility strategy (5pts), Research quality (5pts), Technical feasibility (3pts) = 25pts total.

For the BNB DeFi ecosystem specifically, help me design 6 skills that:
- Cover different user segments (traders, LPs, security-conscious buyers, agent owners)
- Have proven demand (existing paid tools as validation proxy)
- Use holder-gated mechanic where it creates natural share demand
- Are technically feasible given ClawFriend's API (BSCScan + on-chain + social stream)

For each skill, give me:
- Specific target user (not "crypto traders" — a specific persona)
- The existing paid alternatives I should research and price-check
- 2–3 demand proof points I need to verify (which Twitter accounts, which subreddits, which pricing pages)
- Why this works as a ClawFriend skill specifically (not a generic web2 tool)
```

**Verification process after the prompt**:
- Checked @whale_alert followers: 2.5M (verified from multiple sources)
- Checked Nansen pricing: $49/month annual post-Sep 2025 (verified at academy.nansen.ai)
- Checked r/CryptoMoonShots member count: 2.3M+ (verified at reddit.com/r/CryptoMoonShots)
- Checked 3Commas user count: 200K+ registered (verified at coinbureau.com)
- Checked DexScreener traffic: 10M+ monthly (verified at 99bitcoins.com)
- Checked BNB TVL: $52.7B lending (verified at defillama.com/chain/bsc)

**Key discipline**: Every number the AI generated was either verified against a real source or discarded. The final `skill-research.md` contains only verified numbers.

---

## Prompt 5: Distribution Plan — Channel Selection Logic (Day 2 Afternoon)

**Prompt used**:
```
I'm writing a distribution plan for ClawFriend, a Web3 AI agent platform on BNB Chain.

Context:
- Budget: $10,000 for Month 1
- Goal: 500–700 qualified signups (users who install ≥1 skill)
- Key constraint: VirusTotal flag on ClawHub must be resolved before paid marketing
- Audience: BNB DeFi retail traders, developers building AI agents on BNB

For Web3 products specifically:
1. What is the trust hierarchy for acquisition? (why KOLs outperform banner ads)
2. How do I calculate a realistic CAC for Twitter/X ads targeting crypto audiences?
3. What is a reasonable conversion rate from Twitter/X ad click to skill install?
4. How should I structure the KOL brief for a DeFi product? (what to avoid)
5. What organic channels specifically work for BNB ecosystem products?

Then build me a $10,000 budget allocation with:
- Channel breakdown (%)
- Realistic CAC per channel
- Week-by-week timeline
- Cut criteria per channel (at what number do I reallocate?)
```

**Key AI output that I verified**:
- Twitter/X CPC benchmark for crypto: $0.33–$0.50 → I kept this as "conservative" range (industry-standard; not AI speculation)
- KOL signup estimate: 50–200 per KOL → I used 50–200 range and noted it's contingent on KOL quality and relevance
- Mirror.xyz as primary organic channel → Verified it's indexed by search engines and has high domain authority for Web3 content

**What I changed from AI output**: Initial AI draft had $40K budget (hallucinated constraint). I corrected to $10K and recalculated all unit economics manually.

---

## Prompt 6: BGK Q&A Preparation (Day 3 Morning)

**Prompt used**:
```
I'm presenting a Web3 business strategy for ClawFriend to a judging panel (BGK) of experienced startup investors and developers in Vietnam.

Based on my competitive landscape, skill research, and distribution plan, prepare me for the 5 hardest questions they will ask. For each:
- State the question in Vietnamese (as they'll likely ask it)
- Give the optimal answer structure (not just content — what to say first, what data to cite, how to handle the emotional trap in the question)
- Give the version to avoid (what most presenters do wrong)

Specific vulnerabilities they'll probe:
1. Competitor with more users (Virtuals has 18K agents)
2. Is the skill demand real? (not just theoretical)
3. Is $10K enough for 700 users?
4. Why not just use ChatGPT?
5. What's the backup plan if KOLs don't deliver?
```

**Key insight from this prompt**: The "why not just use ChatGPT?" question is actually the easiest to answer if you reframe it correctly. ChatGPT cannot: (a) access BNB on-chain data in real-time, (b) execute transactions, (c) operate autonomously via cron jobs. The answer isn't defensive — it's an opportunity to explain what ClawFriend agents actually are (economic operators, not chatbots).

---

## AI Workflow Summary

**The 3-step verify-before-use discipline**:

```
Step 1: AI generates framework / structure / hypothesis
Step 2: Human verifies every claim against real sources
Step 3: Only verified data enters the deliverable
```

**Where AI added the most value**:
- Structuring the competitive landscape analysis (5 tiers, 4-quadrant lens)
- Designing the 6-skill portfolio for maximum scoring coverage
- Writing the BGK Q&A preparation in the exact framing that works for startup pitches
- Calculating unit economics and CAC formulas quickly

**Where AI was actively wrong** (and I corrected):
- Hallucinated user counts for obscure platforms (no source → discarded)
- Overestimated Twitter Ads conversion rates (I used conservative end of cited benchmarks)
- Missed the VirusTotal flag on ClawHub (found by direct browser research, not AI)
- Initial budget allocation didn't match the $10K constraint

**Rule I followed throughout**: If I can't find a URL for a number, it doesn't appear in a deliverable.
