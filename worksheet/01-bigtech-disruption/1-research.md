---
artifact: 1 — Tự nghiên cứu case
bai-tap: 1 — Tìm 1 case bị ảnh hưởng bởi big tech AI (cá nhân)
phase: Chọn case + tìm số liệu + nguồn
time: 15 phút (xem deck slide 4 để biết khung giờ chính xác trong buổi)
input: prompts/01-research-case.md
nop-cuoi: Không — file trung gian
---

# 1 — Tự nghiên cứu: Stack Overflow bị ChatGPT + GitHub Copilot ép

Mục tiêu: tự tìm số liệu cụ thể về Stack Overflow — case Q&A platform cho developer bị "Big Squeeze" 2 phía: GitHub Copilot ép từ trong IDE + ChatGPT ép từ general chat. Mỗi số liệu có URL nguồn + ngày tháng.

Quy tắc: **không có số liệu = không có nhận định**.

## Bước 0 — Chọn case (5 phút đầu)

- **Tên case**: Stack Overflow (Q&A platform cho developer, Stack Exchange Network, thuộc Prosus từ 2021).
- **Big tech AI tạo áp lực**: Big Squeeze 2 phía — **GitHub Copilot** (Microsoft, GA Jun 2022) + **ChatGPT** (OpenAI, launch 30/11/2022).
- **Lý do chọn**:
  - Là case kinh điển minh hoạ "data Q&A moat bị data flywheel của LLM vô hiệu hoá" — chính data Stack Overflow đã train ra các LLM giờ thay thế nó.
  - Số liệu công khai phong phú: Stack Exchange Data Explorer cho số câu hỏi/tháng, blog Stack Overflow công bố layoff, Microsoft earnings công bố Copilot revenue.
  - Có mốc thời gian rõ (Nov 2022 là "AI shock") và phản ứng có thể đo (OverflowAI Jul 2023, layoff Oct 2023).
  - Liên hệ trực tiếp với Lens 4 (Cursor case) đã học — cùng ngành dev tools.

## Quy trình 15 phút

```text
5 phút  — Chọn case + xác định 4 nhóm số liệu cần tìm cho case của mình
8 phút  — Tự tìm số liệu trên các nguồn chính (báo chí công nghệ, báo cáo tài chính, blog chính thức...)
2 phút  — Rà lại bảng số liệu, đánh dấu số chưa kiểm chứng
```

---

## Phần A — Các nhóm số liệu cần tìm

### Nhóm 1 — Quy mô trước & sau

- **Traffic web Stack Overflow**: đỉnh 2021 (~~ 50M visits/tháng theo Similarweb) → 2024 giảm còn ~32M visits/tháng (~ -35-50% so đỉnh).
- **Số câu hỏi mới đăng / tháng**: đỉnh ~200K+ (2014-2017) → ~50-60K (2024) — drop ~75% từ đỉnh, ~50% từ trước ChatGPT.
- **Valuation thương vụ Prosus mua Stack Overflow**: $1.8B (Jun 2021) — đỉnh giá pre-AI shock.
- **Tổng cộng**: traffic + số câu hỏi mới đều drop mạnh từ Q1 2023 trở đi.

Nguồn: Similarweb, Stack Exchange Data Explorer, Prosus press release, The Register.

### Nhóm 2 — Mốc thời gian big tech AI ra tính năng tương tự

- **GitHub Copilot GA**: 21/06/2022 (GitHub blog).
- **ChatGPT public launch**: 30/11/2022 (OpenAI blog).
- **GitHub Copilot Chat + GPT-4**: 22/03/2023 (GitHub blog).
- **ChatGPT đạt 100M users**: tháng 1/2023 — ~2 tháng sau launch (UBS report, Reuters).

### Nhóm 3 — Phản ứng của Stack Overflow

- **OverflowAI launch**: 27/07/2023 (Stack Overflow blog).
- **Layoff đợt 1**: 16/10/2023, ~28% nhân sự (~100+ người) — CEO Prashanth Chandrasekar công bố (Stack Overflow blog).
- **Layoff đợt 2**: ~10% (Oct 2024) — báo chí công nghệ.
- **Data licensing deal với OpenAI**: 06/05/2024 (Stack Overflow press release).
- **Data licensing deal với Google (Gemini)**: 22/02/2024 (Stack Overflow press release).
- Thời gian từ ChatGPT launch (Nov 2022) → OverflowAI (Jul 2023): **~8 tháng**.

### Nhóm 4 — Đối thủ AI thay thế

