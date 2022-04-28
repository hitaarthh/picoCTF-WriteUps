<img src="https://img.shields.io/badge/Category%3A-General%20Skills-red" height="25"><img src="https://img.shields.io/badge/Points Value%3A%20-10-green[700]" align="right" height="25">

<div align="center">
<h1> Python Wrangling </h1>
</div>

### Information:
Python scripts are invoked kind of like programs in the Terminal... Can you run <a href="https://mercury.picoctf.net/static/5c4c0cbfbc149f3b0fc55c26f36ee707/ende.py">this Python script</a> using <a href="https://mercury.picoctf.net/static/5c4c0cbfbc149f3b0fc55c26f36ee707/pw.txt">this password</a> to get <a href="https://mercury.picoctf.net/static/5c4c0cbfbc149f3b0fc55c26f36ee707/flag.txt.en">the flag</a>?

### Hints:
- Get the Python script accessible in your shell by entering the following command in the Terminal prompt: 
```sh 
$ wget https://mercury.picoctf.net/static/5c4c0cbfbc149f3b0fc55c26f36ee707/ende.py
```
```sh
$ man python
```
### Solutions
I tried running the code in the VS Code but that didn't work. I navigated to the directory where the Python file was (make sure the flag file is in the same directory) and used ```python -d flag.txt.en``` (-d for decode I'm guessing, -e is probably encode). This asked for the password which I pasted from pwd.txt and then it outputted the flag.

#### Issue Faced: 
- Buffer does not work in Python2 and Python3 versions.

```python
sys.stdout.buffer.write(data_c)
```
should be replaced by 

```python
sys.stdout.write(data_c)
```
in order to run the file well.

### Flag:

```sh
picoCTF{4p0110_1n_7h3_h0us3_aa821c16}
```