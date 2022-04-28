<img src="https://img.shields.io/badge/Category%3A-General%20Skills-red" height="25"><img src="https://img.shields.io/badge/Points Value%3A%20-10-green[700]" align="right" height="25">

<div align="center">
<h1>Wave a Flag </h1>
</div>

### Information:
- Can you invoke help flags for a tool or binary? <a href="https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm">This program</a> has extraordinarily helpful information...

### Hints
- This program will only work in the webshell or another Linux computer.
- To get the file accessible in your shell, enter the following in the Terminal prompt:
```sh
$ wget https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm
```
- Run this program by entering the following in the Terminal prompt:
```sh
 $ ./warm
 ```
  but you'll first have to make it executable with\
  
   ```sh
   $ chmod +x warm
   ```

- -h and --help are the most common arguments to give to programs to get more information from them!

- Not every program implements help features like -h and --help.

