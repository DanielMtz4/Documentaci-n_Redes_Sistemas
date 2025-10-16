## Descripción 
Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image: [dds1-alpine.flag.img.gz](https://mercury.picoctf.net/static/f63e4eba644c99e92324b65cbd875db6/dds1-alpine.flag.img.gz)
## Hints
1. Have you ever used `file` to determine what a file was?
2. Relevant terminal-fu in picoGym: https://play.picoctf.org/practice/challenge/85
3. Mastering this terminal-fu would enable you to find the flag in a single command: https://play.picoctf.org/practice/challenge/48
4. Using your own computer, you could use qemu to boot from this disk!
## Solución
```

DanielMtzC-picoctf@webshell:/tmp$ ls
dds1-alpine.flag.img.gz  hsperfdata_root  node-compile-cache
DanielMtzC-picoctf@webshell:/tmp$ gunzip dds1-alpine.flag.img.gz 
DanielMtzC-picoctf@webshell:/tmp$ ls
dds1-alpine.flag.img  hsperfdata_root  node-compile-cache
DanielMtzC-picoctf@webshell:/tmp$ srch_strings dds1-alpine.flag.img | grep pico
ffffffff81399ccf t pirq_pico_get
ffffffff81399cee t pirq_pico_set
ffffffff820adb46 t pico_router_probe
  SAY **picoCTF{f0r3ns1c4t0r_n30phyt3_ad5c96c0}**
DanielMtzC-picoctf@webshell:/tmp$ 
```
## Notas

## Referencias
