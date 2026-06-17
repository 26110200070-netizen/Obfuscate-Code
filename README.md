# Khoa Dev - Universal Obfuscator V3.0

## Giới thiệu

**Universal Obfuscator V3.0** là công cụ đóng gói và làm rối mã nguồn đa ngôn ngữ được phát triển bởi **Khoa Dev**.

Công cụ hỗ trợ xử lý mã nguồn của nhiều ngôn ngữ lập trình như:

- Python
- Lua / Luau
- JavaScript

Mục tiêu của dự án là biến đổi mã nguồn thành dạng khó đọc hơn bằng cách mã hóa dữ liệu, tạo biến ngẫu nhiên và sinh mã loader để thực thi lại nội dung gốc.

---

# Khoa Dev là Admin

Khoa Dev là Admin chính của dự án.

Admin chịu trách nhiệm:

- Phát triển hệ thống
- Quản lý mã nguồn
- Cập nhật tính năng
- Bảo trì công cụ
- Kiểm tra và tối ưu hoạt động

---

# Tính năng

## Hỗ trợ ngôn ngữ

Công cụ hỗ trợ:


Python (.py)
Lua / Luau (.lua)
JavaScript (.js)


---

## Chức năng chính

Universal Obfuscator có thể:

- Mã hóa source code
- Tạo payload đã được đóng gói
- Làm rối tên biến
- Sinh mã ngẫu nhiên (junk code)
- Tạo loader giải mã khi chạy
- Xuất file mới sau khi xử lý
- Hỗ trợ nhập file hoặc dán code trực tiếp

---

# Cách hoạt động

Quy trình xử lý:

            SOURCE CODE

                 |

                 v

         Đọc mã nguồn đầu vào

                 |

                 v

          Encode dữ liệu

                 |

                 v

    Tạo biến ngẫu nhiên + Junk Code

                 |

                 v

      Tạo Polymorphic Stub

                 |

                 v

          Xuất file mới

---

# Cơ chế xử lý

## Python Obfuscator

Cách hoạt động:

- Chuyển ký tự thành mã Unicode
- Thêm khóa mã hóa ngẫu nhiên
- Tạo đoạn code giải mã
- Thực thi bằng cơ chế loader

Output:


Python Source
|
v
Encoded Data
|
v
exec Loader


---

## Lua / Luau Obfuscator

Cách hoạt động:

- Chuyển source thành byte UTF-8
- Lưu dữ liệu dạng bảng
- Giải mã bằng string.char
- Thực thi bằng load/loadstring

Output:


Lua Source
|
v
Byte Data
|
v
Runtime Decode


---

## JavaScript Obfuscator

Cách hoạt động:

- Chuyển ký tự thành mã số
- Tạo mảng dữ liệu
- Khôi phục bằng String.fromCharCode
- Chạy bằng Function()

Output:


JS Source
|
v
Encoded Array
|
v
Dynamic Execute


---

# Giao diện chương trình

Tool có giao diện Terminal với:

- Màu ANSI
- Hiệu ứng loading
- Thanh tiến trình
- Hex dump animation
- Hỗ trợ tiếng Anh và tiếng Việt

---

# Cài đặt

Yêu cầu:


Python 3.x


Kiểm tra Python:

```bash
python --version
Cài thư viện

Chạy:

pip install -r requirements.txt
Cách chạy

Khởi động chương trình:

python obfuscateKhoaDev.py
Hướng dẫn sử dụng
Bước 1: Chọn ngôn ngữ giao diện
[1] English
[2] Tiếng Việt
Bước 2: Chọn ngôn ngữ cần làm rối
[1] Python
[2] Lua / Luau
[3] JavaScript
Bước 3: Chọn nguồn nhập

Có 2 cách:

[1] Chọn file từ máy tính

[2] Dán code trực tiếp

Nếu dán code:

Kết thúc bằng:

END
Bước 4: Xuất file

Nhập tên file:

Ví dụ:

output.py
output.lua
output.js
Cấu trúc dự án
KhoaDev/

│

├── obfuscateKhoaDev.py

├── requirements.txt

└── README.md
Thông tin dự án
Project:
Universal Obfuscator V3.0

Developer:
Khoa Dev

Language:
Python

Version:
3.0
Lưu ý

Công cụ được tạo nhằm mục đích:

Bảo vệ mã nguồn
Nghiên cứu lập trình
Học tập và phát triển phần mềm

Không sử dụng
