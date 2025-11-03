## Descripción 
We received an encrypted message. The modulus is built from primes large enough that factoring them isn’t an option, at least not today. See if you can make sense of the numbers and reveal the flag.Download the [message](https://challenge-files.picoctf.net/c_amiable_citadel/fddf51f15bd9f4145c4a4ebee5dfe7994bdab6393453f41f02c59cfd23a87fda/message.txt).
## Hints
1. When certain values in the encryption setup are smaller than usual, it opens up unexpected shortcuts to recover the plaintext
2. Consider whether you can invert the encryption without factoring `n`.
3. Read more about Coppersmith's_attack [here](https://en.wikipedia.org/wiki/Coppersmith's_attack)
## Solución
```
Código en python:
import gmpy2

e = 20
c = 6406374308104068575005667020962740842386353182361792134741
7147176296292403114340677176>

root, exacto = gmpy2.iroot(c,e)

if not exacto:
        print("no encontrado")

print(root)

print(int(root).to_bytes((root.bit_length()+7)//8, 'big').decode())

picoCTF{t1ny_e_f053d79c}
```
## Notas

## Referencias
