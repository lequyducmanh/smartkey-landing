# Landing page Tiền Tiểu Học SmartKey

Trang giới thiệu chương trình tiền tiểu học SmartKey và nhận đăng ký tư vấn cho phụ huynh.
Toàn bộ trang nằm trong một file: `index.html` (không cần cài đặt hay build).

## Xem trang

- Mở `index.html` bằng trình duyệt, hoặc
- Bật GitHub Pages: **Settings → Pages → Source: Deploy from a branch → Branch: `main` / `(root)` → Save**.
  Sau 1–2 phút trang có địa chỉ dạng `https://<tên-tài-khoản>.github.io/<tên-repo>/`.

## Cập nhật thông tin khóa học

Mở `index.html`, tìm `SMARTKEY_CONFIG` (gần cuối file) và sửa các giá trị trong dấu nháy:

| Trường | Ý nghĩa |
|---|---|
| `trangThai` | `'dang-nhan'` · `'danh-sach-cho'` · `'khoa-tiep-theo'` |
| `tenKhoa`, `doiTuong`, `khaiGiang`, `lichHoc`, `diaDiem` | Thông tin khóa sắp khai giảng |
| `hienHocPhi` | `true` hiện học phí · `false` ẩn và mời phụ huynh liên hệ |
| `hocPhi`, `uuDai` | Học phí và ưu đãi (để `''` nếu không có ưu đãi) |
| `soDienThoai`, `zaloUrl` | Số điện thoại và liên kết Zalo chính thức |
| `hienLoiChungThuc` | Chỉ bật `true` khi đã có phản hồi thật được phụ huynh đồng ý |
| `formEndpoint` | Địa chỉ nơi nhận đăng ký (xem bên dưới) |

Không cần sửa phần giao diện. Trên GitHub có thể sửa trực tiếp: mở `index.html` → biểu tượng bút chì → sửa → **Commit changes**.

## Nơi nhận đăng ký

Khi `formEndpoint` để trống, biểu mẫu chạy **chế độ thử**: phụ huynh vẫn thấy lời cảm ơn nhưng **dữ liệu không được lưu**.
Trước khi công khai, điền địa chỉ nhận đăng ký (Google Apps Script, Formspree hoặc máy chủ riêng).
Trang gửi dữ liệu dạng form (POST) với các trường `ten_ba_me`, `so_dien_thoai`, `nam_sinh_con`, `chia_se`, `thoi_gian`, `khoa`, `trang`,
và chỉ báo thành công khi nơi nhận trả về mã 2xx.

## Còn cần SmartKey bổ sung

Các chỗ ghi **[CẦN BỔ SUNG]** trên trang: ảnh thật cô Phượng và lớp học, video, câu chuyện minh chứng,
số điện thoại, liên kết Zalo, nội dung thông báo quyền riêng tư, logo gốc.
Chỗ thay ảnh và video có ghi chú `THAY ẢNH` / `THAY VIDEO` trong `index.html`.
