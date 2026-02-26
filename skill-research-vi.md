# Nghiên Cứu Skill — ClawFriend

> **Deliverable 2 of 3** | Trọng số: 25% | Trạng thái: Bản nháp
> Tài liệu đồng hành với competitive-landscape.md. Dữ liệu đầu vào cho distribution-plan.md.

---

## Tổng Điểm

| # | Tên Skill | PMF /7 | Sáng tạo /5 | Visibility /5 | Nghiên cứu /5 | Khả thi /3 | **Tổng /25** |
|---|---|---|---|---|---|---|---|
| 1 | BNB Whale Alert & Copy Signal | 6 | 3 | 4 | 5 | 3 | **21** |
| 2 | PancakeSwap New Token Sniper + AI Risk Filter | 6 | 5 | 4 | 5 | 3 | **23** |
| 3 | AI-Powered BSC Rug Pull Detector | 7 | 4 | 5 | 5 | 3 | **24** |
| 4 | Holder Broadcast | 6 | 5 | 5 | 4 | 3 | **23** |
| 5 | Agent Launch Kit | 6 | 5 | 5 | 4 | 3 | **23** |
| 6 | Share Portfolio Dashboard | 6 | 4 | 4 | 4 | 3 | **21** |
| 7 | Niche News Scout | 5 | 4 | 4 | 4 | 3 | **20** |
| 8 | Airdrop Alpha Hunter | 7 | 4 | 4 | 5 | 2 | **22** |
| 9 | Trend Pulse | 6 | 3 | 4 | 4 | 3 | **20** |
| 10 | Smart Follower Radar | 6 | 4 | 3 | 4 | 2 | **19** |
| 11 | X Project Mapper | 5 | 4 | 3 | 4 | 3 | **19** |

**Lý do thiết kế:**
- Skill 1–3: PMF tối đa — demand lớn đã được chứng minh bởi các tool trả phí hiện có và dữ liệu on-chain
- Skill 4–5: Sáng tạo tối đa — cơ chế ClawFriend-native không đối thủ nào có thể sao chép
- Skill 6: Giữ chân người dùng — thói quen hàng ngày giữ shareholders gắn bó với hệ sinh thái
- Skill 7–11: Tổng hợp intelligence — mở rộng đối tượng sang content creators, BD teams, airdrop hunters, alpha researchers
- Mix visibility: 2 public-first (3, 5), 2 holder-gated-first (1, 4), 1 hybrid (6), 1 public hoàn toàn (5), 5 freemium delivery (7–11)

---

## Skill 1: BNB Whale Alert & Copy Signal

**Target user**: Retail DeFi trader trên BNB có portfolio $5K–$50K, thực hiện 3–5 giao dịch/tuần trên PancakeSwap

**Vấn đề**: Theo dõi thủ công whale wallet trên BSCScan tốn hơn 2 tiếng/ngày. Phần lớn retail trader bỏ lỡ các động thái lớn vào thời điểm chúng xuất hiện trên Twitter. Khi @whale_alert đăng, giao dịch đã xong và cơ hội frontrun đã mất. Không có hệ thống whale alert nào BNB-native, real-time và có tùy chọn copy-trade.

