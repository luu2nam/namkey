<p align="center">
  <img src="docs/images/namkey-256.png" width="120" alt="NamKey">
</p>

<h1 align="center">NamKey</h1>

<p align="center">
  Bộ gõ tiếng Việt gọn nhẹ, miễn phí, lõi viết bằng Rust. Có bản cho Windows và macOS.<br>
  <a href="https://github.com/luu2nam/namkey/releases/latest"><b>⬇ Tải bản mới nhất</b></a>
  &nbsp;·&nbsp;
  <a href="https://namlh.net/namkey">namlh.net/namkey</a>
</p>

![Cửa sổ cài đặt của NamKey](docs/images/overview.png)

## Tính năng

- **Telex và VNI, gõ theo thói quen của bạn.** Gõ dấu ở đâu trong từ cũng được, theo thứ tự nào cũng được:
  `nguwowif`, `nguoiwf`, `ngwowif` đều ra **người**; `duongwfd` ra **đường**.
- **Đặt dấu kiểu cũ hoặc kiểu mới:** hòa, khỏe, thủy hoặc hoà, khoẻ, thuỷ.
- **Kiểm tra chính tả với từ điển âm tiết tiếng Việt.** Từ không phải tiếng Việt như `text`, `windows`,
  `google`, `wow`, `data` được giữ nguyên như đã gõ.
- **Gõ lặp phím để bỏ dấu** (`ass` → as). Xoá lùi không mất dấu (tiếng ⌫ → tiến).
- **Bật/tắt nhanh** bằng **Ctrl+Shift**, hoặc qua biểu tượng **V/E** ở khay hệ thống (Windows) hay thanh menu
  (macOS). **Phím tắt gán lại được**, kể cả để chuyển Telex ↔ VNI hay mở cài đặt.
- **Cửa sổ cài đặt rõ ràng**, có bảng phím, ví dụ và ô gõ thử.
- **Tự cập nhật** từ trang này, có kiểm tra mã SHA-256 của file tải về (Windows; bản macOS báo khi có bản mới).
- **Gọn nhẹ.** Bộ gõ chạy nền chưa tới 1 MB, không quảng cáo, không thu thập dữ liệu.

## Tải về

