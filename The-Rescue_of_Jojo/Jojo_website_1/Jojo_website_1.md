# Đề bài:
![Screenshot (517)](https://github.com/anhshidou/nopsctf-2024/assets/152991010/e66868f6-36ed-49a4-9f85-4c8e2642742e)

# Giao diện trang web:
![Screenshot (518)](https://github.com/anhshidou/nopsctf-2024/assets/152991010/6b12299d-5b02-4b99-b473-61d59e5df3ae)

![Screenshot (519)](https://github.com/anhshidou/nopsctf-2024/assets/152991010/8902bea1-b0a7-4b00-aa3d-401a7512f6da)

# Tính năng trang web: Trang web bao gồm:
- Login
- Register
- Cập nhật thông tin
- Bảng id
- Logout
# Khai thác:
- Lỗ hổng của bài là Idor, nằm ở phần cập nhật thông tin:

![Screenshot (520)](https://github.com/anhshidou/nopsctf-2024/assets/152991010/babaca15-c03c-409e-979c-6bdf9bbde566)

- Ta không thể chỉnh username, nhưng trong burp suite ta có thể chỉnh cả username lẫn id

![Screenshot (521)](https://github.com/anhshidou/nopsctf-2024/assets/152991010/29f7fd4d-72c1-4768-ac2e-112acae2f753)

- Vậy sẽ ra sao nếu ta chỉnh id=1 và username= admin ( id mới là thứ quyết định quyền admin)

![Screenshot (522)](https://github.com/anhshidou/nopsctf-2024/assets/152991010/a03b3d66-965a-4be7-9223-74e4f71be88a)

- Hay rồi, giờ thì log out và đăng nhập bằng tài khoản admin nào, lúc này bạn sẽ thấy 1 mục tên admin, click vào thì chúng ta có:

![Screenshot (523)](https://github.com/anhshidou/nopsctf-2024/assets/152991010/63ec4cc8-76e5-4897-8907-c9b779ebdc9b)

# Flag:
N0PS{1d0R_p4zZw0rD_r3Z3t}