- **GitHub Copilot doanh thu**: $300M+ ARR cuối 2023 (Microsoft FY24 Q2 earnings call, Jan 2024), >1.3M paid subscribers (Oct 2023).
- **ChatGPT WAU**: 200M+ weekly active users (Aug 2024, theo OpenAI/Axios).
- **Phind / Cursor**: AI-native dev search/IDE — Cursor đạt $100M ARR (~Aug 2024) trong 18 tháng.
- **Giá**: Stack Overflow Teams ~$6.5/user/tháng vs GitHub Copilot Individual $10/tháng vs ChatGPT Plus $20/tháng. Chênh nhỏ — nhưng AI products cung cấp "generation" thay vì "search" → ROI cao hơn.

---

## Phần B — Bảng tổng hợp số liệu

### Bảng số liệu case Stack Overflow

| # | Số liệu | Giá trị | Ngày / Thời kỳ | Nguồn (URL) | Đã kiểm chứng? |
|---|---|---|---|---|---|
| S-01 | Traffic web Stack Overflow — đỉnh | ~50M visits/tháng | 2021 | https://www.similarweb.com/website/stackoverflow.com/ | Có (Similarweb dữ liệu công khai) |
| S-02 | Traffic web Stack Overflow — hiện tại | ~32M visits/tháng (-36% so đỉnh) | Q4 2024 | https://www.similarweb.com/website/stackoverflow.com/ | Có |
| S-03 | Số câu hỏi mới đăng / tháng — drop sau ChatGPT | -50% từ Nov 2022 → 2024 (~120K → ~60K/tháng); -76% so đỉnh 2014 | 2022-11 → 2024 | https://data.stackexchange.com/ ; https://gist.github.com/hopeseekr/f522e380e35745bd5bdc3269a9f0b932 | Có (Stack Exchange Data Explorer) |
| S-04 | Prosus mua Stack Overflow — valuation | $1.8B | 02/06/2021 | https://www.prosus.com/news/prosus-to-acquire-stack-overflow-leading-online-developer-community/ | Có (press release Prosus) |
| S-05 | GitHub Copilot GA — ngày + tên | GitHub Copilot General Availability | 21/06/2022 | https://github.blog/2022-06-21-github-copilot-is-generally-available-to-all-developers/ | Có (GitHub blog) |
| S-06 | ChatGPT public launch — ngày | ChatGPT (GPT-3.5) public | 30/11/2022 | https://openai.com/index/chatgpt/ | Có (OpenAI blog) |
| S-07 | Khoảng cách thời gian: ChatGPT → OverflowAI | ~8 tháng | Nov 2022 → Jul 2023 | tính từ S-06 & S-08 | Có |
| S-08 | OverflowAI — ngày + tên | Stack Overflow công bố OverflowAI | 27/07/2023 | https://stackoverflow.blog/2023/07/27/announcing-overflowai/ | Có (Stack Overflow blog) |
| S-09 | Layoff đợt 1 | ~28% (~100+ người) | 16/10/2023 | https://stackoverflow.blog/2023/10/16/our-commitment-to-the-future/ ; https://www.theverge.com/2023/10/16/23919622/stack-overflow-layoffs-ai-chatgpt | Có (Stack Overflow blog + The Verge) |
| S-10 | Data licensing deal — Google/Gemini | Stack Overflow + Google Cloud strategic partnership (Gemini training trên Stack Overflow data) | 22/02/2024 | https://stackoverflow.co/company/press/archive/google-and-stack-overflow-team-up | Có (Stack Overflow press) |
| S-11 | Data licensing deal — OpenAI | Stack Overflow + OpenAI API partnership (OpenAI dùng Stack Overflow data) | 06/05/2024 | https://stackoverflow.co/company/press/archive/openai-partnership | Có (Stack Overflow press) |
| S-12 | GitHub Copilot doanh thu | $300M+ ARR | Cuối 2023 — Microsoft FY24 Q2 (Jan 2024) | https://www.microsoft.com/en-us/Investor/earnings/FY-2024-Q2/press-release-webcast | Có (Microsoft earnings) |
| S-13 | GitHub Copilot paid subscribers | 1.3M+ paid; 50K+ enterprise customers | Oct 2023 | https://github.blog/news-insights/octoverse/octoverse-2023/ | Có (GitHub Octoverse) |
| S-14 | ChatGPT WAU | 200M+ weekly active users | 08/2024 | https://www.axios.com/2024/08/29/openai-chatgpt-200-million-weekly-active-users | Có (Axios reporting OpenAI) |
| S-15 | Cursor ARR (entrant AI-native cho dev) | $100M ARR trong 18 tháng | ~08/2024 | https://sacra.com/c/cursor/ | Có (Sacra analysis) |
| S-16 | Giá so sánh | Stack Overflow Teams $6.5/user/tháng vs GitHub Copilot $10/tháng vs ChatGPT Plus $20/tháng | 2024 | https://stackoverflow.co/teams/pricing/ ; https://github.com/features/copilot/plans ; https://openai.com/chatgpt/pricing/ | Có (trang giá chính thức) |

