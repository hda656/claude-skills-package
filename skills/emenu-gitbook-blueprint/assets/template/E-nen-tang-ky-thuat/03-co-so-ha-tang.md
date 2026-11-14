# 3. Cơ sở hạ tầng

_Ẩn dụ: đây là "nền móng, điện nước" — hạ tầng kỹ thuật vận hành phía sau hệ thống._

## Hạ tầng hệ thống

| Thành phần | Mô tả | Trạng thái |
|---|---|---|
| Server | Local / Cloud | |
| Database | Lưu menu, order, phiên bàn | |
| API | Kết nối E-Menu với POS/hệ thống khác | |
| Mạng nội bộ / Internet | Đảm bảo kết nối ổn định tại địa điểm | |
| Môi trường Test | Dùng để kiểm thử trước khi golive | |
| Môi trường Production | Vận hành thực tế | |

## Sơ đồ kiến trúc hệ thống

<figure><img src="../.gitbook/assets/no-image.png" alt=""><figcaption>Dán ảnh vào đây</figcaption></figure>

> _Loại hình: Architecture diagram (server, database, API, thiết bị) · Kích thước đề xuất: 1600 × 900px_

## Ghi chú

- Xác nhận băng thông mạng tại địa điểm triển khai (đặc biệt với mô hình nhiều bàn/đông khách).
- Xác nhận phương án backup dữ liệu.
