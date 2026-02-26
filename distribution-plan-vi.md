# Kế Hoạch Phân Phối — ClawFriend

> **Deliverable 3/3** | Trọng số: 40% | Trạng thái: Draft
> Ngân sách: $10,000 cho Tháng 1. Tài liệu đi kèm competitive-landscape.md và skill-research.md.

---

## Tổng Quan Chiến Lược

Thách thức phân phối của ClawFriend là vấn đề **supply (nguồn cung), độ tin cậy, và nhận thức thương hiệu** — theo đúng thứ tự đó. Platform đang có contract hoạt động, 11 skills đã validate sẵn sàng ra mắt, và cơ chế holder-gated khác biệt. Những gì còn thiếu:

1. **Blocker độ tin cậy**: ClawHub listing có 1,100 lượt xem nhưng chỉ 1 lần cài đặt — cờ VirusTotal "Suspicious" đang giết chết mọi conversion. Phải fix trước khi tiêu bất kỳ đồng nào.
2. **Khoảng trống nhận thức**: Không có platform AI agent economy nào trên BNB đã định vị xong. Cửa sổ cơ hội đang mở nhưng không kéo dài mãi.
3. **Thiếu nội dung viral**: Chưa có bài viết hay thread nào về ClawFriend được lan truyền. Tăng trưởng organic cần những bài viết mà người ta thực sự chia sẻ.

**Chiến lược Tháng 1**: Fix blocker conversion trước (miễn phí). Xây dựng hiện diện organic qua các tài khoản KOL của team và X engagement (miễn phí). Triển khai Article Contest $5K được seeded với các bài viết chất lượng cao do team chuẩn bị sẵn, khuếch đại bởi $4K KOL booking mid-tier. Chạy $1K Taskon event để có follower ban đầu. Mục tiêu: 10,000+ người dùng mới vào Ngày 30.

Contest là khoản đặt cược cốt lõi: nếu viral, $5K tiền thưởng kéo về 10K+ người dùng. Nếu không viral, các bài viết planted của chính team sẽ thắng giải — chi phí thực tế gần bằng $0 tiền thưởng, chỉ mất phần KOL amplification.

---

## Phân Bổ Ngân Sách — $10,000 Tháng 1

| Kênh | Loại | Ngân sách | % | Ưu tiên |
|---|---|---|---|---|
| Kênh 1: Sửa ClawHub | Organic | $0 | — | 🚨 NGÀY 1 — blocker |
| Kênh 2: Xây tài khoản KOL của team | Organic | $0 | — | Tuần 1, liên tục |
| Kênh 3: X Shilling via Lists | Organic | $0 | — | Tuần 1, liên tục |
| Kênh 4: Đổi collab KOL Tier 2-3 | Organic | $0 | — | Tuần 2, liên tục |
| Kênh 5: Collab marketing với dự án khác | Organic | $0 | — | Tuần 2, liên tục |
| Kênh 6: Article Contest | Trả phí | $5,000 | 50% | Announce Ngày 8 |
| Kênh 7: KOL Booking | Trả phí | $4,000 | 40% | Tuần 2–3 |
| Kênh 8: Taskon Event | Trả phí | $1,000 | 10% | Ra mắt Ngày 8 |
| Bonus: Thu hút user từ Friend.tech | Trả phí (nhỏ) | ~$0–200 | — | Tuần 3–4 |
| **TỔNG** | | **$10,000** | **100%** | |

---

## Kênh 1: Sửa ClawHub + Tối Ưu Listing

**Loại**: Organic | **Chi phí**: $0 | **Ưu tiên**: 🚨 Phải hoàn thành TRƯỚC KHI chi bất kỳ tiền paid nào | **Người thực hiện**: Developer

### Tại sao cần kênh này

ClawHub là kênh cài đặt chính của ClawFriend. Listing đã có 1,100 lượt xem — audience đang đến. Nhưng cờ VirusTotal "Suspicious" đang giết chết mọi lần cài đặt. Conversion hiện tại: **0.09%** (1 lần cài từ 1,100 lượt xem). Một listing sạch với conversion 5% thôi đã mang về 55 lượt cài từ cùng lượng traffic đó, với $0 chi phí.

Đây là hành động ROI cao nhất trong toàn bộ kế hoạch.

### Kế hoạch hành động

**Ngày 1 — Nộp báo cáo false-positive lên VirusTotal**
1. Vào virustotal.com → tìm file hash của ClawFriend skill
2. Click "Submit file for re-analysis" hoặc dùng form Dispute/False Positive
3. Trong phần mô tả: đính kèm link GitHub repo, xác nhận không có obfuscation, giải thích đây là Node.js MCP extension
4. Thời gian xử lý: 3–7 ngày

**Ngày 1 — DM @steipete (người tạo ClawHub) trên X**
- Nội dung: *"Hey, skill ClawFriend của chúng tôi (clawhub.ai/leeknowsai/clawfriend) đang bị flag Suspicious bởi VirusTotal — chúng tôi tin đây là false positive. Bạn có thể whitelist hoặc review giúp không? Chúng tôi có 1,100 lượt xem và 1 lần cài đặt. Sẵn sàng chia sẻ source code để kiểm tra."*
- Mục tiêu: whitelist thủ công hoặc review nhanh hơn

**Ngày 1–3 — Repackage nếu VirusTotal mất hơn 3 ngày**
- Build lại skill package: thuần Node.js, không có executable đính kèm, source code đầy đủ trên GitHub
- Package mới = hash mới = VirusTotal bắt đầu kiểm tra từ đầu

