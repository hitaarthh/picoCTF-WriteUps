<img src="https://img.shields.io/badge/Category%3A-Cryptography-red" height="25"><img src="https://img.shields.io/badge/Points Value%3A%20-10-green[700]" align="right" height="25">

<div align="center">
<h1> MOD 26 </h1>
</div>

### Information:
<div>
<h4>Cryptography can be easy, do you know what <a href="https://en.wikipedia.org/wiki/ROT13">ROT13</a> is?</h4>

### Hints: 
- This can be solved online if you don't want to do it by hand! 
```sh
cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_jdJBFOXJ}
```

### ROT13 Encryption and Decryption Program:
```python
# Python program to implement
# ROT13 Caesar cipher

'''This script uses dictionaries instead of 'chr()' & 'ord()' function'''

# Dictionary to lookup the index of alphabets
dict1 = {'A' : 1, 'B' : 2, 'C' : 3, 'D' : 4, 'E' : 5,
		'F' : 6, 'G' : 7, 'H' : 8, 'I' : 9, 'J' : 10,
		'K' : 11, 'L' : 12, 'M' : 13, 'N' : 14, 'O' : 15,
		'P' : 16, 'Q' : 17, 'R' : 18, 'S' : 19, 'T' : 20,
		'U' : 21, 'V' : 22, 'W' : 23, 'X' : 24, 'Y' : 25, 'Z' : 26}

# Dictionary to lookup alphabets
# corresponding to the index after shift
dict2 = {0 : 'Z', 1 : 'A', 2 : 'B', 3 : 'C', 4 : 'D', 5 : 'E',
		6 : 'F', 7 : 'G', 8 : 'H', 9 : 'I', 10 : 'J',
		11 : 'K', 12 : 'L', 13 : 'M', 14 : 'N', 15 : 'O',
		16 : 'P', 17 : 'Q', 18 : 'R', 19 : 'S', 20 : 'T',
		21 : 'U', 22 : 'V', 23 : 'W', 24 : 'X', 25 : 'Y'}

# Function to encrypt the string
# according to the shift provided
def encrypt(message, shift):
	cipher = ''
	for letter in message:
		# checking for space
		if(letter != ' '):
			# looks up the dictionary and
			# adds the shift to the index
			num = ( dict1[letter] + shift ) % 26
			# looks up the second dictionary for
			# the shifted alphabets and adds them
			cipher += dict2[num]
		else:
			# adds space
			cipher += ' '

	return cipher

# Function to decrypt the string
# according to the shift provided
def decrypt(message, shift):
	decipher = ''
	for letter in message:
		# checks for space
		if(letter != ' '):
			# looks up the dictionary and
			# subtracts the shift to the index
			num = ( dict1[letter] - shift + 26) % 26
			# looks up the second dictionary for the
			# shifted alphabets and adds them
			decipher += dict2[num]
		else:
			# adds space
			decipher += ' '

	return decipher

# driver function to run the program
def main():
	# use 'upper()' function to convert any lowercase characters to uppercase
	message = "cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_jdJBFOXJ}"
	shift = 13
	result = encrypt(message.upper(), shift)
	print (result)

	message = "picoCTF{next_time_I'll_try_2_rounds_of_rot13_ZNMldSDw}"
	shift = 13
	result = decrypt(message.upper(), shift)
	print (result)

# Executes the main function
if __name__ == '__main__':
	main()

```
### Method 2:
- The Easier way is by going to this website <a href="https://rot13.com/"> ROT13.com</a> and rotate the given flag by a shift of 13.
### Flag:

```sh
picoCTF{next_time_I'll_try_2_rounds_of_rot13_ZNMldSDw}
```