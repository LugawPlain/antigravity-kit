---
activation: always_on
---

# Technical Standards

Quy chuẩn kỹ thuật áp dụng cho toàn bộ mã nguồn.

## 1. Naming Conventions

- **Ngôn ngữ:** Tiếng Anh 100% cho tên biến, hàm, class
- **camelCase:** biến, hàm (`userId`, `calculateTotal`)
- **PascalCase:** Class, Interface, Component (`UserController`)
- **SCREAMING_SNAKE_CASE:** Constants (`MAX_RETRY`)
- **Boolean:** prefix `is`, `has`, `can`, `should`

✅ `customerAddress`, `isValid`, `fetchUserData()`
❌ `addr`, `val`, `func1()`

## 2. Function & Logic Flow

- **Early Return:** Tránh if/else lồng sâu, return sớm
- **Single Responsibility:** 1 hàm = 1 việc
- **Max 30-50 lines/function**
- **Max 3 parameters**, nếu nhiều hơn dùng Object

```javascript
// ✅ Tốt
function process(order) {
  if (!order) return false;
  if (!order.isValid) return false;
  return executeTransaction(order);
}

// ❌ Xấu - Arrow code
function process(order) {
  if (order) {
    if (order.isValid) {
      return executeTransaction(order);
    }
  }
  return false;
}
```

## 3. Type Safety

- **Không Magic Numbers:** ❌ `if (status == 1)` ✅ `if (status == ORDER_STATUS.PENDING)`
- **Strict Typing:** Khai báo types cho params và return
- **Immutability:** Tạo bản sao thay vì mutate data

## 4. Error Handling

- **Không "nuốt" lỗi:** Luôn log trong try/catch
- **Structured Logging:** `logger.error('Failed', { context })`
- **Fail Fast:** Báo lỗi ngay khi phát hiện vấn đề nghiêm trọng

## 5. Comments

- **Why > What:** Comment giải thích LÝ DO, không phải CÁI GÌ
- **TODO/FIXME:** Đánh dấu việc chưa xong
