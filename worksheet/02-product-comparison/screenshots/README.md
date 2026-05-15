# Folder screenshots — hướng dẫn đặt tên file (tuỳ chọn)

Folder này là phần freestyle của Lab 2. Sản phẩm chính của Lab 2 là `analysis-report.pdf` (slide deck nhóm export PDF — bắt buộc) ở thư mục cha. Folder `screenshots/` này dùng khi nhóm muốn lưu ảnh gốc ở độ phân giải đầy đủ để người chấm tra cứu.

## Quy tắc đặt tên

```text
product-[A|B]-[số thứ tự]-[mô tả ngắn].png
```

## Ví dụ tên file

| File | Nội dung |
|---|---|
| `product-A-1-entry.png` | Giao diện đầu của sản phẩm A — trang chủ hoặc màn hình đầu |
| `product-A-2-input.png` | Sau khi nhóm nhập câu hỏi/yêu cầu |
| `product-A-3-output.png` | Kết quả AI trả về |
| `product-A-4-source.png` | Phần dẫn nguồn (nếu có) |
| `product-A-5-pricing.png` | Trang giá / gói trả phí |
| `product-A-6-limit.png` | Khi hết quota / paywall xuất hiện (nếu gặp) |
| `product-B-1-entry.png` | Tương tự cho sản phẩm B |
| `product-B-2-input.png` | ... |
| ... | ... |

## Yêu cầu

- Folder này tuỳ chọn — yêu cầu bắt buộc là `analysis-report.pdf` ở thư mục cha.
- Khuyến khích: lưu ít nhất 6 ảnh gốc (3 / sản phẩm: entry, input, output) để người chấm có thể đối chiếu khi cần.
- 3 ảnh khuyến khích thêm / sản phẩm: source (dẫn nguồn), pricing (giá), limit (giới hạn).

## Cho D27 (tùy chọn cho D26, bắt buộc cho D27)

Thêm prefix `d27-`:

| File | Nội dung |
|---|---|
| `d27-product-A-pricing-full.png` | Trang giá đầy đủ (cuộn toàn bộ) |
| `d27-product-A-revenue-source.png` | Báo cáo doanh thu / ARR / MAU công khai (nếu tìm được) |

## Định dạng

- Ưu tiên `.png` để giữ chất lượng văn bản.
- `.jpg` cũng chấp nhận nếu file nặng.
- Tránh `.heic`, `.webp` (một số trình duyệt khó xem).

## Kích thước

- Mỗi ảnh < 2MB nếu có thể.
- Nếu ảnh full-page lớn, có thể nén bằng <https://tinypng.com> trước khi commit lên GitHub.

## Lưu ý

- Trước khi commit lên GitHub, kiểm tra ảnh không chứa thông tin cá nhân (email, số điện thoại, mã đăng nhập).
- Nếu ảnh có thông tin tài khoản, dùng công cụ blur (Awesome Screenshot, Cleanshot, macOS Markup) để che trước.

# Screenshots for Product Comparison

This folder contains screenshots for the comparison between **Perplexity** and **Gemini** based on the test prompt:

> "Tôi có 50 triệu, muốn mua laptop cho học AI/ML. Gợi ý 3 mẫu phù hợp đang bán ở Việt Nam + tại sao lại chọn nó."

## Screenshot Naming Convention

- **Perplexity** — 11 ảnh (`perplexity-1.png` … `perplexity-11.png`):
  - `perplexity-1.png` — Home page before entering the prompt.
  - `perplexity-2.png` — After pasting the prompt, before submitting.
  - `perplexity-3.png` → `perplexity-8.png` — Scrolling through full response (6 screenshots).
  - `perplexity-9.png` — Results with full citations.
  - `perplexity-10.png` — Clicking on one cited source to verify.
  - `perplexity-11.png` — Pricing page of Perplexity.

- **Gemini** — 8 ảnh (`gemini-1.png` … `gemini-8.png`):
  - `gemini-1.png` — Home page of Gemini (Search toggle enabled if available).
  - `gemini-2.png` — After pasting the prompt.
  - `gemini-3.png` → `gemini-6.png` — Scrolling through full response (4 screenshots).
  - `gemini-7.png` → `gemini-8.png` — Pricing page of Gemini.

## Notes

- Ensure the prompt is identical for both products.
- Capture screenshots immediately after the first response.
- Include captions with date, time, and subscription plan used.
- Verify at least one source by clicking on it for trust evaluation.
