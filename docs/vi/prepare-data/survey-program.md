---
title: Tạo bộ câu hỏi/Chương trình khảo sát
description: Hướng dẫn tạo chương trình và cấu hình bộ câu hỏi Survey trên Ftrack
---

# Tạo bộ câu hỏi/Chương trình khảo sát

Hướng dẫn tạo một chương trình khảo sát (Program) và cấu hình bộ câu hỏi (Survey) mà nhân viên thị trường sẽ thực hiện tại điểm bán.

## Truy cập chức năng

<!-- TODO: screenshot - Menu điều hướng đến mục Chương trình khảo sát -->

**Bước 1:** Từ menu, vào **Chuẩn bị dữ liệu** → **Chương trình khảo sát**

## Tạo chương trình mới

<!-- TODO: screenshot - Form tạo chương trình mới -->

**Bước 2:** Nhấn **Tạo chương trình mới**

**Bước 3:** Điền thông tin chương trình:

| Trường | Mô tả |
|--------|-------|
| Tên chương trình | Tên hiển thị trên app |
| Mô tả | Mô tả ngắn về mục tiêu chương trình |
| Thời gian bắt đầu / kết thúc | Khoảng thời gian hiệu lực |
| Loại chương trình | <!-- TODO: verify các loại chương trình --> |

## Cấu hình bộ câu hỏi (Survey)

<!-- TODO: screenshot - Giao diện thêm câu hỏi vào chương trình -->

**Bước 4:** Trong phần **Bộ câu hỏi**, nhấn **Thêm câu hỏi**

**Bước 5:** Chọn loại câu hỏi:

| Loại | Mô tả |
|------|-------|
| Câu hỏi Có/Không | Trả lời Yes/No |
| Câu hỏi chọn một | Multiple choice, chọn 1 đáp án |
| Câu hỏi chọn nhiều | Multiple choice, chọn nhiều đáp án |
| Câu hỏi nhập số | Nhập giá trị số (số lượng, doanh số...) |
| Câu hỏi nhập văn bản | Nhập văn bản tự do |
| Câu hỏi chụp ảnh | Yêu cầu nhân viên chụp ảnh |

<!-- TODO: screenshot - Ví dụ một câu hỏi đã được cấu hình -->

## Cài đặt điểm số và trọng số

<!-- TODO: screenshot - Giao diện cài đặt điểm số -->
<!-- TODO: verify - Ftrack có hỗ trợ tính điểm tự động không -->

**Bước 6:** Đặt điểm số cho từng câu hỏi (nếu cần tính tổng điểm đánh giá)

## Đặt điều kiện bắt buộc

<!-- TODO: screenshot - Cài đặt câu hỏi bắt buộc vs không bắt buộc -->

**Bước 7:** Đánh dấu các câu hỏi **Bắt buộc** — nhân viên sẽ không thể Check Out nếu chưa trả lời

## Lưu và kích hoạt chương trình

<!-- TODO: screenshot - Nút lưu và kích hoạt -->

**Bước 8:** Nhấn **Lưu** để lưu nháp, hoặc **Kích hoạt** để chương trình sẵn sàng sử dụng

!!! info "Thông tin"
    Sau khi kích hoạt, chương trình sẽ xuất hiện trong danh sách lựa chọn khi tạo Visit Plan.
