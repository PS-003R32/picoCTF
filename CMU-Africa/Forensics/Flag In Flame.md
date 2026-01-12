# Flag In Flame
### Description
The SOC team discovered a suspiciously large log file after a recent breach. When they opened it, they found an enormous block of encoded text instead of typical logs. 
Could there be something hidden within? Your mission is to inspect the resulting file and reveal the real purpose of it. The team is relying on your skills to uncover any 
concealed information within this unusual log. Download the encoded data here: [Logs Data](https://challenge-files.picoctf.net/c_amiable_citadel/5d0fa1b1244c39428b2d5ca4f966fce8772038c43b9bd56f1c9890cb733c807f/logs.txt). Be prepared—the file is large, and examining it thoroughly is crucial .

---
The text file contains `base64` data. And using the hint it says the output is an image file so we need to pipe the output to base64 and then save to an image file.
Use this command: `cat logs.txt | base64 -d > image.jpg`. Then if you open the image `eog image.jpg` you will find a hexadecimal text, which might reveal the flag after decoding and it did.
I have used my own tool to decode the final hexadecimal string which you can find here, [hotrod](https://github.com/PS-003R32/hotrod).<br>
<img width="732" height="476" alt="image" src="https://github.com/user-attachments/assets/dcbde0b5-e1e3-4783-abb0-fc964de58b46" /><br>
NOTE[The image shows the flag a bit different because i had some minor mistake in copying the hexadecimal text.\]<br>
And that's it we get the flag:
```text
picoCTF{forensics_analysis_is_amazing_2561a194}
```
