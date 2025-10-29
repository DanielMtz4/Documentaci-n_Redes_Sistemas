## Descripción 
How about some hide and seek heh?Look at this image [here](https://artifacts.picoctf.net/c/235/atbash.jpg).
## Hints
1. Download the image and try to extract it.
## Solución
```
DanielMtzC-picoctf@webshell:~$ steghide extract -sf atbash.jpg 
Enter passphrase: 
wrote extracted data to "encrypted.txt".
DanielMtzC-picoctf@webshell:~$ cat encrypted.txt 
krxlXGU{zgyzhs_xizxp_92533667}
DanielMtzC-picoctf@webshell:~$ 

picoCTF{atbash_crack_92533667}
```
## Notas

## Referencias
https://cyberchef.io/#recipe=Atbash_Cipher()&input=a3J4bFhHVXt6Z3l6aHNfeGl6eHBfOTI1MzM2Njd9