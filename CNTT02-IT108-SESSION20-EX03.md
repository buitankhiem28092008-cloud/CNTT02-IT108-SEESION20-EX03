# Bài 3 : Quản lý rủi ro khi mất thiết bị xác thực
## Báo cáo phân tích (IPO) khôi phục tài khoản AWS
**1.input đầu vào** 
- [x] Mã dự phòng (Backup Codes): Dãy mã khẩn cấp gồm một lần sử dụng (one-time use) mà bạn đã tải về và cất giữ an toàn (ví dụ: in ra giấy cất trong tủ hoặc lưu trong Password Manager cá nhân) khi thiết lập MFA lần đầu.
## 2. Process (Quy trình xử lý)
- [x] Xác thực khẩn cấp: Truy cập trang đăng nhập AWS, nhập mật khẩu như bình thường, sau đó chọn phương thức đăng nhập bằng Backup Code thay vì mã Google Authenticato
- [x] Hủy mã cũ & Thu hồi thiết bị mất: Ngay khi vào được hệ thống, lập tức vô hiệu hóa (revoke) thiết bị cũ đang mất để cắt đứt quyền truy cập từ xa.
- [x] Cấp mã mới: Thiết lập ứng dụng Google Authenticator trên điện thoại mới, kích hoạt lại MFA và tạo ra một bộ Backup Codes mới thay thế hoàn toàn bộ cũ.
## 3. Output (Đầu ra)
- [x] Hệ thống an toàn: Lấy lại quyền kiểm soát hạ tầng AWS, đồng thời vô hiệu hóa hoàn toàn nguy cơ kẻ nhặt được điện thoại cũ có thể đột nhập vào hệ thống
## Tại sao tuyệt đối không lưu Backup Codes dạng ảnh trong thư viện điện thoại?
- [x] Dễ lộ dữ liệu lên mây: Ảnh chứa mã có thể tự động đồng bộ lên Google Photos, iCloud... Kẻ gian hack tài khoản đám mây là lấy được mã.
- [x]  Vô hiệu hóa bảo mật (MFA): Khi mất điện thoại, kẻ gian chỉ cần mở Thư viện ảnh là có ngay "chìa khóa", làm lớp bảo mật 2 bước hoàn toàn mất tác dụng.