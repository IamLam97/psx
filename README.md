# Máy chủ PS4 GoldHEN Exploit

Một máy chủ khai thác PS4 toàn diện, hỗ trợ nhiều phiên bản firmware và tải payload GoldHEN.

## Hệ thống chọn Máy chủ (Host)

Trang chính cung cấp một **bộ chọn máy chủ thống nhất**, nơi người dùng có thể chọn máy chủ phù hợp cho phiên bản firmware PS4 của họ:

| Máy chủ | Phiên bản Firmware | Phương pháp Khai thác |
|------|----------------|----------------|
| **5.05 Host** | 5.05 | Khai thác WebKit + Kernel |
| **6.72 Host** | 6.72 | Khai thác WebKit + Kernel |
| **7.xx - 8.xx Host** | 7.00 - 8.52 | pOOBs4 + Lapse |
| **9.xx Host** | 9.00 - 9.60 | pOOBs4 + Lapse |

> **Tại sao phải tách riêng máy chủ cho 7.xx-8.xx và 9.xx?**
> Mặc dù cả hai dải firmware đều sử dụng chuỗi khai thác pOOBs4 + Lapse, nhưng phương pháp kích hoạt cốt lõi giữa chúng lại khác nhau. Việc tách chúng thành các máy chủ chuyên biệt cho phép tối ưu hóa riêng cho từng phiên bản, mang lại độ ổn định và độ tin cậy tối đa cho mỗi dải firmware.

## Các phiên bản Firmware được hỗ trợ

| Phiên bản Firmware | Phương pháp Khai thác | Thư mục Máy chủ | Trạng thái |
|----------------|----------------|----------------|--------|
| **5.05** | Khai thác WebKit + Kernel | `/505` | ✅ Ổn định |
| **6.72** | Khai thác WebKit + Kernel | `/672` | ✅ Ổn định |
| **7.00 - 7.55** | pOOBs4 + Lapse | `/700` | ✅ Ổn định |
| **8.00 - 8.52** | pOOBs4 + Lapse | `/700` | ✅ Ổn định |
| **9.00 - 9.60** | pOOBs4 + Lapse | `/900` | ✅ Ổn định |

### Các phiên bản cụ thể của Firmware 7.xx - 8.xx
- **7.xx**: 7.00, 7.01, 7.02, 7.50, 7.51, 7.55
- **8.xx**: 8.00, 8.01, 8.03, 8.50, 8.52

### Các phiên bản cụ thể của Firmware 9.xx
- **9.xx**: 9.00, 9.03, 9.04, 9.50, 9.51, 9.60

## Các phiên bản GoldHEN

Tất cả các phiên bản firmware được hỗ trợ hiện đều có **bộ chọn phiên bản GoldHEN**:

| Phiên bản | Mô tả |
|---------|-------------|
| **GoldHEN v2.4b18.10** | Phiên bản mới nhất với các tính năng mới |
| **GoldHEN v2.4b18.5** | Phiên bản ổn định với độ tin cậy tối đa |

Mỗi máy chủ đều bao gồm cả `v2.4b18.10` và `v2.4b18.5` với hệ thống lưu cache độc lập.

## Các Payload hiện có

### Firmware 5.05

| Payload | File | Mô tả |
|---------|------|-------------|
| GoldHEN | goldhen.bin / goldhen5.bin | Kích hoạt Homebrew (v2.4b18.10 / v2.4b18.5) |
| Kernel-Clock | Kernel-Clock.bin | Vá lỗi đồng hồ hệ thống |
| FTP Server | ftp.bin | Truy cập file từ xa |
| PS4Debug | ps4debug.bin | Công cụ gỡ lỗi |
| App2USB | app2usb.bin | Chuyển ứng dụng sang ổ cứng ngoài |
| AppCache Install | appcache-install.bin | Trình cài đặt cache ứng dụng |
| Backup | backup.bin | Sao lưu dữ liệu save |
| Restore | restore.bin | Khôi phục dữ liệu save |
| Disable Updates | disable-updates.bin | Chặn cập nhật hệ thống |
| Enable Updates | enable-updates.bin | Cho phép cập nhật hệ thống |
| History Blocker | history-blocker.bin | Bảo vệ lịch sử trình duyệt |
| PUP Decrypt | pup-decrypt.bin | Giải mã firmware |
| RIF Renamer | rif-renamer.bin | Đổi tên file bản quyền |

### Firmware 6.72

