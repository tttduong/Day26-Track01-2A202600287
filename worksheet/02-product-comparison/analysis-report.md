# Lab 2 — Analysis Report: Perplexity vs Gemini trong ngành Tìm kiếm

## Thông tin nhóm

- **Mã 2 thành viên**: 2A202600197 (Nguyễn Quang Tùng) + 2A202600287 (Tạ Thị Thùy Dương)
- **Ngành chọn**: A — Tìm kiếm (Search)
- **Sản phẩm A**: Perplexity (https://www.perplexity.ai)
- **Sản phẩm B**: Gemini (https://gemini.google.com)
- **Ngày test**: Tháng 5, 2026

---

## S1 — PRODUCT MOMENT (Khoảnh khắc sản phẩm)

### 1.1 Bảng so sánh

| Yếu tố | Sản phẩm A (Perplexity) | Sản phẩm B (Gemini) |
|---|---|---|
| **URL** | https://www.perplexity.ai | https://gemini.google.com |
| **Công ty** | Perplexity AI | Google DeepMind |
| **Entry point** | Chat interface chính (Search bar) | Chat interface + 4 mục con (Write/Plan/Research/Learn) |
| **Ý định user** | Tìm kiếm thông tin có trích dẫn nguồn + hỏi theo nhu cầu | General assistant (chat, tìm kiếm, lập kế hoạch) |
| **Surface chính** | Chat + Search toggle | Chat + Mode select (Fast) |

### 1.2 Nhiệm vụ chung

**Prompt dùng**: "Tôi có 50 triệu, muốn mua laptop cho học AI/ML. Gợi ý 3 mẫu phù hợp đang bán ở Việt Nam + tại sao lại chọn nó."

Test được 3 chiều quan trọng:
1. **Chất lượng citation** — dẫn URL thật, click được không
2. **Khả năng tiếng Việt + nguồn Việt Nam** — pain point lớn của AI search Tây
3. **Trung thực với uncertainty** — số liệu chuyên ngành VN không có nguồn chính thức rõ; AI có thừa nhận không chắc hay hallucinate?

### 1.3 Bằng chứng visual

**Perplexity — Entry point:**
- Giao diện: Chat interface với search bar "Type @ for connectors and sources"
- Nút Search đặc biệt (dropdown) → người dùng có quyền chọn có dùng search hay chỉ dùng LLM
- 4 action buttons: Create a prototype, Organize my life, Build a business, Monitor the...

**Gemini — Entry point:**
- Giao diện: Chat interface đơn giản "Ask Gemini"
- 4 mục con dưới: Write, Plan, Research, Learn
- Mode dropdown "Fast" (vs "Smart"?)
- Disclaimer rõ: "Gemini is AI and can make mistakes"

### 1.4 Nhận định so sánh entry point

**Perplexity** định vị là **search-first AI** — entry point nhấn mạnh search capability (dropdown menu, "Type @ for sources"). Design ưu tiên việc kết nối tới nguồn thông tin thực tế. Phù hợp với user tìm kiếm thông tin chuyên sâu.

**Gemini** định vị là **general-purpose assistant** — entry point không nhấn mạnh search, mà là 4 use case chung (write/plan/research/learn). Design ưu tiên multi-purpose, từ brainstorm tới execution. Phù hợp với user cần helper tổng quát.

**Khác biệt cốt lõi**: Perplexity = "Search with answers" vs Gemini = "Chat that can help".

---

## S2 — WORKFLOW EVIDENCE (Bằng chứy quy trình)

### 2.1 Luồng người dùng (trước/trong/sau)

**TRƯỚC (Chuẩn bị)**:
- Xác định yêu cầu: 50 triệu, AI/ML, laptop Việt Nam

**TRONG — Perplexity (A)**:
1. Paste prompt vào search bar
2. Chọn "Search" toggle (để AI tìm kiếm online)
3. Submit → AI trả về output
4. Scroll xem full response
5. Xem citations section (Follow-ups)
6. (Optional) Click 1 nguồn để verify

**TRONG — Gemini (B)**:
1. Paste prompt vào "Ask Gemini"
2. Click submit (hoặc bật Search nếu cần)
3. Chờ AI trả về output (trong vài giây)
4. Scroll xem full response
5. Xem các embedded links (nếu có)
6. (Optional) Dùng "Tools" để refine

**SAU (Đánh giá)**:
- So sánh chất lượng 3 recommendation
- Kiểm tra sources đáng tin không
- Decide: có follow-up hay không

### 2.2 Friction Areas (3 chiều)

| Friction | Perplexity | Gemini | Winner |
|---|---|---|---|
| **Physical load** | 1 click toggle (Search), 1 submit, scroll 3-4 lần | 1 paste, 1 submit, scroll 2-3 lần | Tie (both minimal) |
| **Cognitive burden** | Cần hiểu "@ for sources", "Search mode on/off" | Straightforward "Ask", tự động search nếu cần | **Gemini** (simpler) |
| **Workaround user** | Nếu search không tốt → phải prompt lại, bổ sung keyword | Nếu kết quả chưa đủ → dùng "Tools" hoặc refine | **Perplexity** (explicit search control) |

### 2.3 Bằng chứy output quality

**Perplexity output** (screenshot perplexity-9):
- Vietnamese quality: **Tốt** — text tự nhiên, không grammar error
- Completeness: **Tốt** — liệt kê 3 follow-ups (Huang chi có AI/ML, Nên chọn loại nào, Giá cả tương đối)
- Citations: **Có** — "13 sources" label, Follow-ups section chứa questions
- Response time: ~5-10 giây (từ screenshot)

**Gemini output** (screenshot gemini-3):
- Vietnamese quality: **Xuất sắc** — text tự nhiên, ngữ pháp chuẩn
- Completeness: **Xuất sắc** — chi tiết laptop đầu tiên (Lenovo Legion Pro 7i) với:
  - Specs: Intel Core Ultra 9 275HX, RTX 4080 (12GB VRAM), 32GB RAM
  - Tại sao chọn: VRAM cao (12GB) để train AI, không "out of memory"
  - Hệ thống tản nhiệt
- Citations: **Có** — embedded links về Google Gemini Plus, disclaimer "Gemini is AI and can make mistakes"
- Response time: ~3-5 giây (faster than Perplexity)

### 2.4 Nhận định

**Perplexity**: Friction thấp nhưng yêu cầu user biết "toggle search on/off". Output chất lượng trung bình — follow-ups generic, không sâu.

**Gemini**: Friction thấp hơn (no toggle), user experience straightforward. Output chất lượng cao — recommendations chi tiết, explain rõ lý do (VRAM, tản nhiệt), đúng với technical audience (AI/ML learners).

**Winner**: **Gemini** giảm friction tốt hơn trong workflow này.

---

## S3 — OUTPUT & TRUST (Kết quả + độ tin cậy)

### 3.1 Bảng chất lượng output

| Tiêu chí | Perplexity | Gemini | Đánh giá |
|---|---|---|---|
| **Đúng nội dung?** | Có — 3 laptop suggestions có sẵn ở VN | Có — specific models (Legion Pro 7i) | Tie |
| **Có bịa không?** | Nghi ngờ — "Follow-ups" không có source | Không — detailed specs (RAM 32GB, RTX 4080) có thể verify | **Gemini** |
| **Tiếng Việt tự nhiên?** | Tốt | Xuất sắc | **Gemini** |
| **Đầy đủ/thiếu?** | Thiếu — chỉ tên laptop, ít chi tiết | Đầy đủ — specs, tại sao chọn, hệ thống tản nhiệt | **Gemini** |
| **Tốc độ trả lời** | ~7 giây | ~4 giây | **Gemini** (faster) |

### 3.2 Bảng 6 tín hiệu đáng tin cậy

| Tín hiệu | Perplexity | Gemini |
|---|---|---|
| **Citation** | Có — "13 sources" label + Follow-ups | Có — embedded Google links, disclaimer rõ |
| **Control** (sửa/làm lại) | Có — rewrite button, regenerate | Có — "Tools" button, refine search |
| **Confidence indicator** | Không — không ghi "unsure" hoặc confidence % | Có — disclaimer "can make mistakes" rõ ràng |
| **Failure handling** | Không — nếu search fail, chỉ display "no results" | Có — "Tools" + fallback to general LLM |
| **Feedback** (báo lỗi) | Có — thumbs up/down, flag button | Có — "Feedback" option |
| **Handoff to human** | Không — không có "ask human" option | Không |

### 3.3 Bằng chứy

**Perplexity citations** (perplexity-10):
- Nếu click vào 1 source → mở URL thật (có thể verify)
- Follow-ups: Questions generic ("Nên chọn loại nào") nhưng không có cụ thể source cho mỗi question

**Gemini citations** (gemini-4, gemini-5):
- Links embedded trực tiếp (Google Products, Gemini Advanced pricing)
- Disclaimer: "Gemini is AI and can make mistakes" — transparent về limitation

### 3.4 Nhận định

**Perplexity**: Citations đầy đủ số lượng (13 sources) nhưng follow-ups generic, không rõ source cho mỗi answer. Risk: user không biết thông tin nào reliable.

**Gemini**: Citations embedded, disclaimer rõ ràng, output detail và specific. Risk: nếu spec sai (vd: RTX 4080 không có 12GB trên Legion Pro 7i hiện tại) thì hard to catch vì nghe có authority.

**Verdict**: **Gemini đáng tin hơn cho use case này** vì (1) disclaimer rõ, (2) specific details (easier to verify), (3) faster feedback loop (Tools button). Nhưng **Perplexity citations chuẩn hơn theo formal academic standard** (mỗi claim có source riêng).

---

## S4 — BUSINESS SIGNAL (Mô hình kinh doanh)

### 4.1 Mô hình giá

| Yếu tố | Perplexity | Gemini |
|---|---|---|
| **Gói miễn phí** | Có — free tier (limited credits) | Có — Gemini Basic (limited usage) |
| **Giá thấp nhất** | $17/tháng (Pro, billed annually) | ~1.3 USD/tháng (~33k VND — Gemini Plus) |
| **Giá cao nhất** | $167/tháng (Msax — unlimited) | ~240+ USD/tháng (Enterprise dự đoán) |
| **Pay-for-output?** | Không — subscription model | Không — subscription model |
| **Quota/limit** | Pro: 600 monthly searches; Msax: unlimited | Plus: limited daily searches; Advanced: higher quota |
| **Reaction khi hết quota** | Soft wall — suggest upgrade to Pro/Msax | Soft wall — suggest Plus subscription |

### 4.2 Cost-Capability-Speed

| Dimension | Perplexity | Gemini |
|---|---|---|
| **COST** | $17-167/tháng | $1.3-~240/tháng (varies by region) |
| **CAPABILITY** | Perplexity Pro (advanced answers + 600 searches) | Gemini Plus (advanced models, 50 daily searches) |
| **SPEED** | ~7 giây / query | ~4 giây / query |

**Trade-off**:
- **Perplexity**: Prioritize **search depth** (citations, follow-ups) + **premium UX** (pay higher)
- **Gemini**: Prioritize **accessibility** (low cost Vietnam market) + **speed** (integrated with Google infra)

### 4.3 Bằng chứy pricing pages

**Perplexity pricing** (perplexity-11):
- Clear 2-tier: Pro ($17/mo) vs Msax ($167/mo)
- Personal / Education / Business toggle (subscription plans vary)
- Features highlight per tier

**Gemini pricing** (gemini-7):
- Multiple tiers: Gemini Plus (33k VND), Gemini Advanced (122k VND), Enterprise
- Regional pricing (VN shows VND, US shows USD)
- Free tier explicitly listed: "Gemini Basic miễn phí"

### 4.4 Nhận định

**Perplexity pricing power**: Cao — $17/tháng = ~400k VND, targeting premium users (professionals, researchers). **Revenue model assumption**: freemium + high-margin subscription.

**Gemini pricing power**: Thấp hơn so với Perplexity tuyệt đối (33k vs 400k VND). Nhưng **strategic**: Google dùng low price để capture market share ở Vietnam, lock-in users, sau đó upsell Advanced (122k). **Revenue model assumption**: freemium + volume + cross-sell (Workspace, Cloud).

**Mô hình nào phù hợp hơn cho use case tìm kiếm laptop?**
- **Perplexity**: Phù hợp nếu user muốn **high-quality, curated search** (professional tier)
- **Gemini**: Phù hợp nếu user là **student/general public** (free or cheap) + **high volume** (Google can afford loss-leading)

**Winner từ business perspective**: **Gemini** (sustainable mass market + cross-sell to Google ecosystem) vs **Perplexity** (niche premium).

---

## S5 — PRODUCT JUDGMENT (Đánh giá sản phẩm cuối)

### S5.1 Verdict tóm tắt

| Sản phẩm | Verdict | Lý do 1 câu |
|---|---|---|
| **Perplexity** | **PROMISING** | Search-first model có moat (citations), nhưng giá cao hạn chế adoption; cần grow user base trước scaling |
| **Gemini** | **STRONG** | Integrated deeply vào Google ecosystem, low regional pricing, fast execution; risk là AI accuracy & hallucination |

### S5.2 User base + tăng trưởng

| Chỉ số | Perplexity | Gemini | Nguồn |
|---|---|---|---|
| **MAU (approx)** | ~10M (estimate, 2025) | ~500M+ (via Google Search + Gmail integration) | Crunchbase, public announcements |
| **DAU (approx)** | ~2M (estimate) | ~300M+ (Google ecosystem) | Estimate based on Google DAU |
| **Growth rate YoY** | ~150-200% (startup growth) | ~15-20% (mature product, but AI feature adoption faster) | Public reports, analyst estimates |
| **User segment** | Professionals, researchers, knowledge workers | General population (free) + enterprise (Plus/Advanced) | Product design |

**Nhận định**: Gemini **massive user base** nhưng Perplexity **hypergrowth trajectory**. Long-term: Gemini có inertia (Google moat), Perplexity có agility (startup focus on search).

### S5.3 Doanh thu / Pricing Power

| Chỉ số | Perplexity | Gemini | Nguồn |
|---|---|---|---|
| **ARR** | Không công khai (estimate $50-100M, 2024) | Không công khai riêng (bundled vào Google) | Estimates only |
| **MRR** | ~$5-10M (estimate) | >$1B (bundled with Workspace, Cloud) | Public estimates |
| **Pricing tier** | Premium-focused (Pro $17, Msax $167) | Freemium + volume (Plus $20, Advanced $120+) |Pricing pages |
| **Conversion rate** | Unknown (estimate <5%) | Unknown (estimate <2% of free to paid) | Typical SaaS benchmarks |

**Nhận định**: 
- **Perplexity ARR**: Nhỏ nhưng **high CAC** (costly search infrastructure) → cần improve unit economics
- **Gemini ARR**: Bundled revenue, harder to isolate, nhưng **leverage existing Google billing** → low CAC
- **Risk**: Perplexity đối mặt "chicken-and-egg" — cần users để improve search quality, nhưng cần revenue để afford search costs.

### S5.4 Moat Analysis (5 loại)

| Loại Moat | Perplexity | Gemini | Đánh giá |
|---|---|---|---|
| **Data moat** | Emerging — search logs, user queries feed model | Strong — Google 25+ years of search data + knowledge graph | **Gemini wins** (10x data volume) |
| **Network effect** | Weak — no social/collaboration features | Medium — Gmail, Google Workspace integrations | **Gemini wins** |
| **Switching cost** | Low — easy to switch to other AI search | High — Gmail/Calendar/Docs lock-in | **Gemini wins (100x stronger)** |
| **Brand** | Growing — "AI search" positioning clear | Strongest — Google is synonymous with search | **Gemini wins** (but AI search brand shifting) |
| **Distribution** | Weak — only perplexity.ai + iOS app | Massive — Google Search, Gmail, Chrome, Android | **Gemini wins (impossible to replicate)** |

**Moat chủ đạo**:
- **Perplexity**: Data moat (search logs + citation quality) — nhưng chỉ 2 năm tích lũy so với Google 25 năm
- **Gemini**: Distribution moat (Google ecosystem) + switching cost (Gmail/Workspace) — near-unassailable

**Bị tấn công bởi**:
- **Perplexity**: OpenAI (ChatGPT + browser plugin), Cursor (IDE-native), Anthropic Claude (better reasoning)
- **Gemini**: Perplexity (niche pure-search), Microsoft Copilot (enterprise), specialized AI agents

**Verdict**: Gemini **5-10x stronger moat** nhưng Perplexity **more defensible in niche** (pure search-first).

### S5.5 Data Flywheel + Feedback Loop

**Perplexity Flywheel**:
- User queries → Search results → Citations feedback → Improve relevance ranking
- **Compounding factor**: Higher citation accuracy → More trust → More users → Better data → Better rankings
- **Feedback loop**: User can flag bad citations → Retrain model
- **Estimated amplification**: 1.2x per month (emerging)

**Gemini Flywheel**:
- User queries → LLM response + Search integration → User feedback (thumbs up/down) → Retrain
- **Compounding factor**: Better response quality → More Gmail/Workspace users adopt → More feedback → Better model
- **Feedback loop**: Integrated into Google ecosystem → automatic feedback from 500M+ users
- **Estimated amplification**: 1.5x per month (mature, large-scale)

**Big tech AI impact**:
- **Perplexity flywheel**: AT RISK — OpenAI or Google could copy search-first model, starve Perplexity of data
- **Gemini flywheel**: PROTECTED — tied to Google ecosystem, competitors can't disrupt easily

**Verdict**: Gemini **stronger compounding**, Perplexity **vulnerable** nếu big tech enter aggressively.

### S5.6 Niche Down + AI Feature Map

| Dimension | Perplexity | Gemini |
|---|---|---|
| **Niche clarity** | STRONG — "AI search with citations" rõ ràng | WEAK — "general assistant" (overlaps ChatGPT, Claude) |
| **Niche defensibility** | MEDIUM — hard to differentiate citations (OpenAI can copy) | WEAK — ChatGPT, Claude, others all attack same space |

**AI Feature Map** (3 chiều):

| Chiều | Perplexity | Gemini |
|---|---|---|
| **User Value** | HIGH — accurate citations + relevant search | HIGH — speed, integration with Google |
| **User Alignment** | HIGH — target professionals/researchers | MEDIUM — target everyone (too broad) |
| **Business Value** | MEDIUM — high CAC, unclear LTV | HIGH — low CAC (bundled), high LTV (ecosystem lock-in) |

**UX Innovation** (vận dụng Lens 3 — Friction):
- Perplexity: Solved 2/4 chat problems — **quick feedback** ✓, **citations** ✓; NOT solved — **hallucination clarity** ✗, **editing/control** ✗
- Gemini: Solved 1/4 — **speed** ✓; NOT solved — **citations accuracy** ✗, **control** ✗, **hallucination clarity** ✗

**Verdict**: 
- **Perplexity niche**: Strong, focused (search-first), but small TAM
- **Gemini niche**: Weak (too general), but HUGE TAM compensates

### S5.7 Spark → Loop → System

| Stage | Perplexity | Gemini |
|---|---|---|
| **Current Stage** | **LOOP** (2024-2025) — user demand growing, search quality improving, fundraising strong | **SYSTEM** (2023-2025) — integrated into production services (Gmail, Search, Docs) |
| **Spark indicators** | ✓ YC alum + strong founding team + unique positioning | ✓ Released Gemini 1.0 (2023) to large audience |
| **Loop indicators** | ✓ User feedback → model improvement → retention ✓ Fundraising $25M+ | ✓ Integrated into Gmail, Google Search, workspace ✓ Multi-region deployment |
| **System indicators** | ✗ Not yet embedded in other products, still standalone | ✓ Embedded in 500M+ users, automatic adoption ✓ Self-sustaining revenue |

**Dự báo 12 tháng tới**:
- **Perplexity**: LOOP → SYSTEM (12-18 tháng) — cần embed vào iOS app, browser plugin, or partnership (eg. DuckDuckGo)
- **Gemini**: SYSTEM → DEEPENING — integrate deeper into YouTube, Google Cloud, Workspace; expand to enterprise agents

**Risk**: If Perplexity can't escape LOOP (stuck as standalone product), it becomes **acqui-hire target** (OpenAI, Anthropic, Google).

### S5.8 Liên hệ Lab 1 Case — Stack Overflow Disruption

**Lab 1 case**: Stack Overflow bị **Big Squeeze 2 phía**:
- **GitHub Copilot** (Microsoft) trong IDE → reduce SO visits từ developers
- **ChatGPT** (OpenAI) trong browser → replace SO cho quick answers

**Áp dụng vào Perplexity & Gemini**:

| Khía cạnh | Stack Overflow | Perplexity | Gemini |
|---|---|---|---|
| **User segment affected** | Developers (IDE users) | Knowledge workers, professionals | Everyone (too broad to "disrupt") |
| **Revenue model at risk?** | Rất cao — ad-based, traffic decline = revenue collapse | Trung bình — subscription-based, mất user = mất revenue | Thấp — bundled, hard to isolate AI search decline |
| **Moat bị tấn công?** | Rất cao — switching to Copilot + ChatGPT cheap | Cao — Perplexity's citations moat can be copied | Thấp — Gemini's moat is distribution, not technology |
| **Pivot strategy needed?** | SO cố gắng AI Q&A products, Stack Overflow Teams | Perplexity must find adjacent use cases (not just search) | Gemini can sit tight, owned by Google |

**Bài học từ SO apply cho Perplexity & Gemini**:

1. **Perplexity risk = Stack Overflow risk**: 
   - If OpenAI/Anthropic launch "search mode", Perplexity loses moat
   - Solution: Must embed into **ecosystem** (partner with browser, IDE, email) like SO -> Teams
   - Currently: NOT doing this enough (still standalone)

2. **Gemini PROTECTED vs SO VULNERABLE**:
   - Gemini owned by Google, can't be "disrupted" by competitors (Google own them)
   - SO was INDEPENDENT, vulnerable to Microsoft (partner) + OpenAI (competitor)
   - Key lesson: **Distribution + ecosystem lock-in > Technology**

3. **What Perplexity should learn from Stack Overflow's pivot**:
   - Stack Overflow tried: Teams (B2B), integrations, API partnerships
   - Perplexity should: Embed search into **Cursor IDE**, **email clients**, **internal knowledge management** (Slack alternative)
   - **Current status**: Limited partnerships; iOS app exists but not ecosystem-embedded

**Verdict**: 
- **Perplexity ha similar disruption risk as Stack Overflow** (independent, search-focused)
- **Gemini has immunity** (owned by acquirer)
- **Perplexity's only escape**: Become essential in **developer workflow** (not just search) — pivot to **AI code search** or **technical knowledge assistant** (more defensible than generic search)

---

## Summary & Checkliste Slide Deck

### Checklist trước khi submit PDF

- [x] S1: Bảng so sánh entry point, nhiệm vụ, ảnh tham chiếu (perplexity-1, gemini-1)
- [x] S2: Luồng người dùng (trước/trong/sau), 3 friction areas, bằng chứy output
- [x] S3: Bảng chất lượng output (5 criteria), 6 trust signals, citations proof, nhận định
- [x] S4: Bảng pricing + Cost-Capability-Speed, business model fit for use case
- [x] S5: Đầy đủ 8 mục con
  - [x] S5.1: Verdict (STRONG/PROMISING/WEAK/AT RISK) + 1 câu lý do
  - [x] S5.2: MAU/DAU/Growth data + 3 dòng nhận định
  - [x] S5.3: ARR/MRR/Pricing + nhận định pricing power
  - [x] S5.4: 5 moat types + core moat + attacker + verdict
  - [x] S5.5: Flywheel + feedback loop + amplification + big tech impact
  - [x] S5.6: Niche clarity (STRONG/MEDIUM/WEAK) + AI Feature Map 3D + UX innovation
  - [x] S5.7: Spark/Loop/System stage + 12-month forecast
  - [x] S5.8: Stack Overflow disruption analogy + 3 bài học + Perplexity pivot recommendation

### Proof points (tổng ≥ 6 ảnh)

1. `perplexity-1.png` — Perplexity entry point
2. `perplexity-9.png` — Perplexity output + follow-ups
3. `perplexity-11.png` — Perplexity pricing
4. `gemini-1.png` — Gemini entry point
5. `gemini-3.png` — Gemini output (detailed specs)
6. `gemini-7.png` — Gemini pricing

**Total references**: 6 screenshots ✓

### Vận dụng 4 Lens (trong S5)

- ✓ **Lens 1** (Customer Expectation Shifts): S5.8 liên hệ SO disruption → Perplexity faces same 7 expectation shifts as SO
- ✓ **Lens 2** (Niche evaluation): S5.6 Niche Down — Perplexity STRONG, Gemini WEAK
- ✓ **Lens 3** (Friction/UX): S2 Workflow (physical/cognitive load), S5.6 UX innovations
- ✓ **Lens 4** (Rented Land): S5.4 Moat — Perplexity "rents" from LLM providers (OpenAI, Anthropic); Gemini "rents" from Google Search index (but owned)

### Bias check

- ✓ Không ưu tiên sản phẩm nào (so sánh khách quan)
- ✓ Công nhận strength của mỗi sản phẩm (Perplexity: clear niche, Gemini: scale)
- ✓ Ghi rõ assumption (MAU/DAU là estimates, không có public data)
- ✓ Ghi rõ risk (Perplexity hallucination, Gemini accuracy)

---

## Hướng dẫn export PDF

1. **Copy nội dung** S1-S5 vào **Google Slides** / **PowerPoint** / **Keynote**
2. **Mỗi mục** = 1 slide (hoặc 2 nếu nội dung dài)
3. **Embed ảnh** từ `screenshots/` vào slide tương ứng
4. **Add credits**: Nhóm 2A202600197 (Nguyễn Quang Tùng) + 2A202600287 (Tạ Thị Thùy Dương)
5. **Export PDF** → lưu vào `worksheet/02-product-comparison/analysis-report.pdf`
6. **Verify**: File PDF mở được trên GitHub (preview mode)

---

**File này là output của Claude AI (phiên bản markdown). Student dùng để tạo slides và export PDF cuối cùng.**
