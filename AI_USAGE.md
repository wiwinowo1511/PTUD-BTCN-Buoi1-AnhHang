# AI Usage Log

## 1. Công cụ AI
- ChatGPT: Dùng để phân tích UX/UI và viết code HTML/CSS ban đầu
- Claude: Dùng ở bước kiểm tra, sửa lỗi font tiếng Việt và bổ sung các nút chức năng trong Header/Footer

## 2. Mục đích sử dụng
- Phân tích giao diện website Hasaki, tìm ra các vấn đề cần cải thiện
- Đề xuất bố cục và viết mã HTML/CSS cho trang chi tiết sản phẩm
- Giải quyết vấn đề về thiết kế nút chức năng "Mua ngay"

## 3. Prompt đã sử dụng
- **Prompt 1 (Phân tích):** "Tôi đang thực hiện bài tập phát triển giao diện website thương mại điện tử bằng HTML5 và CSS3.

Tôi muốn cải tiến khu vực: **Các nút thao tác mua hàng (Thêm vào giỏ hàng và Mua ngay) trên trang chi tiết sản phẩm của Hasaki.vn.** Hiện tại, hai nút này đang có thiết kế màu sắc và kích thước giống hệt nhau, gây ra sự nhầm lẫn cho người dùng khi thao tác. Tôi muốn làm nổi bật nút "Mua ngay" để tăng tỷ lệ chuyển đổi.

Đối tượng sử dụng: khách hàng mua sắm trực tuyến tại Việt Nam.

Hãy đề xuất:

1. Bố cục giao diện (Làm sao để bố trí 2 nút này hợp lý và tạo sự khác biệt rõ ràng?)
2. Các thành phần HTML cần sử dụng.
3. Cách tổ chức CSS (Các thuộc tính để làm nổi bật nút Mua ngay).
4. Cách hiển thị trên máy tính và điện thoại.
5. Những điểm cần kiểm tra về khả năng sử dụng.

Trước tiên, hãy giải thích phương án thiết kế. **Chưa tạo toàn bộ mã nguồn cho đến khi tôi yêu cầu.**"
- **Prompt 2 (Tạo mã nguồn):** "Dựa trên phương án đã thống nhất, hãy tạo một trang giao diện chi tiết sản phẩm bằng HTML5 và CSS3.
Yêu cầu:
- Giao diện có tiêu đề và khu vực sản phẩm.
- Hiển thị hình ảnh sản phẩm, giá bán, quà tặng kèm, mô tả chi tiết, thành phần, hướng dẫn sử dụng, đánh giá, các thông tin ưu đãi như miễn phí vận chuyển, cam kết đền bù, các thông số và hỏi đáp về sản phẩm, trạng thái tồn kho ở các chi nhánh và các nút thao tác mua hàng, cột đề xuất sản phẩm khác liên quan
- Bố cục phù hợp với màn hình máy tính và điện thoại.
- Mã HTML có cấu trúc rõ ràng.
- CSS được tách thành file riêng.
- Không sử dụng backend hoặc cơ sở dữ liệu.
- Không đưa thư viện hoặc thành phần không cần thiết vào dự án.
Giải thích cách chạy trang web và những phần tôi cần kiểm tra.
Tôi có cung cấp logo của Hasaki"
- **Prompt 3 (Khắc phục lỗi sau khi kiểm tra):** "Kiểm tra giao diện web phát hiện font chữ bị lỗi font tiếng Việt, ví dụ “DƯỠNG ẨM”, phần header thiếu các nút cơ bản như Đăng nhập, Giỏ hàng, phần footer thiếu thông tin liên hệ, chứng nhận và chính sách, bạn hãy khắc phục những lỗi trên" (Kèm theo logo Hasaki).

## 4. Kết quả AI đề xuất
AI đã cung cấp một bộ code HTML/CSS khá hoàn chỉnh với bố cục 2 cột. AI đã thiết kế nút "Mua ngay" nổi bật hơn bằng màu đỏ. AI cũng sử dụng CSS Grid và Flexbox để xử lý responsive.

## 5. Kiểm tra và điều chỉnh
- **Đã kiểm tra:** Mở file `index.html` trên trình duyệt, dùng F12 (Chrome DevTools) để kiểm tra ở các kích thước 1440px (PC), 768px (Tablet) và 390px (Mobile).
- **Đã sửa:** Ở lần code đầu tiên, AI dùng font không hỗ trợ Việt hóa hoàn toàn ở các tiêu đề in hoa nên bị lỗi font. Sau khi prompt chỉnh sửa thì AI đã chỉnh lại font `Be Vietnam Pro` và tăng `line-height` để dấu không bị cắt.
- **Không sử dụng:** AI có gợi ý thêm các đoạn Javascript phức tạp để làm chức năng giỏ hàng thực sự

## 6. Phần tôi hiểu và có thể giải thích
- **Biến CSS (`:root`):** Em đã hiểu cách tạo các biến màu sắc (`--brand-green`, `--brand-red`) để dễ dàng tái sử dụng và thay đổi màu sắc toàn trang web
- **`.purchase-actions` (Grid):** Sử dụng `display: grid; grid-template-columns: 1fr 1fr;` để chia đều 2 nút mua hàng thành 2 cột bằng nhau
- **`.btn--buy` vs `.btn--cart`:** Tạo class riêng cho từng nút để nút Mua ngay có màu nền đỏ (`background: var(--brand-red)`), còn nút Thêm vào giỏ hàng có nền trắng viền xanh
- **Cách gắn file css link vào html để định dạng cho nội dung trên trang html**