| Payload | File | Mô tả |
|---------|------|-------------|
| GoldHEN | goldhen.bin / goldhen5.bin | Kích hoạt Homebrew (v2.4b18.10 / v2.4b18.5) |
| FTP Server | ftp.bin | Truy cập file từ xa |
| PS4Debug | ps4debug.bin | Công cụ gỡ lỗi |
| App2USB | app2usb.bin | Chuyển ứng dụng sang ổ cứng ngoài |
| AppCache Install | appcache-install.bin | Trình cài đặt cache ứng dụng |
| Backup | backup.bin | Sao lưu dữ liệu save |
| Restore | restore.bin | Khôi phục dữ liệu save |
| Disable Updates | disable-updates.bin | Chặn cập nhật hệ thống |
| Enable Updates | enable-updates.bin | Cho phép cập nhật hệ thống |
| History Blocker | history-blocker.bin | Bảo vệ lịch sử trình duyệt |
| PUP Decrypt | pup-decrypt.bin | Giải mã firmware |
| RIF Renamer | rif-renamer.bin | Đổi tên file bản quyền |

### Firmware 7.xx - 8.xx

| Payload | File | Mô tả |
|---------|------|-------------|
| GoldHEN | goldhen.bin / goldhen5.bin | Kích hoạt Homebrew (v2.4b18.10 / v2.4b18.5) |
| PSFree Fix | ps4-psfree-fix.bin | Bản vá độ ổn định PSFree |
| WebRTE 9.00 | WebRTE_900.bin | Chỉnh sửa theo thời gian thực |
| FTP Server | ftp.bin | Truy cập file từ xa |
| PS4Debug | ps4debug.bin | Công cụ gỡ lỗi |
| App2USB | app2usb.bin | Chuyển ứng dụng sang ổ cứng ngoài |
| AppCache Install | appcache-install.bin | Trình cài đặt cache ứng dụng |
| Backup | backup.bin | Sao lưu dữ liệu save |
| Restore | restore.bin | Khôi phục dữ liệu save |
| Disable Updates | disable-updates.bin | Chặn cập nhật hệ thống |
| Enable Updates | enable-updates.bin | Cho phép cập nhật hệ thống |
| History Blocker | history-blocker.bin | Bảo vệ lịch sử trình duyệt |
| PUP Decrypt | pup-decrypt.bin | Giải mã firmware |
| RIF Renamer | rif-renamer.bin | Đổi tên file bản quyền |

### Firmware 9.xx

| Payload | File | Mô tả |
|---------|------|-------------|
| GoldHEN | goldhen.bin / goldhen5.bin | Kích hoạt Homebrew (v2.4b18.10 / v2.4b18.5) |
| PSFree Fix | ps4-psfree-fix.bin | Bản vá độ ổn định PSFree |
| WebRTE 9.00 | WebRTE_900.bin | Chỉnh sửa theo thời gian thực |
| FTP Server | ftp.bin | Truy cập file từ xa |
| PS4Debug | ps4debug.bin | Công cụ gỡ lỗi |
| App2USB | app2usb.bin | Chuyển ứng dụng sang ổ cứng ngoài |
| AppCache Install | appcache-install.bin | Trình cài đặt cache ứng dụng |
| Backup | backup.bin | Sao lưu dữ liệu save |
| Restore | restore.bin | Khôi phục dữ liệu save |
| Disable Updates | disable-updates.bin | Chặn cập nhật hệ thống |
| Enable Updates | enable-updates.bin | Cho phép cập nhật hệ thống |
| History Blocker | history-blocker.bin | Bảo vệ lịch sử trình duyệt |
| PUP Decrypt | pup-decrypt.bin | Giải mã firmware |
| RIF Renamer | rif-renamer.bin | Đổi tên file bản quyền |

## Các Tối ưu hóa Kỹ thuật

### Phân tách phiên bản để đảm bảo độ ổn định
- **Máy chủ 7.xx-8.xx chuyên biệt** (`/700`) — Được tối ưu hóa đặc biệt cho tiến trình kích hoạt của firmware 7.00–8.52
- **Máy chủ 9.xx chuyên biệt** (`/900`) — Được tối ưu hóa đặc biệt cho tiến trình kích hoạt của firmware 9.00–9.60
- **Script khai thác độc lập** — Mỗi máy chủ sử dụng một chuỗi khai thác, bản vá kernel và ROP gadgets được tinh chỉnh riêng cho dải firmware mục tiêu
- **Giảm tỷ lệ lỗi** — Việc tinh chỉnh theo từng phiên bản giúp loại bỏ sự đánh đổi về tính tương thích chéo giữa các phiên bản

### Ngăn chặn Kernel Panic (Sập nguồn)
- **Tối ưu quản lý bộ nhớ** — Dọn dẹp đúng cách các bộ đệm khai thác sau khi chạy payload
- **Cải thiện thời gian (Timing)** — Tinh chỉnh độ trễ giữa các giai đoạn khai thác để đảm bảo trạng thái kernel ổn định
- **Kiểm soát Garbage collection** — Gọi bộ thu gom rác (GC) có chiến lược để ngăn ngừa hỏng bộ nhớ
- **Nâng cao xử lý lỗi** — Phục hồi an toàn từ các lỗi khai thác cục bộ

