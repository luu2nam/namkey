# Chính sách quyền riêng tư của NamKey

Có hiệu lực từ ngày 31/10/2026.

Tóm tắt: **NamKey không thu thập, không lưu trữ và không gửi đi phím bấm hay dữ liệu cá nhân của bạn.**
Không có tài khoản, không quảng cáo, không theo dõi, không gửi số liệu thống kê sử dụng.

## 1. Phím bấm

Để thêm dấu, NamKey đọc phím bạn bấm và chỉ giữ trong bộ nhớ **từ đang gõ** (vài ký tự). Từ này bị xoá
ngay khi bạn gõ dấu cách, dấu câu, Enter, click chuột hoặc chuyển cửa sổ. Phím bấm không bao giờ được ghi
ra đĩa và không được gửi qua mạng.

## 2. Kết nối mạng

NamKey chỉ dùng mạng để **kiểm tra và tải bản cập nhật**:

- Đọc thông tin bản phát hành mới nhất từ `api.github.com`.
- Tải tệp cập nhật từ `github.com` (và máy chủ lưu trữ tệp của GitHub), khi bạn bấm cập nhật.

Mỗi lần như vậy, GitHub nhận được những thông tin mà mọi trình duyệt cũng gửi: địa chỉ IP, thời điểm, và
tên kèm phiên bản phần mềm (`namkey/<phiên bản>`). Việc GitHub xử lý các thông tin này theo
[Chính sách quyền riêng tư của GitHub](https://docs.github.com/site-policy/privacy-policies/github-general-privacy-statement).
NamKey không gửi bất kỳ thông tin nào khác.

Bạn có thể tắt việc tự kiểm tra trong **Cài đặt → Cập nhật → Tự kiểm tra cập nhật**. Trang namlh.net chỉ
được mở khi bạn tự bấm vào liên kết.

## 3. Dữ liệu lưu trên máy của bạn

NamKey chỉ lưu những thứ sau, và tất cả nằm trên máy của bạn:

| Dữ liệu | Vị trí | Mục đích |
|---|---|---|
| Cài đặt (kiểu gõ, phím tắt...) | `%APPDATA%\namkey\settings.ini` | Ghi nhớ lựa chọn của bạn |
| Khởi động cùng Windows (nếu bật) | Giá trị `namkey` trong `HKCU\Software\Microsoft\Windows\CurrentVersion\Run` | Tự chạy khi đăng nhập |
| Hiện biểu tượng ở thanh tác vụ | Giá trị `IsPromoted` trong `HKCU\Control Panel\NotifyIconSettings` (mục của NamKey) | Đưa biểu tượng ra khỏi ô `^` lần đầu chạy |

## 4. Gỡ NamKey và xoá dữ liệu

1. Tắt **Khởi động cùng Windows** trong Cài đặt → Hệ thống.
2. Thoát NamKey: click phải biểu tượng ở khay rồi chọn **Thoát**.
3. Xoá thư mục chứa `namkey.exe`, và thư mục `%APPDATA%\namkey`.

## 5. Trẻ em

NamKey không thu thập dữ liệu của bất kỳ ai, kể cả trẻ em.

## 6. Thay đổi chính sách

Nếu cách NamKey xử lý dữ liệu thay đổi, chính sách này sẽ được cập nhật trước khi bản mới được phát
hành. Bản mới nhất có trong ứng dụng (**Cài đặt → Pháp lý**) và tại github.com/luu2nam/namkey.

## 7. Liên hệ

Câu hỏi về quyền riêng tư: tạo issue tại github.com/luu2nam/namkey/issues, hoặc liên hệ qua namlh.net.
