## Descripción 
Unzip this archive and find the file named 'uber-secret.txt'

- [Download zip file](https://artifacts.picoctf.net/c/502/files.zip)
## Hints

## Solución
```
DanielMtzC-picoctf@webshell:~$ find uber-secret.txt
find: 'uber-secret.txt': No such file or directory
DanielMtzC-picoctf@webshell:~$ find -d uber-secret.txt
find: warning: the -d option is deprecated; please use -depth instead, because the latter is a POSIX-compliant feature.
find: paths must precede expression: `uber-secret.txt'
DanielMtzC-picoctf@webshell:~$ find . -type f -name "*uber-secret.txt"
./files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
DanielMtzC-picoctf@webshell:~$ cd 
DanielMtzC-picoctf@webshell:~$ cd ./files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
-bash: cd: ./files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt: Not a directory
DanielMtzC-picoctf@webshell:~$ 
DanielMtzC-picoctf@webshell:~$ cd ./files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/               
DanielMtzC-picoctf@webshell:~/files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets$ cat uber-secret.txt 
picoCTF{f1nd_15_f457_ab443fd1}
DanielMtzC-picoctf@webshell:~/files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets$ 
```
## Notas
find . -type f -name "file.txt": Encuentra un archivo en el directorio actual
## Referencias
