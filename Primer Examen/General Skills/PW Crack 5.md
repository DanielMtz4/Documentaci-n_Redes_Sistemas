## Descripción 
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/32/level5.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/32/level5.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/32/level5.hash.bin) in the same directory too. Here's a [dictionary](https://artifacts.picoctf.net/c/32/dictionary.txt) with all possible passwords based on the password conventions we've seen so far.
## Hints
1. Opening a file in Python is crucial to using the provided dictionary.
2. You may need to trim the whitespace from the dictionary word before hashing. Look up the Python string function, `strip`.
3. The `str_xor` function does not need to be reverse engineered for this challenge.
## Solución
```
import hashlib

### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in z>
###############################################################################

flag_enc = open('level5.flag.txt.enc', 'rb').read()
correct_pw_hash = open('level5.hash.bin', 'rb').read()


def hash_pw(pw_str):
    pw_bytes = bytearray()
    pw_bytes.extend(pw_str.encode())
    m = hashlib.md5()
    m.update(pw_bytes)
    return m.digest()
    
def level_5_pw_check():

#    user_pw = input("Please enter correct password for flag: ")
        with open("dictionary.txt") as f:
                lines = f.readlines()
                for line in lines:
                        user_pw = line.strip()
                        user_pw_hash = hash_pw(user_pw)
                        if( user_pw_hash == correct_pw_hash ):
                                print("Welcome back... your flag, user:")
                                decryption = str_xor(flag_enc.decode(), user_pw)
                                print(decryption)
                                return
                        print("That password is incorrect")



level_5_pw_check()

Welcome back... your flag, user:
picoCTF{h45h_sl1ng1ng_40f26f81}
```
## Notas

## Referencias

[From Hex - CyberChef](https://cyberchef.io/#recipe=From_Hex\('Auto'\)&input=MHgzNCAweDY1IDB4NjMgMHgzOQ)