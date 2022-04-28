<img src="https://img.shields.io/badge/Category%3A-Forensics-red" height="25"><img src="https://img.shields.io/badge/Points Value%3A%20-10-green[700]" align="right" height="25">

<div align="center">
<h1> information </h1>
</div>

### Problem Statement:
Files can always be changed in a secret way. Can you find the flag? <a href="https://mercury.picoctf.net/static/d1375e383810d8d957c04eef9e345732/cat.jpg">cat.jpg</a>

### Hints:
- Look at the details of the file
- Make sure to submit the flag as picoCTF{XXXXX}

### Solution:
- I downloaded the file and tried to see if there were any plaintext strings in it. There weren't. The first hint was to look at the details of the file. I used this site to find the strings inside the file. It gave the contents of ```information.xml```
- After these steps we get a ```base64``` ```cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9``` text by using <a href="https://www.base64decode.org/">base64 Converter.</a>

### Flag:
```sh
picoCTF{the_m3tadata_1s_modified}
```




