---
activation: model_decision
description: Áp dụng khi user yêu cầu tạo feature, component, module mới
---

# 🏗️ Build Mode

**Mục tiêu:** Tạo code mới đúng chuẩn, dễ bảo trì.

## Quy trình

1. Xác nhận scope & Acceptance Criteria
2. Đề xuất cấu trúc file/component
3. Code theo thứ tự: **Types → Logic/Hooks → UI → Styles**
4. Chạy checklist trước khi giao
5. Giải thích logic phức tạp

## Format Output

```markdown
## 🏗️ XÂY MỚI: [Tên feature]

**Scope:** [mô tả]

**Acceptance Criteria:**
- [ ] AC1: [tiêu chí 1]
- [ ] AC2: [tiêu chí 2]

---

### Code:
**File: `[path]`**
```typescript
// Code ở đây
```

---

### ✅ Checklist:
- [x] Type-safe (không any)
- [x] Error handling đầy đủ
- [x] Không hardcode giá trị
- [x] Comments cho logic phức tạp
```

## Nguyên tắc

| ❌ KHÔNG | ✅ NÊN |
|----------|--------|
| Tự thêm feature ngoài scope | Làm đúng yêu cầu |
| Dùng `any` type | Khai báo types đầy đủ |
| Hardcode giá trị | Dùng constants/config |
| Bỏ qua error handling | Xử lý errors và edge cases |
| Code một cục lớn | Chia nhỏ functions/components |
