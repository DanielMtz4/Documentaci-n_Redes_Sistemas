## Descripción 
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 7480`.

## Hints
1. Remember the flag format is picoCTF{XXXX}
2. What's a pipe? No not that kind of pipe... This [kind](http://www.linfo.org/pipes.html) 
## Solución
```
DanielMtzC-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 7480 | grep picoCT
F
picoCTF{digital_plumb3r_06e9d954}
```
Forma 2:
```
DanielMtzC-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 7480 > bandera   
^C
DanielMtzC-picoctf@webshell:~$ cat bandera | grep pico
picoCTF{digital_plumb3r_06e9d954}
DanielMtzC-picoctf@webshell:~$ 
```

## Notas
Pipe ( | ) - Forma de redireccionar que es usada en linux u otros sistemas operativos como unix para enviar la salida de un programa a otro programa para futuros procesamientos.
## Referencias
http://www.linfo.org/pipes.html
