# Transformation
### Description
I wonder what this really is... [enc](https://challenge-files.picoctf.net/c_wily_courier/991ad9ef8df265fa72069cd892b73d8bbd8206790a7c4941c89eae4005d8acf1/enc) ''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0, len(flag), 2)])

convert it to hex using python, hex(ord(enc[0tolength]).lstrip("0x").
Use burp decoder to decode it to the final flag.<br>
<img width="749" height="480" alt="image" src="https://github.com/user-attachments/assets/d0d1d460-7519-4abe-a3c1-1a220f7938bd" />

---
Flag:
```text
picoCTF{16_bits_inst34d_of_8_b7f62ca5}
```
