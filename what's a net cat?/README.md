<img src="https://img.shields.io/badge/Category%3A-General%20Skills-red" height="25"><img src="https://img.shields.io/badge/Points Value%3A%20-100-green[700]" align="right" height="25">

<div align="center">
<h1> what's a net cat? </h1>
</div>

### Information:
Using netcat (nc) is going to be pretty important. Can you connect to the given server to get the flag?
```sh
jupiter.challenges.picoctf.org at port 25103
``` 
### Hints: 
nc <a href="https://linux.die.net/man/1/nc"><u>tutorial</u></a>

### Solution:

- After studying how netcat works i ran this command in my terminal.

```sh
nc jupiter.challenges.picoctf.org 25103
```
<img width="638" alt="Screenshot 2022-04-30 at 8 55 08 PM" src="https://user-images.githubusercontent.com/91147942/166111848-c0e0fe4e-ea66-419d-ad7d-c7f1a07299a2.png">

### Flag:
```sh
picoCTF{nEtCat_Mast3ry_d0c64587}
```

