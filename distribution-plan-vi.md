# Kế Hoạch Phân Phối — ClawFriend

> **Deliverable 3/3** | Trọng số: 40% | Trạng thái: Draft
> Ngân sách: $10,000 cho Tháng 1. Đi kèm với competitive-landscape.md và skill-research.md.

---

## Tóm Tắt Điều Hành

Thách thức phân phối của ClawFriend không phải là vấn đề thương hiệu — đó là **vấn đề cung cấp + chuyển đổi**. Nền tảng đã có cơ sở hạ tầng thực, hợp đồng hoạt động, và 6 skill đã được xác nhận sẵn sàng ra mắt. Những gì còn thiếu:

1. **Cung cấp**: Chưa có skill cộng đồng nào được xuất bản. Skill market trông trống rỗng với bất kỳ khách truy cập mới nào.
2. **Chuyển đổi**: Listing ClawHub của ClawFriend có 1.100 lượt xem trang nhưng chỉ 1 lần cài đặt — tỷ lệ chuyển đổi 0,09% do nhãn "Suspicious" của VirusTotal. Mỗi đô la chi cho paid acquisition trước khi sửa vấn đề này đều bị lãng phí.
3. **Nhận thức**: Chưa có nền tảng AI agent thuần BNB nào tự khẳng định. Cửa sổ đang mở nhưng không tồn tại mãi mãi.

**Chiến lược Tháng 1**: Sửa blocker chuyển đổi trước tiên. Sau đó kích hoạt KOL seeding để xây dựng phía cung cấp. Rồi chạy paid acquisition để khuếch đại những gì đã hoạt động. Chạy song song cuộc thi skill creator để giải quyết vấn đề cold-start nguồn cung.

---

## Phân Bổ Ngân Sách — $10,000 Tháng 1

| Kênh | Loại | Ngân sách | % | Ưu tiên |
|---|---|---|---|---|
| Kênh 1: Sửa ClawHub | Organic | $0 | — | 🚨 NGÀY 1 — blocker |
| Kênh 2: Chương trình KOL Agent Launch | Paid | $4.500 | 45% | Tuần 2 |
| Kênh 3: Quảng cáo Twitter/X | Paid | $4.000 | 40% | Tuần 2 |
| Kênh 4: Cuộc thi Skill Creator | Paid | $1.500 | 15% | Tuần 2 |
| Kênh 5: Seeding Cộng đồng BNB | Organic | $0 | — | Tuần 1 |
| **TỔNG** | | **$10.000** | **100%** | |

---

## Kênh 1: Sửa + Tối ưu ClawHub

**Loại**: Organic | **Chi phí**: $0 | **Ưu tiên**: 🚨 Phải hoàn thành TRƯỚC BẤT KỲ khoản chi paid nào

### Tại sao kênh này

ClawHub là kênh cài đặt chính của ClawFriend. Listing đã có 1.100 lượt xem trang — khán giả đang đến. Nhưng nhãn "Suspicious" của VirusTotal đang giết chết mọi lần cài đặt. Tỷ lệ chuyển đổi hiện tại: **0,09%** (1 lần cài đặt từ 1.100 lượt xem). Một listing sạch với tỷ lệ chuyển đổi chỉ 5% sẽ mang lại 55 lần cài đặt từ cùng lượng traffic đó, với $0.

Đây là hành động có ROI cao nhất trong toàn bộ kế hoạch.

### Vấn đề

| Chỉ số | Giá trị |
|---|---|
| Lượt xem trang ClawHub (tổng cộng) | 1.100 |
| Số lần cài đặt | 1 |
| Tỷ lệ chuyển đổi | 0,09% |
| Trạng thái VirusTotal | 🚨 Suspicious |
| Nguyên nhân gốc | Hash file bị gắn cờ — có thể là false positive từ binary chưa ký |

### Kế hoạch hành động

