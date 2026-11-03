# AI Usage Log

## 1. Công cụ AI
ChatGPT (OpenAI).

## 2. Mục đích sử dụng
Phân tích đề xuất cải tiến thanh tìm kiếm trên trang chủ Paula’s Choice Việt Nam và tạo bản nháp HTML5/CSS3.

## 3. Prompt đã sử dụng
**Bước 2:** Đề xuất bố cục, thành phần HTML, tổ chức CSS, hiển thị desktop/mobile và những điểm cần kiểm tra cho thanh tìm kiếm bo tròn có dòng chữ “Tìm kiếm”. Chưa tạo mã nguồn.

**Bước 3:** Dựa trên phương án đã thống nhất, tạo trang HTML5/CSS3 có tiêu đề, tối thiểu 4 sản phẩm mẫu (hình ảnh, tên, giá, nút thao tác), responsive, CSS riêng, không backend/cơ sở dữ liệu/thư viện không cần thiết; giải thích cách chạy và kiểm tra.


## 4. Kết quả AI đề xuất
Tạo thanh tìm kiếm oval trên Header, input nhập từ khóa, nút kính lúp kèm chữ trên desktop; 4 sản phẩm mẫu và thông tin mở rộng bằng `<details>`; responsive với CSS Grid/Flexbox và media queries.

## 5. Kiểm tra và điều chỉnh
**CẦN SINH VIÊN TỰ HOÀN THÀNH SAU KHI CHẠY THỬ:**
- Ngày kiểm tra: 20/10/2026
- Kích thước màn hình đã thử: 1440px
- Vấn đề tự phát hiện: cỡ chữ trong ô tìm kiếm hơi nhỏ
- Dòng CSS/HTML đã tự chỉnh và lý do: chỉnh dòng
.search-form input{width:100%;min-width:0;border:0;background:transparent;color:var(--ink);outline:0;padding:13px 8px 13px 20px;font-size:18px;min-height:48px}
font-size từ 13 lên 18
- Kết quả sau chỉnh sửa: ảnh sau khi chỉnh cỡ chữ trong thư mục images

## 6. Phần tôi hiểu và có thể giải thích
toàn bộ code trong phần này: `<div class="product-grid">` là để hiển thị sản phẩm dạng lưới

`<!doctype html>` --> khai báo HTML5
`<html lang="vi">` --> Khai báo ngôn ngữ sử dụng là tiếng Việt
`<head>`
  `<meta charset="utf-8">` --> Dùng tiếng việt có dấu
  `<meta name="viewport" content="width=device-width, initial-scale=1"> `--> Viewport để hiển thị phù hợp với kích thước màn hình

`<form>` để tạo biểu mẫu tìm kiếm

có thể tự chỉnh nội dung chi tiết của từng sản phẩm
có thể tự chỉnh tên doanh nghiệp (em chỉnh từ Skincare Studio thành Paula's Choice)


---

# BUỔI 2 – HTML & CSS (khu vực danh sách sản phẩm)

## 1. Công cụ AI
Claude (Anthropic).

## 2. Prompt tiêu biểu đã sử dụng
Các prompt theo mẫu đề Buổi 2 (đã điền mã HTML/CSS thật của dự án). Bản đầy đủ nằm trong file Word báo cáo.

| Prompt | Mục đích | Kết quả chính |
|---|---|---|
| 1 | Phân tích mã hiện tại, tìm 3 vấn đề | Ảnh bị cắt; thẻ chưa có cụm thao tác; nội dung thẻ 3 bị lỗi định dạng |
| 2 | Kiểm tra cấu trúc HTML5 | Đổi `div` thành `ul > li > article`; giữ nguyên thứ bậc h1–h3 |
| 3 | Kiểm tra liên kết CSS | `css/style.css` đã liên kết đúng, đường dẫn tương đối hợp lệ |
| 4 | Selector và Box Model | Viết lại CSS thẻ sản phẩm có chú thích |
| 5 | Flexbox | `.product-footer` căn giá và nút bằng `space-between`, `align-items:center`, `gap` |
| 6 | CSS Grid | `repeat(4, minmax(0,1fr))`, đổi còn 2 cột ở ≤ 900px |
| 7 | Hover/focus | `transition`, `:hover`, `:focus-within`, `:focus-visible` |
| 8 | Kiểm tra lỗi | Xác định nguyên nhân ảnh bị cắt và cách sửa |

## 3. Phần tự kiểm tra và điều chỉnh
- Ví dụ của đề dùng liên kết `product-detail.html`. Dự án **không có** trang này nên không dùng, tránh liên kết chết; thay bằng nút **Yêu thích** (chỉ là giao diện).
- Ví dụ của đề dùng `object-fit: cover`. Ảnh sản phẩm là ảnh dọc, nền trắng, nên dùng `object-fit: contain` để không cắt chai/tuýp.
- Lỗi ảnh bị cắt được kiểm chứng bằng cách đo kích thước ảnh so với khung (trước: ảnh cao 395–474px trong khung 250px; sau: ảnh cao 218px).
- Đã kiểm tra lại ở 1366px, 768px, 390px; không có cuộn ngang.

## 4. Phần tôi hiểu và có thể giải thích
Xem phần "Câu hỏi kiểm tra kiến thức" trong file Word và mục 3 của README.
