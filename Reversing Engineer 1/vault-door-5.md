## Descripción 
In the last challenge, you mastered octal (base 8), decimal (base 10), and hexadecimal (base 16) numbers, but this vault door uses a different change of base as well as URL encoding!The source code for this vault is here: [VaultDoor5.java](https://challenge-files.picoctf.net/c_fickle_tempest/bd4f8f70a70dacc0e57dfc24ff34f5297a3db3c9c4366fd8df02f6bf47c794c8/VaultDoor5.java)
## Hints
1. You may find an encoder/decoder tool helpful, such as https://encoding.tools/
2. Read the wikipedia articles on URL encoding and base 64 encoding to understand how they work and what the results look like.
## Solución
```
picoCTF{c0nv3rt1ng_fr0m_ba5e_64_be9f10a4}
```
## Notas

## Referencias
https://cyberchef.io/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true)URL_Decode()&input=SlRZekpUTXdKVFpsSlRjMkpUTXpKVGN5SlRjMEpUTXhKVFpsSlRZM0pUVm0gSlRZMkpUY3lKVE13SlRaa0pUVm1KVFl5SlRZeEpUTTFKVFkxSlRWbUpUTTIgSlRNMEpUVm1KVFl5SlRZMUpUTTVKVFkySlRNeEpUTXdKVFl4SlRNMA