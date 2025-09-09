## Descripción 
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/16/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/16/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/16/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## Hints
1. To view the level3.hash.bin file in the webshell, do: `$ bvi level3.hash.bi`
2. To exit `bvi` type `:q` and press enter.
3. The `str_xor` function does not need to be reverse engineered for this challenge.
## Solución
```
DanielMtzC-picoctf@webshell:~$ cat level3.py 
import hashlib

### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
###############################################################################

flag_enc = open('level3.flag.txt.enc', 'rb').read()
correct_pw_hash = open('level3.hash.bin', 'rb').read()


def hash_pw(pw_str):
    pw_bytes = bytearray()
    pw_bytes.extend(pw_str.encode())
    m = hashlib.md5()
    m.update(pw_bytes)
    return m.digest()


def level_3_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    user_pw_hash = hash_pw(user_pw)
    
    if( user_pw_hash == correct_pw_hash ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")



level_3_pw_check()


# The strings below are 7 possibilities for the correct password. 
#   (Only 1 is correct)
pos_pw_list = ["6997", "3ac8", "f0ac", "4b17", "ec27", "4e66", "865e"]

DanielMtzC-picoctf@webshell:~$ bvi level3.hash.bin 

bvi version 1.4.0 Copyright (C) 1996-2014 by Gerhard Buergmann
DanielMtzC-picoctf@webshell:~$ python3 level3.py 
Please enter correct password for flag: ec27
That password is incorrect
DanielMtzC-picoctf@webshell:~$ nano level3.py 
DanielMtzC-picoctf@webshell:~$ python3 level3.py 
  File "/home/DanielMtzC-picoctf/level3.py", line 39
    The strings below are 7 possibilities for the correct password. 
        ^^^^^^^
SyntaxError: invalid syntax
DanielMtzC-picoctf@webshell:~$ nano level3.py 
DanielMtzC-picoctf@webshell:~$ python3 level3.py 
That password is incorrect
That password is incorrect
That password is incorrect
That password is incorrect
That password is incorrect
That password is incorrect
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_2b072a90}
```
## Notas

nano: permite entrar a un archivo y hacer ciertos modificaciones, las guardas con ctrl + O 
## Referencias
