# Hidden in plainsight
### Description
You’re given a seemingly ordinary JPG image. Something is tucked away out of sight inside the file. 
Your task is to discover the hidden payload and extract the flag. Download the jpg image [here](https://challenge-files.picoctf.net/c_amiable_citadel/31f5b3c0759eba6f7632fcb2eca20424a40c6f066e52c07eabedafafb800d87e/img.jpg).

---
Using the `exiftool` you will find a base64 string `c3RlZ2hpZGU6Y0VGNmVuZHZjbVE9` and if you decode it it returns `steghide:cEF6endvcmQ=`. Which indicated we need to use `steghide`.
Now again if you decode the base64 string next to the output after steghide, you get `pAzzword` which means we need to extract the hidden data using the steghide tool and use `pAzzword` as password.
So finally do the following.<br>
<img width="666" height="426" alt="image" src="https://github.com/user-attachments/assets/764e7a26-7679-4152-b44d-6b9abba08f1d" />

```shell
exiftool img.jpg
echo "c3RlZ2hpZGU6Y0VGNmVuZHZjbVE9" | base64 -d
echo "cEF6endvcmQ=" | base64 -d
sudo steghide extract -sf img.jpg
cat flag.txt
```

---
Flag
```text
picoCTF{h1dd3n_1n_1m4g3_92f08d7c}
```
