## Descripción 
Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/61864/` or http://jupiter.challenges.picoctf.org:61864
## Hints
1. What is that cookie?
2. Have you heard of JWT?
## Solución
 ```
 HMACSHA256( 
    base64UrlEncode(header) + "." +
    base64UrlEncode(payload),

ilovepico

JWT DECODE 
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiYWRtaW4ifQ.gtqDl4jVDvNbEe_JYEZTN19Vx6X9NNZtRVbKPBkhO-s
)
 ```
## Notas

## Referencias
