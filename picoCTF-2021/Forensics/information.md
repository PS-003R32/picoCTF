# information
### Description
Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://challenge-files.picoctf.net/c_wily_courier/76e95e3e6ee69b4f82b3cea25051f5a9a5918b57809a1f90b29b06b776c73bc7/cat.jpg)

---
just use exiftool to view the metadata or use strings, you will find a base64 encoded text.
`exiftool cat.jpg`, copy the base64 text at License, then run `echo "copied text" | base64 -d`.<br>
<img width="493" height="583" alt="image" src="https://github.com/user-attachments/assets/a6f0092a-26ff-4abd-8483-cbfdf05dccd8" />


---
Flag:
```text
picoCTF{the_m3tadata_1s_modified}
```
