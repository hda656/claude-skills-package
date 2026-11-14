---
name: emenu-gitbook-blueprint
description: 'Sinh bộ tài liệu chuẩn "E-Menu Project Blueprint" của F2Tech để đưa lên GitBook — hồ sơ tư vấn và quản lý dự án E-Menu dùng từ buổi họp khách hàng đầu tiên đến khi bàn giao. Dùng skill này BẤT CỨ KHI NÀO người dùng muốn (1) tạo tài liệu blueprint, hồ sơ tư vấn, hoặc tài liệu kickoff cho một dự án E-Menu hoặc F&B mới; (2) tạo bộ khung GitBook theo cấu trúc chuẩn Overview · Các mô hình hoạt động · Giao diện chi tiết · Quy trình · Nền tảng kỹ thuật · Các thay đổi; (3) nhắc tới "blueprint", "tài liệu dự án E-Menu", "hồ sơ tư vấn khách hàng", "workflow theo mô hình kinh doanh", "bộ design system E-Menu", hay "áp dụng cấu trúc tài liệu như dự án trước" — kể cả khi không nói rõ chữ "skill" hay "GitBook". Cũng dùng để sinh bộ template có sẵn chỗ dán hình để điền dần. Đây là bản cập nhật thay cho skill cũ emenu-project-blueprint (đổi thứ tự nhóm, thêm mục Bộ design system, dùng cú pháp GitBook-native).'
---

# E-Menu Project Blueprint — GitBook (F2Tech)

## Skill này làm gì

Sinh ra một bộ tài liệu markdown chuẩn GitBook cho một dự án E-Menu của F2Tech. Bộ tài liệu là **hồ sơ tư vấn + quản lý dự án**: mang đi họp khách hàng lần đầu để tư vấn giải pháp, chọn mô hình vận hành phù hợp, chốt phạm vi/tính năng/timeline, rồi dùng luôn để theo dõi dự án đến khi nghiệm thu và lưu trữ.

Bộ template gốc (27 file `.md` + 1 ảnh placeholder) nằm ở `assets/template/`, đã dùng **cú pháp GitBook-native** (front-matter, `<figure>`, `{% hint %}`, bảng `<table>`) nên push thẳng lên repo Git đã sync với GitBook là hiển thị đúng ngay. Nhiệm vụ khi dùng skill là **copy template làm điểm khởi đầu rồi tùy biến theo dự án cụ thể** — không viết lại từ đầu.

## Ẩn dụ nền tảng: chuẩn bị dự án xây nhà

Toàn bộ tài liệu bám theo một ẩn dụ xuyên suốt, phải giữ nguyên khi trình bày với khách — đây là điều làm tài liệu dễ hiểu với khách không rành kỹ thuật:

| Ẩn dụ xây nhà              | Tương ứng trong tài liệu                                     |
| ------------------------- | ------------------------------------------------------------ |
| Mẫu nhà / bản vẽ công năng | Các mô hình hoạt động (workflow), Giao diện chi tiết          |
| Vật liệu xây dựng         | Phần cứng (QR, POS, máy in, tablet)                          |
| Cấu trúc nhà              | Cơ sở dữ liệu (phần mềm hứng dữ liệu)                        |
| Nền móng, điện nước       | Cơ sở hạ tầng (server, cloud, network)                      |
| Bản vẽ thi công & tiến độ | Quy trình triển khai, Timeline                              |
| Biên bản phát sinh khi xây | Các thay đổi (Change Log, yêu cầu mở rộng)                   |

## Cấu trúc chuẩn (6 nhóm, đúng thứ tự này)

Sidebar GitBook (`SUMMARY.md`) luôn theo đúng thứ tự 6 nhóm:

```
Trang bìa (README.md)   — bảng "Thông tin dự án" + mục đích tài liệu

## Overview
  1. Tổng quan dự án        — mô tả, mô hình KD, output/outcome (+ link demo/Figma)
  2. Đối tượng sử dụng       — thực khách, nhân viên, thu ngân, bếp/bar, quản lý
  3. Phạm vi dự án           — trong / ngoài phạm vi / mở rộng Phase 2
  4. Tính năng               — checklist tính năng, Problems–How to solve
  5. Nguyên tắc thiết kế & UX

## Các mô hình hoạt động
  Workflow (README)          — bảng chọn mô hình + bảng "câu hỏi tư vấn nhanh"
    + 9 trang mô hình con

## Giao diện chi tiết
  Giao diện E-menu (Mobile)  — từng màn hình: ảnh + Mục đích + Thành phần chính + hint xác nhận
  Giao diện E-menu (Tablet)  — cùng cấu trúc, bản tablet

## Quy trình
  1. Quy trình triển khai   — bảng các phase
  2. Vai trò                 — + danh sách liên hệ dự án
  3. Timeline                — ước lượng theo gói + Gantt thực tế

## Nền tảng kỹ thuật
  1. Phần cứng               — vật liệu
  2. Cơ sở dữ liệu           — cấu trúc nhà
  3. Cơ sở hạ tầng           — nền móng
  4. Bộ design system        — Color, Typography, Spacing, Grid, Iconography

## Các thay đổi
  1. Quản lý sự thay đổi     — Change Log
  2. Yêu cầu mở rộng         — Change Request / Phase 2
```

9 mô hình workflow (cố định, mỗi mô hình 1 trang con): Casual Dining · Cafe/trà sữa · Quán phở/mì/bún · Lẩu/nướng/buffet · Nhà hàng cao cấp · Chuỗi nhà hàng · Nhà hàng có Loyalty · Nhà hàng muốn tăng Tip · Lo rủi ro Order từ xa.

## Quy ước trình bày (bắt buộc giữ nhất quán)

