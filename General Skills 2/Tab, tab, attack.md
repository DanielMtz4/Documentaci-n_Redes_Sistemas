## Descripción 
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/e38f6a5b69b45d21e33cf7281d8c2531/Addadshashanammu.zip)

## Hints
After `unzip`ing, this problem can be solved with 11 button-presses...(mostly Tab)...

## Solución
```
lcome to the picoCTF webshell!
DanielMtzC-picoctf@webshell:~$ ls
Addadshashanammu.zip  README.txt
DanielMtzC-picoctf@webshell:~$ ls -la Addadshashanammu.zip 
-rw-rw-r-- 1 DanielMtzC-picoctf DanielMtzC-picoctf 4521 Mar 16  2021 Addadshashanammu.zip
DanielMtzC-picoctf@webshell:~$ unzip Addadshashanammu.zip 
Archive:  Addadshashanammu.zip
   creating: Addadshashanammu/
   creating: Addadshashanammu/Almurbalarammi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet  
DanielMtzC-picoctf@webshell:~$ ls
Addadshashanammu  Addadshashanammu.zip  README.txt
DanielMtzC-picoctf@webshell:~$ cd A
-bash: cd: A: No such file or directory
DanielMtzC-picoctf@webshell:~$ cd Addadshashanammu/
DanielMtzC-picoctf@webshell:~/Addadshashanammu$ ls
Almurbalarammi
DanielMtzC-picoctf@webshell:~/Addadshashanammu$ cd Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
DanielMtzC-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ls
fang-of-haynekhtnamet
DanielMtzC-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ls -la
total 12
drwxr-xr-x 2 DanielMtzC-picoctf DanielMtzC-picoctf   35 Mar 16  2021 .
drwxr-xr-x 3 DanielMtzC-picoctf DanielMtzC-picoctf   27 Mar 16  2021 ..
-rwxr-xr-x 1 DanielMtzC-picoctf DanielMtzC-picoctf 8320 Mar 16  2021 fang-of-haynekhtnamet
DanielMtzC-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ./fang-of-haynekhtnamet 
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_f3553887}
DanielMtzC-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ^C
DanielMtzC-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ^C
DanielMtzC-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ 
```
## Notas
cd: Se va a la carpeta del usuario
cd -: Se va a la carpeta en la que estabas anteriormente
## Referencias
