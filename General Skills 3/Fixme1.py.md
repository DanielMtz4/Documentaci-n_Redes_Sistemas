## Descripción 
Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/27/fixme1.py)
## Hints
1. Indentation is very meaningful in Python
2. To view the file in the webshell, do: `$ nano fixme1.py`
3. To exit `nano`, press Ctrl and x and follow the on-screen prompts.
4. The `str_xor` function does not need to be reverse engineered for this challenge.
## Solución
```
DanielMtzC-picoctf@webshell:~$ python3 fixme1.py 
Traceback (most recent call last):
  File "/home/DanielMtzC-picoctf/fixme1.py", line 22, in <module>
    str_xor()
TypeError: str_xor() missing 2 required positional arguments: 'secret' and 'key'
DanielMtzC-picoctf@webshell:~$ nano fixme1.py 
DanielMtzC-picoctf@webshell:~$ python3 fixme1.py 
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_182342f7}
DanielMtzC-picoctf@webshell:~$ 
```
## Notas

## Referencias
