## Descripción 
Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/27/fixme1.py)
## Hints
1. Indentation is very meaningful in Python
2. To view the file in the webshell, do: `$ nano fixme1.py`
3. To exit `nano`, press Ctrl and x and follow the on-screen prompts.
4. The `str_xor` function does not need to be reverse engineered for this challenge.
## Solución
```

DanielMtzC-picoctf@webshell:~$ ls
README.txt  fixme2.py
DanielMtzC-picoctf@webshell:~$ python3 fixme2.py 
  File "/home/DanielMtzC-picoctf/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
DanielMtzC-picoctf@webshell:~$ nano fixme2.py 
DanielMtzC-picoctf@webshell:~$ python3 fixme2.py 
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_4863e11b}
```
## Notas

## Referencias
