<img src="https://img.shields.io/badge/Category%3A-General%20Skills-red" height="25"><img src="https://img.shields.io/badge/Points Value%3A%20-15-green[700]" align="right" height="25">

<div align="center">
<h1> Nice Netcat
 </h1>
</div>

### Information:
There is a nice program that you can talk to by using this command in a shell: 
```sh
$ nc mercury.picoctf.net 7449
```
but it doesn't speak English...

### Hints :
- You can practice using netcat with this picoGym problem: <a href="https://play.picoctf.org/practice/challenge/34">what's a netcat</a>?

- You can practice reading and writing ASCII with this picoGym problem: <a href="https://play.picoctf.org/practice/challenge/22">Let's Warm Up</a>

### Solution:
- Logged into the the port 
```sh
mercury.picoctf.net 7449
```
- It gave these numbers:
```sh
112 105 99 111 67 84 70 123 103 48 48 100 95 107 49 116 116 121 33 95 110 49 99 51 95 107 49 116 116 121 33 95 102 50 100 55 99 97 102 97 125 10 
```
I found these random numbers very intersting and hence i wrote a python codes to convert these ASCII codes into characters.
```python
nums = [112 ,105, 99, 111, 67, 84, 70, 123, 103, 48, 48, 100, 95, 107, 49, 116, 116, 121, 33, 95, 110, 49, 99, 51, 95, 107, 49, 116, 116, 121, 33, 95, 102, 50, 100, 55, 99, 97, 102, 97, 125, 10]
flag = ""
for number in nums:
    flag += chr(number)
print(flag)
```