**Ngày 3 — Cập nhật ClawHub listing**
- Thêm README đầy đủ: skill làm gì, các bước cài đặt, screenshots, demo GIF
- Thêm link GitHub (xây dựng niềm tin — open source = không đáng nghi)
- Viết lại mô tả: "Cảnh báo cá voi BNB real-time, phát hiện rug, và theo dõi portfolio shares — ngay trong agent OpenClaw của bạn"

**Hàng ngày — Theo dõi**
- Check clawhub.ai/leeknowsai/clawfriend mỗi sáng
- Ghi log vào Google Sheet: lượt xem, lượt cài, trạng thái VirusTotal
- Nếu lượt cài không tăng sau 7 ngày kể từ khi fix → DM @steipete lần nữa

### Kết quả kỳ vọng

| Chỉ số | Trước khi sửa | Sau khi sửa (mục tiêu) |
|---|---|---|
| Trạng thái VirusTotal | Suspicious | Clean |
| Tỷ lệ conversion | 0.09% | 5%+ |
| Lượt cài hàng tháng | 1 | 55+ |

**Tín hiệu dừng**: Nếu VirusTotal không được giải quyết trong 14 ngày → rebuild + repackage với tên package mới.

---

## Kênh 2: Xây Tài Khoản KOL AI Của Team

**Loại**: Organic | **Chi phí**: $0 (chỉ mất thời gian team) | **Timeline**: Bắt đầu Ngày 1, liên tục | **Người thực hiện**: Mỗi thành viên team tự xây 1 tài khoản

### Tại sao cần kênh này

Post trả phí chỉ sống 24 giờ. Một tài khoản có follower thật và lịch sử engagement xây dựng reach tích lũy theo thời gian — mỗi post mới bắt đầu với một audience sẵn có. Chiến lược: mỗi thành viên team trở thành micro-KOL trong một ngách crypto (AI, DeFi, BNB trading, Base ecosystem). Nội dung ClawFriend được đan xen vào dòng post bình thường, không phát quảng cáo ồ ạt.

Quy tắc quan trọng nhất: **tài khoản là nhân cách thật trước, người quảng bá ClawFriend sau.** Tỷ lệ: 80% nội dung ngách thuần túy, 20% đề cập ClawFriend. Điều này xây dựng niềm tin với audience và khiến các lần nhắc đến ClawFriend nghe tự nhiên.

### Cách xây tài khoản (từng bước)

**Bước 1 — Chọn ngách (Ngày 1)**
Mỗi thành viên team chọn 1 ngách: AI agents, BNB DeFi, Base ecosystem, Pumpfun/memecoin, crypto trading. Chọn ngách gần với sở thích thật nhất — bạn sẽ post hàng ngày.

**Bước 2 — Định hình persona tài khoản (Ngày 1–2)**
- Bio: "Theo dõi AI agents ăn DeFi | Đang build tại [công ty] | Quan điểm cá nhân"
- Ảnh đại diện: ảnh chuyên nghiệp hoặc avatar AI-generated
- KHÔNG đặt "ClawFriend team" trong bio — bạn là một người tham gia crypto, tình cờ đang xây dựng ClawFriend

**Bước 3 — Warm up tài khoản (Ngày 1–14)**
- Post 2–3 lần/ngày về nội dung ngách (chưa đề cập ClawFriend)
- RT và reply 10–15 posts/ngày từ KOL trong ngách của bạn
- Mục tiêu: thuật toán nhận diện bạn là tài khoản active
- Ý tưởng nội dung: hot takes về tin tức AI, quan sát dữ liệu on-chain, tóm tắt thread lớn

**Bước 4 — Cross-follow + cross-engage giữa các tài khoản team (Ngày 3 trở đi)**
- Tất cả thành viên team follow lẫn nhau
- Like và RT bài nhau hàng ngày
- Điều này boost reach thuật toán cho tất cả tài khoản

**Bước 5 — Bắt đầu đề cập ClawFriend (Ngày 14 trở đi)**
- Đan xen tự nhiên: "mình đang build cái holder-gated skill thing trên BNB và nó đang rất hay — [ảnh chụp màn hình demo]"
- Không bao giờ: "ClawFriend quá tuyệt vời bạn nên mua shares NGAY BÂY GIỜ"
- Luôn: câu chuyện builder ngôi thứ nhất, phản ứng thật, dựa trên screenshot

**Bước 6 — Vòng RT boost (Ngày 14 trở đi, liên tục)**
- Khi một thành viên team post về ClawFriend → tất cả tài khoản team khác RT trong vòng 1 giờ
- 60 phút đầu sau khi post quyết định thuật toán Twitter có khuếch đại post đó không

### Chỉ tiêu mỗi tài khoản (Tháng 1)

| Chỉ số | Mục tiêu |
|---|---|
| Followers thu được | 200–500 |
| Impressions trung bình mỗi post về ClawFriend | 1,000–3,000 |
| Lần đề cập ClawFriend mỗi tuần | 2–3 |

**Tín hiệu dừng**: Nếu tài khoản nhận < 100 impressions mỗi post sau 14 ngày post đều đặn → review chiến lược nội dung trước khi tiếp tục.

---

## Kênh 3: X Shilling via Lists + Comment Sớm

**Loại**: Organic | **Chi phí**: $0 (+ tùy chọn tool ≤$20/tháng) | **Timeline**: Bắt đầu Ngày 3, liên tục | **Người thực hiện**: Intern (mỗi người quản lý 10 tài khoản)

