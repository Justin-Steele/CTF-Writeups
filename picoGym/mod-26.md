# picoCTF
## picoGym (original date unknown)

# Mod 26
### Cryptography
### 10 points
## Challenge Description:
Cryptography can be easy, do you know what ROT13 is? 
```cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_GYpXOHqX}```

# Solution Steps
The name and description both point towards this being a ROT13 cipher, which is where letters from plaintext are shifted 13 spaces (e.g. A->N, B->O, C->P). We are given the ciphertext, so we just need to shift them back.
It would be easy enough to throw this in a rot13 calculator online, but for the sake of the competition, let's write something up in python:

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

Since the title is mod26, instead of doing any character mappings, I went with a solution that could be implemented similarly in other languages.
