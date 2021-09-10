# keygenme-trial.py
- **picoGym - picoCTF 2021**
- **Category: Reverse Engineering**
- **Points: 30**

## Challenge Description
[keygenme-trial.py](https://mercury.picoctf.net/static/b016c61bd2cc0be05a59da1dde67a2ac/keygenme-trial.py)

## Solution Steps
Opened the file and read through the code. It looks like it hashes the username and grabs indexed pieces of the hash as the dynamic portion of the key, so I replaced the first menu function with something that calculates the hash. Updated function below:

```python

def estimate_burn():
    print(hashlib.sha256(bUsername_trial).hexdigest())
```