### Tại sao cần kênh này

Những post có traffic cao nhất trên X đến từ các KOL đã có tên tuổi. Thuật toán mạnh mẽ promote comment trên post phổ biến — một reply đúng thời điểm lên KOL 100K followers có thể mang về 5,000–50,000 impressions miễn phí. Chiến lược: theo dõi các KOL target qua X Lists, comment trong 30 phút đầu khi post vừa lên trước khi viral, và xây dựng uy tín trong cộng đồng đó vài tuần trước khi nhắc đến ClawFriend.

### Setup (Ngày 3–5)

**Bước 1 — Tạo X Lists theo ngách**

Tạo 4 X Lists riêng tư (không cần public):
- **"AI Agents KOL"**: Thêm 20 tài khoản hàng đầu post về AI agents, elizaOS, Virtuals, OpenClaw
- **"Base + Pumpfun"**: Thêm 20 tài khoản hàng đầu post về Base chain, friend.tech, Pumpfun
- **"BNB DeFi"**: Thêm 20 tài khoản hàng đầu post về BNB, PancakeSwap, BSC trading
- **"Crypto Alpha"**: Thêm 20 tài khoản hàng đầu post whale alerts, dữ liệu on-chain, smart money

Tài khoản gợi ý để thêm:
- AI: @shawmakesmagic, @0xzerebro, @ai16zdao, @virtuals_io, @clanker
- Base: @jessepollak, @0xCygaar, @defi_maxi_420
- BNB: @cz_binance, @BNBChain, @PancakeSwap, @BinanceResearch
- On-chain: @lookonchain, @whale_alert, @onchainlens, @Nansen_ai

**Bước 2 — Bật notification**
- Trên X: Click vào profile mỗi KOL → icon chuông → "All new posts"
- Điều này gửi thông báo điện thoại mỗi khi họ post → bạn có thể comment trong vài phút

**Bước 3 — Phân tài khoản cho intern**
- Mỗi intern quản lý 10 tài khoản X
- Nhiệm vụ hàng ngày: check feed Lists mỗi 2 giờ (sáng + trưa + tối)
- Khi KOL target post: comment trong vòng 30 phút

### Quy tắc comment (quan trọng)

**Nên làm:**
- Thêm value thật sự: "Điều này khớp với những gì tôi thấy trên BNB — smart wallets đang accumulate X"
- Đặt câu hỏi liên quan: "Bạn có nhìn cái này so với [thứ liên quan] không?"
- Chia sẻ dữ liệu on-chain liên quan: "@lookonchain wallet này cũng vừa move vào Y 2 ngày trước"

**Không làm:**
- Spam link ClawFriend trong mọi comment
- Comment chỉ emoji ("🔥🔥🚀")
- Comment nhiều posts liên tiếp từ cùng một tài khoản (trông giống bot)

**Chèn ClawFriend (Tuần 3 trở đi, sau khi tài khoản đã có uy tín):**
- Chỉ đề cập ClawFriend khi tự nhiên phù hợp: "yeah mình build một skill cho chính xác cái này — [screenshot]"
- Không bao giờ paste link trong reply đầu tiên. Chỉ khi ai đó hỏi.

### Post trong X Communities

**Communities mục tiêu:**
- Tìm "AI Agents" trong X Communities
- Tìm "BNB Chain" trong X Communities
- Tìm "DeFi Traders" trong X Communities

**Tần suất post:** 1–2 bài mỗi tuần mỗi community. Chỉ nội dung gốc — không copy-paste từ timeline chính.

### Chỉ tiêu

| Chỉ số | Mục tiêu (Tháng 1) |
|---|---|
| Comments KOL mỗi intern mỗi ngày | 10–20 |
| Impressions trung bình mỗi comment | 200–1,000 |
| Tổng impressions từ comments | 50,000–200,000 |
| Lần đề cập ClawFriend trong comments | Tuần 3+, 2–3/ngày |

**Tín hiệu dừng**: Nếu comments nhận < 50 impressions sau 2 tuần → đổi danh sách KOL target, các tài khoản đang không ở đúng ngách.

---

## Kênh 4: Đổi Collab KOL Tier 2–3

**Loại**: Organic | **Chi phí**: $0 | **Timeline**: Bắt đầu Ngày 8, liên tục | **Người thực hiện**: 1 thành viên team phụ trách outreach

### Tại sao cần kênh này

KOL mid-tier (5K–50K followers) thường sẵn sàng collab vì họ cũng đang cố gắng tăng trưởng. Một pitch thẳng thắn đề nghị đổi value ngang nhau — "mình post về bạn, bạn post về mình, hai bên tag nhau" — có tỷ lệ chấp nhận 20–30% khi thực hiện đúng cách. Điều này nhanh chóng xây dựng credibility và tạo ra nội dung từ những tiếng nói thật.

### Cách tìm ứng viên

**Bước 1 — Xây danh sách target (Ngày 8)**

Tìm kiếm trên X:
- `"BNB" "dự án AI mới"` — KOL cover BNB AI
- `"Base" "AI agents"` — KOL trong không gian Base AI agent
- `"Pumpfun" OR "pumpfun" "alpha"` — KOL memecoin

Tiêu chí lọc:
- 5,000–50,000 followers
- Engagement rate ≥ 2% (tổng likes 10 post gần nhất ÷ followers)
- Post trong 48 giờ qua (tài khoản active)
- Không quá 2 post trả phí rõ ràng trong 30 ngày qua

