# Kiểm tra giao diện — 30/10/2026

Kiểm tra bằng trình duyệt headless trên macOS, mô phỏng kích thước màn hình; chưa kiểm tra trên điện thoại vật lý hoặc trình duyệt tích hợp Zalo/Facebook.

- Chrome: 320×568, 375×667, 390×844, 430×932, 768×1024, 820×1180, 1024×768, 1280×720, 1440×900, 844×390. Cả nhà trai và nhà gái: 20 trường hợp.
- WebKit, có cảm ứng: 375×667, 390×844, 768×1024, 844×390. Cả hai bên: 8 trường hợp.
- Chụp và xem các trạng thái phong bì đóng/mở, trang đầu và lời mời. Kiểm tra tràn ngang, lỗi JavaScript, mở/đóng ảnh album và QR, trạng thái phát nhạc sau khi chạm phong bì.
- Kiểm tra bổ sung trong DOM: tên khách có dấu, lựa chọn nhà trai/nhà gái, nội dung lịch và địa điểm, nút nhạc bật/tắt, an toàn khi tên khách chứa ký tự HTML.

## Đã sửa

- Phong bì che nội dung khi mở trên điện thoại xoay ngang: chuyển sang bố cục lá thư ngang, đưa phong bì ra khỏi vùng đọc.
- Mép phong bì lấn vào tên khách và nút đọc tiếp trên PC: thu gọn phong bì và điều chỉnh khoảng cách chữ.
- Viền ảnh QR chú rể còn một mẩu chữ ngân hàng bị cắt: điều chỉnh vùng hiển thị, giữ nguyên tệp gốc để xem/lưu.

Đã kiểm tra lại các lỗi bố cục trên Chrome ở 1280×720, 1440×900, 844×390, 667×375 và WebKit ở 844×390, 667×375, cho cả hai bên. Không phát hiện lỗi JavaScript hoặc tràn ngang trong các trường hợp đã kiểm tra. Nhạc báo đang phát sau thao tác mở thiệp ở cả hai engine; điều này không thay thế việc nghe thử trên iPhone thật.
