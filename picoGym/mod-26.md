# Goal
Cryptography can be easy, do you know what ROT13 is? 
`cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_GYpXOHqX}

# Steps
It would be easy enough to throw this in a rot13 calculator online, but for the sake of the competition, let's write this up in python:

```python
import sys

plain_text = ""
cipher_text = sys.argv[1]
for letter in cipher_text:
    if letter.islower():
        plain_text += chr((((ord(letter) - 97) + 13) % 26) + 97)
    elif letter.isupper():
        plain_text += chr((((ord(letter) - 65) + 13) % 26) + 65)
    else:
        plain_text += letter

print(plain_text)
```