Tạo danh sách 30 ứng viên trong Google Sheet với các cột: Handle | Followers | Engagement Rate | Ngách | Ngày outreach | Phản hồi.

**Bước 2 — Script DM (gửi Ngày 10–12)**

```
Hey [tên], rất thích content [BNB / AI] của bạn — thread về [chủ đề gần đây] rất có giá trị.

Mình đang build ClawFriend — AI agent economy đầu tiên trên BNB với holder-gated skills.
Còn sớm, nhưng cơ chế rất thú vị: người ta mua "shares" của bạn on-chain để mở khóa
alpha độc quyền từ bạn.

Bạn có muốn collab không? Mình sẵn sàng viết thread thật sự về công việc của bạn
và tag bạn với audience của mình. Mong bạn làm tương tự về phía mình — không cần script,
chỉ cần nhận xét thật sự.

Không vội, chỉ nghĩ có thể hợp lý cho cả hai bên.
```

**Bước 3 — Follow up một lần (Ngày 14 cho những người chưa trả lời)**
- Nếu không có phản hồi sau 4 ngày: một DM follow-up: *"Hey, thấy bạn vừa post về [thứ gần đây] — muốn check tin nhắn của mình có đến không. Cho mình biết nếu bạn muốn thử nhé."*
- Sau 2 lần không trả lời: chuyển sang ứng viên tiếp theo trong danh sách

**Bước 4 — Thực hiện collab (trong 7 ngày sau khi đồng ý)**
- Viết một thread 5-tweet thật sự về công việc của họ
- Tag họ, post lên, DM link cho họ
- Họ post về ClawFriend đổi lại — cung cấp talking points nhưng không viết thay

### Chỉ tiêu

| Chỉ số | Mục tiêu (Tháng 1) |
|---|---|
| Ứng viên KOL được liên hệ | 30 |
| Tỷ lệ chấp nhận | 20–30% → 6–9 collab |
| Impressions trung bình mỗi post collab | 5,000–20,000 |
| Tổng reach từ collab | 30,000–150,000 impressions |
| Followers ClawFriend mới từ collab | 100–300 |

**Tín hiệu dừng**: Nếu 0 phản hồi sau 30 DM outreach → review script + danh sách KOL. Pitch có thể quá dài hoặc không đúng ngách.

---

## Kênh 5: Collab Marketing Với Các Dự Án Khác

**Loại**: Organic (+ có thể chia sẻ ngân sách) | **Chi phí**: $0 hoặc nhỏ | **Timeline**: Bắt đầu Ngày 10, liên tục | **Người thực hiện**: 1 thành viên team phụ trách BD

### Tại sao cần kênh này

Các dự án khác đang build trên BNB hoặc Base có audience trùng chính xác với user target của ClawFriend. Một announcement chung hoặc post co-marketing tiếp cận cộng đồng của họ miễn phí — và sự chứng thực ngầm từ dự án đối tác có sức nặng hơn quảng cáo trả phí.

### Loại dự án mục tiêu

| Loại dự án | Tại sao liên quan | Cái để đề nghị |
|---|---|---|
| DeFi tools trên BNB (portfolio tracker, DEX aggregator) | User của họ trade trên BNB → sẽ dùng whale alerts và rug detector | Cross-promotion: "dùng ClawFriend skills với [tool]" |
| AI agent projects trên Base (elizaOS, OpenClaw builders) | Hiểu kỹ thuật, hiểu cơ chế holder-gated | "Deploy agent lên ClawFriend — kiếm tiền từ skills của bạn" |
| Crypto research tools | User của họ chính là target của Skills 7–11 của ClawFriend | Bundle: "user ClawFriend nhận trial [tool], user [tool] nhận demo ClawFriend" |
| Launchpad / IDO platforms trên BNB | Có access vào cộng đồng token mới, airdrop hunters | Co-announcement: "Các dự án mới launch trên [platform] có thể được track trong ClawFriend" |

### Quy trình outreach (Ngày 10–15)

**Bước 1**: Xác định 10 dự án target từ danh sách trên. Tìm tài khoản X và DM của team.

**Bước 2**: DM pitch:
```
Hey [dự án], rất thích những gì bạn đang làm trên [BNB/Base].

Chúng mình đang build ClawFriend — AI agent economy trên BNB nơi user có thể kiếm tiền
từ skills và khóa alpha sau holder-gated access. Model rất khác các DeFi tools thông thường.

Bạn có muốn làm mutual announcement không? Mình feature bạn với cộng đồng của mình,
bạn feature mình với cộng đồng của bạn. Có thể làm co-branded content nếu muốn sâu hơn.
Zero chi phí, chỉ mutual exposure.

Có thể call nếu bạn thấy có ích.
```

**Bước 3**: Với các đối tác đồng ý → thống nhất format nội dung:
- Phương án A: Cả hai dự án post tweet tag nhau vào cùng ngày
- Phương án B: Một đối tác viết thread ngắn về cách user của họ sẽ dùng ClawFriend
- Phương án C: AMA chung trên Telegram/Discord (team ClawFriend trả lời câu hỏi trong cộng đồng của đối tác)

**Bước 4**: Nếu Article Contest đang chạy → đặc biệt nhờ đối tác chia sẻ contest với cộng đồng của họ. Đây là khuếch đại miễn phí cho contest.

### Chỉ tiêu

| Chỉ số | Mục tiêu (Tháng 1) |
|---|---|
| Dự án được liên hệ | 10 |
| Đối tác xác nhận | 3–5 |
| Impressions từ các announcement đối tác | 20,000–80,000 |
| User mới từ các kênh đối tác | 100–400 |

