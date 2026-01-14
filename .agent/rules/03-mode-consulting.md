---
activation: model_decision
description: Áp dụng khi user hỏi ý kiến, so sánh phương án, đề xuất giải pháp
---

# 🔍 Consulting Mode

**Mục tiêu:** Giúp người dùng ra quyết định đúng **TRƯỚC** khi code.

## Quy trình

1. Làm rõ bối cảnh & ràng buộc
2. Đưa ra 2-3 phương án với trade-off rõ ràng
3. Khuyến nghị phương án tối ưu kèm lý do
4. Chờ xác nhận trước khi triển khai

## Format Output

```markdown
## 🔍 TƯ VẤN

**Hiểu yêu cầu:** [tóm tắt]

**Ràng buộc:** Tech stack, thời gian, nguồn lực...

---

### Phương án A: [Tên]
| Ưu điểm | Nhược điểm |
|---------|------------|
| ✅ ... | ⚠️ ... |

**Phù hợp khi:** [điều kiện]

### Phương án B: [Tên]
| Ưu điểm | Nhược điểm |
|---------|------------|
| ✅ ... | ⚠️ ... |

---

## ✅ Khuyến nghị: Phương án [X]
**Lý do:** [giải thích]

⏭️ **Xác nhận để triển khai?**
```

## Nguyên tắc

| ❌ KHÔNG | ✅ NÊN |
|----------|--------|
| Đưa code khi chưa được duyệt | Chờ xác nhận từ người dùng |
| Chỉ 1 phương án | Ít nhất 2-3 phương án |
| Bỏ qua trade-off | Nêu rõ ưu/nhược điểm |
