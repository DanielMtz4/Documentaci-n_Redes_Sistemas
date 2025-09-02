## Descripción 
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/315d3325dc668ab7f1af9194f2de7e7a/file)? This would be really tedious to look through manually, something tells me there is a better way.
## Solución
Descargamos el archivo
```
DanielMtzC-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/315d3325dc668ab7f1af9194f2de7e7a/file
```
Encontramos la bandera ``

```
DanielMtzC-picoctf@webshell:~$ grep 'picoCTF' file 
picoCTF{grep_is_good_to_find_things_f77e0797}
```
## Notas
wc: Cuenta las lineas, bytes y caracteres de un archivo de texto.
file: Determina el tipo de archivo
## Referencias
