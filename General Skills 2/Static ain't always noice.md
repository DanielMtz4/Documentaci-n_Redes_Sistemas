## Descripción 

## Hints

## Solución
DESCARGAMOS EL PRIMER ARCHIVO
```
DanielMtzC-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/static
--2025-09-03 17:01:07--  https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/static
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 8376 (8.2K) [application/octet-stream]
Saving to: 'static'

static                                         100%[====================================================================================================>]   8.18K  --.-KB/s    in 0s      

2025-09-03 17:01:07 (78.7 MB/s) - 'static' saved [8376/8376]

DanielMtzC-picoctf@webshell:~$ ls
8#TT 1tt$DN static  warm
 @@ 0@)ppCV``^okyDanielMtzC-picoctf@webshell:~$ 
DanielMtzC-picoctf@webshell:~$ cat static
```
DESCARGAMOS EL SEGUNDO ARCHIVO
```DanielMtzC-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/ltdis.sh
--2025-09-03 17:03:26--  https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/ltdis.sh
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 785 [application/octet-stream]
Saving to: 'ltdis.sh'

ltdis.sh                                       100%[====================================================================================================>]     785  --.-KB/s    in 0s      

2025-09-03 17:03:26 (257 MB/s) - 'ltdis.sh' saved [785/785]

DanielMtzC-picoctf@webshell:~$ ls
README.txt  ltdis.sh  static
DanielMtzC-picoctf@webshell:~$ 
```

```
DanielMtzC-picoctf@webshell:~$ ls     
README.txt  ltdis.sh  static  static.ltdis.strings.txt  static.ltdis.x86_64.txt
DanielMtzC-picoctf@webshell:~$ cat static.ltdis.strings.txt | grep pico
   1020 picoCTF{d15a5m_t34s3r_6f8c8200
```
## Notas

## Referencias
