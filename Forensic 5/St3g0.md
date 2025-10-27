## Descripción 
Download this image and find the flag.

- [Download image](https://artifacts.picoctf.net/c/217/pico.flag.png)
## Hints
1. We know the end sequence of the message will be `$t3g0`.
## Solución
```
DanielMtzC-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/217/pico.flag.png
--2025-10-27 05:22:03--  https://artifacts.picoctf.net/c/217/pico.flag.png
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.33, 3.170.131.72, 3.170.131.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.33|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 13443 (13K) [application/octet-stream]
Saving to: 'pico.flag.png'

pico.flag.png        100%[=====================>]  13.13K  --.-KB/s    in 0s      

2025-10-27 05:22:03 (472 MB/s) - 'pico.flag.png' saved [13443/13443]

DanielMtzC-picoctf@webshell:~$ ls
README.txt  cat.jpg  exploit.py  pico.flag.png
DanielMtzC-picoctf@webshell:~$ rm cat.jpg 
DanielMtzC-picoctf@webshell:~$ zsteg pico.flag.png 
b1,r,lsb,xy         .. text: "~__B>VG?G@"
b1,rgb,lsb,xy       .. text: "picoCTF{7h3r3_15_n0_5p00n_a9a181eb}$t3g0"
b1,abgr,lsb,xy      .. text: "E2A5q4E%uSA"
b2,b,lsb,xy         .. text: "AAPAAQTAAA"
b2,b,msb,xy         .. text: "HWUUUUUU"
b2,a,lsb,xy         .. file: Matlab v4 mat-file (little endian) >\004<\305P, numeric, rows 0, columns 0
b2,a,msb,xy         .. file: Matlab v4 mat-file (little endian) | <\243, numeric, rows 0, columns 0
b3,r,lsb,xy         .. file: gfxboot compiled html help file
b4,r,lsb,xy         .. file: Targa image data (16-273) 65536 x 4097 x 1 +4352 +4369 - 1-bit alpha - right "\021\020\001\001\021\021\001\001\021\021\001"
b4,g,lsb,xy         .. file: 0420 Alliant virtual executable not stripped
b4,b,lsb,xy         .. file: Targa image data - Map 272 x 17 x 16 +257 +272 - 1-bit alpha "\020\001\021\001\021\020\020\001\020\001\020\001"
b4,bgr,lsb,xy       .. file: Targa image data - Map 273 x 272 x 16 +1 +4113 - 1-bit alpha "\020\001\001\001"
b4,rgba,lsb,xy      .. file: Novell LANalyzer capture file
b4,rgba,msb,xy      .. file: Applesoft BASIC program data, first line number 8
b4,abgr,lsb,xy      .. file: Novell LANalyzer capture file
DanielMtzC-picoctf@webshell:~$ 

FLAG: picoCTF{7h3r3_15_n0_5p00n_a9a181eb}
```
## Notas

## Referencias
