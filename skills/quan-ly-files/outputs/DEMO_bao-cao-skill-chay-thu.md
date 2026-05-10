# Demo chạy thử — Skill Báo cáo

> File này ghi lại toàn bộ quá trình skill `/bao-cao` chạy tạo báo cáo tuần W19  
> Dành cho người muốn hiểu skill hoạt động như thế nào từng bước

---

## Skill nhận lệnh gì?

```
Người dùng nói:
"Tạo báo cáo tuần W19 (05–11/05/2026) với số liệu sau:
- Facebook Ads: 85 leads, CPL 125k, chi phí 10.625.000đ
- Google Ads: 23 leads, CPL 280k, chi phí 6.440.000đ  
- SEO: 12 leads organic
- Email: 8 leads, open rate 31,4%
- Mục tiêu tháng: 600 leads, ≤150k CPL, 45 đăng ký
Tạo cả 2 phiên bản: lãnh đạo và thực thi."
```

---

## Skill đã làm gì từng bước

```mermaid
flowchart TD
    A([Nhận lệnh từ người dùng]) --> B[Đọc skill bao-cao.md\nđể biết cần làm gì]
    B --> C{Loại báo cáo nào?}
    C -->|Tuần + 2 phiên bản| D[Xác định cần\n2 templates]

    D --> E[Đọc template\nbao-cao-tuan-lanh-dao.md]
    D --> F[Đọc template\nbao-cao-tuan-thuc-thi.md]

    E --> G[Phân tích số liệu\ntheo góc nhìn kinh doanh]
    F --> H[Phân tích số liệu\ntheo từng kênh chi tiết]

    G --> I[Viết bản Lãnh đạo\nngôn ngữ kết quả kinh doanh\nngắn - đọc 3 phút]
    H --> J[Viết bản Thực thi\nchi tiết kênh + checklist\nviệc cần làm tuần tới]

    I --> K[(Lưu file output\n2026-05-11_bao-cao-tuan-W19_lanh-dao.md)]
    J --> L[(Lưu file output\n2026-05-11_bao-cao-tuan-W19_thuc-thi.md)]

    K --> M([Báo cáo hoàn thành\ntrong ~3 phút])
    L --> M

    style A fill:#4A90D9,color:#fff
    style M fill:#27AE60,color:#fff
    style K fill:#F39C12,color:#fff
    style L fill:#F39C12,color:#fff
```

---

## Skill đã "nghĩ" khác nhau như thế nào cho 2 phiên bản?

```mermaid
flowchart LR
    DATA["Cùng 1 bộ số liệu\n128 leads / 17tr chi phí\n9 đăng ký / 7 kênh"]

    DATA --> LD["Góc nhìn LÃNH ĐẠO"]
    DATA --> TT["Góc nhìn THỰC THI"]

    LD --> LD1["Đặt câu hỏi:\nMarketing đang đóng góp\ngì cho việc tuyển sinh?"]
    LD --> LD2["Dùng ngôn ngữ:\nHọc viên · Đăng ký\nDoanh thu · Tăng trưởng"]
    LD --> LD3["Kết quả:\n1 trang · 5 phút đọc\nQuyết định cấp cao"]

    TT --> TT1["Đặt câu hỏi:\nKênh nào tốt? Kênh nào\ncần fix? Fix cụ thể gì?"]
    TT --> TT2["Dùng ngôn ngữ:\nCPL · CTR · Open rate\nCampaign · A/B test"]
    TT --> TT3["Kết quả:\nChecklist việc cần làm\nAi làm gì · Deadline"]

    style DATA fill:#4A90D9,color:#fff
    style LD fill:#8E44AD,color:#fff
    style TT fill:#E67E22,color:#fff
```

---

## Kết quả của lần chạy thử này

| | Chi tiết |
|-|---------|
| **Thời gian thực hiện** | ~3 phút |
| **Số files tạo ra** | 2 files báo cáo + 1 file demo này |
| **Phiên bản lãnh đạo** | `2026-05-11_bao-cao-tuan-W19_lanh-dao.md` |
| **Phiên bản thực thi** | `2026-05-11_bao-cao-tuan-W19_thuc-thi.md` |
| **Trạng thái** | Chạy thành công |

---

## Nếu không có skill — quy trình cũ trông như thế nào?

```
Mở Facebook Ads Manager → kéo số → copy sang Excel
     ↓
Mở Google Analytics → kéo số → copy sang Excel  
     ↓
Mở email tool → kéo số → copy sang Excel
     ↓
Ngồi phân tích, viết nhận xét
     ↓
Viết bản lãnh đạo (1 file)
     ↓
Viết lại bản thực thi (1 file khác)
     ↓
Format cho đẹp, gửi đi

Tổng: 2–3 giờ mỗi thứ 2
```

```
Với skill — quy trình mới:

Cung cấp số liệu → Gõ lệnh → Nhận 2 báo cáo hoàn chỉnh

Tổng: ~5 phút nhập số + 3 phút skill chạy = 8 phút
```

---

## Các bước tiếp theo để dùng thật

1. **Kết nối API** (qua Skill 1) để không cần nhập số tay
2. **Chạy mỗi sáng thứ 2** — skill tự kéo số từ tuần trước, tạo báo cáo
3. **Gửi thẳng** bản lãnh đạo cho sếp, bản thực thi cho team

> File này được tạo tự động bởi skill `/bao-cao` | 11/05/2026
