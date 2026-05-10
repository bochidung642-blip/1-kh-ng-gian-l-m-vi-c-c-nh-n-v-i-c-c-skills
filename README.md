# Không gian làm việc cá nhân với các Skills

Personal workspace sử dụng Claude Code skill system.

## Cấu trúc

```
personal-workspace/
├── .claude/
│   └── skills/
│       ├── ket-noi-nen-tang-ngoai.md    ← Skill 1: Kết nối API / MCP / CLI
│       └── quan-ly-files.md             ← Skill 2: Quản lý files & folders
└── skills/
    ├── ket-noi-nen-tang-ngoai/          ← Files hỗ trợ Skill 1
    │   ├── api/
    │   │   ├── config.json
    │   │   └── request-template.json
    │   ├── mcp/
    │   │   └── config.json
    │   └── cli/
    │       └── common-commands.md
    └── quan-ly-files/                   ← Files hỗ trợ Skill 2
        ├── templates/
        │   ├── document-template.md
        │   ├── report-template.md
        │   └── api-spec-template.md
        └── outputs/                     ← Kết quả từ các skill
```

## Cách dùng

### Kích hoạt Skill 1 — Kết nối nền tảng ngoài
```
/ket-noi-nen-tang-ngoai
```
Hỗ trợ gọi REST API, cấu hình MCP Server, và chạy CLI tools (gh, gcloud, aws, docker).

### Kích hoạt Skill 2 — Quản lý files
```
/quan-ly-files
```
Tạo file từ template, lưu output, tổ chức workspace.

## Cấu hình

- Credentials/API keys: dùng biến môi trường, **không commit vào git**
- MCP servers mới: xem hướng dẫn trong `skills/ket-noi-nen-tang-ngoai/mcp/config.json`
