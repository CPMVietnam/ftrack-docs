---
title: Danh sách nhân viên/Tài khoản
description: Hướng dẫn tạo và quản lý tài khoản nhân viên thị trường trên Ftrack
---

# Danh sách nhân viên/Tài khoản

Hướng dẫn tạo tài khoản đăng nhập cho nhân viên thị trường để họ có thể sử dụng ứng dụng Ftrack Mobile.

## Truy cập chức năng

<!-- TODO: screenshot - Menu điều hướng đến mục Danh sách nhân viên -->

**Bước 1:** Từ menu, vào **Chuẩn bị dữ liệu** → **Danh sách nhân viên/Tài khoản**

## Tạo tài khoản từng người

<!-- TODO: screenshot - Form tạo tài khoản mới -->

**Bước 2:** Nhấn **Thêm mới** để tạo tài khoản cho một nhân viên

**Bước 3:** Điền thông tin:

| Trường | Mô tả | Bắt buộc |
|--------|-------|----------|
| Họ tên | Tên đầy đủ của nhân viên | Có |
| Email | Dùng để đăng nhập | Có |
| Số điện thoại | <!-- TODO: verify --> | Không |
| Vai trò | Nhân viên / Supervisor / Admin | Có |
| Khu vực phụ trách | <!-- TODO: verify --> | Không |

**Bước 4:** Nhấn **Lưu** — hệ thống sẽ gửi email kích hoạt tài khoản cho nhân viên

## Import tài khoản theo file (nhiều người)

<!-- TODO: screenshot - Nút tải template tài khoản -->

**Bước 2 (thay thế):** Nhấn **Tải template** → Điền danh sách nhân viên → **Upload & Import**

!!! tip "Mẹo"
    Dùng cách import file khi cần tạo nhiều tài khoản cùng lúc (ví dụ: đầu dự án).

## Phân quyền và vai trò

<!-- TODO: screenshot - Màn hình cài đặt vai trò/quyền -->

<!-- TODO: verify - mô tả chi tiết các vai trò: Admin, Supervisor, Field Staff -->

Ftrack hỗ trợ các vai trò sau:
- **Admin**: toàn quyền quản trị hệ thống
- **Supervisor**: xem báo cáo, quản lý nhân viên trong khu vực
- **Nhân viên thị trường**: sử dụng app mobile để thực hiện visit

## Cập nhật và vô hiệu hóa tài khoản

<!-- TODO: screenshot - Nút sửa / vô hiệu hóa tài khoản -->

Để **sửa thông tin**: nhấn biểu tượng chỉnh sửa trên dòng tài khoản tương ứng

Để **vô hiệu hóa tài khoản**: nhấn biểu tượng khóa — nhân viên sẽ không thể đăng nhập nhưng dữ liệu lịch sử vẫn được lưu
