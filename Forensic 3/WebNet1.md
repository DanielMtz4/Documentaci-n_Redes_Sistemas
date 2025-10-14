## Descripción 
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.
## Hints
1. Try using a tool like Wireshark.
2. How can you decrypt the TLS stream?
## Solución
```
──(daniel_mtz_4㉿LAPTOP-34F4JT33)-[/mnt/c/WINDOWS/system32]
└─$ cd

┌──(daniel_mtz_4㉿LAPTOP-34F4JT33)-[~]
└─$ cd Downloads/webnet1/

┌──(daniel_mtz_4㉿LAPTOP-34F4JT33)-[~/Downloads/webnet1]
└─$ strings vulture.jpg -n15
picoCTF{honey.roasted.peanuts}
 )/'%'/9339GDG]]}
 )/'%'/9339GDG]]}
%&'()*456789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz
&'()*56789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz

┌──(daniel_mtz_4㉿LAPTOP-34F4JT33)-[~/Downloads/webnet1]
└─$ 


```
## Notas

## Referencias
