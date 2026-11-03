# E-commerce UI Improvement – Paula's Choice Việt Nam

Bài tập cá nhân môn **Phát triển ứng dụng WEB/TMĐT** (UEH).
- Buổi 1: khảo sát website và cải tiến thanh tìm kiếm ở Header.
- **Buổi 2 (HTML & CSS)**: tiếp tục trên cùng website, tập trung hoàn thiện **khu vực danh sách 4 sản phẩm**.

## 1. Giới thiệu bài tập
Trang HTML5/CSS3 thuần mô phỏng trang chủ cải tiến của Paula's Choice Việt Nam. Buổi 2 áp dụng: HTML5 có ngữ nghĩa, CSS selector, Box Model, Flexbox, CSS Grid, hiệu ứng hover/focus và kiểm tra giao diện.

## 2. Website tham khảo và khu vực đã cải tiến
- Website tham khảo: Paula's Choice Việt Nam – https://paulaschoice.vn/
- Khu vực Buổi 1: thanh tìm kiếm tại Header.
- **Khu vực Buổi 2: danh sách sản phẩm (`#products`)**.
- Đây là giao diện minh họa độc lập, **không phải website chính thức**. Sản phẩm, giá và hình minh họa là dữ liệu mẫu.

## 3. Kỹ thuật HTML5/CSS3 đã thực hành
| Nội dung | Áp dụng trong dự án |
|---|---|
| HTML5 ngữ nghĩa | `header`, `nav`, `main`, `section`, `article`, `footer`; thứ bậc `h1` → `h2` → `h3`; `img` có `alt` |
| Danh sách | Danh sách sản phẩm là `<ul class="product-grid">` với mỗi sản phẩm là một `<li>`; lợi ích sản phẩm là `<ul class="benefit-list">` |
| CSS ngoài | `css/style.css` liên kết bằng `<link rel="stylesheet" href="css/style.css">` |
| Selector | element (`h3`), class (`.product-card`), descendant (`.product-info h3`), child (`.product-grid > li`) |
| Box Model | `padding` trong thẻ, `border`, `border-radius`, `box-sizing: border-box`, `margin` |
| Flexbox | `.product-footer` (giá + nút Yêu thích): `justify-content: space-between; align-items: center; gap` |
| CSS Grid | `.product-grid`: `repeat(4, minmax(0, 1fr))` + `gap`; 2 cột ≤ 900px; 1 cột ≤ 350px |
| Hover / focus | `.product-card:hover/:focus-within`, `.btn-wishlist:hover`, `:focus-visible`, `transition` |

## 4. Hướng dẫn chạy website
1. Giải nén toàn bộ dự án.
2. Mở `index.html` bằng Chrome, Edge hoặc Firefox (không cần cài đặt gì).
3. Dùng DevTools (F12 → Ctrl+Shift+M) để thử các chiều rộng 1366px, 768px, 390px.
4. Rê chuột lên thẻ sản phẩm / nút **Yêu thích**; nhấn phím **Tab** để xem viền focus.

## 5. Những thay đổi đã thực hiện ở Buổi 2
- Đổi `div.product-grid` thành `ul > li > article` (HTML có ngữ nghĩa hơn).
- Thêm cụm giá + nút **Yêu thích** (chỉ là giao diện, chưa có JavaScript) và căn bằng Flexbox.
- **Sửa lỗi ảnh sản phẩm bị cắt** (xem mục 6).
- **Sửa lỗi nội dung thẻ Kem dưỡng ẩm**: đoạn "+ ..." bị dính chung một đoạn, đổi sang `<ul><li>`.
- Viết lại phần CSS khu vực sản phẩm theo từng dòng, có chú thích (trước đó viết dồn một dòng).
- Thêm hiệu ứng hover/focus có `transition`.

## 6. Kiểm thử và công cụ AI
- Công cụ AI: ChatGPT (Buổi 1), Claude (Buổi 2). Prompt và phần tự điều chỉnh ghi trong [`AI_USAGE.md`](AI_USAGE.md).
- **Lỗi phát hiện:** ảnh sản phẩm cao 395–474px nhưng khung ảnh chỉ cao 250px nên bị cắt (đo bằng DevTools/Playwright: `clipped = true` cả 4 ảnh).
- **Nguyên nhân:** `.product-image img{height:86%}` đặt trong khung dạng `grid` chưa có hàng cao xác định, nên phần trăm không tính theo 250px.
- **Cách sửa:** khung `.product-image` dùng `display:flex; padding:16px`, ảnh `height:100%; width:auto; object-fit:contain`.

| Nội dung kiểm tra | Kết quả | Ghi chú |
|---|---|---|
| Trang HTML mở được | Đạt | Mở `index.html` bằng file://, không lỗi tải tài nguyên |
| CSS được áp dụng | Đạt | `.product-grid` có `display: grid` |
| Hình ảnh hiển thị đúng | Đạt | 4/4 ảnh tải được; trước khi sửa 4/4 ảnh bị cắt, sau khi sửa 0/4 |
| Liên kết hoạt động | Đạt | 5/5 liên kết neo `#...` trỏ đúng phần tử |
| Bố cục không bị tràn nghiêm trọng | Đạt | Không có cuộn ngang ở 1366 / 768 / 390px; 4 → 2 → 2 cột |
| Hover/focus hoạt động | Đạt | Thẻ nâng 4px + đổ bóng; nút đổi nền; focus viền 3px |
| Đã tự sửa ít nhất một vấn đề | Đạt | Ảnh bị cắt; nội dung thẻ 3 |

Ảnh minh họa trước/sau nằm trong `images/buoi2/` (`truoc-*` và `sau-*`).

## 7. Repository và website
- GitHub repository: _[điền đường dẫn repository]_
- Website triển khai: _[chưa triển khai]_
