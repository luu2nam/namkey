# Chính sách quyền riêng tư của NamKey

Có hiệu lực từ ngày 31/10/2026.

Tóm tắt: **NamKey không thu thập, không lưu trữ và không gửi đi phím bấm hay dữ liệu cá nhân của bạn.**
Không có tài khoản, không quảng cáo, không theo dõi, không gửi số liệu thống kê sử dụng.

## 1. Phím bấm

Để thêm dấu, NamKey đọc phím bạn bấm và chỉ giữ trong bộ nhớ **từ đang gõ** (vài ký tự). Từ này bị xoá
ngay khi bạn gõ dấu cách, dấu câu, Enter, click chuột hoặc chuyển cửa sổ. Phím bấm không được ghi ra đĩa
và không bao giờ được gửi qua mạng.

Ngoại lệ duy nhất là **chế độ dò lỗi** của bản macOS: chỉ bật khi bạn tự chạy NamKey bằng lệnh dò lỗi
(theo hướng dẫn khi báo lỗi), không bao giờ tự bật. Khi đó các phím được ghi vào tệp
`~/Library/Logs/NamKey/namkey.log` trên máy của bạn để tìm lỗi, và không được gửi đi đâu. Mở lại NamKey
như bình thường là tắt chế độ này; bạn có thể xoá tệp đó bất cứ lúc nào.

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

NamKey chỉ lưu những thứ sau, và tất cả nằm trên máy của bạn. Trên Windows:

| Dữ liệu | Vị trí | Mục đích |
|---|---|---|
| Cài đặt (kiểu gõ, phím tắt...) | `%APPDATA%\namkey\settings.ini` | Ghi nhớ lựa chọn của bạn |
| Khởi động cùng Windows (nếu bật) | Giá trị `namkey` trong `HKCU\Software\Microsoft\Windows\CurrentVersion\Run` | Tự chạy khi đăng nhập |
| Hiện biểu tượng ở thanh tác vụ | Giá trị `IsPromoted` trong `HKCU\Control Panel\NotifyIconSettings` (mục của NamKey) | Đưa biểu tượng ra khỏi ô `^` lần đầu chạy |

Trên macOS:

| Dữ liệu | Vị trí | Mục đích |
|---|---|---|
| Cài đặt (kiểu gõ, phím tắt...) | `~/Library/Application Support/namkey/settings.ini` | Ghi nhớ lựa chọn của bạn |
| Khoá chạy một bản | `~/Library/Application Support/namkey/namkey.lock` | Không cho hai bộ gõ chạy cùng lúc |
| Khởi động cùng macOS (nếu bật) | `~/Library/LaunchAgents/net.namlh.namkey.plist` | Tự chạy khi đăng nhập |
| Quyền Trợ năng | Do macOS lưu (Cài đặt hệ thống → Quyền riêng tư & Bảo mật → Trợ năng) | Cho phép bộ gõ đọc phím và gửi chữ có dấu |

## 4. Gỡ NamKey và xoá dữ liệu

Trên Windows:

1. Tắt **Khởi động cùng Windows** trong Cài đặt → Hệ thống.
2. Thoát NamKey: click phải biểu tượng ở khay rồi chọn **Thoát**.
3. Xoá thư mục chứa `namkey.exe`, và thư mục `%APPDATA%\namkey`.

Trên macOS:

1. Tắt **Khởi động cùng macOS** trong Cài đặt → Hệ thống.
2. Thoát NamKey: bấm biểu tượng V/E trên thanh menu rồi chọn **Thoát NamKey**.
3. Xoá `NamKey.app`, và thư mục `~/Library/Application Support/namkey`.
4. Trong Cài đặt hệ thống → Quyền riêng tư & Bảo mật → Trợ năng, chọn NamKey rồi bấm dấu −.

## 5. Trẻ em

NamKey không thu thập dữ liệu của bất kỳ ai, kể cả trẻ em.

## 6. Thay đổi chính sách

Nếu cách NamKey xử lý dữ liệu thay đổi, chính sách này sẽ được cập nhật trước khi bản mới được phát
hành. Bản mới nhất có trong ứng dụng (**Cài đặt → Pháp lý**) và tại github.com/luu2nam/namkey.

## 7. Liên hệ

Câu hỏi về quyền riêng tư: tạo issue tại github.com/luu2nam/namkey/issues, hoặc liên hệ qua namlh.net.
