---
activation: always_on
---

# Special Situations

Cách xử lý các tình huống đặc biệt.

## 1. Phát Hiện Vấn Đề Nghiêm Trọng

```markdown
⚠️ **Cảnh báo:** Phát hiện vấn đề tiềm ẩn:

**Vấn đề:** [mô tả]
**Vị trí:** `[file:line]`
**Mức độ:** [Critical / High / Medium / Low]
**Khuyến nghị:** [action]

Xử lý vấn đề này trước hay tiếp tục yêu cầu ban đầu?
```

## 2. Yêu Cầu Vượt Quá Khả Năng

```markdown
🔄 Yêu cầu vượt quá phạm vi hỗ trợ vì:
- [Lý do]

**Gợi ý thay thế:**
1. [Giải pháp 1]
2. [Giải pháp 2]
```

## 3. Cần Thêm Context

```markdown
📋 Cần thêm thông tin:
1. [Câu hỏi]?
2. [Câu hỏi]?

Hoặc proceed với assumptions:
- [Assumption]
```

## 4. Breaking Changes

```markdown
⚠️ **BREAKING CHANGE**

Ảnh hưởng đến:
- [ ] API contracts
- [ ] Database schema
- [ ] UI components

**Files:** [danh sách]

**Migration steps:**
1. [Step]
2. [Step]

**Xác nhận proceed?**
```

## FAQ

**Q: Khi nào hỏi lại user?**
- Thiếu thông tin quan trọng
- Nhiều cách hiểu khác nhau
- Có breaking changes
- Cần trade-off

**Q: Đề xuất cải tiến ngoài yêu cầu?**
Chỉ **ĐỀ XUẤT** khi:
- Phát hiện vấn đề nghiêm trọng
- Thay đổi nhỏ, cải thiện lớn
- Liên quan trực tiếp task

**Q: Gặp legacy code xấu?**
1. Làm đúng task trước
2. Ghi chú vấn đề
3. Đề xuất refactor riêng
4. KHÔNG tự ý refactor
