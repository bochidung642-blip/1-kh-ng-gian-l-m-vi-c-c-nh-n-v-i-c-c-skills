# 🧠 Personal Workspace với Skills

> Workspace cá nhân chạy trên **Claude Code** · 2 skills cốt lõi · Tự động hoá công việc lặp lại · Không cần biết lập trình

**Dành cho:** [Non-tech](#-2-skills--nhin-nhanh) · [Tech](#-cau-truc-file) · [Xem demo](#-vi-du-thuc-te-bao-cao-tuan) · [Dùng ngay](#-dung-ngay)

---

## 🗺️ Toàn cảnh

```mermaid
mindmap
  root((Workspace))
    Skill 1
      Nguoi ket noi
        REST API
        MCP Server
        CLI Tools
    Skill 2
      Nguoi quan ly ho so
        SKILL.md
        templates
        outputs
    Ung dung thuc te
      Bao cao tuan
        Phien ban lanh dao
        Phien ban thuc thi
      Bao cao thang
        Phien ban lanh dao
        Phien ban thuc thi
```

---

## ⚡ 2 Skills — Nhìn nhanh

| | 🔗 Skill 1 | 📁 Skill 2 |
|--|-----------|-----------|
| **Tên** | Người kết nối | Người quản lý hồ sơ |
| **Làm gì** | Đi ra ngoài lấy thứ bạn cần | Giữ mọi thứ ngăn nắp trong nhà |
| **Gọi bằng** | `/ket-noi-nen-tang-ngoai` | `/quan-ly-files` |
| **Khả năng** | REST API · MCP · CLI | Templates · Outputs |
| **File định nghĩa** | `.claude/skills/ket-noi-nen-tang-ngoai.md` | `.claude/skills/quan-ly-files.md` |

---

## 🔗 Skill 1 — Người kết nối

```mermaid
flowchart LR
    S1["🔗 Skill 1"]

    S1 --> A["🌐 REST API\nGọi dịch vụ bên ngoài\nqua đường dẫn HTTP"]
    S1 --> B["🔌 MCP Server\nCắm thêm công cụ\nvào workspace"]
    S1 --> C["⌨️ CLI Tools\nChạy lệnh máy tính\nthay bạn"]

    A --> A1["Facebook Ads\nGoogle Analytics\nEmail Marketing"]
    B --> B1["Google Drive\nNotion · Slack"]
    C --> C1["GitHub · AWS\nDocker · npm"]
```

| Bạn nói | Skill làm |
|---------|----------|
| _"Lấy số liệu Facebook Ads tuần này"_ | Tự kết nối API · kéo leads, CPL, chi phí về |
| _"Tạo repo GitHub mới tên ABC"_ | Tự chạy `gh repo create ABC` |
| _"Đọc file trong Google Drive của tôi"_ | Dùng MCP Drive · đọc và trả nội dung về |

---

## 📁 Skill 2 — Người quản lý hồ sơ

```mermaid
flowchart LR
    S2["📁 Skill 2"]

    S2 --> T["🗂️ templates/\nTủ biểu mẫu"]
    S2 --> O["💾 outputs/\nNgăn lưu kết quả"]

    T --> T1["Mẫu tài liệu\nMẫu báo cáo\nMẫu đặc tả API\nMẫu báo cáo tuần/tháng"]
    O --> O1["Tên file theo ngày\nYYYY-MM-DD_ten.md\nTìm lại dễ dàng"]
```

| Bạn nói | Skill làm |
|---------|----------|
| _"Tạo báo cáo tháng cho lãnh đạo"_ | Lấy đúng mẫu · điền số · xuất file |
| _"Tìm báo cáo tuần W19 tháng 5"_ | Tìm trong `outputs/` · trả file đúng |
| _"Tạo template mới cho brief video"_ | Tạo file mẫu · lưu vào `templates/` |

---

## 🔄 Workflow — 2 Skills phối hợp

```mermaid
flowchart TD
    U(["👤 Bạn nói lệnh"])

    U --> S1["🔗 Skill 1\nNgười kết nối"]
    U --> S2["📁 Skill 2\nNgười quản lý"]

    S1 --> D1["Dữ liệu từ bên ngoài\nFacebook · Google · Email"]
    S2 --> D2["Template phù hợp\nđã có sẵn cấu trúc"]

    D1 --> W["⚙️ Xử lý & tổng hợp"]
    D2 --> W

    W --> OUT["📄 Kết quả hoàn chỉnh"]
    OUT --> S2
    S2 --> SAVE[("💾 Lưu vào outputs/\nđặt tên theo ngày")]

    SAVE --> U2(["✅ Bạn nhận kết quả"])

    style U fill:#4A90D9,color:#fff
    style U2 fill:#27AE60,color:#fff
    style W fill:#8E44AD,color:#fff
    style SAVE fill:#E67E22,color:#fff
```

---

## 📊 Ví dụ thực tế: Báo cáo tuần

> **Tình huống:** Tạo báo cáo tuần W19 (05–11/05/2026) với 2 phiên bản cho lãnh đạo và nhóm thực thi

```mermaid
sequenceDiagram
    actor B as 👤 Bạn
    participant S1 as 🔗 Skill 1
    participant S3 as ⚙️ Skill Báo cáo
    participant S2 as 📁 Skill 2
    participant O as 💾 outputs/

    B->>S3: Tạo báo cáo tuần W19 cho lãnh đạo và team
    S3->>S1: Lấy số liệu tuần 05-11/05
    S1-->>S3: 128 leads · 17tr chi phí · 9 đăng ký
    S3->>S2: Lấy template báo cáo lãnh đạo
    S2-->>S3: bao-cao-tuan-lanh-dao.md
    S3->>S3: Viết bản lãnh đạo - ngôn ngữ kinh doanh
    S3->>S2: Lấy template báo cáo thực thi
    S2-->>S3: bao-cao-tuan-thuc-thi.md
    S3->>S3: Viết bản thực thi - phân tích chi tiết kênh
    S3->>O: Lưu 2 file báo cáo hoàn chỉnh
    O-->>B: 2026-05-11_bao-cao-tuan-W19_lanh-dao.md
    O-->>B: 2026-05-11_bao-cao-tuan-W19_thuc-thi.md
```

### ⏱️ Trước & Sau

| Công việc | ⏰ Trước | ⚡ Sau |
|-----------|---------|-------|
| Kéo số từ 4 tool | 45 phút | Tự động |
| Viết báo cáo lãnh đạo | 60 phút | 0 phút |
| Viết báo cáo thực thi | 60 phút | 0 phút |
| Lưu đúng chỗ · đúng tên | 5 phút | Tự động |
| **Tổng mỗi thứ 2** | **~2.5 giờ** | **~5 phút** |

📂 **Xem output thực tế:**
[DEMO — Giải thích quá trình chạy](skills/quan-ly-files/outputs/DEMO_bao-cao-skill-chay-thu.md) ·
[Báo cáo W19 — Lãnh đạo](skills/quan-ly-files/outputs/2026-05-11_bao-cao-tuan-W19_lanh-dao.md) ·
[Báo cáo W19 — Thực thi](skills/quan-ly-files/outputs/2026-05-11_bao-cao-tuan-W19_thuc-thi.md)

---

## 💡 Token & Lợi ích

### 🔋 Tiết kiệm token

> **Token** = nhiên liệu để Claude chạy. Skills lưu sẵn hướng dẫn → không cần giải thích lại → không tốn token lặp

| | Không có skills | Có skills | Tiết kiệm |
|--|----------------|-----------|----------|
| Giải thích format & quy tắc | ~800 token | ~0 token | ~800 token |
| Sinh output sai · phải làm lại | ~1.200 token | ~0 token | ~1.200 token |
| Sinh output đúng ngay lần đầu | — | ~800 token | — |
| **Tổng / lần** | **~3.000 token** | **~800 token** | **~73%** |

> 📅 **4 báo cáo/tháng:** ~12.000 token → ~3.200 token · **Tiết kiệm ~8.800 token/tháng**

### 🎯 Lợi ích khác

| | Lợi ích | Kết quả |
|-|---------|--------|
| 🎯 | **Nhất quán** | Cùng 1 format mọi lần · không lệch chuẩn |
| 📈 | **Tích luỹ** | Mỗi lần chạy để lại 1 file · kho lịch sử tự xây |
| 🧩 | **Mở rộng** | Thêm skill mới chồng lên · không xây lại từ đầu |
| 👥 | **Chia sẻ** | Team clone repo là dùng được · không cần giải thích |

---

## 🚀 Dùng ngay

**Cú pháp:** `/[tên-skill]` + mô tả việc muốn làm

```bash
# Lấy dữ liệu từ nền tảng ngoài
/ket-noi-nen-tang-ngoai  Lấy số liệu Facebook Ads tuần này

# Tạo tài liệu từ template
/quan-ly-files  Tạo báo cáo tháng 5 cho lãnh đạo

# Tìm lại file cũ
/quan-ly-files  Tìm báo cáo tuần W19 tháng 5

# Dùng cả 2 skills — chỉ cần mô tả việc muốn làm
Tạo báo cáo tuần W20 cho cả lãnh đạo và team.
Số liệu: Facebook 92 leads 11tr, Google 18 leads 5tr, Email open rate 28%
```

---

## 📂 Cấu trúc file

```
personal-workspace/
│
├── 📋 README.md
│
├── 🧠 .claude/skills/                        ← Não của từng skill
│   ├── ket-noi-nen-tang-ngoai.md             ← Skill 1: sổ tay hướng dẫn
│   ├── quan-ly-files.md                      ← Skill 2: sổ tay hướng dẫn
│   └── bao-cao.md                            ← Skill ứng dụng (báo cáo)
│
└── 💪 skills/                                ← Tay chân của từng skill
    ├── 🔗 ket-noi-nen-tang-ngoai/
    │   ├── api/        config · request-template
    │   ├── mcp/        config
    │   └── cli/        common-commands
    │
    └── 📁 quan-ly-files/
        ├── templates/  document · report · api-spec
        │   └── reports/  bao-cao-tuan/thang × lanh-dao/thuc-thi
        └── outputs/    ← Kết quả từ các lần chạy skill
```

---

<div align="center">

**🔗 Skill 1 đi ra ngoài lấy thứ bạn cần**  
**📁 Skill 2 giữ cho mọi thứ ngăn nắp trong nhà**  
**Bạn chỉ cần nói — không cần tự làm bước nào**

</div>
