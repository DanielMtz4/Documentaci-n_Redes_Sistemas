## Descripción 
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 29221`.
## Hints
1. Can grep be instructed to look at every file in a directory and its subdirectories?
2. It might help to have multiple windows open.

## Solución
Deciframos el código en binario, después en octal (Se sabe que es octal porque no tiene números arriba de 7) y por último convertir a hexadecimal
```
DanielMtzC-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 29221
Let us see how data is stored
chair
Please give the 01100011 01101000 01100001 01101001 01110010 as a word.
...
you have 45 seconds.....

Input:
chair
Please give me the  146 141 154 143 157 156 as a word.
Input:
falcon
Please give me the 6c696d65 as a word.
Input:
lime
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_00a975ff}
```
## Notas
Such as: Tales como
## Referencias
- [Download zip file](https://artifacts.picoctf.net/c/503/big-zip-files.zip)
