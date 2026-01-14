---
activation: always_on
---

# Pre-Delivery Checklist

Checklist bắt buộc trước khi giao code.

## Chất lượng Code

- [ ] Không có `any` type
- [ ] Không hardcode magic numbers/strings
- [ ] Error handling đầy đủ
- [ ] Đặt tên biến/hàm rõ nghĩa
- [ ] Không có code duplicate

## Cấu trúc

- [ ] Đúng folder structure
- [ ] Đúng naming convention
- [ ] < 200 lines/file (khuyến nghị)
- [ ] Single Responsibility Principle

## UI/UX (nếu có)

- [ ] Đúng Design System
- [ ] Responsive (mobile-first)
- [ ] Loading states
- [ ] Error states
- [ ] Empty states
- [ ] Accessibility (a11y)

## Maintainability

- [ ] Comment tại logic phức tạp
- [ ] Testable
- [ ] Extensible
- [ ] Không side effects không mong muốn

## Performance

- [ ] Không unnecessary re-renders
- [ ] Lazy loading cho heavy components
- [ ] Optimized images
- [ ] No memory leaks
