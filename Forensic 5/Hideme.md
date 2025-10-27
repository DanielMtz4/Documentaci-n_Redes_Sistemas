## Descripción 
Every file gets a flag.The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://artifacts.picoctf.net/c/260/flag.png).
## Hints

## Solución
```
anielMtzC-picoctf@webshell:~$ ls
README.txt  exploit.py  flag.png
DanielMtzC-picoctf@webshell:~$ binwalk -e flag.png 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 512 x 504, 8-bit/color RGBA, non-interlaced
41            0x29            Zlib compressed data, compressed
39739         0x9B3B          Zip archive data, at least v1.0 to extract, name: secret/
39804         0x9B7C          Zip archive data, at least v2.0 to extract, compressed size: 2944, uncompressed size: 3095, name: secret/flag.png
42983         0xA7E7          End of Zip archive, footer length: 22

DanielMtzC-picoctf@webshell:~$ ls
README.txt  _flag.png.extracted  exploit.py  flag.png
DanielMtzC-picoctf@webshell:~$ cd _flag.png.extracted/
DanielMtzC-picoctf@webshell:~/_flag.png.extracted$ ls
29  29.zlib  9B3B.zip  secret
DanielMtzC-picoctf@webshell:~/_flag.png.extracted$ cd secret/
DanielMtzC-picoctf@webshell:~/_flag.png.extracted/secret$ ls
flag.png
DanielMtzC-picoctf@webshell:~/_flag.png.extracted/secret$ sz flag.png 
DanielMtzC-picoctf@webshell:~/_flag.png.extracted/secret$ 

Flag: picoCTF{Hiddinng_An_imag3_within_@n_ima9e_ad9f6587}
```
![[Pasted image 20251026233209.png]]
## Notas

## Referencias
