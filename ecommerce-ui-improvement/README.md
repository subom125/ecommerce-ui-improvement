# E-commerce UI Improvement

## 1. Giới thiệu
Bài tập HTML5/CSS3: thiết kế lại khu vực tìm kiếm trên trang thương mại điện tử, theo hướng dễ nhìn và dễ thao tác.

## 2. Website tham khảo
- Tên: Paula’s Choice Việt Nam
- URL: https://paulaschoice.vn/
- Khu vực khảo sát và cải tiến: thanh tìm kiếm tại Header.
- Đây là giao diện minh họa độc lập, **không phải website chính thức**. Sản phẩm, giá và hình minh họa đều là dữ liệu mẫu.

## 3. Chức năng
- Thanh tìm kiếm hình oval, có placeholder "Tìm kiếm sản phẩm..." và nút tìm kiếm.
- Hiển thị bốn sản phẩm mẫu, có hình, tên, giá và chi tiết mở rộng bằng thẻ HTML `<details>`.
- Responsive trên máy tính, máy tính bảng và điện thoại.
- **Giới hạn**: form tìm kiếm chỉ gửi từ khóa thành tham số URL `?q=...`, chưa có xử lý hoặc lọc kết quả; không có giỏ hàng hay thanh toán.

## 4. Công nghệ
HTML5 và CSS3 thuần. Không dùng JavaScript, thư viện, backend hay cơ sở dữ liệu.

## 5. Cách chạy
1. Giải nén toàn bộ dự án.
2. Mở `index.html` trực tiếp bằng Chrome, Edge hoặc Firefox.
3. Kiểm tra responsive, thử 1440px, 390px.
4. Nhấp ô tìm kiếm, nhập từ khóa và nhấn Enter. Chú ý chưa có kết quả tìm kiếm vì bài chỉ làm giao diện.
5. Bấm **Xem thông tin** trên thẻ sản phẩm để thử thao tác HTML không cần JavaScript.

## 6. Cải tiến đã thực hiện
Thay ý tưởng icon kính lúp đơn lẻ bằng thanh tìm kiếm có đường viền oval, ô nhập, chữ gợi ý và nút thao tác rõ ràng; sử dụng `:focus-within`, kích thước vùng bấm phù hợp và media queries cho mobile.

## 7. Hỗ trợ từ AI
ChatGPT hỗ trợ đề xuất bố cục và tạo bản nháp HTML/CSS. Sinh viên phải tự chạy thử, ghi lại ít nhất một điểm tự phát hiện và điều chỉnh trong `AI_USAGE.md` trước khi nộp.
