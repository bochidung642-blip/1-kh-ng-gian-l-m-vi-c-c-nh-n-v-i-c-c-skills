# Không gian làm việc cá nhân với các Skills

> Đây là không gian làm việc cá nhân được xây dựng với 2 skills chạy trên Claude Code.  
> Tài liệu này giải thích mỗi skill làm gì, giúp ích gì, và workflow khi dùng — viết cho người chưa biết lập trình.

---

## Hình dung đơn giản nhất

Hãy tưởng tượng bạn vừa thuê **2 trợ lý riêng** ngồi cùng phòng làm việc với bạn.  
Mỗi người có một chuyên môn rõ ràng, và bạn chỉ cần nói — họ tự làm.

---

## Trợ lý 1 — "Người kết nối"

**Tên skill:** `ket-noi-nen-tang-ngoai`

Mỗi khi bạn cần "đi ra ngoài" lấy thông tin hoặc làm việc với một dịch vụ khác, trợ lý này đứng ra thay bạn.

Trợ lý này biết làm 3 việc:

| Việc | Là gì | Ví dụ thực tế |
|------|-------|--------------|
| **Gọi API** | Kết nối đến dịch vụ bên ngoài để lấy hoặc gửi dữ liệu | Bạn nói "lấy dữ liệu thời tiết hôm nay" → trợ lý tự kết nối dịch vụ thời tiết và trả kết quả về |
| **Dùng MCP** | Cắm thêm "thiết bị ngoại vi" để mở rộng khả năng | Kết nối thêm Google Drive, Notion, Slack → tôi có thể đọc/ghi trực tiếp vào đó thay bạn |
| **Chạy lệnh CLI** | Thực hiện các lệnh máy tính phức tạp thay bạn | Bạn nói "tạo repo GitHub mới" → trợ lý tự chạy lệnh, không cần bạn mở terminal |

### Cấu trúc files hỗ trợ Skill 1

```
skills/ket-noi-nen-tang-ngoai/
├── api/
│   ├── config.json              ← Danh sách API đã cấu hình sẵn
│   └── request-template.json   ← Mẫu để gọi một API mới
├── mcp/
│   └── config.json              ← Danh sách MCP server có thể kết nối
└── cli/
    └── common-commands.md       ← Bộ lệnh CLI phổ biến (GitHub, Google Cloud, AWS, Docker...)
```

---

## Trợ lý 2 — "Người quản lý hồ sơ"

**Tên skill:** `quan-ly-files`

Giữ cho bàn làm việc của bạn gọn gàng — có sẵn biểu mẫu khi cần, và lưu kết quả đúng chỗ sau mỗi công việc.

| Việc | Là gì | Ví dụ thực tế |
|------|-------|--------------|
| **Dùng Templates** | Tủ hồ sơ chứa sẵn các biểu mẫu | Bạn nói "tạo báo cáo tuần" → có ngay bản mẫu, chỉ cần điền thông tin vào |
| **Lưu Outputs** | Mọi kết quả được đặt đúng ngăn, đặt tên theo ngày | Sau mỗi lần chạy Skill 1, kết quả được lưu tự động, không bị lẫn lộn |

### Cấu trúc files hỗ trợ Skill 2

```
skills/quan-ly-files/
├── templates/
│   ├── document-template.md    ← Mẫu tài liệu chung
│   ├── report-template.md      ← Mẫu báo cáo (tuần/tháng/quý)
│   └── api-spec-template.md    ← Mẫu đặc tả khi kết nối API mới
└── outputs/                    ← Nơi lưu kết quả từ các lần chạy
```

---

## Workflow mỗi khi dùng

```
Bạn gõ lệnh
      ↓
/ket-noi-nen-tang-ngoai   hoặc   /quan-ly-files
      ↓
Claude đọc "sổ tay hướng dẫn" của skill đó
      ↓
Claude biết chính xác cần làm gì, lấy template nào, lưu kết quả ở đâu
      ↓
Claude thực hiện → trả kết quả về cho bạn
```

### Ví dụ một lần chạy thực tế

> **Bạn gõ:** `/ket-noi-nen-tang-ngoai` — gọi API thời tiết Hà Nội hôm nay
>
> **Claude làm:**  
> 1. Đọc skill → biết đây là yêu cầu gọi API  
> 2. Lấy cấu hình từ `api/config.json`  
> 3. Gọi request đến dịch vụ thời tiết  
> 4. Nhận dữ liệu về  
> 5. Lưu kết quả vào `outputs/2026-05-11_thoi-tiet.md`  
> 6. Báo cáo cho bạn bằng ngôn ngữ tự nhiên

---

## Tóm lại bằng 1 câu

> **Skill 1 đi ra ngoài lấy thứ bạn cần — Skill 2 giữ cho mọi thứ ngăn nắp trong nhà.**  
> Bạn chỉ cần nói, không cần tự làm gì.

---

## Cấu trúc toàn bộ workspace

```
personal-workspace/
├── README.md                                    ← Bạn đang đọc file này
├── .claude/
│   └── skills/
│       ├── ket-noi-nen-tang-ngoai.md            ← Sổ tay hướng dẫn Skill 1
│       └── quan-ly-files.md                     ← Sổ tay hướng dẫn Skill 2
└── skills/
    ├── ket-noi-nen-tang-ngoai/                  ← Files hỗ trợ Skill 1
    │   ├── api/
    │   ├── mcp/
    │   └── cli/
    └── quan-ly-files/                           ← Files hỗ trợ Skill 2
        ├── templates/
        └── outputs/
```
