## Descripción 
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/21/level4.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/21/level4.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/21/level4.hash.bin) in the same directory too.There are 100 potential passwords with only 1 being correct. You can find these by examining the password checker script.
## Hints
1. A for loop can help you do many things very quickly.
2. The `str_xor` function does not need to be reverse engineered for this challenge.
## Solución
```
DanielMtzC-picoctf@webshell:~$ python level4.py 
9f63
DanielMtzC-picoctf@webshell:~$ nano level4.py
DanielMtzC-picoctf@webshell:~$ python level4.py 
Please enter correct password for flag: 9f63
Welcome back... your flag, user:
picoCTF{fl45h_5pr1ng1ng_d770d48c}
9f63
```
## Notas

## Referencias

[From Hex - CyberChef](https://cyberchef.io/#recipe=From_Hex\('Auto'\)&input=MHgzNCAweDY1IDB4NjMgMHgzOQ)