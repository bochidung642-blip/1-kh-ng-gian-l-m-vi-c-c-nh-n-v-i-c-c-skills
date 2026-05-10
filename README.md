# Không gian làm việc cá nhân với các Skills

> Workspace chạy trên Claude Code với 2 skills — viết cho người chưa biết lập trình.

---

## Toàn cảnh workspace

```mermaid
mindmap
  root((Workspace của bạn))
    Skill 1 - Người kết nối
      Gọi API
        Lấy hoặc gửi dữ liệu từ dịch vụ ngoài
      MCP Server
        Cắm thêm công cụ
        Google Drive - Notion - Slack
      CLI Tools
        Chạy lệnh máy tính
        GitHub - AWS - Docker
    Skill 2 - Người quản lý hồ sơ
      Templates
        Mẫu tài liệu
        Mẫu báo cáo
        Mẫu đặc tả API
      Outputs
        Lưu kết quả đúng chỗ
        Đặt tên theo ngày
```

---

## 2 Trợ lý trong workspace

### Trợ lý 1 — Người kết nối
*Đi ra ngoài lấy thứ bạn cần*

| Khả năng | Bạn nói gì | Trợ lý làm gì |
|----------|-----------|--------------|
| Gọi API | "Lấy dữ liệu thời tiết Hà Nội" | Kết nối dịch vụ thời tiết, trả kết quả về |
| MCP Server | "Đọc file trong Google Drive của tôi" | Cắm kết nối Drive, đọc file thay bạn |
| CLI Tools | "Tạo repo GitHub mới tên ABC" | Chạy lệnh `gh repo create ABC` thay bạn |

### Trợ lý 2 — Người quản lý hồ sơ
*Giữ cho mọi thứ ngăn nắp trong nhà*

| Khả năng | Bạn nói gì | Trợ lý làm gì |
|----------|-----------|--------------|
| Templates | "Tạo báo cáo tuần cho tôi" | Lấy mẫu sẵn có, điền thông tin, xuất file |
| Lưu Outputs | *(tự động)* | Đặt tên file theo ngày, lưu đúng ngăn |

---

## Workflow khi dùng

```mermaid
flowchart TD
    A([Bạn gõ lệnh skill]) --> B{Muốn làm gì?}

    B -->|Lấy dữ liệu ngoài| C[Skill 1 - ket-noi-nen-tang-ngoai]
    B -->|Tạo file từ mẫu| D[Skill 2 - quan-ly-files]

    C --> C1{Loại kết nối}
    C1 -->|API| C2[Gọi HTTP request đến dịch vụ ngoài]
    C1 -->|MCP| C3[Dùng công cụ đã cắm sẵn]
    C1 -->|CLI| C4[Chạy lệnh máy tính]

    D --> D1[Chọn template phù hợp]
    D1 --> D2[Điền thông tin vào mẫu]

    C2 --> E[(Lưu vào outputs/)]
    C3 --> E
    C4 --> E
    D2 --> E

    E --> F([Báo cáo cho bạn bằng ngôn ngữ tự nhiên])

    style A fill:#4A90D9,color:#fff
    style F fill:#27AE60,color:#fff
    style E fill:#F39C12,color:#fff
```

---

## Ví dụ thực tế từng bước

```mermaid
sequenceDiagram
    actor Bạn
    participant S1 as Skill 1 - Người kết nối
    participant S2 as Skill 2 - Người quản lý
    participant Out as outputs/

    Bạn->>S1: Gọi API thời tiết Hà Nội
    S1->>S1: Đọc config API
    S1->>S1: Gọi request đến dịch vụ
    S1->>S2: Trả kết quả thô
    S2->>Out: Lưu 2026-05-11_thoi-tiet.md
    S2->>Bạn: Báo cáo bằng tiếng Việt dễ hiểu
```

---

## Cấu trúc thư mục

```
personal-workspace/
│
├── .claude/skills/
│   ├── ket-noi-nen-tang-ngoai.md   ← Sổ tay hướng dẫn Skill 1
│   └── quan-ly-files.md            ← Sổ tay hướng dẫn Skill 2
│
└── skills/
    ├── ket-noi-nen-tang-ngoai/
    │   ├── api/         ← Cấu hình & mẫu gọi API
    │   ├── mcp/         ← Danh sách MCP server
    │   └── cli/         ← Bộ lệnh CLI phổ biến
    └── quan-ly-files/
        ├── templates/   ← Biểu mẫu tái sử dụng
        └── outputs/     ← Kết quả từ các lần chạy
```

---

> **Tóm lại:** Skill 1 đi ra ngoài lấy thứ bạn cần — Skill 2 giữ cho mọi thứ ngăn nắp trong nhà.  
> Bạn chỉ cần nói, không cần tự làm gì.
