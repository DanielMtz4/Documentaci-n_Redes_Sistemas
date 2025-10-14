## Descripción 
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/2978e1270538613cd8181c7b0dabe9bd/dolls.jpg)
## Hints
1. Wait, you can hide files inside files? But how do you find them?
2. Make sure to submit the flag as picoCTF{XXXXX}
## Solución
```
┌──(daniel_mtz_4㉿LAPTOP-34F4JT33)-[~/Downloads/matryoshka_doll]
└─$ binwalk -e dolls.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378942, uncompressed size: 383937, name: base_images/2_c.jpg

WARNING: One or more files failed to extract: either no utility was found or it's unimplemented


┌──(daniel_mtz_4㉿LAPTOP-34F4JT33)-[~/Downloads/matryoshka_doll]
└─$ ls
dolls.jpg  _dolls.jpg.extracted

┌──(daniel_mtz_4㉿LAPTOP-34F4JT33)-[~/Downloads/matryoshka_doll]
└─$ cd _dolls.jpg.extracted/

┌──(daniel_mtz_4㉿LAPTOP-34F4JT33)-[~/Downloads/matryoshka_doll/_dolls.jpg.extracted]
└─$ ls
4286C.zip  base_images

┌──(daniel_mtz_4㉿LAPTOP-34F4JT33)-[~/Downloads/matryoshka_doll/_dolls.jpg.extracted]
└─$ 

──(daniel_mtz_4㉿LAPTOP-34F4JT33)-[~/Downloads/matryoshka_doll/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└─$ cd _4_c.jpg.extracted/

┌──(daniel_mtz_4㉿LAPTOP-34F4JT33)-[~/Downloads/matryoshka_doll/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted]
└─$ ls
136DA.zip  flag.txt

┌──(daniel_mtz_4㉿LAPTOP-34F4JT33)-[~/Downloads/matryoshka_doll/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted]
└─$ cat flag.txt 
picoCTF{4cf7ac000c3fb0fa96fb92722ffb2a32}
┌──(daniel_mtz_4㉿LAPTOP-34F4JT33)-[~/Downloads/matryoshka_doll/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted]
└─$ 


```
## Notas

## Referencias
