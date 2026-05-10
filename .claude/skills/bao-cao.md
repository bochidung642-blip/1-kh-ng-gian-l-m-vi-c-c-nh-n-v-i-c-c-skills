---
name: bao-cao
description: Tạo báo cáo tuần và tháng với 2 phiên bản — ban lãnh đạo và nhóm thực thi — cho Marketing Executive trong ngành giáo dục
---

# Skill: Hệ thống Báo cáo Marketing

Skill này tạo ra 2 loại báo cáo × 2 phiên bản = 4 dạng tài liệu khác nhau.

## Khi nào dùng loại nào

| Người dùng nói | Loại báo cáo | Template dùng |
|---------------|-------------|--------------|
| "báo cáo tuần cho sếp / ban lãnh đạo" | Tuần - Lãnh đạo | `reports/bao-cao-tuan-lanh-dao.md` |
| "báo cáo tuần cho team / nhân sự" | Tuần - Thực thi | `reports/bao-cao-tuan-thuc-thi.md` |
| "báo cáo tháng cho sếp / ban lãnh đạo" | Tháng - Lãnh đạo | `reports/bao-cao-thang-lanh-dao.md` |
| "báo cáo tháng cho team / nhân sự" | Tháng - Thực thi | `reports/bao-cao-thang-thuc-thi.md` |

## Quy trình tạo báo cáo

### Bước 1 — Xác định loại báo cáo
Hỏi người dùng nếu chưa rõ:
- Báo cáo tuần hay tháng?
- Phiên bản lãnh đạo hay thực thi?
- Có số liệu sẵn không hay cần kéo từ API?

### Bước 2 — Thu thập số liệu
Nếu có kết nối API (qua skill ket-noi-nen-tang-ngoai):
- Facebook Ads: leads mới, chi phí, CPL, CTR, ROAS
- Google Analytics: sessions, conversion rate, top landing pages
- Email: open rate, click rate, unsubscribe rate
- Google Search Console: impressions, clicks, top keywords

Nếu người dùng cung cấp số liệu thủ công:
- Nhận số và điền vào template tương ứng

### Bước 3 — Phân tích và điền template
Đọc template từ `skills/quan-ly-files/templates/reports/`

**Với phiên bản Lãnh đạo:**
- Dùng ngôn ngữ kết quả kinh doanh (doanh thu, học viên, tăng trưởng)
- Không dùng thuật ngữ marketing kỹ thuật (CPL, CTR, ROAS)
- Luôn kết nối số liệu marketing với mục tiêu tuyển sinh của trường
- Phần hành động: chiến lược cấp cao, không đi vào chi tiết thực thi

**Với phiên bản Thực thi:**
- Dùng số liệu cụ thể theo từng kênh
- Phân tích rõ từng chiến dịch: tốt / chưa tốt / nguyên nhân
- Hành động phải cụ thể: ai làm gì, deadline khi nào
- Tone thẳng thắn, không cần làm mượt như bản lãnh đạo

### Bước 4 — Lưu file
Lưu vào `skills/quan-ly-files/outputs/` theo format:
- Tuần: `YYYY-MM-DD_bao-cao-tuan-W[so]_[lanh-dao|thuc-thi].md`
- Tháng: `YYYY-MM_bao-cao-thang_[lanh-dao|thuc-thi].md`

### Bước 5 — Xuất bản
Hỏi người dùng muốn:
- Đọc trực tiếp trong chat
- Copy để dán vào Google Docs / Notion
- Tạo file markdown để chia sẻ

## Lưu ý quan trọng

- Phiên bản lãnh đạo: tối đa 1 trang đọc — ngắn, súc tích, có thể đọc trong 3 phút
- Phiên bản thực thi: chi tiết, có checklist hành động cụ thể
- Luôn so sánh với kỳ trước (tuần trước / tháng trước) nếu có dữ liệu
- Khi kết quả không tốt: đưa ra 2-3 giả thuyết nguyên nhân, không chỉ nêu số
