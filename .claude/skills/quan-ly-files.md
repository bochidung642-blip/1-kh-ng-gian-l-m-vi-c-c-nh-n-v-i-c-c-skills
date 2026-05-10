---
name: quan-ly-files
description: Quản lý files và folders trong workspace — lưu templates, tổ chức outputs từ các skill khác
---

# Skill: Quản lý Files và Folders

Skill này quản lý toàn bộ files và folders trong workspace, bao gồm templates tái sử dụng và outputs từ các skill khác.

## Cấu trúc thư mục

```
skills/quan-ly-files/
├── templates/       ← File mẫu tái sử dụng
└── outputs/         ← Kết quả từ các skill khác
```

## 1. Sử dụng Templates

Khi người dùng cần tạo file mới từ mẫu:

1. Liệt kê các template có sẵn trong `skills/quan-ly-files/templates/`
2. Đọc template phù hợp
3. Điền thông tin cụ thể vào
4. Lưu file đã điền vào vị trí người dùng chỉ định hoặc vào `outputs/`

**Các template có sẵn:**
- `document-template.md` — Template tài liệu chung
- `report-template.md` — Template báo cáo
- `api-spec-template.md` — Template đặc tả API

## 2. Lưu Outputs

Khi một skill khác tạo ra kết quả:

1. Xác định loại output (log, report, data, v.v.)
2. Đặt tên file theo format: `YYYY-MM-DD_ten-mo-ta.extension`
3. Lưu vào `skills/quan-ly-files/outputs/`
4. Cập nhật index nếu có `outputs/INDEX.md`

**Quy tắc đặt tên:**
- Log kết nối: `YYYY-MM-DD_connection-log.md`
- Báo cáo: `YYYY-MM-DD_report-ten.md`
- Data export: `YYYY-MM-DD_data-ten.json`

## 3. Tổ chức và dọn dẹp

Khi workspace trở nên lộn xộn:

1. Đọc toàn bộ `outputs/` và `templates/`
2. Nhóm các file liên quan
3. Tạo subfolder nếu cần
4. Xóa file cũ hơn 30 ngày trong `outputs/` (hỏi user trước)

## 4. Tạo template mới

Khi người dùng muốn thêm template:

1. Tạo file trong `skills/quan-ly-files/templates/`
2. Đặt tên rõ ràng: `ten-muc-dich-template.extension`
3. Thêm header mô tả mục đích và cách dùng vào đầu file
