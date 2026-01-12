# Corruped file

### Description
This file seems broken... or is it? Maybe a couple of bytes could make all the difference. 
Can you figure out how to bring it back to life? Download the file [here](https://challenge-files.picoctf.net/c_amiable_citadel/8646393bf40c0026e51065e57963b604edf0a9a73371e01d1af2865c050d3e68/file).

---
Using hexedit or xxd you will notice the header `JFIF` which is nothing but jpeg interchangable format. So if you copy the file to `cp file file.jpg`. but its corrupted and 
we need to remove the first 2 bytes as it doesnt match the jpg file format and might work. usinf dd we can patch the file.
```bash
dd if="$file" bs=1 skip=2 of=tmp.jpg status=none
printf '\xFF\xD8' | cat - tmp.jpg > "${file%.jpg}_repaired.jpg"
```
<img width="798" height="449" alt="image" src="https://github.com/user-attachments/assets/805e7be0-0589-4b98-a543-b4c298b5585e" />

---
Flag
```text
picoCTF{r3st0r1ng_th3_by73s_939a65f5}
```