### Độ tin cậy của chuỗi khai thác
- **Cải thiện độ ổn định khai thác UAF** — Tinh chỉnh các tham số heap spray để khai thác nhất quán hơn
- **Tối ưu hóa khai thác WebKit** — Giảm thiểu các rủi ro race condition
- **Tinh chỉnh chuỗi Kernel ROP** — Tối ưu hóa các trình tự lập trình return-oriented
- **Cải tiến Payload loader** — Tăng cường khả năng tải file binary với các bài kiểm tra tính toàn vẹn

### Cải tiến Thuật toán
- **Xác minh khai thác đa giai đoạn** — Mỗi giai đoạn đều xác nhận thành công trước khi tiếp tục
- **Logic thử lại tự động** — Các giai đoạn thất bại có thể tự động thử lại mà không cần tải lại toàn bộ trang
- **Nhận diện firmware động** — Tự động chọn đúng offset và bản vá
- **Quản lý phiên bản Cache manifest** — Đảm bảo tính năng ngoại tuyến hoạt động chuẩn xác và ngăn chặn việc chạy mã cũ (stale code)

### Tối ưu hóa GoldHEN
- **Hệ thống tải kép** — BinLoader cục bộ với dự phòng tải trực tuyến
- **Lưu cache độc lập** — Tách biệt file cache manifest cho từng phiên bản GoldHEN
- **Tự động kích hoạt** — Tự động chạy khai thác ở chế độ ngoại tuyến
- **Quản lý luồng (Thread)** — Tối ưu hóa việc chạy payload để ngăn ngừa treo máy

## Hỗ trợ Ngoại tuyến (Offline)

Mỗi máy chủ đều đi kèm các file cache manifest để hoạt động ngoại tuyến:

| Máy chủ | Các file Manifest |
|------|----------------|
| 505 | cache.manifest |
| 672 | cache.manifest |
| 700 | PSPulse.cache (v2.4b18.10), PSPulse5.cache (v2.4b18.5) |
| 900 | PSPulse.manifest (v2.4b18.10), PSPulse5.manifest (v2.4b18.5) |

## Cách sử dụng

1. Lưu trữ các file này trên một web server cục bộ hoặc sử dụng dịch vụ hosting
2. Trên PS4 của bạn, truy cập vào URL của máy chủ bằng trình duyệt web
3. Chọn phiên bản firmware của bạn từ trang chính
4. Chọn phiên bản GoldHEN bạn muốn (v2.4b18.10 hoặc v2.4b18.5)
5. Làm theo hướng dẫn trên màn hình để tải GoldHEN

---

## Nhật ký thay đổi (Changelog)

### v2.4b18.10 — Phiên bản mới nhất

#### Đã cập nhật GoldHEN
- Cập nhật GoldHEN từ **v2.4b18.9** lên **v2.4b18.10** trên tất cả các máy chủ (5.05, 6.72, 7.xx-8.xx, 9.xx)

#### Cải tiến PSFree
- Tích hợp các cải tiến độ ổn định mới nhất của **PSFree 1.7** cho chuỗi khai thác pOOBs4 + Lapse
- Tinh chỉnh thời gian khai thác cho các dải firmware 7.xx–8.xx và 9.xx
- Giảm tỷ lệ lỗi trong quá trình khai thác WebKit và kernel

#### Sửa lỗi (Bug Fixes)
- **Sửa lỗi tải payload trên máy chủ 7.xx-8.xx** — Tất cả các nút payload (PSFree Fix, FTP Server, PS4Debug, v.v.) trước đây không gửi được file nhị phân tới PS4 khi sử dụng đường dẫn trực tuyến (không dùng BinLoader). Hàm `toogle_payload` bị thiếu trong chuỗi khai thác 7.xx-8.xx (`lapse.mjs` / `lapse5.mjs`), gây ra lỗi ngầm. Điều này đã được khắc phục và hiện hoạt động giống với máy chủ 9.xx

#### Cải tiến độ ổn định
- Cải thiện việc dọn dẹp bộ nhớ sau khi chạy payload trên firmware 7.xx-8.xx
- Báo lỗi chi tiết hơn trong đầu ra console của chuỗi khai thác
- Hoạt động của cache ngoại tuyến nhất quán hơn trên tất cả các máy chủ

---

**Tác giả:** [BlackArch](https://t.me/sudoBlackArch)  
**Telegram:** [PlayStation Pulse](https://t.me/PlayStation_Pulse)