---

## Kênh 6: ClawFriend Article Contest

**Loại**: Trả phí (prize pool) | **Ngân sách**: $5,000 | **Timeline**: Announce Ngày 8, đóng Ngày 30 | **Người thực hiện**: Trưởng nhóm marketing

### Tại sao cần kênh này

Post trả phí sống 24 giờ. Một bài viết hay về ClawFriend tồn tại vĩnh viễn trên internet, rank trên search, và được chia sẻ trong nhiều tuần. Một contest tạo ra khối lượng — thay vì team viết 1 bài, contest tạo ra 10–50 bài. Article Contest là content acquisition flywheel: giải thưởng thu hút người viết, người viết tạo nội dung, nội dung thu hút người đọc, người đọc trở thành user.

**Cơ chế**: Announce giải thưởng headline lớn ($20,000) để thu hút sự chú ý và người viết. Payout thực tế: top 5 bài chia sẻ prize pool, với toàn bộ payout theo milestone (đảm bảo sàn: $5,000 tổng, bonus đến $20K nếu đạt milestone platform vào Ngày 30). Nếu contest viral và kéo 10,000+ user → trả full $20K. Nếu không → payout sàn $5–8K.

**Bảo hiểm tích hợp**: Cài sẵn 3–5 bài viết chất lượng cao của team từ các tài khoản không lộ liên hệ. Điều này đảm bảo (1) contest trông active từ Ngày 1 (social proof), (2) nếu không có submission organic thắng, bài của team thắng — tiền thưởng quay lại team.

### Announcement contest (post Ngày 8)

**Headline**: ClawFriend Article Contest — $20,000 tiền thưởng cho những bài viết hay nhất về AI agent economy

**Format post** (Twitter thread từ @ClawFriend):
```
🚨 ClawFriend Article Contest — $20,000 tiền thưởng

Viết bài hay nhất về AI agent economy trên BNB và chiến thắng.

Top 5 tác giả chia sẻ prize pool:
🥇 Hạng 1: đến $8,000
🥈 Hạng 2: đến $5,000
🥉 Hạng 3: đến $3,000
Hạng 4 + 5: đến $2,000 mỗi người

Full prizes khi platform đạt 10,000 users vào Ngày 30.
Payout sàn: $1,000 cho top 5 bất kể kết quả.

Cách tham gia: [chi tiết trong tweet tiếp theo]
```

**Tweet quy tắc (tiếp theo)**:
```
Cách tham gia #ClawFriendArticle contest:

1. Viết 500+ từ về ClawFriend, AI agents, hoặc holder-gated economy
2. Đăng trên Medium, Mirror, Substack, hoặc blog của bạn
3. Post link trên X với tag @ClawFriend + #ClawFriendArticle
4. Deadline: Ngày 30 (ngày cụ thể)

Chấm điểm: lượt xem + chia sẻ + tính nguyên bản
Công bố winner Ngày 32
```

### Bài viết planted — hành động nội bộ team

**Ngày 8–10**: Team viết 3–5 bài chất lượng cao từ tài khoản riêng (không rõ ràng liên quan đến ClawFriend):

**Ý tưởng bài cho nội dung planted:**
1. "Cơ chế Friend.tech đã chết — đây là những gì BNB đang làm thay thế với holder-gated AI"
2. "Tôi đã dùng whale alert skill của ClawFriend 2 tuần — đây là những gì tôi tìm thấy"
3. "Tại sao AI agent economy trên BNB sẽ 10x trước Base: một phân tích"
4. "Virtuals Protocol kiếm $39M fees — ClawFriend là phiên bản BNB và miễn phí để thử"
5. "11 AI skills mà ClawFriend's holder economy hỗ trợ — xếp hạng theo độ hữu ích"

**Tiêu chuẩn chất lượng**: Mỗi bài planted phải thật sự hay — ít nhất 800 từ, dữ liệu thật, screenshots, không shill lộ liễu. Nếu writer organic submit bài tốt hơn → writer organic thắng (đó là mục tiêu).

### Nơi announce contest

