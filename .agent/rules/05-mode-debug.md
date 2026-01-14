---
activation: model_decision
description: Áp dụng khi user báo lỗi, bug, error cần fix
---

# 🔧 Debug Mode

**Mục tiêu:** Tìm đúng nguyên nhân, sửa đúng chỗ, phòng ngừa tái phát.

## Quy trình

1. Thu thập thông tin (5W1H)
2. Tái hiện lỗi (reproduce)
3. Phân tích nguyên nhân gốc (root cause)
4. Đề xuất cách sửa + giải thích
5. Đề xuất cách phòng ngừa

## Câu Hỏi Bắt Buộc Nếu Thiếu Thông Tin

1. Error message cụ thể? (Copy nguyên văn)
2. Xảy ra ở màn hình/chức năng nào?
3. Có thể tái hiện? Các bước cụ thể?
4. Có thay đổi code gì gần đây?
5. Console log có gì bất thường?

## Format Output

```markdown
## 🔧 SỬA LỖI

**Triệu chứng:** [mô tả lỗi]

**Tái hiện:**
1. [Bước 1]
2. [Bước 2]
3. [Lỗi xuất hiện]

---

### Phân tích:
**Root Cause:** [nguyên nhân gốc]
**Vị trí:** `[file:line]`

### Cách sửa:
```diff
- [code cũ]
+ [code mới]
```

**Lý do:** [giải thích]

### Phòng ngừa:
| Đề xuất | Ưu tiên |
|---------|---------|
| [Thêm validation] | 🔴 Cao |
| [Viết unit test] | 🟡 TB |
```

## Nguyên tắc

| ❌ KHÔNG | ✅ NÊN |
|----------|--------|
| Đoán mò | Yêu cầu log/screenshot |
| Refactor lung tung | Sửa đúng chỗ, minimal change |
| Fix xong rồi thôi | Đề xuất phòng ngừa |
| Sửa triệu chứng | Tìm fix root cause |
