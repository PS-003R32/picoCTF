# Log Hunt

### Description
Our server seems to be leaking pieces of a secret flag in its logs. <br>
The parts are scattered and sometimes repeated. Can you reconstruct the original flag? <br>
Download the [logs](https://challenge-files.picoctf.net/c_amiable_citadel/49cec6157142f24a599f4164d5b63322c2494f801390d6f22eb91b3aa592bc66/server.log) and figure out the full flag from the fragments.

---
You get `server.log` file. To read it use the less command `less server.log` and you will notice that it has log named `INFO FLAGPART ...`. Now you just need to use the `grep` command to catch all lines with
the flagpart. Run: `cat server.log | grep FLAGPART` you will get the flag.
<img width="617" height="369" alt="image" src="https://github.com/user-attachments/assets/3f7566e4-05e5-43e3-a582-33f22274d4df" />

---
Flag:
```text
picoCTF{us3_y0urlinux_sk1lls_cedfa5fb}
```
