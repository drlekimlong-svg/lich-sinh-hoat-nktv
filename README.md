# Soạn lịch sinh hoạt · CLB Ngoại khoa Trưng Vương

Trang web tĩnh để nhóm trực soạn lịch và tải ảnh PNG, mang màu và mascot của nhóm trực.

- Hai mẫu: **Lịch sinh hoạt tuần** (nền trắng) và **Chương trình đặc biệt** (cột màu nhóm bên trái, tên chương trình làm tiêu đề, có mô tả ngắn).
- Hai khổ: **bài đăng 4:5** (1080 × 1350) và **story 9:16** (1080 × 1920, chừa khoảng trên và dưới cho thanh của ứng dụng).
- Mã QR tùy chọn: dán link, ảnh tự in mã.
- Nút **Xác nhận và gửi**: tạo file Excel thông tin buổi và gửi cùng ảnh lịch về hộp thư CLB.

## Trong thư mục này

- `index.html`: toàn bộ trang (giao diện, cách vẽ ảnh, phần soát lỗi, thư viện tạo mã QR).
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

1. **Loại lịch.** Chọn lịch tuần hoặc chương trình đặc biệt. Với chương trình đặc biệt, điền tên chương trình; dòng phụ (mùa, tập, chủ đề) và mô tả ngắn nếu có.
2. **Nhóm trực.**
3. **Ngày, giờ, địa điểm.**
4. **Chương trình.** Mỗi mục ghi nội dung, chức danh và họ tên người trình bày, rồi chọn Nhóm, Cố vấn (BCV) hoặc Khách mời. Ảnh in dạng "ThS. BSCK I. Nguyễn Văn A – Cố vấn". Gõ cả cụm "SV. Nguyễn Văn A - Nhóm Kirin" vào ô họ tên thì trang tự tách phần nhóm. Chọn nhóm thì ảnh gắn mascot nhỏ của nhóm đó. Mục tên "Giải lao" được in nghiêng, nhạt hơn.
5. **Chủ trì, điều hành.**
6. **Mã QR (không bắt buộc).** Dán link đăng ký hoặc bài đăng và ghi chú thích ngắn. Link càng ngắn, mã càng dễ quét.
7. Ở khung xem trước, chọn **Bài đăng 4:5** hoặc **Story 9:16**, xem mục **Cần xem lại**, rồi bấm **Tải ảnh PNG**. Trên điện thoại có thêm nút **Chia sẻ ảnh** để lưu vào thư viện ảnh hoặc gửi thẳng qua Zalo, Facebook.
8. Ở khung **Xác nhận và gửi về CLB**, nhập email của bạn rồi bấm **Xác nhận và gửi**. Còn lỗi thì chưa gửi được; còn cảnh báo thì trang hỏi lại một lần. Sửa lịch sau khi gửi thì bấm **Gửi bản cập nhật**.

## Dữ liệu

- Không có máy chủ: mọi thứ chạy trong trình duyệt. Bản nháp chỉ lưu trên máy đang dùng.
- Chuyển cho người khác soạn tiếp: bấm **Lưu bản nháp** (file `.json`), gửi file; người nhận bấm **Mở bản nháp**. Bản nháp lưu từ bản cũ vẫn mở được; tên kiểu "Họ tên - Nhóm Kirin" được tự tách.
- Repo Public thì ai có link cũng mở được trang và đọc được mã nguồn. Không ghi số điện thoại, email hay thông tin cá nhân vào mã.

## Gửi lịch về CLB

Khi bấm **Xác nhận và gửi**, trang tạo file Excel (trang *Buổi sinh hoạt* và trang *Chương trình*) ngay trong trình duyệt, rồi gửi file đó cùng ảnh lịch tới một Google Apps Script của CLB. Script gửi email về hộp thư CLB (bấm Trả lời là trả lời người làm lịch) và ghi buổi đó vào một Google Sheet tổng hợp.

- Mã Apps Script không nằm trong repo này vì có địa chỉ hộp thư nhận. Người quản lý giữ file `Code.gs` riêng.
- Địa chỉ trang nhận đặt ở hằng `SEND_URL` trong `index.html`. Để trống thì nút gửi tắt, người dùng vẫn tải được file Excel.
- Email người làm lịch được nhớ trên máy đang dùng để lần sau khỏi gõ lại; không lưu vào file bản nháp.

## Đổi màu, mascot, logo

- Màu và tên từng nhóm: bảng `THEMES` trong `index.html` (`name` tên in trên ảnh, `ink` màu chữ trên nền trắng, `acc` màu nhấn, `tint` nền nhạt của huy hiệu, `col` màu cột của mẫu chương trình đặc biệt, `colAcc` màu nhấn trên cột, `mode` cách chuyển mascot sang màu trắng).
- Ảnh: thay file `.webp` cùng tên, giữ nền trong suốt. Mascot được chuyển sang một màu ngay trong trình duyệt, không cần thêm file.
- Năm học trên ảnh tự tính theo ngày sinh hoạt: từ tháng 9 trở đi tính sang năm học mới (hàm `schoolYear`).
- Font: Source Serif 4 (tiêu đề), IBM Plex Mono (giờ), Be Vietnam Pro (chữ còn lại), tải từ Google Fonts.
- Mã QR dùng thư viện QR Code Generator của Kazuhiko Arase (giấy phép MIT), đã nhúng sẵn trong `index.html`.