| Kênh | Hành động | Ngày |
|---|---|---|
| X (@ClawFriend) | Thread announcement | Ngày 8 |
| Tất cả tài khoản KOL team | RT + comment bài announcement | Ngày 8 |
| KOL booking (Kênh 7) | KOL shill contest với audience của họ | Ngày 10–14 |
| BNB Chain Discord (#dapps, #announcements) | Post contest với chi tiết giải thưởng | Ngày 8 |
| r/bnbchain + r/CryptoCurrency | Post: "ClawFriend đang chạy $20K article contest cho writers AI/crypto" | Ngày 9 |
| Cộng đồng viết crypto trên Discord | DM moderators: "chúng tôi có thể post contest ở đây không?" | Ngày 9–10 |
| Dự án đối tác (Kênh 5) | Nhờ đối tác chia sẻ với cộng đồng của họ | Tuần 2–3 |

### Chỉ tiêu

| Chỉ số | Mục tiêu |
|---|---|
| Bài viết submission cho contest | 20–50 bài |
| Tổng lượt xem các bài contest | 50,000–200,000 |
| User ClawFriend mới từ contest | 3,000–10,000 |
| X impressions từ tag #ClawFriendArticle | 100,000+ |
| Ngân sách so với kết quả | $5K → 10,000 users = $0.50 CAC |

**Tín hiệu dừng**: Nếu < 5 submission organic vào Ngày 20 (không tính bài planted) → activate thêm KOL budget để boost contest. Nếu < 500 users vào Ngày 25 → chấp nhận payout sàn ($5K) là chi phí, chuyển năng lượng sang lập kế hoạch Tháng 2.

---

## Kênh 7: KOL Booking — Bài Viết + Khuếch Đại Contest

**Loại**: Trả phí | **Ngân sách**: $4,000 (4 KOL × ~$800–1,000 mỗi người) | **Timeline**: Tuần 2–3 | **Người thực hiện**: Trưởng nhóm marketing

### Tại sao cần kênh này

KOL mid-tier (10K–100K followers) trong ngách AI/crypto có audience tin tưởng sẽ đọc một review thread thật sự. Yêu cầu KHÔNG phải là "post tweet shill" — mà là "viết thread thật về ClawFriend làm gì và đề cập contest với audience của bạn." Format này có engagement gấp 3× post trả phí thông thường vì nó cung cấp giá trị cho audience.

KOL với 50K followers viết thread 10 tweets tạo ra 30,000–100,000 impressions. Bốn KOL như vậy = 120,000–400,000 tổng impressions. Với $4,000 tổng chi phí, đó là $0.01–$0.03 mỗi impression.

### Tiêu chí chọn KOL

| Tiêu chí | Yêu cầu | Lý do |
|---|---|---|
| Twitter followers | 10,000–100,000 | Cân bằng reach + authenticity |
| Ngách | AI agents, crypto tools, BNB/Base trading | Audience trùng với target ClawFriend |
| Engagement rate | ≥ 1.5% | Audience thật, không bot |
| Tần suất post trả phí | ≤ 1 post paid/tuần | Không phải tài khoản shill chuyên nghiệp |
| Kinh nghiệm format | Đã viết threads (không chỉ tweet đơn) | Phải có khả năng tạo nội dung dạng article |

### Cách tìm ứng viên KOL

**Bước 1**: Tìm kiếm X cho nội dung về AI agents, BNB DeFi analysis. Nhìn vào những ai đã viết về Virtuals Protocol, elizaOS, Base AI agents — những audience đó là lý tưởng.

**Bước 2**: Tạo shortlist 20 ứng viên. Check 20 posts gần nhất của họ: họ có đang thực sự phân tích không hay chỉ gọi giá?

**Bước 3**: Check engagement rate thủ công: tổng likes 10 posts gần nhất ÷ followers. Target ≥ 1.5%.

**Bước 4**: DM 12 ứng viên hàng đầu trong Tuần 2. Kỳ vọng 30–40% response rate → xác nhận 4 từ 12 outreach.

### Deliverables KOL (mỗi $800–1,000)

| Deliverable | Mô tả | Khi nào |
|---|---|---|
| Chính: Thread hoặc bài viết | 8–12 tweets HOẶC bài 600+ từ trên Medium/Substack về ClawFriend + AI agent economy | Tuần 2–3 |
| Phụ: Shill contest | 1–2 posts về Article Contest ("writers, check cái này — $20K đang chờ: [link]") | Cùng tuần với post chính |
| Tùy chọn: Space hoặc AMA | 30–60 phút X Space thảo luận về AI agent economy trên BNB | Tuần 3 |

**Cung cấp cho mỗi KOL:**
- Access vào demo ClawFriend
- Tài liệu talking points (KHÔNG phải script): cơ chế platform, tổng quan skills, holder-gated model, lợi thế BNB
- Announcement contest $20K để chia sẻ
- Số liệu họ có thể cite: contract address, số skills, context hệ sinh thái BNB

**KHÔNG yêu cầu KOL:**
- KHÔNG đưa cho họ script viết sẵn
- KHÔNG yêu cầu họ nói ClawFriend là "tốt nhất" hoặc claim về giá
- CÓ yêu cầu họ chia sẻ trải nghiệm thật khi dùng demo

### Script DM outreach

```
Hey [tên], rất thích các threads về [AI agents / BNB DeFi] của bạn — bạn rõ ràng
hiểu phần infra mà hầu hết KOL bỏ qua.

Chúng mình đang launch ClawFriend — AI agent economy trên BNB với holder-gated skills.
Nghĩ như Virtuals Protocol nhưng trên BNB và "sản phẩm" không phải token, mà là skill access.

Chúng mình đang tìm 4 writer thực sự hiểu không gian này để viết thread/article thật sự
về cơ chế — không phải shill, mà là phân tích. $800–1,000 cho bài chính + chúng mình
rất trân trọng nếu bạn đề cập Article Contest mình đang chạy.

Sẵn sàng cho bạn demo walkthrough trước. Bạn có muốn thử không?
```

### Timeline

| Ngày | Hành động |
|---|---|
| Ngày 8–10 | DM 12 ứng viên KOL |
| Ngày 12 | Follow up với người chưa reply. Xác nhận 4 KOL trả phí. |
| Ngày 13 | Brief KOL đã xác nhận: demo walkthrough, cung cấp talking points, set ngày post |
| Ngày 15–17 | KOL 1 + KOL 2 publish thread/article. RT ngay từ tất cả tài khoản team. |
| Ngày 22–24 | KOL 3 + KOL 4 publish. |
| Ngày 28 | Thu thập kết quả: impressions, lượt xem bài, contest submissions từ link KOL |

### Chỉ tiêu

| Chỉ số | Mục tiêu mỗi KOL | Tổng (4 KOL) |
|---|---|---|
| Impressions thread/article | 20,000–80,000 | 80,000–320,000 |
| Entries contest từ posts KOL | 2–5 | 8–20 |
| User ClawFriend mới | 200–500 | 800–2,000 |
| Posts #ClawFriendArticle từ audience KOL | 3–10 | 12–40 |

**Tín hiệu dừng**: Nếu thread KOL nhận < 5,000 impressions sau 48 giờ → audience KOL không engaged với ngách này. Không book posts thêm với họ.

---

## Kênh 8: Taskon Event — Base Follower Ban Đầu

**Loại**: Trả phí | **Ngân sách**: $1,000 | **Timeline**: Ra mắt Ngày 8 | **Người thực hiện**: Intern hoặc trưởng nhóm marketing

### Tại sao cần kênh này

Trước khi article contest và KOL posts lên sóng, các tài khoản social của ClawFriend không được trông trống rỗng. Một Taskon quest campaign kéo 500–2,000 người follow @ClawFriend, vào Telegram, và engage với các post đầu tiên — tạo ra vẻ ngoài của một cộng đồng active mà visitor mới nhìn thấy khi họ đến từ nội dung KOL.

Đây là "social proof floor" — $1,000 khiến $10,000 contest và KOL spend trông như có cộng đồng thật ở phía sau.

### Setup (Ngày 6–7, trước khi ra mắt Ngày 8)

**Bước 1 — Tạo Taskon Space**
1. Vào taskon.xyz
2. Connect wallet
3. Tạo "Space" cho ClawFriend — upload logo, banner, mô tả
4. Viết mô tả ngắn: "ClawFriend — AI agent economy trên BNB. Nắm giữ shares, truy cập skills độc quyền."

**Bước 2 — Tạo Quest**

Tiêu đề quest: **"ClawFriend Early Supporter Quest"**

Nhiệm vụ (theo thứ tự):
1. Follow @ClawFriend trên X (xác minh qua Taskon)
2. RT bài announcement contest đã pin (xác minh qua Taskon)
3. Tham gia Telegram channel ClawFriend (xác minh qua link)
4. Truy cập clawfriend.ai và ở lại 30 giây (xác minh qua pixel hoặc thủ công)
5. Tùy chọn: Reply post đã pin của @ClawFriend với #ClawFriendArticle

Phần thưởng: 100 Taskon points mỗi lần hoàn thành (đổi được NFT badge OAT + whitelist cho drops tương lai)

**Bước 3 — Đặt ngân sách**
- Taskon thu phí theo phân phối rewards + platform fee
- Ngân sách: $800 cho rewards, $200 cho platform/promotion
- Mục tiêu: 1,000 quest completions (= 1,000 Twitter followers mới, 1,000 thành viên Telegram)

**Bước 4 — Timing ra mắt**
- Ra mắt quest cùng ngày với Announcement Article Contest (Ngày 8)
- Quest tasks bao gồm RT bài contest → giúp boost contest visibility theo thuật toán

### Nơi promote Taskon quest

| Kênh | Post | Ngày |
|---|---|---|
| X (@ClawFriend) | "Hoàn thành Early Supporter Quest trên Taskon — NFT badge + whitelist: [link]" | Ngày 8 |
| Telegram/Discord BNB Chain community | Chia sẻ link quest | Ngày 8–9 |
| Phần featured của Taskon | Yêu cầu được featured (submit qua Taskon support) | Ngày 6 (trước launch) |
| Dự án đối tác (Kênh 5) | Nhờ chia sẻ quest với cộng đồng của họ | Ngày 10 |

### Chỉ tiêu

| Chỉ số | Mục tiêu |
|---|---|
| Quest completions | 1,000 |
| X followers mới (@ClawFriend) | 800–1,000 |
| Thành viên Telegram mới | 800–1,000 |
| Contest RTs từ người tham gia quest | 500–800 |
| CAC qua Taskon | ≤ $1.00 mỗi follower |

**Tín hiệu dừng**: Nếu < 200 completions sau 7 ngày → tăng reward mỗi task hoặc promote quest mạnh hơn trong cộng đồng crypto.

---

## Bonus: Thu Hút User Từ Friend.tech / Base Chain

**Loại**: Chi phí nhỏ (NFT mint) | **Chi phí**: $0–200 | **Timeline**: Tuần 3–4 | **Người thực hiện**: Developer + marketing

### Tại sao cần kênh này

User Friend.tech và Base chain là **audience pre-qualified nhất** cho ClawFriend. Họ đã:
1. Trả tiền cho "shares" của creator (cùng cơ chế với ClawFriend)
2. Trải nghiệm holder-gated content (quen với value proposition)
3. Chứng minh sẵn sàng chi tiền cho social/creator tokens (không chỉ DeFi)

Thu hút họ không cần giải thích gì — họ đã hiểu model. Yêu cầu: *"thử thứ bạn đã thích trên Base, nhưng giờ là trên BNB với AI skills."*

### Cơ chế thu hút

**Phương án được khuyến nghị: Free NFT Mint cho holder Friend.tech**

**Từng bước thực hiện (Ngày 21–22)**:
1. Developer tạo NFT collection đơn giản trên BNB dùng thirdweb hoặc manifold.xyz
2. Điều kiện eligibility: ví đã từng hold Friend.tech share có thể claim (Merkle proof hoặc snapshot từ Dune Analytics)
3. Tạo trang mint: "ClawFriend Early Supporter NFT — miễn phí cho Friend.tech veterans"
4. Post announcement trên X + tag các tài khoản cộng đồng Friend.tech
5. Submit vào Discord cộng đồng Base/Friend.tech: "Free NFT cho holder ft.tech — không drain ví, chỉ là badge + lời mời ClawFriend"

**Phương án B (nhanh hơn, không cần dev)**: Airdrop lượng BNB nhỏ cho ví Friend.tech với message trong transaction: "Bạn đã hold Friend.tech shares. ClawFriend là phiên bản BNB với AI skills. Thử ngay: clawfriend.ai"

### Chỉ tiêu

| Chỉ số | Mục tiêu |
|---|---|
| NFT claims | 500–2,000 |
| % truy cập ClawFriend | 20–40% → 100–800 |
| % tạo agent hoặc cài skill | 5–10% → 25–200 |

---

## Timeline Theo Tuần

| Tuần | Ngày | Hành động chính | Ngân sách triển khai |
|---|---|---|---|
| **Tuần 1** | Ngày 1–7 | 🚨 Sửa ClawHub (Ngày 1). DM @steipete (Ngày 1). Mỗi thành viên team setup tài khoản KOL + post 3x/ngày. Tạo 4 X Lists cho tất cả ngách. Bật notification cho 20 KOL hàng đầu mỗi list. Research 30 ứng viên KOL collab. Research 10 dự án đối tác. Setup Taskon Space (Ngày 6–7). | $0 |
| **Tuần 2** | Ngày 8–14 | Ra mắt Taskon quest (Ngày 8). Announce Article Contest (Ngày 8). Post contest trên BNB Discord + Reddit (Ngày 9). DM 20 ứng viên KOL booking (Ngày 8–10). Đăng 2–3 bài planted đầu tiên. DM 30 ứng viên KOL collab exchange. DM 10 dự án đối tác. X commenting: 10–20 comments/intern/ngày liên tục. | $1,000 (Taskon) |
| **Tuần 3** | Ngày 15–21 | KOL 1 + KOL 2 publish articles/threads (Ngày 15–17). Team RT boost ngay lập tức. Contest đang tích lũy submissions organic. Bài planted 4–5 đăng. Các post collab KOL lên sóng. Announcement dự án đối tác. Setup Friend.tech NFT mint (Ngày 21). | $2,000 (KOL 1+2) |
| **Tuần 4** | Ngày 22–30 | KOL 3 + KOL 4 publish articles (Ngày 22–24). Contest đóng Ngày 30. Công bố winners Ngày 32. Friend.tech NFT mint live (Ngày 22+). Push cuối cùng trên tất cả organic channels. Thu thập metrics Tháng 1. | $2,000 (KOL 3+4) + $5K contest payout |
| **Tổng** | | | **$5,000** (Contest) + **$4,000** (KOL) + **$1,000** (Taskon) = **$10,000** |

---

## Dashboard Chỉ Số Thành Công — Tháng 1

| Chỉ số | Baseline (Ngày 0) | Mục tiêu (Ngày 30) | Cách đo |
|---|---|---|---|
| ClawHub installs | 1 | 100+ | clawhub.ai/leeknowsai/clawfriend |
| Trạng thái VirusTotal | Suspicious | Clean | virustotal.com |
| X followers (@ClawFriend) | Nhỏ | 2,000+ | Twitter Analytics |
| Followers tài khoản KOL team (tổng) | 0 | 1,500+ (cộng lại) | Analytics từng tài khoản |
| Submissions Article Contest | 0 | 20–50 bài | Tag #ClawFriendArticle |
| Tổng lượt xem bài viết | 0 | 100,000+ | Stats Medium/Substack |
| User mới từ nội dung contest | 0 | 5,000–10,000 | UTM links trong bài |
| Taskon completions | 0 | 1,000 | Dashboard Taskon |
| Impressions thread KOL | 0 | 200,000+ | Twitter Analytics |
| Tổng agents được launch | ~5 | 20+ | ClawFriend platform |
| Share trades | Không rõ | 500+ | Events contract ClawFriendV1 |
| CAC (blended) | N/A | ≤ $2.00 | UTM tracking |

---

## Preview Tháng 2 (Mở Khóa Khi Thành Công)

Nếu mục tiêu Tháng 1 đạt được (5,000+ users, 20+ agents, VirusTotal sạch):
- **Article Contest Series**: Chạy Contest Vòng 2 với ngân sách lớn hơn — tái đầu tư từ doanh thu Tháng 1
- **KOL Program mở rộng**: Book 8–10 KOL mỗi tháng thay vì 4
- **Twitter/X Ads**: Bây giờ đã có social proof (bài viết, KOL posts, Taskon completions) → paid ads convert tốt hơn. Thêm $3K–$5K X Ads vào Tháng 2.
- **Exchange listings**: Trình bày metrics Tháng 1 với các sàn Tier 2–3 để listing ClawFriend share token
- **BNB MVB grant**: Nộp đơn với metrics thực tế → $10K–$50K tiềm năng
- **Mở rộng cross-chain**: Thành công Friend.tech → nhân rộng acquisition cho các cộng đồng holder-economy khác (Stars Arena, DeSo)

Kế hoạch Tháng 1 được tối ưu hóa cho một kết quả duy nhất: **nội dung viral khiến ClawFriend trở thành dự án AI agent được nói đến nhiều nhất trên BNB**. Mỗi đồng và mỗi giờ đều hướng vào mục tiêu đó.

---

*Kế hoạch phân phối được tổng hợp dựa trên phân tích competitive landscape, nghiên cứu skills, và khả năng platform ClawFriend. Chiến lược cập nhật tháng 2 năm 2026.*
