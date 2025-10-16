## Descripción 

Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/213/disk.flag.img.gz)
## Hints

## Solución
```
DanielMtzC-picoctf@webshell:/tmp$ mmls disk.flag.img 
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000411647   0000204800   Linux Swap / Solaris x86 (0x82)
004:  000:002   0000411648   0000819199   0000407552   Linux (0x83)
DanielMtzC-picoctf@webshell:/tmp$ 
DanielMtzC-picoctf@webshell:/tmp$ fls disk.flag.img -o 411648
d/d 460:        home
d/d 11: lost+found
d/d 12: boot
d/d 13: etc
d/d 81: proc
d/d 82: dev
d/d 83: tmp
d/d 84: lib
d/d 87: var
d/d 96: usr
d/d 106:        bin
d/d 120:        sbin
d/d 466:        media
d/d 470:        mnt
d/d 471:        opt
d/d 472:        root
d/d 473:        run
d/d 475:        srv
d/d 476:        sys
d/d 2041:       swap
V/V 51001:      $OrphanFiles
DanielMtzC-picoctf@webshell:/tmp$ fls disk.flag.img 472 -o 411648
r/r 1875:       .ash_history
r/r * 1876(realloc):    flag.txt
r/r 1782:       flag.txt.enc
DanielMtzC-picoctf@webshell:/tmp$ ls
disk.flag.img  flag.txt.enc  hsperfdata_root  node-compile-cache
DanielMtzC-picoctf@webshell:/tmp$ openssl aes256 -salt -in flag.txt.enc -out flag.txt -k un
breakablepassword1234567
*** WARNING : deprecated key derivation used.
Using -iter or -pbkdf2 would be better.
DanielMtzC-picoctf@webshell:/tmp$ ls
disk.flag.img  flag.txt  flag.txt.enc  hsperfdata_root  node-compile-cache
DanielMtzC-picoctf@webshell:/tmp$ cat flag.txt
picoCTF{h4un71ng_p457_5113beab}
DanielMtzC-picoctf@webshell:/tmp$ openssl aes256 -salt -in flag.breakablepassword1234567 unb
```

## Notas

## Referencias
