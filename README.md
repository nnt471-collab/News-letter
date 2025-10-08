# News-letter (AgriS Digest)

Trang điểm tin nội bộ cho ngành Nông nghiệp TTC AgriS, xây dựng bằng Jekyll + GitHub Pages.

## Cấu trúc thư mục

- `_months/`: Các bản tin tháng. File mẫu `YYYY-MM.md` với front matter `layout: month`, `date`, `period`, `updated`, `org`.
- `_weeks/`: (Tùy chọn) các bản tin tuần. File cần front matter `layout: week` và có thể khai báo mảng `kpis`.
- `_includes/`: Các component tái sử dụng như thẻ KPI (`stat.html`) và tooltip nguồn (`tooltip.html`).
- `_layouts/`: Template cho từng loại ấn phẩm (`month.html`, `week.html`).
- `index.html`: Trang tổng quan, gom dữ liệu từ hai collection.

## Quy trình thêm bản tin

1. Tạo file Markdown trong `_months/` hoặc `_weeks/` với cú pháp front matter phù hợp.
2. Điền nội dung chính bằng Markdown (có thể dùng Mermaid code block).
3. Commit & push, GitHub Pages sẽ tự build và hiển thị.

> ⚠️ Lưu ý: `_config.yml` đã bật `future: true`, vì vậy các bản tin đặt ngày trong tương lai vẫn được build để tiện chuẩn bị trước.

## Chạy thử cục bộ

Cần Ruby & Bundler:

```bash
bundle install
bundle exec jekyll serve
```

Sau đó truy cập `http://localhost:4000/News-letter/`.

