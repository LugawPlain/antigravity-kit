---
activation: always_on
---

# Task Classification

Khi nhận yêu cầu, **BẮT BUỘC** xác định thuộc 1 trong 4 loại:

| Ký hiệu | Loại | Mô tả |
|:-------:|:-----|:------|
| 🔍 | **TƯ VẤN** | Hỏi ý kiến, so sánh phương án, đề xuất giải pháp |
| 🏗️ | **XÂY MỚI** | Tạo feature, component, module, page mới |
| 🔧 | **SỬA LỖI** | Fix bug, error, hành vi không đúng mong đợi |
| ⚡ | **TỐI ƯU** | Cải thiện performance, refactor, clean code |

## Quy Tắc Nhận Diện

```plaintext
TƯ VẤN  → "nên", "có cách nào", "so sánh", "đề xuất", "tư vấn", "ý kiến"
XÂY MỚI → "tạo", "làm", "build", "thêm", "viết code", "implement"
SỬA LỖI → "lỗi", "bug", "không chạy", "sai", "error", "fix", "crash"
TỐI ƯU  → "chậm", "refactor", "clean", "cải thiện", "optimize"
```

## Khi Không Rõ Loại

Hỏi lại người dùng:
> "Tôi muốn xác nhận loại nhiệm vụ này:
> A. Tư vấn (so sánh, đề xuất)
> B. Xây mới (tạo code mới)
> C. Sửa lỗi (fix bug)
> D. Tối ưu (refactor, cải thiện)"

## Nhiệm Vụ Phức Hợp

Xử lý tuần tự: **Tư vấn → Xây mới/Sửa lỗi → Tối ưu**
