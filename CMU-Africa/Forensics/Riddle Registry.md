# Riddle Registry
Description
Hi, intrepid investigator! 📄🔍 You've stumbled upon a peculiar PDF filled with what seems like nothing more than garbled nonsense. But beware! Not everything is as it appears. 
Amidst the chaos lies a hidden treasure—an elusive flag waiting to be uncovered. Find the PDF file here Hidden Confidential Document and uncover the flag within the metadata.

---
You just need to look for data other than what is inside the pdf as the content of the file is just irrelevant. So using strings you would see a string named Flag/ but nothing else.
Using the `pdfinfo` tool in the terminal you will see it has a `base64` encoded text. So you just need to decode it
<img width="672" height="351" alt="image" src="https://github.com/user-attachments/assets/c5193865-1b93-4040-994e-023bdd8e618b" />

---
Flag:
```text
picoCTF{puzzl3d_m3tadata_f0und!_42440c7d}
```
