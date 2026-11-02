# Chính sách quyền riêng tư của NamKey

Có hiệu lực từ ngày 31/10/2026. Cập nhật ngày 02/11/2026 (danh sách ứng dụng, bảng gõ tắt, góp ý).

Tóm tắt: **NamKey không thu thập, không lưu trữ và không gửi đi phím bấm hay dữ liệu cá nhân của bạn.**
Không có tài khoản, không quảng cáo, không theo dõi, không gửi số liệu thống kê sử dụng. Góp ý chỉ được gửi
khi bạn tự viết và bấm Gửi.

## 1. Phím bấm

Để thêm dấu, NamKey đọc phím bạn bấm và chỉ giữ trong bộ nhớ **từ đang gõ** (vài ký tự). Từ này bị xoá
ngay khi bạn gõ dấu cách, dấu câu, Enter, click chuột hoặc chuyển cửa sổ. Phím bấm không được ghi ra đĩa
và không bao giờ được gửi qua mạng.

Trên macOS, khi bật **Sửa tiếp từ cũ sau khi click** (tắt sẵn), hoặc khi phát hiện phím bị lọt, NamKey đọc vài chữ
ngay trước con trỏ qua quyền Trợ năng để biết từ đang sửa. Các chữ này cũng chỉ giữ trong bộ nhớ như từ đang gõ.

Ngoại lệ duy nhất là **chế độ dò lỗi** của bản macOS: chỉ bật khi bạn tự chạy NamKey bằng lệnh dò lỗi
(theo hướng dẫn khi báo lỗi), không bao giờ tự bật. Khi đó các phím được ghi vào tệp
`~/Library/Logs/NamKey/namkey.log` trên máy của bạn để tìm lỗi, và không được gửi đi đâu. Mở lại NamKey
như bình thường là tắt chế độ này; bạn có thể xoá tệp đó bất cứ lúc nào.

## 2. Kết nối mạng

NamKey chỉ dùng mạng vào hai việc: **kiểm tra, tải bản cập nhật** và **gửi góp ý khi bạn bấm Gửi**.

Cập nhật:

- Đọc thông tin bản phát hành mới nhất từ `api.github.com`.
- Tải tệp cập nhật từ `github.com` (và máy chủ lưu trữ tệp của GitHub), khi bạn bấm cập nhật.

