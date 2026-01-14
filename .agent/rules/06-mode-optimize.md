---
activation: model_decision
description: Áp dụng khi user yêu cầu refactor, optimize, cải thiện performance
---

# ⚡ Optimize Mode

**Mục tiêu:** Cải thiện chất lượng mà **KHÔNG thay đổi hành vi** (behavior).

## Quy trình

1. Đo lường hiện trạng (baseline)
2. Xác định bottleneck chính
3. Đề xuất cải tiến + dự đoán kết quả
4. Refactor theo thứ tự ưu tiên
5. So sánh trước/sau
6. Đảm bảo tests vẫn pass

## Tiêu Chí Đánh Giá

| Tiêu chí | Công cụ | Ngưỡng tốt |
|----------|---------|------------|
| Bundle size | `npm run build` | < 500KB |
| Render time | React DevTools | < 16ms |
| Memory | Chrome DevTools | Không leak |
| Complexity | ESLint | Cyclomatic < 10 |

## Format Output

```markdown
## ⚡ TỐI ƯU

**Vấn đề:** [chậm / code lặp / khó maintain]

**Baseline:**
- Bundle: X KB
- Render: X ms
- LOC: X

---

### Bottleneck:
| Vấn đề | Vị trí | Mức độ |
|--------|--------|--------|
| [Mô tả] | `file:line` | 🔴 Cao |

### Đề xuất:
| Hạng mục | Trước | Sau | Δ |
|----------|-------|-----|---|
| Bundle | 800KB | 450KB | -44% |

### Regression Check:
- [ ] Tests vẫn pass
- [ ] Behavior không đổi
```

## Nguyên tắc

| ❌ KHÔNG | ✅ NÊN |
|----------|--------|
| Tối ưu sớm | Đo trước, tối ưu sau |
| Thay đổi behavior | Giữ nguyên behavior |
| Ưu tiên cleverness | Readability > Performance |
| Bỏ qua tests | Chạy lại tests |
