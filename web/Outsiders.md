# Đề bài:
![Screenshot (512)](https://github.com/anhshidou/nopsctf-2024/assets/152991010/a8fe55eb-61bd-4a74-8b01-a8d55839f3b9)

# Giao diện trang web:
![Screenshot (513)](https://github.com/anhshidou/nopsctf-2024/assets/152991010/d0b2151b-65c3-4b4d-87ac-6ab369fe6fd1)


# Hint:
- Thật sự thì bài này mình không hiểu đầu bài muốn bảo làm gì mà thử referer không được, vậy nên mình đã đi xin hint

![Screenshot (514)](https://github.com/anhshidou/nopsctf-2024/assets/152991010/aa5d9c1a-d5de-46c3-8b66-5c87d82134c6)

- Vậy thì bài này sẽ phải sử dụng ```X-Forwarded-For: 127:0:0:1```

# Exploit:
- Bài có đúng 1 bước thôi, đó là thêm header ```X-Forwarded-For: 127.0.0.1```

![Screenshot (490)](https://github.com/anhshidou/nopsctf-2024/assets/152991010/62b4d5da-598f-426c-b8c0-ecbc8d309447)

# Flag:
N0PS{XF0rw4Rd3D}