**Ngôn ngữ:** Tiếng Việt. Thuật ngữ nghiệp vụ giữ nguyên (workflow, upsell, loyalty, POS, course...).

**Độ dài:** Mỗi trang ngắn, đọc nhanh, chốt nhanh. Ưu tiên bảng và checklist hơn văn xuôi dài.

**Cú pháp GitBook-native (bắt buộc dùng):**

- Front-matter mô tả trang (tùy chọn) ở đầu file:
  ```
  ---
  description: 'Mô tả ngắn 1 dòng'
  ---
  ```
- Callout cho phần cần khách xác nhận / ghi chú nổi bật:
  ```
  {% hint style="info" %}
  **Cần khách xác nhận:** ...
  {% endhint %}
  ```
- Bảng dùng cú pháp `<table>` của GitBook khi cần cột ẩn (`data-hidden`) hoặc set độ rộng cột (`width`); bảng đơn giản dùng markdown table thường cũng được.
- Ảnh cạnh nhau: bọc nhiều `<figure>` trong một `<div>`.

**Chỗ dán ảnh — dùng một ảnh placeholder no-image:** mọi vị trí ảnh đều để sẵn khối `<figure>` trỏ tới `no-image.png` kèm figcaption "Dán ảnh vào đây", để trên GitBook hiển thị một ô ảnh xám rõ ràng — người dùng chỉ việc thay ảnh thật vào. Chọn đúng độ sâu đường dẫn theo vị trí file:

```
Root (README.md):          <figure><img src=".gitbook/assets/no-image.png" alt=""><figcaption>Dán ảnh vào đây</figcaption></figure>
Thư mục cấp 1:             <figure><img src="../.gitbook/assets/no-image.png" alt=""><figcaption>Dán ảnh vào đây</figcaption></figure>
Thư mục cấp 2 (workflow):  <figure><img src="../../.gitbook/assets/no-image.png" alt=""><figcaption>Dán ảnh vào đây</figcaption></figure>
```

Ảnh `no-image.png` nằm ở `assets/template/.gitbook/assets/no-image.png` — giữ nguyên, tất cả trang dùng chung.

**Cấu trúc chuẩn cho mỗi trang mô hình workflow:**
Mục tiêu → Phù hợp với → Workflow tổng quan (ảnh no-image) → Tính năng bắt buộc → Tính năng tùy chọn → Cơ chế an toàn → Giá trị mang lại → Ảnh hưởng đến timeline.
(Riêng "Nhà hàng cao cấp" và "Loyalty" có thêm mục "Các bước chính" ngay sau Workflow tổng quan.)

**Cấu trúc chuẩn cho mỗi màn hình trong Giao diện chi tiết:**
Tiêu đề màn hình → ảnh no-image → **Mục đích** → **Thành phần chính** → (tùy chọn) `{% hint %}` **Cần khách xác nhận**.

## Quy trình làm việc khi dùng skill

1. **Hỏi thông tin dự án trước khi sinh file:** tên khách hàng, mô hình kinh doanh, và mô hình workflow nào là trọng tâm. Nếu người dùng chưa cung cấp, hỏi ngắn gọn.
2. **Outline trước, chờ duyệt, rồi mới tạo file.** Đây là nhịp làm việc ưa thích: tóm tắt cấu trúc bằng gạch đầu dòng, xác nhận với người dùng, sau đó mới sinh file. Đừng tạo file vội nếu chưa được duyệt.
3. **Copy template rồi tùy biến:** dùng `assets/template/` làm điểm khởi đầu. Điền tên khách hàng + bảng "Thông tin dự án" vào trang bìa; nếu dự án chỉ dùng một số mô hình workflow, có thể lược bớt các trang mô hình không liên quan (và cập nhật `SUMMARY.md` tương ứng).
4. **Giữ nguyên khối ảnh no-image** — người dùng sẽ tự thay ảnh thật trên GitBook sau. Không xóa `no-image.png`.
5. **Đóng gói:** nén thư mục thành `.zip` để import vào GitBook (qua Git Sync hoặc copy-paste thủ công), rồi trả file cho người dùng qua `present_files`.

## Cách dùng template trong assets

`assets/template/` chứa bộ đầy đủ đã điền nội dung mẫu cho cả 9 mô hình + bộ design system chuẩn. Hai cách dùng:

- **Tạo bộ mới cho một dự án:** copy toàn bộ template, đổi thông tin trang bìa (`[TÊN KHÁCH HÀNG]`, bảng Thông tin dự án), tinh chỉnh nội dung theo mô hình kinh doanh của khách, cập nhật color/typography trong "Bộ design system" theo brand khách, lược bớt mô hình không dùng nếu cần.
- **Tạo bộ template để điền dần:** giữ nguyên nội dung mẫu (đã đủ tốt làm khung), chỉ cần đóng gói và giao.

Các placeholder trong template dùng dạng `[...]` (VD `[TÊN KHÁCH HÀNG]`, `[Họ tên]`, `[Dán link Figma]`) — tìm và thay khi tùy biến.

Khi lược bớt trang, luôn cập nhật `SUMMARY.md` để sidebar GitBook không trỏ tới file không tồn tại.

## Cách import vào GitBook

- **Git Sync (khuyến nghị):** push toàn bộ nội dung thư mục template (gồm cả `.gitbook/assets/`) lên repo Git đã kết nối với space GitBook. `SUMMARY.md` tự thành sidebar. Lưu ý sync hai chiều: nếu khách chỉnh trực tiếp trên GitBook, GitBook sẽ commit ngược về repo.
- **Thủ công:** copy nội dung từng file `.md` dán vào từng trang tương ứng trên GitBook UI, và upload ảnh thật thay cho các ô no-image.
