## Descripción 
Someone's commits seems to be preventing the program from working. Who is it?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/157/challenge.zip)
## Hints
1. In collaborative projects, many users can make many changes. How can you see the changes within one file?
2. Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control).
3. You can use `python3 <file>.py` to try running the code, though you won't need to for this challenge.
## Solución
```
DanielMtzC-picoctf@webshell:~/drop-in$ git log
DanielMtzC-picoctf@webshell:~/drop-in$ git log message.py
DanielMtzC-picoctf@webshell:~/drop-in$ 
```
## Notas
**`git log`**: Muestra el **historial de commits** en un repositorio.  
Es como la “bitácora” de todo lo que ha pasado en el proyecto.
## Referencias
