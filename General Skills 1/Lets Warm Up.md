## Descripción
If I told you a word started with 0x70 in hexadecimal, what would it start with in ASCII?. Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'picoCTF{hello}' as the flag.
## Solución
Forma 1: Usar un sitio web 
0x70 = p

Forma 2
==========================================================================
==========================================================================

DanielMtzC-picoctf@webshell:~$ python
Python 3.10.12 (main, Feb  4 2025, 14:57:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> int(0x70)
112
>>> chr(112)
'p'
>>> 
## Notas 
## Referencias