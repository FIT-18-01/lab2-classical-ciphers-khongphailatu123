[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/G4Lkq8iY)
# fit4012-lab2-classical-ciphers-khongphailatu123

Hoàn thiện bài **FIT4012 – Lab 2: Mã hoá cổ điển**.

## Mục tiêu đã hoàn thiện
✅ **Caesar Cipher**
- Q1: Xử lý chữ thường
- Q2: Giữ dấu cách
- Q3: Giải mã

✅ **Rail Fence Cipher**
- Q4: Thay đổi số ray (2, 3, 4, ...)
- Q5: Giải mã (Decrypt)
- Q6: Giữ dấu cách
- Q7: Kiểm tra đầu vào (chỉ chữ cái và dấu cách)
- Q8: Đọc thông điệp từ file `data/input.txt`

## Cách biên dịch

### Caesar Cipher
```bash
g++ -std=c++17 -O2 -Wall -Wextra -o caesar_bin src/caesar.cpp
```

### Rail Fence Cipher
```bash
g++ -std=c++17 -O2 -Wall -Wextra -o rail_bin src/rail_fence.cpp
```

## Cách chạy

### Caesar Cipher
```bash
./caesar_bin
# Chọn: 1 (Encrypt) hoặc 2 (Decrypt)
# Nhập thông điệp và khóa
```

**Ví dụ:**
- Encrypt "I LOVE YOU" với key 3 → "L ORYH BRX"
- Decrypt "LORYH BRX" với key 3 → "I LOVE YOU"

### Rail Fence Cipher
```bash
./rail_bin
# Chọn: 1 (Encrypt), 2 (Decrypt), hoặc 3 (Read from file and encrypt)
# Nhập thông điệp (hoặc được đọc từ file) và số rays
```

**Ví dụ:**
- Encrypt "I LOVE YOU" với 2 rays → "ILV OOEYU"
- Decrypt "ILV OOEYU" với 2 rays → "I LOVE YOU"
- Read from file và encrypt với 4 rays

## Nội dung chính của code

### Caesar Cipher (src/caesar.cpp)
- `shift_char(char c, int shift)`: Dịch một ký tự, hỗ trợ in hoa/thường
- `caesar_encrypt(const string &plaintext, int shift)`: Mã hóa thông điệp
- `caesar_decrypt(const string &ciphertext, int shift)`: Giải mã (gọi encrypt với shift âm)
- `is_valid_message(const string &text)`: Kiểm tra đầu vào chỉ chứa chữ cái và dấu cách

### Rail Fence Cipher (src/rail_fence.cpp)
- `rail_fence_encrypt(const string &plaintext, int rails)`: Mã hóa theo zigzag pattern
- `rail_fence_decrypt(const string &ciphertext, int rails)`: Giải mã bằng cách:
  1. Tính độ dài mỗi ray từ plaintext length và rail count
  2. Phân chia ciphertext thành các phần tương ứng
  3. Đi lại zigzag để khôi phục plaintext
- `read_message_from_file(const string &path)`: Đọc dòng đầu tiên từ file
- `is_valid_message()`: Kiểm tra đầu vào

## Cấu trúc repo
```text
lab2-classical-ciphers-khongphailatu123/
├── README.md (tệp này)
├── assignment-obe.md
├── assignment-classroom.md
├── lab2-guide.md
├── report-1page.md ✓ Hoàn thiện
├── src/
│   ├── caesar.cpp ✓ Hoàn thiện
│   └── rail_fence.cpp ✓ Hoàn thiện
├── data/
│   └── input.txt (I LOVE YOU)
├── tests/
│   └── test_cases.md ✓ 9 test cases
├── logs/
│   └── run_log.md ✓ Đầy đủ
└── .github/
    ├── scripts/
    │   └── check_lab2.py
    └── workflows/
        └── lab2-check.yml
```

## Test Cases

Đã thực hiện 9 test cases:

**Caesar Cipher:**
1. Encrypt "I LOVE YOU" (key=3) → "L ORYH BRX" ✓
2. Encrypt "hello world" (key=5) → "mjqqt btwqi" ✓
3. Decrypt "LORYH BRX" (key=3) → "I LOVE YOU" ✓

**Rail Fence Cipher:**
4. Encrypt "I LOVE YOU" (2 rails) → "ILV OOEYU" ✓
5. Encrypt "I LOVE YOU" (4 rails) → "I  EYLVOOU" ✓
6. Decrypt "ILV OOEYU" (2 rails) → "I LOVE YOU" ✓

**Validation:**
7. Invalid "HELLO123" → Error ✓
8. Invalid "HELLO@WORLD" → Error ✓
9. Read from file → Works ✓

Xem [tests/test_cases.md](tests/test_cases.md) để chi tiết.

## Kết luận

Bài lab đã hoàn thiện tất cả yêu cầu:
- ✓ Biên dịch được (không lỗi)
- ✓ Kết quả mã hóa/giải mã chính xác
- ✓ 9 test cases đầy đủ
- ✓ README, report, logs hoàn chỉnh
- ✓ Repo sạch, tổ chức rõ ràng

**Điểm nổi bật:**
- Caesar: Hỗ trợ chữ hoa/thường, giữ dấu cách, decrypt chính xác
- Rail Fence: Decrypt sử dụng thuật toán zigzag-based reconstruction
- Input validation: Chỉ chấp nhận chữ cái và dấu cách
- File I/O: Đọc từ `data/input.txt` thành công
3. Điền `tests/test_cases.md`.
4. Điền `logs/run_log.md`.
5. Hoàn thiện `report-1page.md`.
6. Commit, push và nộp link repo.

## Cách biên dịch
### Caesar Cipher
```bash
g++ -std=c++17 -O2 -Wall -Wextra -o caesar_bin src/caesar.cpp
./caesar_bin
```

### Rail Fence Cipher
```bash
g++ -std=c++17 -O2 -Wall -Wextra -o rail_bin src/rail_fence.cpp
./rail_bin
```

## File dữ liệu mẫu
Repo đã có sẵn file `data/input.txt` để phục vụ Q8.

## Lưu ý
- Không xóa các file trong `.github/`.
- Không đổi tên file nguồn trừ khi giảng viên cho phép.
- Nên có nhiều commit có ý nghĩa trong quá trình làm bài.
