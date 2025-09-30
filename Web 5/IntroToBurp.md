
## Descripción 

## Hints
1. Try using burpsuite to intercept request to capture the flag.
2. Try mangling the request, maybe their server-side code doesn't handle malformed requests very well.
## Solución
```
ANTES
Referer: http://titan.picoctf.net:53684/dashboard
Cookie: session=.eJw1jcsOwiAQRX-lYe2ClwXcGd36Dc2UobGWQgM0xhj_3YmJy3vu68383F7sxNBDWnAGdmC-lmloeQmJuBFHa_vRCFDInZH9KNVkg0Hdc2e59IjKGyepN-0xDgnWQLUrpDnEDuKCKULnIWMHWB-ecrltlLA0ZjTJDWp95oLEhFQ_cs8pDGlfx1CIKim0E5JrS95eQ_l_nG8X9vkCXfA5yA.aNsL2A.kpBxcsxXUsOhZ_l5MKeshc0K7yY
Upgrade-Insecure-Requests: 1
Priority: u=0, i

otp = Otp 

DESPUES 
Referer: http://titan.picoctf.net:53684/dashboard
Cookie: session=.eJw1jcsOwiAQRX-lYe2ClwXcGd36Dc2UobGWQgM0xhj_3YmJy3vu68383F7sxNBDWnAGdmC-lmloeQmJuBFHa_vRCFDInZH9KNVkg0Hdc2e59IjKGyepN-0xDgnWQLUrpDnEDuKCKULnIWMHWB-ecrltlLA0ZjTJDWp95oLEhFQ_cs8pDGlfx1CIKim0E5JrS95eQ_l_nG8X9vkCXfA5yA.aNsL2A.kpBxcsxXUsOhZ_l5MKeshc0K7yY
Upgrade-Insecure-Requests: 1
Priority: u=0, i

RESULTADO ANTES
Invalid OTP

RESULTADO DESPUES
Welcome, DAMC you sucessfully bypassed the OTP request. 
Your Flag: picoCTF{#0TP_Bypvss_SuCc3$S_b3fa4f1a}
```
## Notas

## Referencias