Mỗi lần như vậy, GitHub nhận được những thông tin mà mọi trình duyệt cũng gửi: địa chỉ IP, thời điểm, và
tên kèm phiên bản phần mềm (`namkey/<phiên bản>`). Việc GitHub xử lý các thông tin này theo
[Chính sách quyền riêng tư của GitHub](https://docs.github.com/site-policy/privacy-policies/github-general-privacy-statement).
Bạn có thể tắt việc tự kiểm tra trong **Cài đặt → Cập nhật → Tự kiểm tra cập nhật**.

Góp ý (**Cài đặt → Góp ý**): chỉ gửi khi bạn bấm **Gửi**, tới máy chủ của tác giả tại `namlh.net`. Nội dung gửi
gồm đúng những gì hiện trên trang đó:

- Loại góp ý, tiêu đề và nội dung bạn viết; tên và email/số điện thoại nếu bạn tự điền.
- Phiên bản NamKey, và nếu bạn để chọn ô "Kèm hệ điều hành và các tuỳ chọn đang bật": tên, phiên bản hệ điều
  hành và các tuỳ chọn gõ đang bật (không kèm nội dung bảng gõ tắt).
- Tên một ứng dụng, nếu bạn tự chọn ứng dụng đang gặp lỗi.
- Một **mã cài đặt ngẫu nhiên** do NamKey tạo lần đầu bạn gửi góp ý và ghi vào tệp cài đặt, để máy chủ giới hạn
  số góp ý mỗi ngày. Mã này không gắn với phần cứng, tài khoản hay tên máy.

Máy chủ nhận được địa chỉ IP của bạn như mọi trang web, nhưng chỉ lưu dạng mã băm (không đọc ngược ra IP) để
chống gửi rác, và mã băm này tự xoá sau 2 ngày. Góp ý chỉ tác giả đọc, dùng để sửa lỗi và cải tiến NamKey,
không chia sẻ cho ai. Muốn xoá góp ý đã gửi, liên hệ tác giả qua namlh.net. NamKey không bao giờ gửi chữ bạn
gõ, bảng gõ tắt hay danh sách ứng dụng.

NamKey không gửi bất kỳ thông tin nào khác. Trang namlh.net chỉ được mở khi bạn tự bấm vào liên kết.

## 3. Dữ liệu lưu trên máy của bạn

NamKey chỉ lưu những thứ sau, và tất cả nằm trên máy của bạn. Trên Windows:

| Dữ liệu | Vị trí | Mục đích |
|---|---|---|
| Cài đặt (kiểu gõ, phím tắt, bảng gõ tắt, ứng dụng đã dùng, mã cài đặt nếu đã gửi góp ý...) | `%APPDATA%\namkey\settings.ini` | Ghi nhớ lựa chọn của bạn |
| Tệp gõ tắt (khi bạn bấm Xuất ra tệp) | `%APPDATA%\namkey\go-tat.txt` | Sao lưu, chép bảng gõ tắt sang máy khác |
| Khởi động cùng Windows (nếu bật) | Giá trị `namkey` trong `HKCU\Software\Microsoft\Windows\CurrentVersion\Run` | Tự chạy khi đăng nhập |
| Hiện biểu tượng ở thanh tác vụ | Giá trị `IsPromoted` trong `HKCU\Control Panel\NotifyIconSettings` (mục của NamKey) | Đưa biểu tượng ra khỏi ô `^` lần đầu chạy |

Trên macOS:

| Dữ liệu | Vị trí | Mục đích |
|---|---|---|
| Cài đặt (kiểu gõ, phím tắt, bảng gõ tắt, ứng dụng đã dùng, mã cài đặt nếu đã gửi góp ý...) | `~/Library/Application Support/namkey/settings.ini` | Ghi nhớ lựa chọn của bạn |
| Tệp gõ tắt (khi bạn bấm Xuất ra tệp) | `~/Library/Application Support/namkey/go-tat.txt` | Sao lưu, chép bảng gõ tắt sang máy khác |
| Khoá chạy một bản | `~/Library/Application Support/namkey/namkey.lock` | Không cho hai bộ gõ chạy cùng lúc |
| Khởi động cùng macOS (nếu bật) | `~/Library/LaunchAgents/net.namlh.namkey.plist` | Tự chạy khi đăng nhập |
| Quyền Trợ năng | Do macOS lưu (Cài đặt hệ thống → Quyền riêng tư & Bảo mật → Trợ năng) | Cho phép bộ gõ đọc phím và gửi chữ có dấu |

Để đổi chế độ Việt/Anh theo ứng dụng (Cài đặt → Ứng dụng), NamKey ghi **tên các ứng dụng** bạn chuyển tới
(vd. `Microsoft Word`, `code.exe`) và chế độ dùng lần cuối vào tệp cài đặt. Không ghi tên cửa sổ, tên tài
liệu hay nội dung bạn gõ. Bạn xoá được từng ứng dụng, hoặc cả danh sách, trong trang đó.

Để báo khi có bộ gõ tiếng Việt khác đang chạy, NamKey xem tên các chương trình đang chạy trên máy (lúc khởi
động, và khi cửa sổ cài đặt đang mở). Danh sách này chỉ dùng ngay lúc đó, không được lưu hay gửi đi. Tắt được
trong Cài đặt → Hệ thống → Tương thích.

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

NamKey không thu thập dữ liệu của bất kỳ ai, kể cả trẻ em. Góp ý chỉ chứa những gì người gửi tự viết và chọn.

## 6. Thay đổi chính sách

Nếu cách NamKey xử lý dữ liệu thay đổi, chính sách này sẽ được cập nhật trước khi bản mới được phát
hành. Bản mới nhất có trong ứng dụng (**Cài đặt → Pháp lý**) và tại github.com/luu2nam/namkey.

## 7. Liên hệ

Câu hỏi về quyền riêng tư: gửi trong Cài đặt → Góp ý, liên hệ qua namlh.net, hoặc tạo issue tại
github.com/luu2nam/namkey/issues.
