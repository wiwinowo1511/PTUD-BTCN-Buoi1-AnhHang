# Cải tiến một chức năng nhỏ trang chi tiết sản phẩm Hasaki

## 1. Giới thiệu
Bài tập cải tiến giao diện trang chi tiết sản phẩm của website thương mại điện tử Hasaki.vn bằng HTML5 và CSS3. Khu vực được chọn để cải tiến là cụm nút thao tác mua hàng (Thêm vào giỏ hàng và Mua ngay) nhằm giải quyết vấn đề nhầm lẫn cho người dùng.
**Link xem giao diện website trực tiếp (GitHub Pages):** https://wiwinowo1511.github.io/PTUD-BTCN-Buoi1-AnhHang/

## 2. Website tham khảo
- Tên website: Hasaki.vn
- URL: https://hasaki.vn/
- Khu vực đã khảo sát: Trang chủ, Tìm kiếm, Danh mục sản phẩm, Trang chi tiết sản phẩm, Giỏ hàng và Thanh toán.

## 3. Chức năng
- Hiển thị hình ảnh sản phẩm, giá bán, quà tặng kèm, mô tả chi tiết, thành phần, hướng dẫn sử dụng, đánh giá, các thông tin ưu đãi như miễn phí vận chuyển, cam kết đền bù, các thông số và hỏi đáp về sản phẩm, trạng thái tồn kho ở các chi nhánh và các nút thao tác mua hàng, cột đề xuất sản phẩm khác liên quan
- Phân biệt rõ ràng nút "Thêm vào giỏ hàng" và "Mua ngay" bằng màu sắc và kiểu dáng.
- Bố cục responsive hỗ trợ tốt trên cả màn hình máy tính và điện thoại di động 

## 4. Công nghệ
- HTML5
- CSS3
- JavaScript (Chỉ dùng để mô phỏng tương tác click nút, không dùng backend).

## 5. Cách chạy
Mở file `index.html` bằng trình duyệt web 

## 6. Cải tiến đã thực hiện
- **Vấn đề ban đầu:** Trên giao diện gốc của Hasaki, nút "Thêm vào giỏ hàng" và nút "Mua ngay" được thiết kế với màu sắc (xanh lá) và kích thước giống hệt nhau. Điều này khiến khách hàng dễ bấm nhầm, làm giảm trải nghiệm người dùng (UX) khi muốn thanh toán nhanh.
- **Thay đổi đã thực hiện:** 
  - Giữ nguyên thiết kế nút "Thêm vào giỏ hàng" (nền trắng, viền xanh).
  - Thiết kế lại nút "Mua ngay": Đổi sang **màu đỏ đậm** (màu `--brand-red`), bo góc tròn, chữ in hoa và có icon sấm sét ⚡ để tạo sự nổi bật (visual hierarchy).
  - Bổ sung thanh thanh toán cố định (sticky bar) ở dưới cùng màn hình điện thoại để tối ưu hóa thao tác bằng ngón tay cái.

## 7. Hỗ trợ từ AI
- AI (ChatGPT) đã hỗ trợ lên khung bố cục HTML/CSS cơ bản và gợi ý màu sắc cho nút Mua ngay.
- AI (Claude) đã hỗ trợ tôi sửa lỗi font chữ tiếng Việt bị lỗi (chuyển sang font Be Vietnam Pro) và thêm header/footer cho giống thực tế.
- Tôi đã tự kiểm tra lại toàn bộ code, chạy thử trên nhiều kích thước màn hình (DevTools) và tự tay tinh chỉnh lại khoảng cách (padding/margin) để giao diện thoáng và dễ nhìn hơn.
