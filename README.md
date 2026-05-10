# 🎓 Marketing Workspace — Trung tâm Anh ngữ

> Workspace của **Leader Marketer** · Trung tâm Anh ngữ · Chạy trên Claude Code  
> Tối ưu cho 2 sản phẩm: **Tiếng Anh Giao Tiếp** (người đi làm) & **Luyện thi IELTS** (HS · SV)

**Xem nhanh:** [2 Skills](#-2-skills-cốt-lõi) · [Templates](#-hệ-thống-4-templates-báo-cáo) · [Workflow](#-workflow-hàng-tuần--sáng-thứ-2) · [Demo output](#-output-thực-tế) · [Dùng ngay](#-dùng-ngay)

---

## 🗺️ Toàn cảnh

```mermaid
mindmap
  root((Marketing Workspace))
    San pham
      Tieng Anh Giao Tiep
        Nguoi di lam 25-40 tuoi
        B2C va B2B doanh nghiep
      Luyen thi IELTS
        Hoc sinh SV 16-22 tuoi
        Hop tac truong Dai hoc
    Kenh tiep can
      Online
        Facebook & Instagram Ads
        TikTok Ads
        Google Ads & SEO
      Offline & B2B
        Hop tac truong Dai hoc
        Dao tao nhan su doanh nghiep
    2 Skills
      Skill 1 Ket noi nen tang
        REST API
        CLI Tools
      Skill 2 Quan ly ho so
        4 Templates bao cao
        Outputs theo ngay
    KPI theo doi
      Leads theo tung khoa
      CPL theo kenh
      Hoc thu ra dang ky
      Lap day lop hoc
```

---

## 📦 2 Sản phẩm · 3 Kênh tiếp cận

```mermaid
flowchart LR
    subgraph SP ["📦 2 Sản phẩm"]
        GT["🗣️ Giao Tiếp\nNgười đi làm 25–40"]
        IE["📝 IELTS\nHS · SV 16–22"]
    end

    subgraph ON ["🌐 Online"]
        FB["Facebook & Instagram"]
        TT["TikTok Ads"]
        GG["Google Ads & SEO"]
    end

    subgraph OF ["🤝 Offline & B2B"]
        DH["Trường Đại học"]
        DN["Doanh nghiệp"]
    end

    FB --> GT
    FB --> IE
    TT --> IE
    GG --> GT
    GG --> IE
    DH --> IE
    DN --> GT

    style SP fill:#EBF5FB,stroke:#2E86C1
    style ON fill:#EAFAF1,stroke:#1E8449
    style OF fill:#FEF9E7,stroke:#F39C12
```

---

## ⚡ 2 Skills cốt lõi

| | 🔗 Skill 1 | 📁 Skill 2 |
|--|-----------|-----------|
| **Vai trò** | Người kết nối | Người quản lý hồ sơ |
| **Làm gì** | Kéo số từ tất cả kênh về 1 chỗ | Giữ template & lưu output đúng chỗ |
| **Gọi bằng** | `/ket-noi-nen-tang-ngoai` | `/quan-ly-files` |
| **Phục vụ** | Báo cáo · Phân tích · So sánh kênh | Brief · Kết quả · Tài liệu đối tác |

---

## 🔗 Skill 1 — Kết nối nền tảng

```mermaid
flowchart TD
    S1["🔗 Skill 1"]

    S1 --> ON["🌐 Online"]
    S1 --> OF["🤝 Offline & B2B"]

    ON --> FB["Facebook & Instagram\nLeads · CPL · ROAS theo khoá"]
    ON --> TT["TikTok Ads\nIELTS segment · Views · CTR"]
    ON --> GG["Google Ads & SEO\nSearch intent · Conversion rate"]

    OF --> DH["Trường Đại học\nSV tiếp cận · Tỷ lệ quan tâm IELTS"]
    OF --> DN["Doanh nghiệp\nNhân sự đăng ký · Fill rate B2B"]

    style S1 fill:#2E86C1,color:#fff
    style ON fill:#1E8449,color:#fff
    style OF fill:#E67E22,color:#fff
```

| Bạn nói | Skill làm |
|---------|----------|
| _"Leads tuần này theo từng khoá và từng kênh"_ | Kéo FB + TikTok + Google → tách IELTS vs Giao Tiếp |
| _"So sánh CPL online vs offline tháng này"_ | Tổng hợp chi phí · CPL từng nguồn · highlight bất thường |
| _"Hiệu quả hợp tác trường ĐH tháng này"_ | Tổng hợp leads offline · so sánh CPL với online |

---

## 📁 Skill 2 — Quản lý hồ sơ

```mermaid
flowchart LR
    S2["📁 Skill 2"]

    S2 --> T["🗂️ templates/"]
    S2 --> O["💾 outputs/"]

    T --> R["reports/\n4 templates báo cáo"]
    T --> B["Brief chiến dịch\nOnline · Offline · B2B"]
    T --> P["Tài liệu đối tác\nProposal trường ĐH · DN"]

    O --> O1["Lưu theo ngày & khoá\nTìm lại trong vài giây"]

    style S2 fill:#1E8449,color:#fff
    style T fill:#F39C12,color:#fff
    style O fill:#27AE60,color:#fff
```

---

## 📋 Hệ thống 4 Templates báo cáo

```mermaid
flowchart TD
    ROOT["📋 Hệ thống báo cáo\n2 loại × 2 phiên bản = 4 templates"]

    ROOT --> TU["📅 Báo cáo TUẦN\nCập nhật mỗi thứ 2"]
    ROOT --> TH["📆 Báo cáo THÁNG\nTổng kết & chiến lược"]

    TU --> TUL["👔 Phiên bản Lãnh đạo\nbao-cao-tuan-lanh-dao.md"]
    TU --> TUT["👥 Phiên bản Thực thi\nbao-cao-tuan-thuc-thi.md"]

    TH --> THL["👔 Phiên bản Lãnh đạo\nbao-cao-thang-lanh-dao.md"]
    TH --> THT["👥 Phiên bản Thực thi\nbao-cao-thang-thuc-thi.md"]

    TUL --> C1["KPI vs mục tiêu · 2 khoá\nẢnh hưởng tuyển sinh\nHành động tuần tới"]
    TUT --> C2["Số theo kênh · theo khoá\nTốt / chưa tốt / nguyên nhân\nChecklist cụ thể"]
    THL --> C3["Kết quả kinh doanh\nĐóng góp doanh thu\nChiến lược tháng tới"]
    THT --> C4["Phân tích sâu từng kênh\nStop · Continue · Start\nPhân bổ ngân sách"]

    style ROOT fill:#4A90D9,color:#fff
    style TU fill:#8E44AD,color:#fff
    style TH fill:#8E44AD,color:#fff
    style TUL fill:#2E86C1,color:#fff
    style TUT fill:#E67E22,color:#fff
    style THL fill:#2E86C1,color:#fff
    style THT fill:#E67E22,color:#fff
```

| Template | Đọc trong | Ai đọc | Nội dung chính |
|----------|----------|--------|---------------|
| `bao-cao-tuan-lanh-dao.md` | 3 phút | Ban lãnh đạo | KPI · 2 khoá · ảnh hưởng phòng ban |
| `bao-cao-tuan-thuc-thi.md` | 10 phút | Team marketing | Số theo kênh · tốt/chưa tốt · checklist |
| `bao-cao-thang-lanh-dao.md` | 5 phút | Ban lãnh đạo | Kết quả tháng · chiến lược tháng tới |
| `bao-cao-thang-thuc-thi.md` | 15 phút | Team marketing | Phân tích sâu · Stop/Continue/Start |

---

## 📅 Workflow theo mùa tuyển sinh

```mermaid
flowchart LR
    T2["📅 Tháng 2–3\nSau Tết"] --> T4["📅 Tháng 3–4\nTrước thi IELTS"] --> T8["📅 Tháng 8–9\nĐầu năm học"] --> T10["📅 Tháng 9–10\nTrước thi IELTS"]
```

| Đợt | Ưu tiên khoá | Kênh đẩy mạnh | Hành động chính |
|-----|-------------|--------------|----------------|
| **Tháng 2–3** (Sau Tết) | 🗣️ Giao Tiếp | Facebook · Google | Người đi làm đặt mục tiêu năm mới |
| **Tháng 3–4** (Trước IELTS) | 📝 IELTS | TikTok · SEO · ĐH | HS-SV chuẩn bị kỳ thi quốc tế |
| **Tháng 8–9** (Đầu năm học) | Cả 2 khoá | Tất cả kênh | Tăng ngân sách · Hợp tác doanh nghiệp |
| **Tháng 9–10** (Trước IELTS) | 📝 IELTS | Retarget · Lookalike | Học viên đã đậu làm social proof |

---

## 🔄 Workflow hàng tuần — Sáng thứ 2

```mermaid
flowchart TD
    A(["⏰ Sáng thứ 2"]) --> B["🔗 Skill 1 kéo số toàn kênh"]
    B --> C["Tách: Giao Tiếp vs IELTS\nOnline vs Offline"]
    C --> D["📁 Skill 2 lấy template"]
    D --> E["⚙️ Sinh báo cáo\n2 khoá × 2 phiên bản"]
    E --> F["👔 Bản Lãnh đạo\nKPI · Doanh thu · Kế hoạch"]
    E --> G["👥 Bản Thực thi\nSố kênh · Tốt/Chưa · Checklist"]
    F --> H(["✅ Gửi trong ~5 phút"])
    G --> H

    style A fill:#4A90D9,color:#fff
    style H fill:#27AE60,color:#fff
    style C fill:#E67E22,color:#fff
    style E fill:#8E44AD,color:#fff
```

---

## 📊 Ví dụ thực tế — Báo cáo tuần W19

> **Số liệu thực chạy:** FB 85 · TikTok 23 · Google 20 · Offline/ĐH 12 · Tổng **140 leads**

**So sánh 2 khoá:**

| KPI | 🗣️ Giao Tiếp | 📝 IELTS | Ghi chú |
|-----|------------|--------|---------|
| Leads tuần | 59 | 81 | IELTS cao — gần mùa thi T3-4 |
| CPL trung bình | 132.000đ | 124.000đ | Cả 2 dưới ngưỡng 150k ✅ |
| Leads offline (ĐH · DN) | 8 | 4 | Giao Tiếp từ DN · IELTS từ ĐH |
| Học thử → đăng ký | 9,1% | 6,8% | Giao Tiếp convert tốt hơn |
| Lấp đầy lớp | 78% | 65% | IELTS cần đẩy thêm |

```mermaid
sequenceDiagram
    actor B as 👤 Leader Marketer
    participant S1 as 🔗 Skill 1
    participant S3 as ⚙️ Skill Báo cáo
    participant S2 as 📁 Skill 2

    B->>S3: Báo cáo W19 — 2 khoá · lãnh đạo + team
    S3->>S1: Kéo số online và offline tuần 05-11/05
    S1-->>S3: IELTS 81 leads - FB+TikTok+GG+ĐH
    S1-->>S3: Giao Tiếp 59 leads - FB+GG+DN
    S3->>S2: Lấy 2 template báo cáo
    S2-->>S3: bao-cao-tuan-lanh-dao + bao-cao-tuan-thuc-thi
    S3->>S3: Phân tích · so sánh 2 khoá · viết nhận xét
    S3->>S2: Lưu 2 file output
    S2-->>B: W19_lanh-dao.md và W19_thuc-thi.md ✅
```

---

## 📂 Output thực tế

> Tất cả file kết quả nằm trong [`skills/quan-ly-files/outputs/`](skills/quan-ly-files/outputs/)

| File | Mô tả |
|------|-------|
| [`DEMO_bao-cao-skill-chay-thu.md`](skills/quan-ly-files/outputs/DEMO_bao-cao-skill-chay-thu.md) | Giải thích từng bước skill chạy như thế nào |
| [`2026-05-11_bao-cao-tuan-W19_lanh-dao.md`](skills/quan-ly-files/outputs/2026-05-11_bao-cao-tuan-W19_lanh-dao.md) | Báo cáo W19 — phiên bản ban lãnh đạo |
| [`2026-05-11_bao-cao-tuan-W19_thuc-thi.md`](skills/quan-ly-files/outputs/2026-05-11_bao-cao-tuan-W19_thuc-thi.md) | Báo cáo W19 — phiên bản nhóm thực thi |

---

## ⏱️ Trước & Sau khi có Skills

| Công việc | ⏰ Trước | ⚡ Sau |
|-----------|---------|-------|
| Tổng hợp số online + offline 2 khoá | 45 phút | Tự động |
| Báo cáo lãnh đạo (2 khoá) | 75 phút | 0 phút |
| Báo cáo team thực thi | 75 phút | 0 phút |
| Brief chiến dịch + proposal đối tác | 60 phút | 15 phút |
| **Tổng / tuần** | **~4.5 giờ** | **~15 phút** |

---

## 💡 Token & Lợi ích

```mermaid
flowchart LR
    T["Token tiết kiệm\nnhờ 2 Skills"] --> A["Hướng dẫn viết 1 lần\ndùng mãi\n~1.200 token/lần"]
    T --> B["Template sẵn\nkhông sinh từ đầu\n~400 token/lần"]
    T --> C["Đúng ngay lần đầu\nkhông sửa lại\n~1.200 token/lần"]
```

| | Không có Skills | Có Skills | Tiết kiệm |
|--|----------------|-----------|----------|
| Giải thích 2 khoá · 3 kênh · 2 phiên bản | ~1.200 token | ~0 token | ~1.200 token |
| Sinh sai format · làm lại | ~1.200 token | ~0 token | ~1.200 token |
| Sinh đúng ngay lần đầu | — | ~800 token | — |
| **Tổng / lần báo cáo** | **~3.400 token** | **~800 token** | **~76%** |

> 📅 **8 báo cáo/tháng** (4 tuần × 2 phiên bản): ~27.200 → ~6.400 token · **Tiết kiệm ~20.800 token/tháng**

| | Lợi ích | Với trung tâm Anh ngữ |
|-|---------|----------------------|
| 🎯 | **Nhất quán** | Báo cáo 2 khoá cùng format · so sánh dễ qua các tuần |
| 📈 | **Tích luỹ** | Kho lịch sử leads theo mùa thi · benchmark năm sau |
| 🤝 | **Chia sẻ** | Proposal trường ĐH · brief agency dùng chung template |
| 🧩 | **Mở rộng** | Thêm khoá TOEIC · Business English → thêm template là xong |

---

## 🚀 Dùng ngay

```bash
# Báo cáo tuần — 2 khoá · online + offline
/bao-cao  Báo cáo W20 cho lãnh đạo.
          IELTS: FB 52 leads, TikTok 19 leads, Google 14 leads, ĐH 6 leads. CPL 124k.
          Giao Tiếp: FB 38 leads, Google 16 leads, DN 8 leads. CPL 132k.

# So sánh hiệu quả kênh
/ket-noi-nen-tang-ngoai  So sánh CPL và tỷ lệ chuyển đổi
                          online vs offline tháng 5, tách riêng IELTS và Giao Tiếp.

# Brief chiến dịch mùa thi IELTS
/quan-ly-files  Tạo brief IELTS tháng 9. Target HS-SV thi tháng 10-11.
                Kênh: Facebook + TikTok + SEO + trường ĐH. Ngân sách 50tr.

# Proposal đào tạo doanh nghiệp
/quan-ly-files  Tạo proposal Tiếng Anh Giao Tiếp cho doanh nghiệp 50-200 nhân sự.
```

---

## 📂 Cấu trúc file

```
personal-workspace/
│
├── 📋 README.md
│
├── 🧠 .claude/skills/
│   ├── ket-noi-nen-tang-ngoai.md    ← FB · TikTok · Google · Offline tracking
│   ├── quan-ly-files.md             ← Template theo khoá · kênh · mùa tuyển sinh
│   └── bao-cao.md                   ← Báo cáo × 2 khoá × 2 phiên bản
│
└── 💪 skills/
    ├── 🔗 ket-noi-nen-tang-ngoai/
    │   ├── api/     Facebook · TikTok · Google Analytics config
    │   ├── mcp/     Google Sheets — tracking offline leads
    │   └── cli/     gh · export data tools
    │
    └── 📁 quan-ly-files/
        ├── templates/
        │   ├── document-template.md
        │   ├── report-template.md
        │   ├── api-spec-template.md
        │   └── reports/
        │       ├── bao-cao-tuan-lanh-dao.md      ← KPI · 2 khoá · online+offline
        │       ├── bao-cao-tuan-thuc-thi.md      ← Phân tích kênh · checklist
        │       ├── bao-cao-thang-lanh-dao.md     ← Chiến lược · mùa tuyển sinh
        │       └── bao-cao-thang-thuc-thi.md     ← Stop · Continue · Start
        └── outputs/
            ├── DEMO_bao-cao-skill-chay-thu.md
            ├── 2026-05-11_bao-cao-tuan-W19_lanh-dao.md
            └── 2026-05-11_bao-cao-tuan-W19_thuc-thi.md
```

---

<div align="center">

**🗣️ Tiếng Anh Giao Tiếp · 📝 Luyện thi IELTS**  
**🌐 Online · 🤝 Offline · 🏢 B2B Doanh nghiệp**

*Skill 1 kéo số từ mọi kênh · Skill 2 giữ template & lưu kết quả · Bạn chỉ cần ra quyết định*

</div>
