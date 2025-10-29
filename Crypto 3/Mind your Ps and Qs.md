## Descripción 
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/38f30029ab93478310e906d3d084a4c1/values)
## Hints
1. Bits are expensive, I used only a little bit over 100 to save money
## Solución
```
pytDanielMtzC-picoctf@webshell:~$ python3
Python 3.10.12 (main, Feb  4 2025, 14:57:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> from Crypto.Util.number import long_to_bytes
>>> from Crypto.Util.number import inverse
>>> 
>>> c= 240986837130071017759137533082982207147971245672412893755780400885108149004760496
>>> 
>>> n = 831416828080417866340504968188990032810316193533653516022175784399720141076262857
>>> e = 65537
>>> 
>>> p= 1593021310640923782355996681284584012117
>>> 
>>> q = 521911930824021492581321351826927897005221
>>> 
>>> tn = (p-1) * (q-1)
>>> d = pow(e, -1, tn)
>>> m = pow(c,d,n)
>>> 
>>> flag = bytes.fromhex(hex(m)[2:]).decode()
>>> 
>>> print(flag)
picoCTF{sma11_N_n0_g0od_23540368}

```
## Notas

## Referencias