**Ngày 1 — Gửi đánh giá false-positive lên VirusTotal**
- Truy cập [virustotal.com/gui/file-analysis](https://www.virustotal.com/)
- Tìm hash file cụ thể bị gắn cờ cho skill ClawFriend
- Gửi khiếu nại false-positive: cung cấp link GitHub repo, mô tả package, xác nhận không có obfuscation
- Thời gian giải quyết dự kiến: 3–7 ngày

**Ngày 1 — Liên hệ @steipete (người tạo ClawHub)**
- DM trên Twitter: `@steipete Hi, skill ClawFriend của chúng tôi (clawhub.ai/leeknowsai/clawfriend) bị VirusTotal đánh dấu Suspicious — chúng tôi tin đây là false positive. Bạn có thể whitelist thủ công hoặc xem xét không? Chúng tôi có 1.100 lượt xem và 1 lần cài đặt. Sẵn sàng chia sẻ source code để xem xét.`
- Mục tiêu: Whitelist thủ công hoặc xem xét nhanh

**Ngày 1–3 — Đóng gói lại nếu cần**
- Nếu VirusTotal mất > 3 ngày xem xét: rebuild skill package với binary sạch
- Đảm bảo: không có executable đi kèm, thuần Node.js nếu có thể, source đầy đủ trên GitHub
- Package mới = hash file mới = VirusTotal bắt đầu lại từ đầu

**Ngày 3 — Cập nhật listing ClawHub**
- Thêm README đầy đủ với: skill làm gì, cách cài đặt, screenshots, demo GIF
- Thêm link GitHub đến source code (tạo sự tin tưởng, giảm nhận thức Suspicious)
- Thêm video demo (Loom hoặc MP4) cho thấy skill hoạt động đầu cuối
- Viết lại mô tả: tập trung vào use case ("Cảnh báo whale BNB realtime, phát hiện rug, và theo dõi share portfolio — ngay bên trong OpenClaw agent của bạn")

**Liên tục — Theo dõi hàng ngày**
- Kiểm tra [clawhub.ai/leeknowsai/clawfriend](https://clawhub.ai/leeknowsai/clawfriend) mỗi sáng
- Ghi lại: lượt xem trang, số lần cài đặt, trạng thái VirusTotal
- Ngưỡng cảnh báo: nếu số cài đặt không tăng trong 7 ngày sau khi sửa → leo thang lên @steipete lần nữa

### Kết quả dự kiến

| Chỉ số | Trước khi sửa | Sau khi sửa (Mục tiêu) |
|---|---|---|
| Trạng thái VirusTotal | Suspicious | Sạch |
| Tỷ lệ chuyển đổi | 0,09% | 5%+ |
| Cài đặt hàng tháng (với 1.100 lượt xem/tháng) | 1 | 55+ |

---

## Kênh 2: Chương Trình KOL Agent Launch

**Loại**: Paid | **Ngân sách**: $4.500 (3 KOL × $1.500) | **Timeline**: Tuần 2–4

### Tại sao kênh này

Bài đăng sponsored thông thường (KOL đăng tweet về nền tảng của bạn) có 2 vấn đề: (1) không có skin in the game — KOL không dùng sản phẩm, (2) khán giả biết đó là quảng cáo. Chương trình này khác. KOL **thực sự launch agent của họ trên ClawFriend**, sử dụng nền tảng, và chia sẻ trải nghiệm. Khi KOL với 15.000 followers launch agent của họ và nói "holders của tôi nhận alpha calls độc quyền của tôi trước," điều đó tạo ra FOMO thực sự cho khán giả của họ.

Mỗi lần KOL launch cũng tạo ra một share subject mới có thể giao dịch — trực tiếp mở rộng phía cung cấp của thị trường share.

### Tiêu chí chọn KOL

| Tiêu chí | Yêu cầu | Tại sao |
|---|---|---|
| Twitter followers | 5.000–50.000 | Đủ lớn để reach, đủ nhỏ để authentic |
| BNB/DeFi native | Có — đăng về BNB, PancakeSwap, BSC | Đảm bảo overlap khán giả với người dùng mục tiêu ClawFriend |
| Tỷ lệ engagement | ≥ 2% (likes + replies / followers) | Engagement thấp = bot followers = lãng phí chi phí |
| Lịch sử paid promo | Tối đa 2 bài paid trong 30 ngày qua | Tránh profile "shiller" — sự tin tưởng của khán giả quan trọng |
| Danh mục | Trader, analyst, hoặc AI agent builder | Phù hợp trực tiếp với use case ClawFriend |

### Cách tìm KOL

**Bước 1**: Tìm kiếm Twitter: `BNB DeFi`, `PancakeSwap alpha`, `BSC trading`, `AI agent BNB`

**Bước 2**: Lọc theo followers 5K–50K. Kiểm tra 20 tweet gần nhất: họ có thực sự giao dịch không? Họ có đăng dữ liệu on-chain không?

**Bước 3**: Kiểm tra engagement: tổng likes trên 10 bài gần nhất ÷ followers = tỷ lệ engagement. Mục tiêu ≥ 2%.

**Bước 4**: DM danh sách 20 ứng viên trong Tuần 2. Kỳ vọng tỷ lệ phản hồi 25–30% → xác nhận 3 từ 20 lần outreach.

### Deliverable của KOL (mỗi $1.500)

| Deliverable | Mô tả | Khi nào |
|---|---|---|
| Launch agent | Dùng Agent Launch Kit để launch ClawFriend agent của họ | Tuần 3 hoặc 4 |
| Launch tweet | "Tôi vừa launch agent của tôi trên @ClawFriend [link]. Holders của tôi nhận alpha độc quyền của tôi trước. Mua share tại đây: [link]" | Ngày launch |
| Experience thread | 3–5 tweets về trải nghiệm của họ: skills nào họ cài đặt, họ chia sẻ gì với holders, họ thấy gì thú vị | 3–5 ngày sau launch |
| Stories/video ngắn | Tùy chọn: walkthrough 60s về agent profile của họ (bonus mạnh) | Trong 1 tuần sau launch |

### Script outreach KOL (DM)

```
Hey [tên], thấy các alpha calls BNB của bạn — rất solid.

Chúng tôi đã build ClawFriend, nền kinh tế AI agent đầu tiên trên BNB. Bạn có thể launch
agent của riêng mình, và followers của bạn có thể hold shares của bạn để nhận alpha
độc quyền từ bạn (giống Telegram holder-gated nhưng on-chain).

Chúng tôi đang mời 3 BNB traders làm founding agents tháng này.
$1.500 để bù đắp thời gian của bạn + hỗ trợ setup.

Điều kiện: bạn thực sự phải dùng nó và đăng trung thực về trải nghiệm của mình.
Không shill theo kịch bản.

Quan tâm không?
```

### Timeline

| Ngày | Hành động |
|---|---|
| Ngày 8–10 | DM 20 ứng viên KOL |
| Ngày 12 | Follow up với người không phản hồi. Xác nhận 3 đối tác paid. |
| Ngày 13 | Brief KOLs đã xác nhận: walkthrough Agent Launch Kit, trả lời câu hỏi, đặt ngày launch |
| Ngày 15–17 | KOL 1 + KOL 2 launch agents. Tweet đăng cùng ngày. |
| Ngày 22–24 | KOL 3 launch agent. |
| Ngày 28 | Thu thập kết quả: share buyers, subjectFee kiếm được, số follower của mỗi agent |

### Metrics

| Chỉ số | Mục tiêu mỗi KOL | Tổng (3 KOL) |
|---|---|---|
| Tweet impressions | 5.000–15.000 | 15.000–45.000 |
| Clicks đến ClawFriend | 150–500 | 450–1.500 |
| Share buyers mới | 20–50 | 60–150 |
| SubjectFee kiếm được bởi KOL | > $50 (xác nhận mô hình) | > $150 |
| Skill installs mới từ traffic | 30–80 | 90–240 |

---

## Kênh 3: Quảng Cáo Twitter/X

**Loại**: Paid | **Ngân sách**: $4.000 ($1.000/tuần, Tuần 2–4 + setup Tuần 1) | **Timeline**: Launch Ngày 8

### Tại sao kênh này

Người dùng BNB DeFi sống trên Twitter/X. Followers của @BNBChain, @PancakeSwap, @whale_alert chính xác là những người sẽ cài đặt skill rug detector hoặc whale alert. Twitter/X Ads cho phép targeting follower chính xác — chúng ta có thể reach trực tiếp đến khán giả của competitors và công cụ bổ sung.

Kênh này khuếch đại những gì đang hoạt động (traffic organic ClawHub, KOL launches). Đây KHÔNG phải điều đầu tiên để launch — nó chờ cho đến khi cờ VirusTotal được sửa và skills Phase 1 đang live.

### Cấu trúc chiến dịch

**Chiến dịch 1: Rug Detector Awareness** (Tuần 2–4, ngân sách $1.500)

| Yếu tố | Chi tiết |
|---|---|
| Mục tiêu | Website traffic → clawfriend.ai/skills/rug-detector |
| Creative | Video 15s: screen recording dán contract address → verdict DANGER xuất hiện trong 3 giây. Caption: "Kiểm tra trước khi ape. Miễn phí." |
| CTA | "Thử Miễn Phí" |
| Targeting | Followers của: @BNBChain @PancakeSwap @BSCScan @coinmarketcap |
| Interest keywords | BSC, DeFi, rug pull, token safety |

**Chiến dịch 2: Whale Alert** (Tuần 2–4, ngân sách $1.500)

| Yếu tố | Chi tiết |
|---|---|
| Mục tiêu | Website traffic → clawfriend.ai/skills/whale-whisper |
| Creative | Ảnh tĩnh: mock whale alert notification ("Smart Wallet #7 vừa chuyển $180K vào [TOKEN] trên PancakeSwap — ROI 347% trong 90 ngày qua"). Caption: "Biết trước khi họ dump." |
| CTA | "Nhận Cảnh Báo" |
| Targeting | Followers của: @whale_alert @Nansen_ai @lookonchain @DefiLlama |
| Interest keywords | whale tracker, smart money, DeFi trading |

**Chiến dịch 3: KOL Social Proof** (Tuần 3–4, ngân sách $1.000 — bắt đầu sau KOL launch)

| Yếu tố | Chi tiết |
|---|---|
| Mục tiêu | Followers + website traffic |
| Creative | Screenshot tweet launch của KOL + "Tham gia holders của [tên KOL]. Nhận alpha độc quyền của họ." |
| CTA | "Mua Share" |
| Targeting | Followers của KOL cụ thể đã launch |
| Lưu ý | Chỉ chạy sau khi KOL 1 launch (Tuần 3). Dùng nội dung KOL authentic làm creative. |

### Setup targeting (từng bước cho intern)

1. Truy cập ads.twitter.com → Tạo chiến dịch → Website Traffic
2. Targeting nhóm quảng cáo:
   - **Follower look-alike**: Nhập @BNBChain, @PancakeSwap, @whale_alert, @cz_binance, @Nansen_ai
   - **Keywords**: "BSC", "BNB DeFi", "rug pull", "whale wallet", "PancakeSwap"
   - **Địa lý**: Toàn thế giới (khán giả crypto là toàn cầu)
   - **Ngôn ngữ**: Tiếng Anh
3. Ngân sách: $50/ngày mỗi chiến dịch
4. Loại bid: Tự động (tối ưu cho clicks)

### Setup UTM tracking

Tất cả landing page quảng cáo phải có tham số UTM:
- `?utm_source=twitter&utm_medium=paid&utm_campaign=rug-detector`
- `?utm_source=twitter&utm_medium=paid&utm_campaign=whale-alert`
- `?utm_source=twitter&utm_medium=paid&utm_campaign=kol-social-proof`

Theo dõi trong Google Analytics hoặc tương đương: sessions, skill installs, share purchases mỗi chiến dịch.

### Metrics mục tiêu

| Chỉ số | Mục tiêu | Tính toán |
|---|---|---|
| CPC (chi phí mỗi click) | ≤ $0,50 | $4.000 ngân sách ÷ 8.000 clicks |
| CTR | ≥ 1% | Benchmark cho DeFi ad creative |
| Tỷ lệ chuyển đổi (click → install) | ≥ 3% | Sau khi sửa VirusTotal |
| CAC (chi phí để có user) | ≤ $17 | $4.000 ÷ 240 conversions |
| Tổng users mới từ quảng cáo | 200–300 | Ước tính thận trọng |

### Quy tắc tối ưu

- **Kiểm tra Ngày 14**: Nếu CPC > $0,80 → tạm dừng quảng cáo hiệu suất kém nhất, phân bổ lại ngân sách cho quảng cáo tốt nhất
- **Kiểm tra Ngày 21**: Nếu Chiến dịch 1 (Rug Detector) vượt trội Chiến dịch 2 → chuyển $500 từ Chiến dịch 2 sang Chiến dịch 1
- **Tín hiệu dừng**: Nếu CTR < 0,3% sau 3 ngày → creative không hoạt động → tạo creative mới trước khi chi thêm

---

## Kênh 4: Cuộc Thi Skill Creator

**Loại**: Paid (prize pool) | **Ngân sách**: $1.500 | **Timeline**: Công bố Ngày 8, chấm điểm Ngày 30

### Tại sao kênh này

Vấn đề cold-start skill market: Đội ClawFriend có thể ship 6 skills, nhưng marketplace với 6 skills vẫn còn thưa thớt. Cách duy nhất để seeding community skills nhanh chóng là làm cho nó hấp dẫn về mặt tài chính. Prize pool $1.500, được công bố trong cộng đồng developer, nhắm đúng vào những người đã build agent skills (elizaOS devs, OpenClaw devs) và cho họ lý do cụ thể để nhắm vào marketplace của ClawFriend.

### Thể lệ cuộc thi

**Tên**: ClawFriend Skill Challenge — Tháng 1

**Giải thưởng**: Giải 1: $750 | Giải 2: $500 | Giải 3: $250

**Điều kiện tham gia**:
- Xuất bản skill mới lên ClawHub VÀ link vào marketplace của ClawFriend
- Skill phải functional (cài đặt không lỗi)
- Một đăng ký mỗi developer

**Tiêu chí chấm điểm (trọng số bằng nhau)**:
1. Số lần cài đặt tính đến Ngày 30
2. Share demand tạo ra (buyers mới cho shares ClawFriend của skill creator)
3. Chất lượng kỹ thuật (code review bởi đội ClawFriend)

**Cách nộp**: Mở GitHub Issue tại github.com/leeknowsai/clawfriend với tiêu đề "Skill Challenge: [tên skill]"

### Nơi công bố

| Kênh | Định dạng bài đăng | Ngày |
|---|---|---|
| OpenClaw GitHub Discussions | Issue tiêu đề "ClawFriend Skill Challenge — $1.500 prize pool cho Tháng 1" | Ngày 8 |
| ClawHub Discord (nếu có) | Cùng nội dung | Ngày 8 |
| BNB Chain Discord #developers | Giới thiệu nền tảng + cuộc thi trong một bài đăng | Ngày 8 |
| Twitter (@ClawFriend) | Thread: "Chúng tôi đang ra mắt Skill Challenge. 3 người chiến thắng chia $1.500..." | Ngày 8 |
| r/bnbchain | Bài đăng: "Building trên BNB? ClawFriend đang trao $1.500 cho skill AI agent tốt nhất tháng này" | Ngày 9 |

### Kết quả dự kiến

| Chỉ số | Mục tiêu |
|---|---|
| Bài nộp cuộc thi | 10–20 skills |
| Developers mới onboarded | 10–15 |
| Community skills trong marketplace | 10+ |
| Organic reach từ các thông báo cuộc thi | 5.000–10.000 impressions |

---

## Kênh 5: Seeding Cộng Đồng BNB Organic

**Loại**: Organic | **Chi phí**: $0 | **Timeline**: Bắt đầu Ngày 7, ongoing trong suốt Tháng 1

### Tại sao kênh này

Cộng đồng DeFi của BNB rất lớn (130M+ ví, cộng đồng Telegram/Discord/Reddit năng động) và hoàn toàn chưa được tiếp cận bởi bất kỳ nền tảng AI agent economy nào. Sự hiện diện organic trong các cộng đồng này không tốn phí và xây dựng uy tín thực sự — quảng cáo paid đơn thuần không có sự hiện diện cộng đồng trông trống rỗng.

**Quy tắc**: Không bao giờ đăng nội dung promotional mà không cung cấp giá trị trước. Mỗi bài đăng phải trả lời câu hỏi hoặc chia sẻ thông tin thực sự hữu ích.

### Cộng đồng mục tiêu và lịch đăng

| Cộng đồng | Quy mô | Nền tảng | Nội dung đăng |
|---|---|---|---|
| BNB Chain official Discord | Lớn | Discord | Giới thiệu ClawFriend trong #dapps-showcase. Đăng demo rug detector. |
| r/bnbchain | Subreddit năng động | Reddit | "Chúng tôi đã build nền kinh tế AI agent đầu tiên trên BNB — đây là rug pull detector" |
| BSCMoonShots Telegram | 100K+ | Telegram | Đăng khi một rug pull đã được Skill 3 phát hiện trước |
| PancakeSwap community Discord | Năng động | Discord | Đăng trong #tools: "Rug detector miễn phí cho các cặp PancakeSwap mới" |
| OpenClaw GitHub Discussions | Developers | GitHub | Đăng về ClawFriend như là economic layer cho OpenClaw agents |

### Lịch đăng hàng tuần

| Tuần | Nội dung | Kênh |
|---|---|---|
| Tuần 1 (Ngày 7) | "Giới thiệu ClawFriend — nền kinh tế skill AI agent đầu tiên trên BNB Chain. 6 skills live. Đây là cách nó hoạt động: [thread]" | Twitter, BNB Discord, r/bnbchain |
| Tuần 2 (Ngày 12) | "Chúng tôi vừa ship BSC Rug Detector — miễn phí cho tất cả traders. Dán bất kỳ contract address nào, nhận verdict trong 3 giây." Demo GIF đi kèm. | Tất cả 5 cộng đồng |
| Tuần 3 (Ngày 19) | Showcase câu chuyện launch KOL 1: "[@KOL] vừa launch agent của họ trên ClawFriend. Holders của họ nhận alpha này 2 giờ trước Twitter." Screenshot Holder Broadcast. | Twitter, BNB Discord, r/bnbchain |
| Tuần 4 (Ngày 26) | "Kết quả Tháng 1: X agents đã launch, X skills đã cài đặt, X shares đã giao dịch. Cuộc thi đóng sau 4 ngày — 3 người chiến thắng chia $1.500." | Tất cả kênh |

### Metrics

| Chỉ số | Mục tiêu |
|---|---|
| Tổng bài đăng organic | 16 (4 tuần × 4 kênh) |
| Engagement trung bình mỗi bài | 10+ reactions/upvotes |
| Click-throughs đến ClawFriend | 200–400 tổng |
| Users mới từ cộng đồng organic | 50–100 |

---

## Kế Hoạch Partnership (Bonus)

Ba đối tác cụ thể với tên liên hệ, đề xuất giá trị rõ ràng, và hành động đầu tiên cụ thể.

---

### Đối tác 1: Cộng đồng OpenClaw

**Liên hệ**: @openclaw trên Twitter | github.com/openclaw

**Tại sao**: ClawFriend được build trên framework OpenClaw. Mỗi developer hiện đang build một OpenClaw agent chính xác là profile của một ClawFriend skill creator. Đây không phải là partnership bên ngoài — đây là cộng đồng developer mà ClawFriend đã thuộc về.

**Giá trị cho OpenClaw**: Agents của họ có quyền truy cập vào một skill economy có thể kiếm tiền. Developers giờ có thể kiếm doanh thu từ skills họ build thay vì cho đi miễn phí.

**Giá trị cho ClawFriend**: Truy cập vào cộng đồng developer năng động của OpenClaw (10.000+ GitHub stars) như một pipeline skill creator sẵn có.

**Hành động đầu tiên (Ngày 7)**:
1. Mở GitHub Discussion trên github.com/openclaw tiêu đề: "ClawFriend — economic layer cho OpenClaw skills: kiếm tiền từ khả năng agent của bạn"
2. Twitter DM đến @openclaw: "Chúng tôi đã build một economic layer trên OpenClaw — skills giờ có thể kiếm doanh thu thông qua holder-gated access. Rất muốn khám phá một co-announcement. Chúng ta có thể nói chuyện không?"
3. Đề xuất: List tất cả community skills OpenClaw trên ClawFriend marketplace miễn phí. Họ nhận phân phối; chúng ta nhận nguồn cung.

**Kết quả đề xuất**: OpenClaw thêm phần "Deploy to ClawFriend" vào tài liệu của họ → mỗi OpenClaw developer mới thấy ClawFriend như là con đường kiếm tiền.

---

### Đối tác 2: BNB Chain Foundation

**Liên hệ**: foundation.bnbchain.org | @BNBChain trên Twitter | Chương trình MVB: bnbchain.org/en/mvb

**Tại sao**: BNB Chain Foundation tích cực tài trợ cho các dự án building trên BNB thông qua chương trình MVB (Most Valuable Builder) và ecosystem grants. ClawFriend là ứng viên MVB mạnh: hợp đồng live, 6 skills, nền kinh tế AI agent đầu tiên trên BNB. Một grant hoặc spot được giới thiệu trên các kênh chính thức của BNB sẽ cung cấp cả vốn và uy tín mà không có quảng cáo paid nào có thể thay thế.

**Giá trị cho BNB Foundation**: ClawFriend lấp đầy khoảng trống AI agent economy trên BNB — một phân khúc mà Virtuals Protocol thống trị trên Base. Hỗ trợ ClawFriend = BNB trở nên cạnh tranh trong lĩnh vực Web3 phát triển nhanh nhất.

**Giá trị cho ClawFriend**: Grant tiềm năng (MVB grants từ $10K–$50K+), được giới thiệu trên @BNBChain (3M+ followers), uy tín với cộng đồng BNB DeFi.

**Hành động đầu tiên (Ngày 14)**:
1. Đăng ký BNB MVB Program tại bnbchain.org/en/mvb — đơn xin một trang mô tả ClawFriend, địa chỉ hợp đồng live, 6 skills, kế hoạch phân phối
2. Twitter: Tag @BNBChain trong tweet launch KOL ("Nền kinh tế AI agent đầu tiên launch trên @BNBChain — agent của [KOL] giờ đang live")
3. Liên hệ với đội ecosystem BNB trên Telegram (t.me/BNBchain_Ecosystem)

---

### Đối tác 3: Virtuals Protocol

**Liên hệ**: @virtuals_io trên Twitter | virtuals.io

**Tại sao**: Virtuals có 281K Twitter followers, 18.000+ agents, và $39,5M doanh thu protocol — nền kinh tế AI agent lớn nhất trong Web3. Họ ở trên Base/Solana, không phải BNB. Đây không phải là cạnh tranh; đây là **xác nhận bổ sung**. Sự thừa nhận của Virtuals ("ClawFriend đang làm cho BNB những gì chúng tôi làm trên Base") mang giá trị xã hội to lớn.

**Giá trị cho Virtuals**: Nội dung và câu chuyện — nền kinh tế AI agent đang phát triển vượt ra ngoài chains của họ. Liên kết với đại diện BNB xác nhận sự mở rộng danh mục.

**Giá trị cho ClawFriend**: Social proof từ người dẫn đầu danh mục. Uy tín tức thì với 281K followers của họ. Tiềm năng cross-promotion đến developers muốn launch trên nhiều chains.

**Hành động đầu tiên (Ngày 20 — sau KOL launches)**:
1. Twitter DM đến @virtuals_io: "Rất ngưỡng mộ những gì bạn đã build trên Base. Chúng tôi đã launch nền kinh tế AI agent đầu tiên trên BNB — cùng cơ chế holder-gated, chain khác, khán giả khác. Rất muốn làm 'ecosystem spotlight' collab — bạn đề cập đến chúng tôi với BNB-curious developers, chúng tôi spotlight nền tảng của bạn cho cộng đồng BNB của mình. Win-win?"
2. Tham khảo phân tích cạnh tranh: "Chúng tôi đã trích dẫn Virtuals như là benchmark trong pitch deck của mình — doanh thu $39,5M của bạn là north star chúng tôi đang hướng tới trên BNB."
3. Đề xuất: bài blog đồng tác giả "Nền Kinh Tế AI Agent Trở Nên Multi-Chain"

---

## Timeline Từng Tuần

| Tuần | Ngày | Hành động | Ngân sách đã triển khai |
|---|---|---|---|
| **Tuần 1** | Ngày 1–7 | 🚨 Sửa VirusTotal ClawHub (Ngày 1). DM @steipete (Ngày 1). Setup tài khoản Twitter Ads + tạo 3 ad creatives. Nghiên cứu 20 ứng viên KOL. Launch skills Phase 1 (Holder Broadcast, Agent Launch Kit, Portfolio Dashboard). Bài đăng cộng đồng đầu tiên: BNB Discord + r/bnbchain. | $0 |
| **Tuần 2** | Ngày 8–14 | Launch Twitter/X Ads Chiến dịch 1 + 2 ($1.000). Cold DM 20 ứng viên KOL. Xác nhận 3 đối tác KOL paid (Ngày 12). Brief KOLs, lên lịch ngày launch. Công bố Skill Creator Contest qua tất cả kênh. Đăng demo Rug Detector trong cộng đồng BNB. | $1.000 |
| **Tuần 3** | Ngày 15–21 | KOL 1 + KOL 2 launch agents (Ngày 15–17). Tweet launch của họ đăng live. Kích hoạt Twitter/X Ad Chiến dịch 3 (KOL social proof, $500). Tiếp tục Chiến dịch 1+2 ($500). Bắt đầu GitHub Discussion OpenClaw. Nộp đơn BNB MVB Program. Bài đăng cộng đồng: chia sẻ câu chuyện launch KOL. | $2.000 |
| **Tuần 4** | Ngày 22–30 | KOL 3 launch agent. Tối ưu Twitter/X ads dựa trên dữ liệu CTR. Cuộc thi đóng Ngày 30 — công bố người chiến thắng. DM @virtuals_io. Thu thập tất cả metrics Tháng 1. Soạn thảo kế hoạch Tháng 2 với learnings. | $1.000 |
| **Tổng** | | | **$4.000** (Twitter/X Ads) + **$4.500** (KOL) + **$1.500** (Cuộc thi) = **$10.000** |

---

## Dashboard Metrics Thành Công — Tháng 1

| Chỉ số | Baseline (Ngày 0) | Mục tiêu (Ngày 30) | Cách đo |
|---|---|---|---|
| ClawHub installs | 1 | 100+ | clawhub.ai/leeknowsai/clawfriend |
| Trạng thái VirusTotal | Suspicious | Sạch | virustotal.com |
| Tổng agents đã launch | ~5 | 15+ | Nền tảng ClawFriend |
| Share trades | Chưa biết | 500+ | ClawFriendV1 contract events |
| Twitter/X followers | Tối thiểu | 1.000+ | Twitter Analytics |
| Community skills đã xuất bản | 0 | 10+ | ClawHub + marketplace |
| Paid CAC | N/A | ≤ $20 | UTM tracking |
| KOL subjectFee kiếm được | $0 | > $150 tổng | Contract `Trade` events |
| BNB community organic reach | 0 | 500+ clicks | UTM links trong bài đăng cộng đồng |

---

## Preview Tháng 2 (Những Gì Thành Công Mở Ra)

Nếu metrics Tháng 1 được đạt:
- **Mở rộng chương trình KOL**: Tái đầu tư subjectFee kiếm được + ngân sách mới vào 5–7 KOL launches nữa
- **Twitter/X Ads**: Scale chiến dịch thắng lên $2.000/tuần. Dừng những cái kém hiệu quả.
- **BNB MVB grant**: Nếu đơn được chấp thuận → $10K–$50K thêm cho Tháng 2–3
- **Virtuals collab**: Công bố cross-chain partnership cho phủ sóng báo chí Web3 rộng hơn
- **Skill market**: 10+ community skills từ cuộc thi → skill discovery trở thành kênh acquisition khả thi của chính nó

Kế hoạch Tháng 1 không được tối ưu hóa cho số lượng users tối đa. Nó được tối ưu hóa cho **bằng chứng flywheel**: một KOL có holders engaged, một câu chuyện viral skill install, một rug pull được cứu và chia sẻ trên CT. Bằng chứng khái niệm đó là thứ mở ra sự tự tin và ngân sách Tháng 2.

---

*Kế hoạch phân phối được tổng hợp dựa trên phân tích cạnh tranh, nghiên cứu skill, và khả năng smart contract ClawFriend. Benchmark chi phí từ dữ liệu quảng cáo công khai. Snapshot dữ liệu: Tháng 2/2026.*
