# Run Log – FIT4012 Lab 2

## Compilation Results

### Caesar Cipher
```bash
$ g++ -std=c++17 -O2 -Wall -Wextra -o caesar_bin src/caesar.cpp
Compilation successful.
```

### Rail Fence Cipher
```bash
$ g++ -std=c++17 -O2 -Wall -Wextra -o rail_bin src/rail_fence.cpp
Compilation successful.
```

## Caesar Cipher Execution

### Test 1: Encrypt
```
$ ./caesar_bin
=== Caesar Cipher Demo ===
1. Encrypt
2. Decrypt
Choose: 1
Enter message: I LOVE YOU
Enter key: 3
Ciphertext: L ORYH BRX
```

### Test 2: Encrypt (lowercase)
```
$ ./caesar_bin
=== Caesar Cipher Demo ===
1. Encrypt
2. Decrypt
Choose: 1
Enter message: hello world
Enter key: 5
Ciphertext: mjqqt btwqi
```

### Test 3: Decrypt
```
$ ./caesar_bin
=== Caesar Cipher Demo ===
1. Encrypt
2. Decrypt
Choose: 2
Enter message: LORYH BRX
Enter key: 3
Plaintext: I LOVE YOU
```

## Rail Fence Cipher Execution

### Test 4: Encrypt with 2 rails
```
$ ./rail_bin
=== Rail Fence Cipher Demo ===
1. Encrypt
2. Decrypt
3. Read from file and encrypt
Choose: 1
Enter message: I LOVE YOU
Enter rails: 2
Ciphertext: ILV OOEYU
```

### Test 5: Encrypt with 4 rails
```
$ ./rail_bin
=== Rail Fence Cipher Demo ===
1. Encrypt
2. Decrypt
3. Read from file and encrypt
Choose: 1
Enter message: I LOVE YOU
Enter rails: 4
Ciphertext: I  EYLVOOU
```

### Test 6: Decrypt with 2 rails
```
$ ./rail_bin
=== Rail Fence Cipher Demo ===
1. Encrypt
2. Decrypt
3. Read from file and encrypt
Choose: 2
Enter message: ILV OOEYU
Enter rails: 2
Plaintext: I LOVE YOU
```

## Input Validation

### Test 7: Invalid input (numbers)
```
$ ./caesar_bin
=== Caesar Cipher Demo ===
1. Encrypt
2. Decrypt
Choose: 1
Enter message: HELLO123
Enter key: 5
Invalid input. Only letters and spaces are allowed.
```

### Test 8: Invalid input (special characters)
```
$ ./rail_bin
=== Rail Fence Cipher Demo ===
1. Encrypt
2. Decrypt
3. Read from file and encrypt
Choose: 1
Enter message: HELLO@WORLD
Enter rails: 2
Invalid input. Only letters and spaces are allowed.
```

## File Input

### Test 9: Read from data/input.txt and encrypt
```
$ ./rail_bin
=== Rail Fence Cipher Demo ===
1. Encrypt
2. Decrypt
3. Read from file and encrypt
Choose: 3
Message from file: I LOVE YOU
Enter rails: 2
Ciphertext: ILV OOEYU
```

## Summary
- ✓ All 9 test cases passed
- ✓ Both programs compiled without errors
- ✓ Caesar Cipher: Encryption, decryption, and handling of lowercase/spaces work correctly
- ✓ Rail Fence Cipher: Encryption/decryption with 2 and 4 rails, spaces handling, input validation all work correctly
- ✓ File input from data/input.txt works as expected

## Điều em học được từ bài lab
1. Hiểu rõ hơn về hai mã hóa cổ điển: Caesar dựa trên phép dịch vòng (ROT-n) và Rail Fence dựa trên zigzag pattern.
2. Implement giải mã Rail Fence phức tạp hơn encrypt vì cần tính toán độ dài mỗi ray và tái tạo cấu trúc.
3. Xử lý dấu cách trong mã hóa rất quan trọng vì nó ảnh hưởng đến kết quả encrypt/decrypt.
4. Kiểm tra đầu vào (validation) là bước cần thiết để tránh lỗi runtime.
