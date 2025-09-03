## Descripción 
Unzip this archive and find the flag.

- [Download zip file](https://artifacts.picoctf.net/c/503/big-zip-files.zip)
## Hints
Can grep be instructed to look at every file in a directory and its subdirectories?
## Solución
```
 11  wget https://artifacts.picoctf.net/c/503/big-zip-files.zip
   12  ls
   13  rm enc_flag 
   14  unzip big-zip-files.zip 
   15  ls
   16  cd big-zip-files/
   17  ls
   18  cd ..
   19  cd big-zip-files/ | grep pico
   20  grep -r pico big-zip-files
   21  history
DanielMtzC-picoctf@webshell:~$ 
```
## Notas
grep -r: Busca una palabra o conjunto de palabras dentro de subdirectorios de una carpeta
## Referencias