Vào trang [Releases](https://github.com/luu2nam/namkey/releases/latest) và tải file cho máy của bạn:

| Máy | File |
|---|---|
| Windows 10/11, 64-bit | `namkey-<phiên bản>-windows-x64.zip` |
| macOS 11 trở lên, chip Apple (M1, M2...) | `namkey-<phiên bản>-macos-arm64.zip` |

## Cài đặt trên Windows

1. Tải file `namkey-<phiên bản>-windows-x64.zip` (xem [Tải về](#tải-về)).
2. Giải nén vào một thư mục của bạn, ví dụ `C:\Users\<tên bạn>\namkey`.
   Không nên đặt trong `Program Files`, vì bộ cập nhật cần ghi được vào thư mục này.
3. Chạy **`namkey.exe`**. Biểu tượng **V** sẽ hiện ở khay hệ thống, góc phải thanh tác vụ. Nếu không thấy, bấm mũi tên **^** ở đó.
4. Click phải vào biểu tượng rồi chọn **Cài đặt...** để chọn kiểu gõ và bật **Khởi động cùng Windows**.

> **Lưu ý**
> - NamKey chưa được ký số. Lần đầu chạy, Windows SmartScreen có thể cảnh báo: bấm **More info → Run anyway**.
>   Một số phần mềm diệt virus có thể nghi ngờ, vì bộ gõ nào cũng phải đọc phím bấm để thêm dấu.
> - Nếu máy đang có bộ gõ khác (chẳng hạn UniKey), hãy tắt nó hoặc chuyển nó sang chế độ tiếng Anh.
>   Nếu không, chữ sẽ bị thêm dấu hai lần và phím Ctrl+Shift bị tranh nhau.

## Cài đặt trên macOS

1. Tải file `namkey-<phiên bản>-macos-arm64.zip` (xem [Tải về](#tải-về)), mở file để giải nén ra **NamKey.app**.
2. Kéo **NamKey.app** vào thư mục **Ứng dụng** (Applications), rồi mở nó.
3. Lần đầu mở, macOS sẽ báo không mở được vì NamKey chưa được Apple công chứng. Vào **Cài đặt hệ thống →
   Quyền riêng tư & Bảo mật**, kéo xuống dưới và bấm **Vẫn mở**, rồi mở lại NamKey.
4. NamKey sẽ hướng dẫn cấp quyền **Trợ năng**: bật công tắc cạnh NamKey trong **Cài đặt hệ thống → Quyền riêng
   tư & Bảo mật → Trợ năng**. macOS chỉ cho bộ gõ đọc phím và gửi chữ có dấu khi được cấp quyền này.
5. Biểu tượng **V** hiện trên thanh menu, góc trên bên phải màn hình, là gõ được. Bấm vào biểu tượng rồi chọn
   **Cài đặt...** để chọn kiểu gõ và bật **Khởi động cùng macOS**.

> Trên macOS, phím **Control** đóng vai trò Ctrl. Nếu đang dùng bộ gõ tiếng Việt khác, hãy chuyển nguồn nhập
> về **ABC** để chữ không bị thêm dấu hai lần.

## Sử dụng

| Thao tác | Kết quả |
|---|---|
| **Ctrl+Shift** (bấm rồi thả, không kèm phím khác) | Bật/tắt tiếng Việt |
| Windows: click trái biểu tượng ở khay | Bật/tắt tiếng Việt |
| Windows: nháy đúp biểu tượng ở khay | Mở cửa sổ cài đặt |
| Windows: click phải biểu tượng ở khay | Chọn Telex/VNI, Cài đặt, Kiểm tra cập nhật, Thoát |
| macOS: bấm biểu tượng trên thanh menu | Chọn Tiếng Việt/Tiếng Anh, Telex/VNI, Cài đặt, Kiểm tra cập nhật, Thoát |

### Bảng phím

| Dấu | Telex | VNI | Ví dụ Telex |
|---|---|---|---|
| Sắc, huyền, hỏi, ngã, nặng | `s` `f` `r` `x` `j` | `1` `2` `3` `4` `5` | `vieetj` → việt |
| Xoá dấu thanh | `z` | `0` | `asz` → a |
| â ê ô | `aa` `ee` `oo` | `6` | `quoocs` → quốc |
| ă | `aw` | `8` | `hoawcj` → hoặc |
| ơ ư | `ow` `uw` (hoặc `w`) | `7` | `nguwowif` → người |
| đ | `dd` | `9` | `dduwowngf` → đường |

![Trang Dấu & chính tả](docs/images/rules.png)

## Cập nhật

NamKey tự kiểm tra bản mới khi khởi động và mỗi ngày một lần. Cũng có thể chọn **Kiểm tra cập nhật...** trong
menu của biểu tượng V/E.

- **Windows:** khi có bản mới, cửa sổ cập nhật hiện lên, bấm **Tải về và cập nhật** là xong.
- **macOS:** NamKey báo có bản mới và mở trang tải về. Thoát NamKey, tải file zip mới, giải nén rồi thay
  **NamKey.app** cũ trong thư mục Ứng dụng. Quyền Trợ năng vẫn giữ nguyên.

## Hạn chế đã biết

- Windows: chưa gõ được vào ứng dụng chạy bằng quyền Administrator.
- Thanh địa chỉ của trình duyệt (có gợi ý tự động) đôi khi làm sai chữ.
- Từ tiếng Anh trùng với âm tiết tiếng Việt có thật vẫn được gõ thành tiếng Việt (`this` → thí, `six` → sĩ),
  vì đó cũng là cách gõ tiếng Việt hợp lệ. Khi gõ tiếng Anh, bấm Ctrl+Shift để tắt.
- macOS: chỉ có bản cho máy chip Apple, chưa được Apple công chứng (notarize), chưa tự cài bản cập nhật.
- Chưa có bản cho Linux.

Góp ý hoặc báo lỗi: tạo [issue](https://github.com/luu2nam/namkey/issues) tại đây.

## Pháp lý

- [Giấy phép sử dụng](LICENSE)
- [Điều khoản sử dụng](legal/DIEU-KHOAN-SU-DUNG.md)
- [Chính sách quyền riêng tư](legal/CHINH-SACH-QUYEN-RIENG-TU.md): NamKey không thu thập, không lưu và không gửi
  đi phím bấm hay dữ liệu cá nhân của bạn.
- [Bản quyền và nhãn hiệu](legal/BAN-QUYEN.md)
- [Thông báo phần mềm bên thứ ba](legal/THONG-BAO-BEN-THU-BA.md) · [toàn văn giấy phép](legal/THIRD-PARTY-LICENSES.txt)

NamKey là phần mềm miễn phí, mã nguồn đóng. © 2026 Lưu Hải Nam, giữ mọi quyền · [namlh.net](https://namlh.net)
