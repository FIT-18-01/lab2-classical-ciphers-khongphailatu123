# Report 1 Page – FIT4012 Lab 2

## 1. Mục tiêu
Implement và mở rộng hai mã hóa cổ điển: Caesar Cipher và Rail Fence Cipher. Cụ thể:
- **Caesar Cipher**: Mã hóa/giải mã dựa trên phép dịch vòng, xử lý chữ cái in hoa/thường, giữ dấu cách.
- **Rail Fence Cipher**: Mã hóa/giải mã dựa trên zigzag pattern, xử lý dấu cách, kiểm tra đầu vào, đọc từ file.

## 2. Cách làm
1. **Caesar Cipher**: Sử dụng hàm `shift_char()` để dịch từng ký tự. Xử lý chữ cái in hoa và thường riêng biệt.
2. **Rail Fence Cipher**: 
   - **Encrypt**: Đi theo zigzag pattern, ghi ký tự vào mỗi ray, sau đó nối lại.
   - **Decrypt**: Tính độ dài mỗi ray từ plaintext, phân chia ciphertext, rồi đi lại zigzag để khôi phục plaintext.
3. **Input Validation**: Kiểm tra chỉ chấp nhận chữ cái và dấu cách.
4. **File Input**: Đọc thông điệp từ `data/input.txt`.

## 3. Kết quả chính

### 3.1 Caesar Cipher
| Input | Key | Ciphertext | Nhận xét |
|---|---:|---|---|
| I LOVE YOU | 3 | L ORYH BRX | Mã hóa thành công, giữ dấu cách |
| hello world | 5 | mjqqt btwqi | Xử lý chữ thường đúng |
| LORYH BRX | 3 (decrypt) | I LOVE YOU | Giải mã chính xác |

### 3.2 Rail Fence Cipher
| Input | Rails | Ciphertext | Nhận xét |
|---|---:|---|---|
| I LOVE YOU | 2 | ILV OOEYU | Zigzag với 2 đường ray |
| I LOVE YOU | 4 | I  EYLVOOU | Zigzag với 4 đường ray, dấu cách được giữ |
| ILV OOEYU | 2 (decrypt) | I LOVE YOU | Giải mã Rail Fence chính xác |

### 3.3 Input Validation & File Input
- **Invalid input**: Chương trình từ chối "HELLO123" (chứa số) và "HELLO@WORLD" (chứa ký tự đặc biệt) ✓
- **File input**: Đọc "I LOVE YOU" từ `data/input.txt` và mã hóa thành công ✓

## 4. Kết luận
Bài lab giúp hiểu rõ nguyên lý của hai mã cổ điển và cách implement chúng bằng C++. 
- **Khó khăn chính**: Implement giải mã Rail Fence vì cần tính toán chính xác độ dài mỗi ray trong quá trình zigzag.
- **Kỹ năng đạt được**: Xử lý string, validation input, file I/O, và thuật toán pattern-based (zigzag).
- **Ứng dụng thực tế**: Mã cổ điển không an toàn với máy tính hiện đại nhưng giúp hiểu nền tảng của cryptography.