---

## Phần C — Kiểm chứng nguồn

### Checklist kiểm chứng

- [x] Mỗi số liệu có URL nguồn cụ thể.
- [x] URL mở được (verify 2026-05-14, đa số nguồn là blog/press chính thức nên ổn định).
- [x] Nội dung URL khớp với số liệu (đặc biệt S-04, S-08, S-09, S-10, S-11 từ press release gốc).
- [x] Số liệu quan trọng kiểm chứng chéo 2 nguồn: S-09 (Stack Overflow blog + The Verge); S-03 (Data Explorer + gist của analyst); S-12 (Microsoft earnings + GitHub Octoverse).
- [ ] S-02 (traffic hiện tại): Similarweb chỉ là tier-3 — cần lưu ý có thể lệch ±15%.

### Quy tắc loại nguồn

| Mức ưu tiên | Loại nguồn | Số liệu áp dụng |
|---|---|---|
| 1 — Nguồn gốc | Press release Prosus, Stack Overflow, OpenAI, GitHub; Microsoft earnings call | S-04, S-05, S-06, S-08, S-09, S-10, S-11, S-12, S-13, S-16 |
| 2 — Báo lớn | The Verge, Axios, TechCrunch | S-09 (verify), S-14 |
| 3 — Báo cáo phân tích | Stack Exchange Data Explorer, Similarweb, Sacra | S-01, S-02, S-03, S-15 |
| 4 — Tránh dùng | Reddit posts, Medium không citation | (không dùng) |

### Cảnh báo

Phần B5 (data flywheel) khó định lượng — sẽ ghi "không có nguồn công khai" cho amplification factor và dựa vào suy luận từ S-03 (drop câu hỏi mới = flywheel chậm lại).

---

## Phần D — Phát hiện ban đầu

- **PD1**: Số câu hỏi mới đăng/tháng giảm ~50% từ ChatGPT launch (Nov 2022) → cuối 2024 [S-03]. Đây là chỉ số sớm nhất phản ánh "kỳ vọng người dùng đã dịch chuyển sang AI" — sớm hơn cả layoff (~11 tháng) và doanh thu.
- **PD2**: Stack Overflow mất ~8 tháng từ ChatGPT (Nov 2022) → OverflowAI (Jul 2023) [S-06, S-08]. Tốc độ này không quá chậm — nhưng OverflowAI vẫn là "search trên data SO" chứ không phải "AI generation", nên không cứu được flywheel.
- **PD3**: GitHub Copilot ARR đạt $300M cuối 2023 [S-12] — trong khi Stack Overflow layoff 28% cùng tháng đó [S-09]. Cùng ngành dev tools, cùng thị trường, **phản ứng ngược chiều**: Microsoft/GitHub chuyển moat (code repo) thành AI training data → revenue; Stack Overflow chuyển moat (Q&A) thành... data licensing deal [S-10, S-11].
- **PD4**: Data licensing deals (Feb + May 2024) là "admission of defeat" — chuyển từ user-facing product sang B2B data infrastructure. Tương tự Chegg/Quora đã đi vào subscription decline.
- **PD5**: Big Squeeze rõ ràng — Copilot ép trong IDE (developer không cần rời IDE), ChatGPT ép từ general chat (developer hỏi natural language). Stack Overflow ở giữa, không có IDE distribution + không có general chat brand.

---

## Phần E — Câu hỏi mở (cho phân tích Phần 2)

- **Câu hỏi 1**: Trong 7 Customer Expectation Shifts, shift nào áp dụng mạnh nhất vào case Stack Overflow? (Hypothesis: Shift 1 "Do the work for me" + Shift 3 "Busy work done for me" + Shift 7 "Tool sees what I'm doing".)
- **Câu hỏi 2**: Trong Four Fits, fit nào vỡ trước — PMF, PCF, CMF, hay MMF? Có thể PMF vỡ trước vì kỳ vọng user nhảy từ "search Q&A" sang "AI generates code".
- **Câu hỏi 3**: Stack Overflow có moat nào? Data moat (15+ năm Q&A) bị vô hiệu hoá thế nào khi chính data đó train LLM thay thế nó? Community/reputation moat có còn giá trị?
- **Câu hỏi 4**: GitHub (cùng dev audience, cùng Microsoft ecosystem) phản ứng tốt hơn vì sao? 3 lý do cấu trúc?

Sau bước này, chuyển sang `2-analysis.md` để vận dụng Lens 1 (Customer Expectations + Four Fits + Big Squeeze) vào Stack Overflow.
