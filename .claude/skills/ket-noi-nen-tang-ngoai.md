---
name: ket-noi-nen-tang-ngoai
description: Kết nối và tương tác với các nền tảng bên ngoài qua REST API, MCP Server, và CLI tools
---

# Skill: Kết nối nền tảng ngoài

Skill này hỗ trợ 3 loại kết nối: REST API, MCP Server, và CLI Tools.

## 1. REST API

Khi người dùng yêu cầu gọi API bên ngoài:

1. Đọc file cấu hình tại `skills/ket-noi-nen-tang-ngoai/api/config.json`
2. Dùng template tại `skills/ket-noi-nen-tang-ngoai/api/request-template.json` để định dạng request
3. Thực hiện gọi API bằng `curl` hoặc code phù hợp với ngôn ngữ đang dùng
4. Lưu kết quả vào `skills/quan-ly-files/outputs/` nếu cần

**Các bước xử lý:**
- Xác định endpoint, method (GET/POST/PUT/DELETE), headers, body
- Kiểm tra authentication (Bearer token, API key, Basic auth)
- Xử lý response và error handling
- Log kết quả nếu cần debug

## 2. MCP Server

Khi người dùng muốn kết nối MCP:

1. Đọc cấu hình tại `skills/ket-noi-nen-tang-ngoai/mcp/config.json`
2. Kiểm tra MCP server đã được khai báo trong `.claude/settings.json` chưa
3. Hướng dẫn user thêm MCP nếu chưa có
4. Sử dụng tool của MCP server đó trong conversation

**Ví dụ cấu hình MCP cần thêm vào settings.json:**
```json
{
  "mcpServers": {
    "ten-mcp": {
      "command": "npx",
      "args": ["-y", "@ten-package/mcp-server"],
      "env": {}
    }
  }
}
```

## 3. CLI Tools

Khi người dùng muốn chạy CLI:

1. Tham khảo danh sách CLI phổ biến tại `skills/ket-noi-nen-tang-ngoai/cli/common-commands.md`
2. Xác nhận tool đã được cài đặt (`gh --version`, `gcloud version`, v.v.)
3. Chạy lệnh phù hợp qua Bash tool
4. Lưu output vào `skills/quan-ly-files/outputs/` nếu cần

**CLI tools được hỗ trợ:**
- `gh` — GitHub CLI (issues, PRs, repos)
- `gcloud` — Google Cloud CLI
- `aws` — AWS CLI
- `docker` — Docker CLI
- `npm` / `npx` — Node.js package manager
- `python` / `pip` — Python tools

## Lưu ý chung

- Không hard-code credentials. Dùng biến môi trường hoặc file `.env` (không commit lên git)
- Sau mỗi kết nối thành công, ghi log tóm tắt vào `skills/quan-ly-files/outputs/connection-log.md`
