# 🐱 Nghiêng đầu chọn đáp án – Game ôn tập tiểu học

Game trắc nghiệm vui cho học sinh tiểu học: cả lớp đứng trước camera, **nghiêng đầu sang trái để chọn A, sang phải để chọn B**. Giáo viên tự nhập câu hỏi cho **mọi môn học** (Toán, Tiếng Việt, Tự nhiên – Xã hội, Tiếng Anh…).

- Giao diện chibi dễ thương, có nhân vật mèo đổi biểu cảm, pháo giấy và âm thanh vui.
- Chạy hoàn toàn trên trình duyệt, **không cần máy chủ**, không gửi hình ảnh camera đi đâu cả.
- Nhận diện nhiều bạn cùng lúc: bên nào có nhiều bạn nghiêng hơn sẽ được chọn.

## Cách chơi

1. Mở trang, nhập hoặc chỉnh câu hỏi (mỗi câu gồm: câu hỏi, đáp án đúng, đáp án sai, emoji minh họa tùy chọn).
2. Bấm **Chơi bằng camera** và cho phép trình duyệt dùng camera.
3. Học sinh nghiêng đầu về phía **trái** (A) hoặc **phải** (B) của mình như soi gương, giữ khoảng 1 giây.
4. Không có camera? Bấm **Chơi không camera** hoặc dùng phím `A` / `B` (`Space` để sang câu tiếp).

Có thể dán nhiều câu một lúc, mỗi dòng: `Câu hỏi | Đáp án đúng | Đáp án sai | Emoji`. Dán từ Excel (cột cách nhau bằng Tab) cũng được.

## Triển khai lên GitHub Pages

1. Tạo repository mới trên GitHub (ví dụ `nghieng-dau`), để chế độ **Public**.
2. Tải lên 3 file: `index.html`, `README.md`, `.nojekyll` (kéo thả vào trang repo → **Commit changes**).
3. Vào **Settings → Pages**. Ở mục **Build and deployment**, chọn **Source: Deploy from a branch**, **Branch: main**, thư mục **/ (root)**, rồi **Save**.
4. Đợi 1–2 phút, trang sẽ có địa chỉ: `https://<tên-tài-khoản>.github.io/<tên-repo>/`

> GitHub Pages dùng HTTPS nên trình duyệt cho phép bật camera. Nếu mở file trực tiếp từ máy (`file://`) vẫn chạy được trên Chrome/Edge.

## Yêu cầu

- Trình duyệt Chrome hoặc Edge bản mới, có camera.
- Có Internet khi bật camera lần đầu: trang tải thư viện nhận diện khuôn mặt (MediaPipe Face Landmarker) từ jsDelivr và Google Storage, cùng phông chữ Baloo 2 từ Google Fonts.
- Câu hỏi được lưu trong trình duyệt (`localStorage`) trên từng máy, không đồng bộ giữa các máy.

## Tùy chỉnh

- **Độ nhạy nghiêng** (Cao 8° / Vừa 12° / Thấp 18°), **số giây mỗi câu**, **đọc to** và **trộn câu** chỉnh ngay trong trang.
- Bộ câu hỏi mẫu nằm ở biến `DEF` trong `index.html`; sửa biến này nếu muốn đổi bộ câu mặc định cho tất cả máy.
- Thời gian giữ để chốt đáp án là hằng số `HOLD` (mili giây) trong `index.html`.

## Tác giả

Thầy Hợi · Trường Tiểu học Bảo Đài số 2 - TP Bắc Ninh · 0967 834 824
