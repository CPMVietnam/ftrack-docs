---
title: Danh sách điểm bán
description: Hướng dẫn import danh sách điểm bán/cửa hàng vào hệ thống Ftrack
---

# Danh sách điểm bán

Hướng dẫn import danh sách điểm bán (cửa hàng, đại lý, siêu thị...) vào hệ thống Ftrack để làm cơ sở cho Visit Plan và các chương trình khảo sát.

## Truy cập chức năng

<!-- TODO: screenshot - Menu điều hướng đến mục Danh sách điểm bán -->

**Bước 1:** Từ menu, vào **Chuẩn bị dữ liệu** → **Danh sách điểm bán**

## Tải file template

<!-- TODO: screenshot - Nút tải template trên màn hình danh sách điểm bán -->

**Bước 2:** Nhấn **Tải template mẫu** để tải file Excel về máy

!!! info "Thông tin"
    Luôn dùng template mới nhất tải từ hệ thống. Không dùng template cũ hoặc tự tạo file.

## Điền thông tin vào file

<!-- TODO: screenshot - Ví dụ file Excel đã điền thông tin điểm bán -->

**Bước 3:** Mở file template và điền thông tin cho từng điểm bán:

| Cột | Mô tả | Bắt buộc |
|-----|-------|----------|
| Mã điểm bán | Mã định danh duy nhất | Có |
| Tên điểm bán | Tên cửa hàng/đại lý | Có |
| Địa chỉ | Địa chỉ đầy đủ | Có |
| Tỉnh/Thành phố | <!-- TODO: verify các cột bắt buộc --> | Có |
| Khu vực | Vùng địa lý | Không |
| Kinh độ / Vĩ độ | Tọa độ GPS | Không |

!!! warning "Lưu ý"
    - Không xóa hoặc thay đổi dòng tiêu đề (header row)
    - Mã điểm bán phải là duy nhất trong toàn bộ file
    - Tránh ký tự đặc biệt trong các ô dữ liệu

## Upload file lên hệ thống

<!-- TODO: screenshot - Giao diện upload file -->

**Bước 4:** Quay lại hệ thống, nhấn **Chọn file** và upload file Excel đã điền

**Bước 5:** Nhấn **Import** để bắt đầu quá trình import

## Kiểm tra kết quả import

<!-- TODO: screenshot - Màn hình kết quả import (số lượng thành công/lỗi) -->

**Bước 6:** Xem kết quả import:
- **Thành công**: số bản ghi được thêm vào hệ thống
- **Lỗi**: danh sách các dòng bị lỗi và nguyên nhân

!!! tip "Mẹo"
    Nếu có bản ghi lỗi, tải file log lỗi về, sửa trong file template rồi import lại chỉ phần lỗi.

## Xem danh sách điểm bán đã import

<!-- TODO: screenshot - Danh sách điểm bán trong hệ thống sau khi import -->

Sau khi import thành công, danh sách điểm bán sẽ xuất hiện trong hệ thống và có thể được dùng để tạo Visit Plan.
