## Descripción 
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings) without running it?
## Hints
[strings](https://linux.die.net/man/1/strings)
## Solución
```
DanielMtzC-picoctf@webshell:~$ ls
README.txt
AGREGAMOS EL ARCHIVO LLAMADO 'STRINGS'
DanielMtzC-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings
--2025-09-03 16:37:22--  https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 776032 (758K) [application/octet-stream]
Saving to: 'strings'

strings              100%[=====================>] 757.84K  1.87MB/s    in 0.4s    

2025-09-03 16:37:22 (1.87 MB/s) - 'strings' saved [776032/776032]

DanielMtzC-picoctf@webshell:~$ ls 
README.txt  strings
VEMOS QUE TIPO DE ARCHIVO ES
DanielMtzC-picoctf@webshell:~$ file strings 
strings: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=0cdedfba33422d235dba8c90e00fb77b235f1ff8, not stripped
DanielMtzC-picoctf@webshell:~$ strings 
.bash_history    .cache/          .profile         README.txt
.bash_logout     .config/         .python_history  strings
.bashrc          .local/          .wget-hsts   
EJECUTAMOS EL STRING A EL ARCHIVO 'STRINGS' Y HACER UN GREP A PICO   
DanielMtzC-picoctf@webshell:~$ strings strings | grep pico
picoCTF{5tRIng5_1T_7f766a23}
DanielMtzC-picoctf@webshell:~$
```
## Notas
rm -rf: Borra carpetas con todos sus caracteres

Grep no puede buscar palabras en un archivo ejecutable

string: nos da las cadenas de texto de un archivo ejecutable, quitando los caracteres no imprimibles.

./ : Nos ayuda a ejecutar un archivo ejecutable

chmod: change mods, cambia permisos de lectura, escritura o ejecución a archivos que no lo tienen en primera instancia
## Referencias

[strings](https://linux.die.net/man/1/strings)
