# Thông báo phần mềm bên thứ ba

NamKey được xây dựng với sự giúp đỡ của nhiều dự án mã nguồn mở. Xin cảm ơn tác giả của các dự án này.

Tất cả thành phần bên thứ ba trong NamKey đều dùng giấy phép **dễ dãi** (permissive), như MIT, Apache 2.0,
BSD, ISC, Zlib, Unicode, Boost, CDLA-Permissive. Phông chữ dùng SIL Open Font License và Ubuntu Font
Licence. Không có thành phần nào dùng giấy phép copyleft như GPL, LGPL hay MPL.

## Thành phần chính

| Thành phần | Dùng để | Giấy phép |
|---|---|---|
| [egui / eframe](https://github.com/emilk/egui) | Giao diện cửa sổ cài đặt | MIT hoặc Apache 2.0 |
| [winit](https://github.com/rust-windowing/winit), glutin | Tạo cửa sổ, OpenGL | Apache 2.0 |
| glow | Vẽ đồ hoạ | MIT, Apache 2.0 hoặc Zlib |
| [AccessKit](https://github.com/AccessKit/accesskit) | Hỗ trợ trình đọc màn hình | MIT hoặc Apache 2.0 |
| [windows-sys](https://github.com/microsoft/windows-rs) | Gọi API Windows | MIT hoặc Apache 2.0 |
| [objc2](https://github.com/madsmtm/objc2) (objc2-app-kit, objc2-foundation, block2, dispatch2) | Gọi API macOS (AppKit, Foundation) | MIT; một số gói MIT, Apache 2.0 hoặc Zlib |
| core-foundation, core-graphics | Gọi API macOS cho cửa sổ cài đặt | MIT hoặc Apache 2.0 |
| [ureq](https://github.com/algesten/ureq) | Kết nối HTTPS để kiểm tra cập nhật | MIT hoặc Apache 2.0 |
| [rustls](https://github.com/rustls/rustls) | Mã hoá TLS | Apache 2.0, ISC hoặc MIT |
| ring | Thuật toán mã hoá | Apache 2.0 và ISC |
| rustls-webpki | Kiểm tra chứng chỉ | ISC |
| webpki-roots | Danh sách chứng chỉ gốc | CDLA-Permissive 2.0 |
| [serde_json](https://github.com/serde-rs/json) | Đọc dữ liệu từ GitHub | MIT hoặc Apache 2.0 |
| [sha2](https://github.com/RustCrypto/hashes) | Kiểm tra mã SHA-256 của tệp tải về | MIT hoặc Apache 2.0 |
| ICU4X (icu_*) | Xử lý tên miền quốc tế | Unicode 3.0 |
| embed-resource | Nhúng biểu tượng vào tệp chạy (chỉ lúc build) | MIT |

## Phông chữ đi kèm cửa sổ cài đặt

| Phông | Giấy phép |
|---|---|
| Ubuntu Light | Ubuntu Font Licence 1.0 |
| Hack | MIT / Bitstream Vera License |
| Noto Emoji | SIL Open Font License 1.1 |
| emoji-icon-font | MIT |

Cửa sổ cài đặt dùng phông có sẵn của hệ điều hành: Segoe UI trên Windows, Arial trên macOS. Các phông này
không được phân phối kèm NamKey.

## Toàn văn giấy phép

Danh sách đầy đủ 163 thành phần của bản Windows và bản macOS, kèm phiên bản và toàn văn giấy phép của từng
thành phần, có trong tệp **`THIRD-PARTY-LICENSES.txt`**. Tệp này có sẵn trong ứng dụng (Cài đặt → Pháp lý)
và trên github.com/luu2nam/namkey.