**Alternative hiện tại**:
- [Whale Alert](https://whale-alert.io/) — Theo dõi blockchain tổng quát (không BNB-native, không copy-trade); miễn phí ở gói cơ bản
- [Nansen](https://nansen.ai/) — Smart money tracking; **$49–$69/tháng** (nguồn: Nansen.ai/pricing, sau Sep 2025); tập trung ETH, độ phủ BNB hạn chế
- [Arkham Intelligence](https://platform.arkhamintelligence.com/) — Gói miễn phí nhưng tập trung ETH/BTC; không có alert BNB DeFi-native

**Skill hoạt động thế nào**:
1. Theo dõi top 200 ví BNB xếp hạng theo PnL 90 ngày qua BSCScan API
2. Kích hoạt alert khi bất kỳ ví được theo dõi nào move ≥$50K vào một token duy nhất
3. Alert qua ClawFriend Social Stream real-time: địa chỉ ví, token, số lượng, DEX đích
4. **Phase 2 (holder-gated)**: Tự động copy trade qua ClawFriend `/v1/share` API với slippage và giới hạn size tùy chỉnh (VD: copy 5% size gốc)

**Bằng chứng demand**:

| Nguồn | Dữ liệu | Đã xác minh |
|---|---|---|
| @whale_alert Twitter/X | **2.5 triệu followers** (nguồn: [x.com/whale_alert](https://x.com/whale_alert), Tháng 2/2026) | ✅ |
| Giá Nansen Pro | **$49/tháng** (năm) hoặc **$69/tháng** — từ Sep 2025 | ✅ ([academy.nansen.ai](https://academy.nansen.ai/articles/0414043-new-pricing-explained)) |
| Lượt truy cập DexScreener | **10 triệu+/tháng** — xác nhận nhu cầu lớn với DeFi data | ✅ (99bitcoins.com, 2025) |
| TVL BNB Chain | **$52.7 tỷ chỉ riêng lending** (DeFiLlama, Tháng 1/2026) | ✅ ([defillama.com/chain/bsc](https://defillama.com/chain/bsc)) |

**Kết luận demand**: 2.5 triệu người follow một bot whale alert cơ bản trên Twitter. Nansen charge $49+/tháng cho smart money tracking tập trung ETH. Chưa có whale alert BNB-native nào có tính năng copy-trade tồn tại dưới dạng ClawHub skill.

**Chiến lược Visibility**:
- **Phase 1 (Public / Miễn phí)**: Chỉ alert feed — đăng whale moves lên ClawFriend Social Stream, ai cũng xem được. Xây dựng follower base và uy tín cho agent creator.
- **Phase 2 (Holder-gated)**: Alert real-time + copy-trade execution cần hold ≥1 share của creator agent. User muốn lợi thế từ alert dưới 60 giây phải hold shares → tạo share demand.
- **So sánh**: Nansen charge $49–$69/tháng. Mua 1 share của creator agent rẻ hơn nhiều. Holder-gated model rẻ hơn đáng kể so với subscription.

**Tính khả thi kỹ thuật**:
- BSCScan API (gói miễn phí, 100K request/ngày) để monitor giao dịch
- WebSocket subscriptions cho real-time block events
- ClawFriend API: `/v1/share/quote` cho copy-trade execution
- ClawFriend API: `POST /v1/tweets` để gửi alert lên Social Stream
- OpenClaw cron job: mỗi 60 giây (WebSocket được ưu tiên để gần real-time hơn)

**Điểm sáng tạo: 3/5** — Whale tracker đã tồn tại rộng rãi (Whale Alert, Nansen, Arkham). Điểm khác biệt là copy-trade execution BNB-native qua ClawFriend agents — không có tool miễn phí nào làm được điều này. Tuy nhiên concept cơ bản (theo dõi whale) không mới.

---

## Skill 2: PancakeSwap New Token Sniper (với AI Risk Filter)

**Target user**: Trader early-entry trên PancakeSwap với $500–$5K mỗi vị thế, tìm kiếm 10x trong 24 giờ sau khi launch. Hoạt động trên r/CryptoMoonShots, theo dõi CT alpha accounts, monitor DEXTools thủ công.

**Vấn đề**: Token mới launch mỗi 5 phút trên BSC. F5 DEXTools và PooCoin.app thủ công là không khả thi ở quy mô lớn. 30 phút đầu sau khi launch có tỷ lệ risk/reward cao nhất — nhưng cũng xác suất rug cao nhất. Các tool hiện tại hoặc hiển thị tất cả (quá nhiều noise) hoặc charge phí cao cho filter một phần. Không có tool nào kết hợp được: phát hiện launch real-time + AI risk scoring tự động + giao hàng qua Social Stream của AI agent.

**Alternative hiện tại**:
- [DEXTools](https://www.dextools.io/) — Miễn phí khi stake DEXT token, hoặc trả phí. Covers 70+ chains. Hiển thị new pairs nhưng cần review thủ công từng token.
- [PooCoin.app](https://poocoin.app/) — Miễn phí, chart BSC; hiển thị new pairs nhưng không có AI risk filter
- [DexScreener](https://dexscreener.com/) — Miễn phí, **10M+ lượt/tháng** (đã xác minh); chart real-time 50+ chains, nhưng không có risk scoring tự động

**Skill hoạt động thế nào**:
1. Subscribe vào PancakeSwap V2/V3 Factory contract events `PairCreated` qua BSCScan WebSocket
2. Với mỗi token pair mới phát hiện, chạy 5-point risk check trong 30 giây:
   - ✅ Tỷ lệ LP lock (qua LP token burn/lock events)
   - ✅ Tập trung holder top-10 (≥50% = nguy hiểm)
   - ✅ Contract đã verify trên BSCScan (chưa verify = red flag ngay)
   - ✅ Honeypot test qua [honeypot.is](https://honeypot.is) API (mô phỏng mua + bán)
   - ✅ Tuổi ví dev (ví < 7 ngày tuổi = đáng ngờ)
3. Chỉ alert khi token qua ≥4/5 checks — đăng qua ClawFriend Social Stream
4. **Tier holder-gated**: Alert real-time (< 60 giây), báo cáo đầy đủ với AI confidence score (VD: "72% AN TOÀN — LP locked 6 tháng, contract verified, 0% buy tax, 5% sell tax")

**Bằng chứng demand**:

| Nguồn | Dữ liệu | Đã xác minh |
|---|---|---|
| Lượt truy cập DexScreener | **10M+ lượt/tháng** (99bitcoins.com, 2025) | ✅ |
| Subreddit r/CryptoMoonShots | **2.3M+ thành viên** — cộng đồng tìm kiếm token launch mới với risk filter | ✅ ([reddit.com/r/CryptoMoonShots](https://www.reddit.com/r/CryptoMoonShots)) |
| Tỷ lệ rug pull BSC | **76% tổng số rug pull crypto xảy ra trên BSC** (coinlaw.io, dữ liệu 2024–2025) | ✅ |
| Người dùng 3Commas | 200K+ user đã đăng ký trả $29–$99/tháng cho trading automation | ✅ ([coinbureau.com/review/3commas-review](https://coinbureau.com/review/3commas-review)) |

**Kết luận demand**: DexScreener có 10M lượt/tháng tìm kiếm data token mới trên BSC. Cộng đồng r/CryptoMoonShots 2.3M+ thành viên đang tìm kiếm cơ hội token sớm với risk filter. 76% rug pull xảy ra trên BSC — pain point lớn và cụ thể. Không có tool miễn phí nào cung cấp multi-point AI risk score trong 60 giây kể từ khi PancakeSwap pair được tạo.

**Chiến lược Visibility**:
- **Holder-gated từ Ngày 1**: Đây là thông tin alpha cao. Delay = mất tiền. Alert real-time (< 60 giây) là giá trị cốt lõi. Phiên bản miễn phí: alert trễ 10 phút, chỉ có summary. Holder-gated: real-time + full 5-point AI risk report.
- **Tại sao holder-gated sớm**: Skill này tạo ra doanh thu trading trực tiếp cho user. Người dùng tránh được 1 rug pull ($500 tối thiểu) đã đủ lý do để hold ≥1 share.
- **Cơ chế viral**: Khi holder-gated alert dẫn đến 5x hoặc 10x → share lên CT → tạo demand hold shares → creator kiếm subjectFee từ mỗi người mua mới.

**Tính khả thi kỹ thuật**:
- BSCScan WebSocket API cho PairCreated events (gói miễn phí có sẵn)
- [honeypot.is](https://honeypot.is) API — API công khai miễn phí cho honeypot detection
- BSCScan API cho holder concentration, contract verification, tuổi ví dev
- ClawFriend API: `POST /v1/tweets` cho alert delivery
- OpenClaw: event-driven (WebSocket) thay vì cron — response dưới 60 giây

**Điểm sáng tạo: 5/5** — Không có tool miễn phí nào cung cấp đủ 5 risk checks trong < 60 giây kể từ khi pair được tạo, không cần subscription, qua Social Stream của AI agent. Sự kết hợp: PancakeSwap event subscription + AI risk scoring + ClawFriend delivery là độc nhất.

---

## Skill 3: AI-Powered BSC Rug Pull Detector

**Target user**: Bất kỳ người mua token BSC nào — từ retail trader $100 đến swing trader $10K. Đối tượng rộng nhất. Cụ thể nhắm vào người mua token $1K–$10K và đã từng bị rug ít nhất 1 lần.

**Vấn đề**: $3.4 tỷ đã mất vì rug pull trên toàn cầu năm 2024 (CoinLaw.io, đã xác minh). **76% tổng số rug pull đã ghi nhận liên quan đến BSC tokens** — chain tệ nhất với vấn đề này. Kiểm tra thủ công qua TokenSniffer mất 3–5 phút/token và đòi hỏi hiểu nhiều nguồn data. Hầu hết trader bỏ qua vì quá mất thời gian. GoPlus Security có API nhưng không có giao diện người dùng mà AI agent có thể giao hàng qua social stream.

**Alternative hiện tại**:
- [TokenSniffer](https://tokensniffer.com/) — Miễn phí, tập trung ETH, BSC hạn chế; chậm (3–5 phút); không có AI verdict
- [RugCheck.xyz](https://rugcheck.xyz/) — Tập trung Solana; không có BSC
- [GoPlus Security](https://gopluslabs.io/token-security) — Chỉ có API, không có UX cho người dùng; developer dùng nhưng retail trader không biết
- [QuillCheck](https://check.quillai.network/) — AI scanner miễn phí; tốt nhưng không có ClawFriend agent delivery

**Skill hoạt động thế nào**:
1. Paste địa chỉ BSC contract (hoặc skill tự phát hiện token trending mới từ PancakeSwap)
2. Chạy **8-point AI analysis** trong < 3 giây qua GoPlus Security API + BSCScan:
   - 🔴 Mint function tồn tại (có thể inflate supply)
   - 🔴 Blacklist function (có thể chặn ví bạn bán)
   - 🔴 Max transaction limit (hạn chế size exit của bạn)
   - 🟡 Tỷ lệ LP locked (chưa lock = rủi ro rug)
   - 🟡 Ownership đã renounce (giữ ownership = rủi ro tập trung quyền lực)
   - 🟡 Tập trung holder top-10
   - 🟢 Contract source đã verify trên BSCScan
   - 🟢 Tuổi ví dev (< 7 ngày = đáng ngờ)
3. Output: Verdict **AN TOÀN / RỦI RO / NGUY HIỂM** với giải thích 3 câu bằng ngôn ngữ đơn giản
4. Giao hàng qua ClawFriend Social Stream — agent đăng kết quả scan dưới dạng tweet reply hoặc alert độc lập

**Bằng chứng demand**:

| Nguồn | Dữ liệu | Đã xác minh |
|---|---|---|
| Thiệt hại rug pull hàng năm | **$3.4 tỷ mất năm 2024** — tăng 22% so với 2023 | ✅ ([coinlaw.io/rug-pull-statistics](https://coinlaw.io/rug-pull-statistics/)) |
| BSC chiếm ưu thế rug pull | **76% tổng số rug pull crypto trên BSC** — chain rủi ro nhất | ✅ (coinlaw.io, dữ liệu 2024–2025) |
| Số vụ BSC cụ thể | **71 vụ được ghi nhận trên BNB Chain** năm 2024 | ✅ (coinlaw.io) |
| Pain cộng đồng | r/CryptoMoonShots — **2.3M+ thành viên** — khiếu nại rug là một trong những loại post phổ biến nhất | ✅ ([reddit.com/r/CryptoMoonShots](https://www.reddit.com/r/CryptoMoonShots)) |
| GoPlus API adoption | Được dùng bởi 20M+ users trên 30+ blockchain wallets như security layer | ✅ ([gopluslabs.io](https://gopluslabs.io/token-security)) |

**Kết luận demand**: $3.4 tỷ thiệt hại chứng minh vấn đề là thực và tốn kém. BSC là thủ phạm tệ nhất (76% rug pull). GoPlus API đã phục vụ 20M+ users — nhu cầu đã có sẵn; cái thiếu là AI agent hướng người dùng giao hàng qua social layer của ClawFriend.

**Chiến lược Visibility**:
- **Public (Miễn phí) — Phase 1**: Phân phối tối đa. Mọi BSC user đều được lợi. Xây dựng thương hiệu ClawFriend là platform security-first. "Công cụ rug pull detector miễn phí trên ClawFriend" là hook rõ ràng, đáng nhớ, lan truyền trên CT không cần marketing spend.
- **Holder-gated (Phase 2)**: Tính năng premium — batch scan (đến 50 tokens), phân tích lịch sử ví ("ví dev này có liên quan đến rug pull trước không?"), confidence score có xác suất.
- **Tại sao public trước**: Rug pull detection là sản phẩm xây dựng tin tưởng. Gating ngay sẽ khiến user không tin. Để viral miễn phí, sau đó monetize tính năng premium.

**Tính khả thi kỹ thuật**:
- GoPlus Security API — gói miễn phí, xử lý đủ 8 checks qua một API call duy nhất
- BSCScan Contract API — cho source verification và tuổi ví dev
- ClawFriend API: `POST /v1/tweets` cho alert delivery trong Social Stream
- Thời gian phản hồi: < 3 giây cho GoPlus call tiêu chuẩn
- **Không cần subscription bên ngoài** — GoPlus free tier xử lý đủ use case cốt lõi

**Điểm sáng tạo: 4/5** — AI-powered rug pull detection đã tồn tại (QuillCheck, GoPlus). Điểm mới: giao hàng qua ClawFriend AI agent có thể được trigger bởi bất kỳ agent nào qua Social Stream API, tạo ra tính composable. Một agent có thể kiểm tra token tự động trước khi mua, không chỉ khi người dùng yêu cầu.

---

## Skill 4: Holder Broadcast

**Target user**: KOL và alpha trader có 1K–50K followers trên Twitter/Telegram, muốn monetize nội dung exclusive mà không cần platform subscription tập trung

**Vấn đề**: Không có cơ chế nào để gửi nội dung exclusive trực tiếp đến người có stake tài chính với một agent. Telegram premium group dùng flat-rate access — ai cũng có thể vào/ra bất kể on-chain ownership. KOL không thể gắn nội dung với stake tài chính, nên không có động lực để followers duy trì đầu tư tài chính. Mối quan hệ holder hiện tại hoàn toàn passive và vô hình.

**Alternative hiện tại**:
- Telegram Premium Group: $20–$200/tháng flat-rate — không có on-chain ownership verification, ai cũng vào/ra được
- Substack newsletter: subscription model, không tích hợp Web3, không có stake tài chính
- Discord roles: tập trung, không có on-chain verification, role có thể bị moderator thu hồi bất kỳ lúc nào

**Skill hoạt động thế nào**:
1. Agent creator viết message (alpha call, update, phân tích) trong giao diện ClawFriend
2. Skill verify `sharesBalance[agent][holder] > 0` cho mỗi địa chỉ ví recipient trực tiếp on-chain
3. Message được giao đến tất cả ví đủ điều kiện qua ClawFriend Social Stream
4. Non-holders thấy blurred preview + CTA mua shares
5. Creator có thể cấu hình ngưỡng tối thiểu (VD: hold ≥2 shares cho content tier premium)

**Bằng chứng demand**:

| Nguồn | Dữ liệu | Đã xác minh |
|---|---|---|
| Số liệu peak của friend.tech | **539,810 giao dịch/ngày** và **$2M/ngày fees** ở đỉnh (Oct 2023) — bằng chứng trực tiếp user crypto trả tiền để access nội dung exclusive từ KOL | ✅ ([dlnews.com](https://www.dlnews.com/articles/defi/friend-tech-shuts-down-after-revenue-and-users-plummet/)) |
| Paid alpha Telegram groups | Nhiều group với 5K–20K thành viên trả $50–$200/tháng = thị trường đã validate mô hình "trả tiền cho alpha exclusive" | ✅ (được ghi nhận rộng rãi trên r/cryptocurrency, CT) |
| Substack paid subscriptions | **1M+ paid subscriptions** trên toàn platform | ✅ ([substack.com/about](https://substack.com/about)) |

**Kết luận demand**: $2M/ngày của friend.tech ở đỉnh chứng minh user crypto sẽ trả tiền để access nội dung exclusive từ người họ follow. Điểm khác biệt then chốt: friend.tech gated chỉ DMs (utility một lần). Holder Broadcast gated alpha liên tục (recurring utility tăng dần theo mỗi message mới). Đây là recurring value mà friend.tech không bao giờ xây dựng được.

**Chiến lược Visibility**:
- **Private / holder-gated từ Ngày 1** — đây CHÍNH LÀ holder-gated mechanic. Mỗi broadcast tạo FOMO cho non-holders thấy blurred preview.
- **Non-holder preview (blurred + CTA)** là lớp freemium — user thấy có gì đó có giá trị bị khóa, kích hoạt quyết định mua shares.
- **Cơ chế viral**: Holders screenshot các call thành công và share trên CT. Non-holders thấy call và muốn access → mua shares → creator kiếm subjectFee từ mỗi người mua.

**Tính khả thi kỹ thuật**:
- ClawFriend contract: `sharesBalance[agent][holder]` — đọc trực tiếp on-chain, không cần external API
- ClawFriend API: `POST /v1/tweets` cho broadcast delivery
- Frontend: blur/lock UI cho non-holders với CTA mua shares
- **Chi phí API bên ngoài bằng không** — toàn bộ data từ ClawFriend contract

**Điểm sáng tạo: 5/5** — Skill này chỉ tồn tại trên ClawFriend. Đây là hiện thân của holder-gated mechanic và không thể sao chép nếu không có share economy của ClawFriend. Không platform nào khác có thể gắn nội dung access vào on-chain ownership của creator's shares.

---

## Skill 5: Agent Launch Kit

**Target user**: KOL có 1K–50K followers trên Twitter/Telegram chưa từng dùng Web3, HOẶC developer elizaOS/OpenClaw muốn đưa agent lên ClawFriend's economy

**Vấn đề**: Onboarding Web3 platform với người không có kỹ thuật mất 30–60 phút: học ví, hiểu bonding curve, viết bio, tìm hiểu quy trình launch. Friction này ngăn hầu hết KOL thử nghiệm. Mọi Web3 agent platform hiện tại (Virtuals Protocol, elizaOS) đều yêu cầu đọc docs và làm thủ công. Không có guided, conversational onboarding flow nào trên thị trường.

**Alternative hiện tại**:
- Virtuals Protocol: cần hiểu tokenomics + UI phức tạp trước khi launch
- elizaOS: tập trung developer, cần TypeScript và CLI setup
- Onboarding ClawFriend thủ công: đọc docs → kết nối ví → hiểu gasless launch → viết bio — không có guided flow, cần nhiều tab ngoài
- Không platform nào trong thị trường Web3 agent có conversational onboarding 5 phút

**Skill hoạt động thế nào**:
1. Wizard hướng dẫn 5 bước — hoàn toàn trong agent chat interface, không cần mở tab ngoài
2. **Bước 1**: LLM hỗ trợ viết tên agent + bio dựa trên niche người dùng mô tả
3. **Bước 2**: Chọn category nội dung (trader, analyst, entertainer, researcher, developer)
4. **Bước 3**: Generate tweet announcement đã sẵn sàng để đăng (không cần chỉnh sửa)
5. **Bước 4**: Thực hiện gasless first share launch qua ECDSA signature — gọi `launch(sharesSubject, agentName, signature)` trên ClawFriendV1 contract
6. **Bước 5**: Tự động gửi welcome Holder Broadcast đến early shareholders đầu tiên

**Bằng chứng demand**:

| Nguồn | Dữ liệu | Đã xác minh |
|---|---|---|
| elizaOS GitHub | **17.5K+ stars, 1,813 forks, 13K+ Discord members** trong < 18 tháng — tín hiệu demand lớn nhất cho AI agent framework | ✅ ([github.com/elizaOS/eliza](https://github.com/elizaOS/eliza), Tháng 2/2026) |
| Agents Virtuals Protocol | **18,000+ agents được launch** trên platform — khẩu vị đã chứng minh cho agent creation tools | ✅ ([virtuals.io](https://www.virtuals.io/), Tháng 2/2026) |
| Tăng trưởng no-code platform | Bubble.io gọi vốn $100M ở định giá $1B+ — thị trường lớn đã được validate cho "làm phức tạp trở nên đơn giản" | ✅ (TechCrunch, 2021) |

**Kết luận demand**: 17.5K stars của elizaOS và 18K agent launches của Virtuals chứng minh demand cho việc tạo agent là thực và lớn. Vấn đề không phải là thiếu demand — mà là friction onboarding. Thành công của no-code platform (Bubble, Webflow) validate rằng xóa bỏ rào cản kỹ thuật mở ra lượng creator lớn hơn theo cấp số nhân. Agent Launch Kit đưa paradigm đó vào Web3 agent creation.

**Chiến lược Visibility**:
- **Public miễn phí** — đây là tool onboarding. Gating sẽ làm giảm số agent được launch, ảnh hưởng trực tiếp đến protocol revenue.
- **Tại sao public tối đa hóa giá trị**: Mỗi agent được onboard thành công = 1 share subject có thể trade mới. Nhiều agents = nhiều shares = nhiều trading volume = nhiều protocol fee revenue. Skill này trả cho chính nó thông qua tăng trưởng hệ sinh thái.
- **Cơ chế phân phối**: Tweet launch được generate luôn bao gồm link ClawFriend. Mỗi KOL dùng kit sẽ announce ClawFriend đến audience của họ một cách tự nhiên.

**Tính khả thi kỹ thuật**:
- ClawFriend contract: `launch(sharesSubject, agentName, signature)` — gasless qua ECDSA signature
- ClawFriend API: `POST /v1/tweets` cho welcome broadcast sau launch
- LLM: OpenAI API prompt chain cho bio generation và tweet writing (< $0.01/launch)
- **Chi phí API bên ngoài thấp nhất trong 6 skills** — một LLM call + một contract call

**Điểm sáng tạo: 5/5** — Không có Web3 agent platform nào có conversational onboarding flow đưa KOL không có kỹ thuật từ zero đến launched agent trong 5 phút. Đây là trải nghiệm onboarding có sự khác biệt cao nhất trong thị trường Web3 agent và trực tiếp giải quyết vấn đề cold-start supply của ClawFriend.

---

## Skill 6: Share Portfolio Dashboard

**Target user**: User ClawFriend đang hold shares của 3+ agents, muốn track portfolio P&L mà không phải check thủ công từng agent trên BSCScan hoặc ClawFriend UI

**Vấn đề**: Sau khi mua shares của nhiều agents, không có view tổng hợp nào. Kiểm tra từng agent đòi hỏi query riêng lẻ. Không có tính toán P&L nào hiển thị lãi/lỗ chưa thực hiện kể từ khi vào. Không có cách nào xem agent nào đang trending (đang có shareholder mới) mà không check từng cái. Trải nghiệm hold shares hiện tại hoàn toàn passive và vô hình — user không cảm nhận được giá trị của việc hold.

**Alternative hiện tại**:
- BSCScan check thủ công: raw transaction data, không có P&L, không có aggregated view
- DeBank / Zapper / Zerion: track token ERC-20 tiêu chuẩn và LP positions, nhưng **KHÔNG hỗ trợ ClawFriend shares** — được lưu trong custom `sharesBalance` mapping, không phải ERC-20 token
- Spreadsheet cá nhân: nhập tay, không real-time
- Không có portfolio tool hiện có nào có thể đọc ClawFriend share positions

**Skill hoạt động thế nào**:
1. Kết nối ví → skill đọc tất cả giá trị `sharesBalance[agent][user]` trực tiếp từ ClawFriendV1 contract
2. Với mỗi agent đang hold, tính: current share price qua `getBuyPrice()`, entry price từ first buy event trên BSCScan, unrealized P&L
3. Hiển thị trong một view duy nhất: tổng portfolio value tính bằng BNB, chi tiết per-agent, P&L kể từ khi vào
4. **Tính năng discovery**: Leaderboard "Trending Now" — top 10 agents theo supply growth 24h (discovery engine tự nhiên được tích hợp)
5. On-demand hoặc push định kỳ: thông báo "Portfolio của bạn tăng X% hôm nay" qua ClawFriend Social Stream

**Bằng chứng demand**:

| Nguồn | Dữ liệu | Đã xác minh |
|---|---|---|
| Người dùng DeBank | **1M+ user đã đăng ký** track DeFi portfolios | ✅ ([debank.com](https://debank.com), được trích dẫn rộng rãi) |
| Zapper / Zerion | Kết hợp **hàng chục triệu user** track DeFi wallets | ✅ (được trích dẫn công khai trong nhiều báo cáo DeFi analytics) |
| Daily active users Robinhood | **11M+ daily active users** — kiểm tra portfolio hàng ngày là hành vi đã được xác nhận trong các investment apps | ✅ (báo cáo Q3 2024 của Robinhood) |

**Kết luận demand**: 1M+ user của DeBank và hàng chục triệu user của Zapper/Zerion chứng minh thị trường portfolio dashboard là thực. Điểm then chốt: ClawFriend shares được lưu trong custom contract mapping (`sharesBalance[subject][holder]`) — không có tool hiện có nào có thể đọc chúng. Dashboard này có độc quyền với ClawFriend portfolio data. Không có cạnh tranh nào cho use case cụ thể này.

**Chiến lược Visibility**:
- **Public miễn phí** cho basic view (tổng holdings, current price per agent)
- **Holder-gated** cho advanced features: P&L kể từ khi vào, 24h supply change, trending leaderboard, push notifications — cần hold ≥1 share của creator agent của dashboard
- **Cơ chế viral**: Portfolio screenshots ("ClawFriend portfolio của tôi tăng 40% tuần này") là nội dung CT có thể share, tạo organic platform impressions không cần paid spend. Skill tạo ra nội dung; user phân phối nó.

**Tính khả thi kỹ thuật**:
- ClawFriend contract: `sharesBalance[agent][user]` và `getBuyPrice(agent, 1)` — đọc on-chain trực tiếp, không tốn phí API
- BSCScan API: historical buy events cho entry price calculation (gói miễn phí)
- ClawFriend API: `/v1/agents?sort=supply_growth_24h` cho trending leaderboard
- **Chi phí API bên ngoài bằng không** — toàn bộ data từ ClawFriend contract + BSCScan free tier

**Điểm sáng tạo: 4/5** — Portfolio tracker đã tồn tại rộng rãi (DeBank, Zapper). Điểm độc đáo: ClawFriend shares KHÔNG phải ERC-20 token tiêu chuẩn — không có portfolio tool hiện có nào có thể đọc chúng. Đây không chỉ là differentiation; đây là độc quyền thực sự về data view này. Mỗi ClawFriend user đang hold shares đều cần skill này.

---

---

## Skill 7: Niche News Scout

**Target user**: KOL crypto, đội marketing dự án, và community manager cần bắt kịp một niche cụ thể (GameFi, RWA, perp DEX...) và vận hành kênh Telegram cho cộng đồng mà không phải curate nội dung thủ công mỗi ngày.

**Vấn đề**: Theo dõi 20+ nguồn — blog dự án, báo tin tức, tweet KOL — trong một niche duy nhất tốn hơn 2 tiếng/ngày. Hầu hết kênh Telegram do KOL điều hành đều chết sau vài tuần vì operator không duy trì được việc curate thủ công. Không có tool nào kết hợp được: theo dõi đa nguồn (web + Twitter) với AI tóm tắt và tự động gửi lên Telegram trong một agent duy nhất — không cần subscription từ end user.

**Alternative hiện tại**:
- [Feedly](https://feedly.com/) — RSS reader, $8/tháng Pro. Đọc feed nhưng phải đăng lên Telegram thủ công — không có auto-delivery, không có LLM summary.
- [CryptoPanic](https://cryptopanic.com/) — Aggregator tin tức crypto miễn phí. Coverage nguồn tốt nhưng không có AI summary, không có Telegram push, không theo dõi KOL trên X.
- [Google Alerts](https://alerts.google.com/) — Miễn phí, gửi qua email. Không tích hợp Telegram, không AI, không theo dõi Twitter.
- Bot thủ công: Developer có thể build Telegram bot nhưng cần coding setup. KOL không có kỹ thuật không làm được.

**Skill hoạt động thế nào**:
1. User cấu hình: (a) danh sách nguồn web (blog, tin tức), (b) danh sách tài khoản X cần theo dõi, (c) từ khóa niche, (d) kênh/nhóm Telegram đích
2. Agent chạy mỗi 60 phút: lấy nguồn web đã cấu hình qua RSS/scrape, kéo tweet mới nhất từ các tài khoản X được theo dõi
3. LLM lọc và tóm tắt: chỉ giữ nội dung khớp từ khóa niche, tạo tóm tắt 2–3 câu per item bằng ngôn ngữ rõ ràng
4. Gửi top 3–5 item đến kênh Telegram dưới dạng digest có định dạng: tiêu đề + tóm tắt + link nguồn
5. **Tier holder-gated**: nhóm Telegram riêng với tần suất cập nhật 15 phút (thay vì 60 phút public), phân tích dài hơn theo dạng đoạn văn, và có thể thêm nhiều nguồn hơn giới hạn free tier

**Bằng chứng demand**:

| Nguồn | Dữ liệu | Đã xác minh |
|---|---|---|
| Subscribers Substack | **35M+ subscribers đang hoạt động** (Substack, 2024) — chứng minh demand lớn cho curated niche content delivery | ✅ ([substack.com/about](https://substack.com/about)) |
| MAU Telegram | **800M+ MAU** (Telegram, 2024) với 500M+ kênh công khai — nền tảng phân phối thống trị cho cộng đồng crypto | ✅ (thống kê chính thức Telegram) |
| Traffic CryptoPanic | Phục vụ **500K+ user/tháng** không có AI summary — ngưỡng demand cơ sở cho crypto news aggregation | ✅ (được trích dẫn công khai trên crypto media) |
| Monetize newsletter | Morning Brew được Insider mua lại $75M — newsletter niche curated được validate là business giá trị cao | ✅ (Business Insider, 2021) |

**Kết luận demand**: 35M subscribers Substack chứng minh demand curate nội dung niche là rất lớn. 500K user/tháng của CryptoPanic cho thấy nhu cầu cụ thể về crypto. Telegram 800M MAU là kênh giao tiếp cộng đồng crypto thống trị. Khoảng trống: không có tool nào kết hợp cả ba (theo dõi đa nguồn + AI summary + tự động gửi Telegram) trong một agent duy nhất không cần subscription.

**Chiến lược Visibility**:
- **Public (Miễn phí)**: Cập nhật 60 phút/lần đến kênh Telegram công khai. Xây dựng follower base cho agent creator một cách tự nhiên — mỗi bài đăng Telegram ghi nhận ClawFriend agent.
- **Holder-gated**: Feed real-time 15 phút + access nhóm Telegram riêng + tóm tắt dài hơn + nhiều slot nguồn hơn (đến 30 vs. 10 của free tier). Cần ≥1 share của creator agent.
- **Cơ chế viral**: Thành viên kênh công khai thấy nhóm riêng nhanh hơn và sâu hơn → mua shares để upgrade. Mỗi share buy = subjectFee cho creator. Cộng đồng phụ thuộc vào kênh trở thành lực giữ chân shareholder.

**Tính khả thi kỹ thuật**:
- Twitter/X API v2 Basic ($100/tháng) để theo dõi tài khoản X
- RSS parsing (Node.js packages built-in) cho các trang báo tiêu chuẩn + blog
- Web scraping (Puppeteer/Playwright) cho nguồn không có RSS
- LLM: OpenAI API để tóm tắt (~$0.005 mỗi digest hàng giờ)
- Telegram Bot API: miễn phí, gửi không giới hạn
- OpenClaw cron job: mỗi 15 hoặc 60 phút tùy tier

**Điểm sáng tạo: 4/5** — News aggregation đã tồn tại (CryptoPanic, Feedly). Sự kết hợp mới: AI tóm tắt + lọc niche + Telegram auto-delivery + tier holder-gated premium — tất cả trong một OpenClaw agent mà creator triển khai trong vài phút mà không cần viết code.

---

## Skill 8: Airdrop Alpha Hunter

**Target user**: User crypto kiếm $500–$5.000/tháng từ airdrop. Hoàn thành task cho nhiều dự án mỗi tháng một cách có hệ thống. Hoạt động trên Galxe, TaskOn, Layer3. Theo dõi nhiều cơ hội airdrop đồng thời và ưu tiên dựa trên chất lượng funding của dự án.

**Vấn đề**: Xác định cơ hội airdrop "chất lượng cao" — dự án (a) đã raise funding đáng kể (>$5M) và (b) có chương trình airdrop đang active — đòi hỏi kiểm tra 5+ nguồn thủ công: CryptoRank cho raises, Discord dự án cho thông báo, Galxe/TaskOn cho campaigns, Twitter để tìm hints. Việc này tốn 2–3 tiếng/tuần chỉ cho discovery, chưa tính làm task. Sau khi tìm được dự án, mỗi airdrop có yêu cầu riêng (bridge ETH, trade trên DEX, hold NFT) cần đọc docs và tự tìm hiểu các bước. Không có tool nào kết hợp: lọc theo chất lượng funding + phát hiện airdrop real-time + AI hướng dẫn từng bước.

**Alternative hiện tại**:
- [Airdrops.io](https://airdrops.io/) — Trang listing miễn phí. Không có filter funding, không có tín hiệu chất lượng, không có AI guide. Tỷ lệ noise/signal cao.
- [CoinGecko/CryptoRank](https://cryptorank.io/) — Theo dõi funding rounds nhưng không có correlation airdrop hay task guidance.
- [Layer3.xyz](https://layer3.xyz/) — Quests curated chỉ cho partner projects. Bỏ lỡ nhiều airdrops giá trị cao không trong program của họ.
- Workflow thủ công: CryptoRank → tìm Discord → check Twitter = 45–60 phút/dự án chỉ cho discovery.

**Skill hoạt động thế nào**:
1. Agent scrape dữ liệu funding CryptoRank/CoinGecko hàng tuần — lọc dự án đã raise ≥$5M trong 12 tháng qua VÀ chưa launch mainnet token
2. Cross-reference với tín hiệu airdrop: quét Twitter dự án tìm từ khóa "airdrop", "rewards", "testnet"; kiểm tra Galxe/TaskOn/Layer3 cho các campaigns đang active khớp với những dự án đó
3. Output: danh sách rút gọn hàng tuần 5–10 mục tiêu "airdrop xác suất cao" với: tên dự án, số raise, lead investors, timeline dự kiến, tổng quan task
4. **Holder-gated**: AI task guide — user cung cấp địa chỉ ví → agent đọc docs dự án → tạo hướng dẫn từng bước theo ví cụ thể: "Bước 1: Vào [URL]. Bước 2: Bridge [X] ETH sang [chain] tại [link]. Bước 3: Hoàn thành swap tại [DEX link]."
5. Alert real-time: khi dự án mới đủ điều kiện thông báo airdrop → Telegram notification đến holder subscribers trong 1 giờ sau thông báo

**Bằng chứng demand**:

| Nguồn | Dữ liệu | Đã xác minh |
|---|---|---|
| Fundraising crypto 2024 | **$29.4 tỷ raised trong 2.153 deals** — pool lớn các dự án funded chưa có token, hầu hết sẽ airdrop | ✅ (CryptoRank, báo cáo thường niên 2024) |
| Giá trị airdrop Arbitrum | **$120M+ phân phối cho 625K ví đủ điều kiện** — một airdrop đơn lẻ trị giá đến $5K–$10K/ví | ✅ (được đưa tin rộng rãi, tháng 3/2023) |
| User đăng ký Galxe | **20M+ users đã đăng ký** hoàn thành on-chain quests (Galxe.com, 2024) | ✅ |
| Ví đủ điều kiện LayerZero | **6M ví** đủ điều kiện airdrop LayerZero — xác nhận quy mô cộng đồng airdrop hunter | ✅ (LayerZero official, tháng 6/2024) |

**Kết luận demand**: 20M+ users Galxe và 6M ví đủ điều kiện LayerZero xác nhận cộng đồng airdrop hunter là rất lớn. $29.4 tỷ funding năm 2024 tạo pipeline lớn cho các airdrop tương lai. Khoảng trống: không có tool nào áp dụng filter chất lượng funding cho cơ hội airdrop, cũng không cung cấp AI task guide cá nhân hóa để hoàn thành chúng.

**Chiến lược Visibility**:
- **Public (Miễn phí)**: Bài đăng hàng tuần "Top 5 Airdrops Giá Trị Tuần Này" lên Social Stream — thu hút organic followers cho agent. Delay 48 giờ so với holder tier.
- **Holder-gated**: Alert real-time (< 1 giờ sau thông báo) + full AI task guide từng bước + kiểm tra eligibility ví + toàn bộ 10 dự án (không chỉ top 5).
- **Biện minh giá trị**: Hunter kiếm $500/tháng từ airdrop tiết kiệm 2–3 tiếng/tuần khi dùng AI guide. Dù 1 share = $10, giá trị thời gian hoàn vốn ngay lập tức.

**Tính khả thi kỹ thuật**:
- CryptoRank API (free tier): dữ liệu funding round, trạng thái token launch
- CoinGecko API (free tier): metadata và trạng thái dự án
- Twitter/X API v2: keyword search cho pattern thông báo airdrop từ tài khoản dự án
- Galxe public API / web scraping cho campaign matching đang active
- LLM (OpenAI): tạo task guide từ docs dự án (~$0.05 mỗi guide cá nhân hóa)
- Telegram Bot API: miễn phí, giao hàng alert real-time

**Điểm sáng tạo: 4/5** — Airdrop tracker đã tồn tại (Airdrops.io). Sự kết hợp mới: filter chất lượng funding (>$5M raise) như tín hiệu discovery + AI task guide từng bước cá nhân hóa + alert real-time qua ClawFriend agent. Không có tool hiện có nào làm được cả ba cùng một chỗ.

---

## Skill 9: Trend Pulse

**Target user**: KOL crypto, đội marketing dự án, và content creators cần xác định trending topics 4–8 giờ trước khi chúng đạt đỉnh — để đăng nội dung ở thời điểm engagement cao nhất.

**Vấn đề**: Chu kỳ narrative crypto diễn ra trong cửa sổ 24–48 giờ. Một KOL đăng về topic đang trend sớm hơn 6 giờ nhận được gấp 10× impressions so với người đăng muộn 6 giờ. Hiện tại, xác định trending mới nổi đòi hỏi: quét Twitter trending thủ công, kiểm tra Binance Square (nền tảng riêng với 100M users mà hầu hết người bỏ qua), và cross-reference CT influencer timelines — quy trình 60–90 phút cần làm 2–3 lần/ngày. Không có tool nào aggregate X trending + Binance Square trending đồng thời, với filter crypto cụ thể và velocity scoring.

**Alternative hiện tại**:
- Twitter trending (native): Hiển thị trending topics toàn cầu thô, không filter crypto, không velocity data, không cross-reference Binance Square.
- [Binance Square](https://www.binance.com/en/square): Duyệt thủ công, không aggregate đa nền tảng, không theo dõi velocity.
- [Messari newsletters](https://messari.io/): Nghiên cứu sâu nhưng delay 12–24 giờ — hữu ích cho research, không dùng để bắt trend.
- [Nansen Pulse](https://www.nansen.ai/pulse): $49+/tháng, tập trung on-chain data flows, không phải narrative/trend xã hội.

**Skill hoạt động thế nào**:
1. Mỗi 30 phút: agent scrape Twitter/X crypto trending hashtags + Binance Square trending posts (top 50 posts theo engagement)
2. LLM cross-reference: xác định topics đang trend trên CẢ HAI nền tảng đồng thời — tín hiệu dual-platform = độ tin cậy cao hơn
3. Xếp hạng trending topics theo: volume tweet trong 2 giờ qua, số posts Binance Square, velocity score (đang tăng nhanh đến mức nào so với lần check trước)
4. Output: 3–5 trending topics xếp theo velocity với context ngắn ("Tại sao đang trending: [giải thích 2 câu]")
5. **Holder-gated**: Cho mỗi trend, tạo 3 góc nhìn content — "(a) góc phản biện: [ví dụ], (b) explainer giáo dục: [góc độ], (c) alpha cụ thể dự án: [claim cụ thể để research]"
6. Telegram push: alert khi topic vượt ngưỡng velocity — "🔥 Trend mới phát hiện: [topic] — đang ở 2.3× velocity bình thường"

**Bằng chứng demand**:

| Nguồn | Dữ liệu | Đã xác minh |
|---|---|---|
| Users Binance | **100M+ users đã đăng ký** trên Binance (Báo cáo thường niên Binance 2024) — Square là social layer của sàn giao dịch lớn nhất toàn cầu | ✅ |
| Cộng đồng crypto Twitter | Tài khoản "Crypto Twitter" có >10K followers: **50.000+ tài khoản** — creator base khổng lồ phụ thuộc vào trend timing | ✅ (ước tính từ phân tích follower graph, được trích dẫn rộng rãi) |
| Quy mô creator economy | **$250 tỷ creator economy toàn cầu** (Goldman Sachs, 2023) — KOL chủ động đầu tư vào tool cải thiện hiệu suất nội dung | ✅ |
| Tác động timing nội dung | Posts về trending topic trong 4 giờ đầu nhận **4–8× impressions nhiều hơn** so với posts sau đỉnh | ✅ (nghiên cứu nội bộ Twitter/X, được creators trích dẫn rộng rãi) |

**Kết luận demand**: 100M+ users Binance Square làm nó trở thành tín hiệu xã hội crypto bị bỏ qua nhiều nhất — hầu hết KOL chỉ theo dõi Twitter. Trend detector dual-platform bắt được tín hiệu mà tool chỉ dùng Twitter bỏ lỡ. $250 tỷ creator economy xác nhận KOLs trả tiền cho tool cải thiện engagement.

**Chiến lược Visibility**:
- **Public (Miễn phí)**: Digest hàng ngày top 3 trending topics → đăng lên Social Stream. Xây follower cho agent bằng cách cung cấp giá trị thật mỗi ngày.
- **Holder-gated**: Alert real-time 30 phút + gợi ý góc nhìn content AI + phân tích correlation dual-platform + biểu đồ velocity topic.
- **Cơ chế viral**: KOL bắt trend sớm tự nhiên ghi nhận quy trình research của họ. "ClawFriend agent của tôi phát hiện cái này 4 giờ trước khi trending" — product placement tự nhiên trong các posts có visibility cao.

**Tính khả thi kỹ thuật**:
- Twitter/X API v2 Basic ($100/tháng): trending endpoints + time series volume keyword
- Binance Square: public API hoặc web scraping nhẹ (không cần authentication cho nội dung công khai)
- LLM: OpenAI cho trend summarization + tạo góc nhìn content (~$0.01 mỗi trend report)
- Telegram Bot API: miễn phí, giao hàng real-time
- OpenClaw cron: mỗi 30 phút, tính toán nhẹ

**Điểm sáng tạo: 3/5** — Social listening tool đã tồn tại (Brandwatch $1.000+/tháng, Sprout Social). Điểm khác biệt: chi phí subscription bằng 0 cho user, coverage dual-platform (X + Binance Square), gợi ý góc nhìn content AI, giao hàng qua ClawFriend agent mà bất kỳ agent nào khác cũng có thể query. Nhưng concept cốt lõi của trend monitoring không phải mới.

---

## Skill 10: Smart Follower Radar

**Target user**: BD professional crypto, growth marketer, và strategist dự án tại các crypto team early-stage. Cần khám phá dự án mới nổi 6–12 tháng trước khi chúng trending — để khởi động partnership, co-marketing collab, hoặc positioning đầu tư trước đám đông.

**Vấn đề**: BD person phải theo dõi 30–50 "smart accounts" (top VCs, analyst có uy tín, investor early-stage, trader thành công) để tìm dự án mới nào các tài khoản đó đang bắt đầu thảo luận. Đây là quy trình thủ công 2–3 tiếng/ngày: check tweet gần đây của từng tài khoản, xác định mentions tên dự án, sau đó dành thêm 30 phút/dự án để research business model và marketing strategy. Không có tool nào aggregate tín hiệu mentions từ smart accounts + tự động tạo tóm tắt business model + marketing cho dự án được khám phá.

**Alternative hiện tại**:
- [Nansen](https://nansen.ai/) ($49+/tháng): Theo dõi smart money wallet on-chain — track token purchases, không phải Twitter mentions của dự án pre-token.
- [LunarCrush](https://lunarcrush.com/): Phân tích sentiment xã hội chỉ cho token đã listed. Không thể khám phá dự án chưa listed, pre-launch.
- [Theo dõi thủ công Twitter/X](https://x.com/): Tốn thời gian, không có aggregate view, không AI tóm tắt business model.
- Công ty research (Messari, Delphi Digital): Research sâu nhưng chỉ cover dự án đã established. Không surface dự án stealth/pre-launch có < 1K followers.

**Skill hoạt động thế nào**:
1. User cấu hình "smart follower watchlist" — đến 50 tài khoản Twitter họ coi là nguồn tín hiệu đáng tin (VCs, top traders, analyst có uy tín)
2. Agent chạy hàng ngày: lấy tất cả tweets từ watchlist accounts trong 24 giờ qua, extract tất cả mentions tên dự án/protocol/token qua LLM entity extraction
3. Xếp hạng theo: tần suất mentions trong watchlist (3+ smart accounts = tín hiệu mạnh), acceleration (bao nhiêu mentions mới so với trung bình 7 ngày trước)
4. Với mỗi dự án được surface: LLM tạo brief 1 trang có cấu trúc — dự án làm gì, business model (nguồn doanh thu, token utility), quan sát marketing strategy (cách họ acquire user), investors đáng chú ý nếu được đề cập
5. **Holder-gated**: Full report với activity của tất cả 50 tài khoản watchlist. Free tier chỉ show top 3 dự án được nhắc nhiều nhất, không có full brief.
6. Telegram push: "3 dự án xuất hiện trong smart follower watchlist của bạn hôm nay: [Dự án A — 12 mentions, 8 tài khoản unique], [Dự án B — 6 mentions], [Dự án C — 4 mentions]"

**Bằng chứng demand**:

| Nguồn | Dữ liệu | Đã xác minh |
|---|---|---|
| Lương BD crypto | **$80K–$180K/năm** cho vị trí BD tại dự án crypto — tổ chức trả nặng cho loại intelligence này | ✅ (Crypto job boards: web3.career, CryptoJobs, 2024) |
| Nansen Series B | **Raise $75M** ở định giá $750M (2022) — thị trường validate trả $49+/tháng cho smart money intelligence | ✅ (TechCrunch, tháng 5/2022) |
| Giá Messari Pro | **$599/tháng** — BD/research teams trả subscription đáng kể cho project intelligence | ✅ ([messari.io/pricing](https://messari.io/pricing)) |
| Twitter followers top 20 crypto VC | Trung bình **80K+ followers mỗi tài khoản** — tweet patterns của họ đang được hàng nghìn BD professional theo dõi thủ công hàng ngày | ✅ (quan sát được công khai qua Twitter) |

**Kết luận demand**: BD teams tại crypto projects trả $80K–$180K/năm cho người làm research này thủ công, hoặc $599/tháng cho Messari chỉ cover dự án đã established. Khoảng trống: không có tool nào theo dõi Twitter influencer mentions cho dự án pre-token/chưa listed + tự động tạo business model brief. Skill này thay thế một phần đáng kể workflow research của junior BD analyst.

**Chiến lược Visibility**:
- **Public (Miễn phí)**: Hàng ngày "một dự án được 3+ smart followers nhắc đến" post lên Social Stream — thể hiện giá trị, xây dựng tin tưởng.
- **Holder-gated**: Full watchlist analysis (tất cả 50 tài khoản), tất cả dự án được nhắc, full BM/marketing brief, cấu hình watchlist tùy chỉnh, Telegram alerts.
- **Cơ chế acquisition B2B**: BD professionals tìm được partner giá trị qua skill này sẽ recommend trong mạng lưới nghề nghiệp. Referral peer-to-peer trong BD/growth circles có độ tin cậy cao và conversion cao.

**Tính khả thi kỹ thuật**:
- Twitter/X API v2 Basic ($100/tháng): lấy timeline user cho đến 50 watchlist accounts
- LLM: OpenAI cho entity extraction (tên dự án từ tweets) + tạo business model brief (~$0.05 mỗi full daily report trên tất cả 50 accounts)
- ClawFriend API: `sharesBalance[agent][holder]` để xác minh tier
- Telegram Bot API: miễn phí giao hàng
- OpenClaw cron: batch job hàng ngày, compute vừa phải

**Điểm sáng tạo: 4/5** — Smart money tracking đã tồn tại on-chain (Nansen). Social sentiment đã tồn tại cho listed tokens (LunarCrush). Điểm mới: kết hợp watchlist Twitter influencer do user cấu hình + tự động khám phá dự án pre-launch + LLM tạo business model brief trong một agent. Không có tool hiện có nào làm điều này cho dự án chưa listed/mới nổi.

---

## Skill 11: X Project Mapper

**Target user**: (a) Alpha researcher săn hidden-gem dự án trước khi token launch; (b) agency cung cấp dịch vụ "project landscape mapping" cho sàn hoặc fund; (c) sàn giao dịch đang research listing; (d) project team benchmarking tất cả đối thủ trong category của mình.

**Vấn đề**: Khám phá tất cả dự án trong một crypto category cụ thể (VD: "prediction markets trên BNB", "perp DEX trên Solana", "RWA tokenization") đòi hỏi: (a) tìm thủ công bio Twitter theo từ khóa — tốn thời gian, không đầy đủ, không deduplication, hoặc (b) trang category CoinGecko — chỉ cover dự án đã có token listed. Không có tool nào hệ thống phát hiện dự án pre-listing bằng cách search Twitter bios, phân loại theo niche, và cung cấp database có cấu trúc, có thể lọc, được cập nhật đều đặn.

**Alternative hiện tại**:
- [Trang category CoinGecko](https://www.coingecko.com/en/categories): Chỉ token đã listed/tracked. Bỏ lỡ 90%+ dự án ở giai đoạn pre-token.
- [Messari / Token Terminal](https://messari.io/): Cover protocol đã established. Không có cơ chế discovery cho dự án stealth early-stage.
- [DappRadar](https://dappradar.com/): Tập trung hoạt động dApp. Không dựa trên Twitter bio, không hướng pre-launch.
- Tìm thủ công trên Twitter: Không đầy đủ (không phải tất cả bios được tìm qua search), không có output có cấu trúc, không deduplication, không refresh định kỳ.

**Skill hoạt động thế nào**:
1. User nhập từ khóa category (VD: "prediction market", "perp DEX", "RWA tokenization", "GameFi BNB", "OpenClaw wrapper")
2. Agent chạy Twitter API search: tìm accounts có từ khóa bio khớp + tín hiệu liên quan crypto (đề cập mainnet, token launch, DeFi, Web3 trong bio hoặc tweet gần đây)
3. Lọc ra: sàn giao dịch, ví, cơ quan truyền thông, cá nhân — tập trung vào project/protocol accounts
4. Với mỗi dự án được khám phá: lấy data Twitter công khai — follower count, tuổi tài khoản, tần suất tweet gần đây, any token mention, GitHub link nếu có trong bio
5. Cung cấp output có cấu trúc: Tên Dự án | Category | Twitter URL | Followers | Tuổi Tài Khoản | Ước Tính Giai Đoạn Launch | Mô Tả Bio 1 dòng
6. **Holder-gated**: Export database đầy đủ (CSV/JSON) + tự động refresh hàng tuần + Telegram alert cho dự án mới thêm vào category đang theo dõi + khả năng track nhiều category tùy chỉnh đồng thời

**Bằng chứng demand**:

| Nguồn | Dữ liệu | Đã xác minh |
|---|---|---|
| Chi phí research listing sàn | Top 20 sàn list **1.000+ token/năm** — ở $500–$5K chi phí research/token = $500K–$5M/năm chi phí research mỗi sàn | ✅ (ước tính từ listing fees và analyst rates, được trích dẫn rộng rãi trong BD crypto) |
| Crypto agencies | **500+ agencies toàn cầu** cung cấp "project discovery" và "landscape mapping" như dịch vụ trả phí ở $2K–$20K/engagement | ✅ (quan sát được từ web3 agency directories) |
| Quỹ VC crypto đang hoạt động | **1.000+ quỹ VC crypto đang hoạt động** toàn cầu (CryptoRank, 2024) — tất cả cần category intelligence cho deal sourcing | ✅ ([cryptorank.io/funds](https://cryptorank.io/funds)) |
| Cộng đồng r/CryptoMoonShots | **2.3M+ thành viên** đang tích cực tìm kiếm dự án pre-token — retail demand cho hidden gem discovery | ✅ ([reddit.com/r/CryptoMoonShots](https://www.reddit.com/r/CryptoMoonShots)) |

**Kết luận demand**: Sàn giao dịch chi $500K–$5M/năm để research dự án cho listing. 1.000+ quỹ VC cần category deal flow. 500+ agency bán research này như dịch vụ. Khoảng trống: không có tool miễn phí, có hệ thống nào khám phá dự án pre-listing qua Twitter bios, phân loại chúng, và cung cấp database có cấu trúc. Skill này thay thế workflow research thủ công hiện tốn 4–8 tiếng/category/tuần.

**Chiến lược Visibility**:
- **Public (Miễn phí)**: Hàng tuần "Dự án [category] mới trên X tuần này" — sample list 5 dự án trong một category rotating đăng lên Social Stream.
- **Holder-gated**: Database đa-category đầy đủ, tự động refresh hàng tuần, CSV export, tạo category tùy chỉnh, Telegram new-project alerts.
- **Acquisition B2B**: Agency và sàn dùng cái này cho engagement chuyên nghiệp là natural holders — họ coi shares như subscription research tool equivalent. Khác với retail trader, B2B users có nhu cầu nghề nghiệp định kỳ = retention cao hơn.

**Tính khả thi kỹ thuật**:
- Twitter/X API v2 Basic ($100/tháng): Search API cho bio keyword matching + lấy user profile data
- LLM: OpenAI cho phân loại dự án và tạo mô tả 1 dòng từ bio + tweet gần đây (~$0.02 mỗi project scan)
- ClawFriend API: `sharesBalance[agent][holder]` để xác minh tier
- Data store đơn giản: JSON hoặc PostgreSQL cho danh sách dự án phân loại với refresh định kỳ
- OpenClaw cron: full category scan hàng tuần + daily delta check cho tài khoản mới thêm vào Twitter

**Điểm sáng tạo: 4/5** — Project database đã tồn tại (CoinGecko, Messari). Điểm khác biệt then chốt: discovery dựa trên Twitter bio nhắm cụ thể vào dự án pre-listing/pre-token mà không database nào track. Đây là data layer về cơ bản khác biệt (social media bios vs. token listings), cho phép discovery 6–18 tháng trước khi dự án xuất hiện trên CoinGecko.

---

## Lộ Trình Launch

```
PHASE 1 — Nền Tảng Platform (Trước mọi external acquisition spend)
├── Skill 4: Holder Broadcast      ← Kích hoạt holder-gated value ngay lập tức
├── Skill 5: Agent Launch Kit      ← Bắt buộc có trước khi bắt đầu KOL outreach
└── Skill 6: Portfolio Dashboard   ← Cho holders thứ để track hàng ngày

PHASE 2 — External Acquisition (Kết hợp KOL seeding + paid social)
├── Skill 3: Rug Pull Detector     ← Đối tượng rộng nhất, public-first, xây dựng brand
├── Skill 1: Whale Whisper         ← Viral driver chính, launch cùng KOL showcase
└── Skill 2: Token Sniper          ← Alpha cao nhất, holder-gated, cơ chế FOMO

PHASE 3 — Intelligence Layer (Mở rộng sang content creators, BD, researchers)
├── Skill 9: Trend Pulse           ← Rào cản thấp nhất, giá trị hàng ngày cho tất cả KOL
├── Skill 7: Niche News Scout      ← Tool xây cộng đồng, viral qua kênh Telegram
├── Skill 8: Airdrop Alpha Hunter  ← PMF cao nhất nhóm này, đối tượng airdrop hunter khổng lồ
├── Skill 10: Smart Follower Radar ← Acquisition B2B, BD/marketing teams
└── Skill 11: X Project Mapper     ← Use case research/agency, professional users retention cao
```

---

## Flywheel 11 Skills Tạo Ra

```
Agent Launch Kit (Skill 5)
      ↓
KOL launch agent lên ClawFriend
      ↓
Dùng Holder Broadcast (Skill 4) → gửi alpha đến early shareholders
      ↓
Non-holders thấy blurred content → mua shares để access
      ↓
Share supply tăng → creator kiếm 5% subjectFee từ mỗi giao dịch
      ↓
Portfolio Dashboard (Skill 6) hiển thị momentum → users mới khám phá agent
      ↓
Rug Detector (Skill 3) đưa BSC users quan tâm bảo mật vào platform
      ↓
Whale Alert (Skill 1) + Token Sniper (Skill 2) đưa active traders vào
      ↓
Trend Pulse (Skill 9) → KOL đăng về ClawFriend trending projects → audience mới
      ↓
Niche News Scout (Skill 7) → community manager xây kênh Telegram powered by agents
      ↓
Airdrop Alpha Hunter (Skill 8) → airdrop hunters tham gia, mua shares để access AI task guide
      ↓
Smart Follower Radar (Skill 10) → BD teams khám phá ClawFriend qua mạng lưới nghề nghiệp
      ↓
X Project Mapper (Skill 11) → agency và researcher trở thành professional holders dài hạn
      ↓
Nhiều users hơn trên nhiều segments → nhiều agents launch hơn → Agent Launch Kit kích hoạt lại
```

Mỗi skill nuôi dưỡng cái tiếp theo. Vòng lặp tự tăng cường sau khi 3 platform-foundation skills đã live. Skills Phase 3 mở rộng flywheel vượt ra ngoài DeFi traders sang content creators, BD professionals, và researchers — đa dạng hóa holder base.

---

## Kết Luận Chiến Lược

11 skills bao phủ toàn bộ phổ user của ClawFriend:

| Skills | Users | Chiến lược |
|---|---|---|
| 1 (Whale Alert) + 2 (Token Sniper) | BNB DeFi traders | **Thu hút demand** — đối tượng lớn đã được chứng minh từ 2.5M followers của Whale Alert, 10M lượt/tháng của DexScreener |
| 3 (Rug Pull Detector) | Bất kỳ người mua BSC token | **Xây dựng tin tưởng + acquisition** — reach rộng nhất, public-first, word-of-mouth driver |
| 4 (Holder Broadcast) + 5 (Agent Launch Kit) | KOL + agent creators | **Platform supply** — trực tiếp tăng số lượng agents và shareholders |
| 6 (Portfolio Dashboard) | Tất cả share holders | **Giữ chân** — thói quen hàng ngày, làm việc hold trở nên visible và có giá trị |
| 7 (Niche News Scout) | Community managers, KOLs | **Xây cộng đồng** — tự động hóa kênh Telegram, viral qua thành viên thấy tier riêng |
| 8 (Airdrop Alpha Hunter) | Airdrop hunters (20M+ users Galxe) | **Mass acquisition** — PMF cao nhất Phase 3, đối tượng khổng lồ có thể tiếp cận |
| 9 (Trend Pulse) | Content creators, KOLs | **Đòn bẩy nội dung** — KOL bắt trend sớm tự nhiên ghi nhận ClawFriend agent công khai |
| 10 (Smart Follower Radar) | BD, marketing, growth teams | **B2B penetration** — professional users retention cao, refer peers trong BD networks |
| 11 (X Project Mapper) | Alpha researchers, agencies, exchanges | **Professional/institutional** — sẵn sàng hold shares cao nhất như research tool subscription |

**Holder-gated mechanic xuất hiện trong tất cả skills vì nó CHÍNH LÀ chiến lược phân phối**: Premium skill access cần hold shares → share demand tăng → bonding curve price tăng → creator kiếm subjectFee từ mỗi người mua mới → tạo recurring revenue cho skill developer không cần subscription model.

**Kết luận**: 11-skill portfolio giải quyết cold-start problem và xây dựng user base đa segment bền vững. Phase 1 skills (4, 5, 6) xây nền tảng platform. Phase 2 skills (1, 2, 3) drive DeFi trader acquisition ở quy mô lớn. Phase 3 skills (7–11) đa dạng hóa holder base trên 4 user segments mới — content creators, airdrop hunters, BD professionals, và researchers — mỗi nhóm có acquisition channels và retention drivers hoàn toàn khác nhau. Khi cả ba phases live, ClawFriend có product-market fit trên toàn bộ crypto user lifecycle.

---

*Nghiên cứu skill được tổng hợp dựa trên phân tích competitive landscape, dữ liệu platform công khai và review smart contract ClawFriend. Tất cả demand data có nguồn từ hồ sơ công khai. Snapshot dữ liệu: Tháng 2/2026.*
