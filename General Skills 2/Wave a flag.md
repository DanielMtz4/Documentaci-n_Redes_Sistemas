## Descripción 
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/a00f554b16385d9970dae424f66ee1ab/warm) has extraordinarily helpful information...
## Hints
1. This program will only work in the webshell or another Linux computer.
2. To get the file accessible in your shell, enter the following in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/a00f554b16385d9970dae424f66ee1ab/warm`
3. Run this program by entering the following in the Terminal prompt: `$ ./warm`, but you'll first have to make it executable with `$ chmod +x warm`
4. h and --help are the most common arguments to give to programs to get more information from them!
5. Not every program implements help features like -h and --help.

## Solución
```
DanielMtzC-picoctf@webshell:~$ ls
README.txt
DanielMtzC-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings
DanielMtzC-picoctf@webshell:~$ ls
README.txt  strings
DanielMtzC-picoctf@webshell:~$ rm strings 
DanielMtzC-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/a00f554b16385d9970dae424f66ee1ab/warm
--2025-09-03 16:52:07--  https://mercury.picoctf.net/static/a00f554b16385d9970dae424f66ee1ab/warm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10936 (11K) [application/octet-stream]
Saving to: 'warm'

warm                 100%[=====================>]  10.68K  --.-KB/s    in 0s      

2025-09-03 16:52:07 (353 MB/s) - 'warm' saved [10936/10936]

DanielMtzC-picoctf@webshell:~$ ls   
README.txt  warm
DanielMtzC-picoctf@webshell:~$ file warm 
warm: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=985d9586d46e8651ab66c2fbb5a5473492466aa3, with debug_info, not stripped
DanielMtzC-picoctf@webshell:~$ chmod +x warm 
DanielMtzC-picoctf@webshell:~$ ./warm 
Hello user! Pass me a -h to learn what I can do!
DanielMtzC-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_18788aaa}
DanielMtzC-picoctf@webshell:~$ 
```
## Notas
History: Muestra todos los comandos que se han ejecutado desde la terminal
History -c: Elimina el historial de comandos
Ctrl + a: Va al inicio de la terminal de linux.
Ctrl + e: Va al final de la terminal de linux.
## Referencias
