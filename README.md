# Soạn lịch sinh hoạt · CLB Ngoại khoa Trưng Vương

Trang web tĩnh để nhóm trực soạn lịch sinh hoạt hằng tuần và tải ảnh PNG 1080 × 1350 (tỉ lệ 4:5), mang màu và mascot của nhóm trực.

## Trong thư mục này

- `index.html`: toàn bộ trang (giao diện, cách vẽ ảnh, phần soát lỗi).
- `logo.webp`: logo chính thức của CLB.
- `seiryu.webp`, `suzaku.webp`, `byakko.webp`, `genbu.webp`, `kirin.webp`, `koi.webp`: 6 mascot.
- `.nojekyll`: để GitHub Pages phục vụ nguyên trạng các file.

## Đưa lên GitHub Pages

1. Đăng nhập GitHub, bấm **New repository**. Đặt tên, ví dụ `lich-sinh-hoat-nktv`, chọn **Public**, bấm **Create repository**.
2. Trong repo mới, bấm **uploading an existing file** (hoặc **Add file → Upload files**). Kéo toàn bộ file trong thư mục này vào. Bấm **Commit changes**.
   - `.nojekyll` là file ẩn. Máy không hiện file ẩn thì bỏ qua file này, trang vẫn chạy.
3. Vào **Settings → Pages**. Ở mục *Build and deployment*, chọn *Source*: **Deploy from a branch**, *Branch*: **main** và **/ (root)**, bấm **Save**.
4. Chờ 1–2 phút. Trang có địa chỉ dạng `https://<tên-tài-khoản>.github.io/lich-sinh-hoat-nktv/`. Gửi link này cho các nhóm.

## Cập nhật trang

Tải đè file mới vào repo (**Add file → Upload files**) rồi **Commit changes**. Khoảng 1 phút sau trang tự cập nhật; người dùng tải lại trang để thấy bản mới.

## Cách dùng (cho nhóm trực)

1. Chọn nhóm trực.
2. Điền ngày, giờ, địa điểm, các mục chương trình, chủ trì, điều hành.
3. Xem mục **Cần xem lại**, rồi bấm **Tải ảnh PNG**. Trên điện thoại có thêm nút **Chia sẻ ảnh** để lưu vào thư viện ảnh hoặc gửi thẳng qua Zalo, Facebook.

Người trình bày hoặc phụ trách hiện ở dòng dưới nội dung của từng mục. Ô này ghi đúng tên nhóm (Seiryu, Suzaku, Byakko, Genbu, Kirin, Koi) thì ảnh tự gắn mascot nhỏ của nhóm đó.

## Dữ liệu

- Không có máy chủ: mọi thứ chạy trong trình duyệt. Bản nháp chỉ lưu trên máy đang dùng.
- Chuyển cho người khác soạn tiếp: bấm **Lưu bản nháp** (file `.json`), gửi file; người nhận bấm **Mở bản nháp**.
- Repo Public thì ai có link cũng mở được trang và đọc được mã nguồn. Không ghi số điện thoại, email hay thông tin cá nhân vào mã.

## Đổi màu, mascot, logo

- Màu từng nhóm: bảng `THEMES` trong `index.html`; họa tiết nền: bảng `PATTERNS`.
- Ảnh: thay file `.webp` cùng tên, giữ nền trong suốt.
- Font: Be Vietnam Pro, tải từ Google Fonts.
