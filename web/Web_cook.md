# Đề bài:
![Screenshot (506)](https://github.com/anhshidou/nopsctf-2024/assets/152991010/84d4b7cc-e5e5-45e4-b4d9-8936b27764ee)

## Giao diện trang web:
![Screenshot (507)](https://github.com/anhshidou/nopsctf-2024/assets/152991010/4394f464-098c-4a88-8693-5ae1d48abeb9)

# Exploit:
- Trước tiên cứ thử nhập username vào, ta có:

![Screenshot (508)](https://github.com/anhshidou/nopsctf-2024/assets/152991010/a00dd640-72fe-4e17-8cc2-af5fde51e01d)

- Đọc hint, ta nhận thấy viêc mình cần làm là decode base64 của cookie, sửa isadmin=1, sau đó thay thế giá trị cookie cũ bằng cái mình vừa encode xong.

![Screenshot (509)](https://github.com/anhshidou/nopsctf-2024/assets/152991010/cd229509-6635-4679-867a-c9abf2ce2bf4)

- Sửa isadmin=1

![Screenshot (489)](https://github.com/anhshidou/nopsctf-2024/assets/152991010/fb2c0442-ce4b-4336-acee-f716d6ee68da)

- Thay thế giá trị cookie bằng cái vừa tìm dc:

![Screenshot (510)](https://github.com/anhshidou/nopsctf-2024/assets/152991010/b1569066-7a26-4180-bdbe-2c596b96a898)

- Kết quả:

![Screenshot (511)](https://github.com/anhshidou/nopsctf-2024/assets/152991010/3de0fbe2-1292-461b-b732-870f8116c52a)

# Flag:
 N0PS{y0u_Kn0W_H0w_t0_c00K_n0W}
