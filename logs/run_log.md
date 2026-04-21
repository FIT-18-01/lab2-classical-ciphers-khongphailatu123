# Run Log – FIT4012 Lab 2

## Caesar Cipher Execution
- [x] Đã chạy Caesar encrypt với `I LOVE YOU`, key `3` → "L ORYH BRX"
- [x] Đã chạy Caesar encrypt với `hello world`, key `5` → "mjqqt btwqi"
- [x] Đã chạy Caesar decrypt với `LORYH BRX`, key `3` → "I LOVE YOU"

## Rail Fence Cipher Execution
- [x] Đã chạy Rail Fence encrypt với `2` rails → "ILV OOEYU"
- [x] Đã chạy Rail Fence encrypt với `4` rails → "I  EYLVOOU"
- [x] Đã chạy Rail Fence decrypt với `2` rails → "I LOVE YOU"

## Input Validation & File Input
- [x] Đã kiểm tra đầu vào không hợp lệ (numbers và special chars)
- [x] Đã đọc dữ liệu từ `data/input.txt` thành công

## Test Summary
| Test Case | Status | Output |
|-----------|--------|--------|
| Caesar Encrypt | ✓ PASS | L ORYH BRX |
| Caesar Decrypt | ✓ PASS | I LOVE YOU |
| Rail Fence 2 rails | ✓ PASS | ILV OOEYU |
| Rail Fence 4 rails | ✓ PASS | I  EYLVOOU |
| Rail Fence Decrypt | ✓ PASS | I LOVE YOU |
| File Input | ✓ PASS | Read successfully |

## Điều em học được từ bài lab
Bài lab giúp em hiểu rõ nguyên lý của Caesar Cipher (phép dịch vòng) và Rail Fence Cipher (zigzag pattern).
Điểm khó nhất là implement Rail Fence Decrypt vì cần tính toán độ dài mỗi ray chính xác.
Xử lý dấu cách và validation input là bước quan trọng để tránh lỗi runtime.
