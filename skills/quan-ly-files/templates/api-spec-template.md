# API Spec: [Tên API]

**Base URL:** `https://api.example.com/v1`  
**Auth:** Bearer Token / API Key / Basic Auth  

---

## Endpoints

### GET /resource

**Mô tả:** Lấy danh sách resource

**Headers:**
```
Authorization: Bearer {{TOKEN}}
Content-Type: application/json
```

**Response 200:**
```json
{
  "data": [],
  "total": 0
}
```

---

### POST /resource

**Mô tả:** Tạo resource mới

**Body:**
```json
{
  "field1": "value",
  "field2": "value"
}
```

**Response 201:**
```json
{
  "id": "string",
  "created_at": "ISO8601"
}
```

## Error Codes

| Code | Ý nghĩa |
|------|---------|
| 400  | Bad Request |
| 401  | Unauthorized |
| 404  | Not Found |
| 500  | Server Error |
