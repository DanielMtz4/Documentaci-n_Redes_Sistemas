## Descripción 
How about we take you on an adventure on exploring certificate signing requestsTake a look at this CSR file [here](https://artifacts.picoctf.net/c/425/readmycert.csr).
## Hints
1. Download the certificate signing request and try to read it.
## Solución
```
DanielMtzC-picoctf@webshell:~$ ls
README.txt  exp.py  exploit.py  readmycert.csr
DanielMtzC-picoctf@webshell:~$ cat readmycert.csr 
-----BEGIN CERTIFICATE REQUEST-----
MIICpzCCAY8CAQAwPDEmMCQGA1UEAwwdcGljb0NURntyZWFkX215Y2VydF82OTNm
N2MwM30xEjAQBgNVBCkMCWN0ZlBsYXllcjCCASIwDQYJKoZIhvcNAQEBBQADggEP
ADCCAQoCggEBAPp+XuDB3ZkmrkvAsgtjP+mjIcYDWfptuZsJieu6eRl39wl4Sg38
+/OfY24LV9sNmgKyTGvpmCaUoZMYkvkulYSoFzE0xqPBo6kruLEyIvqqpAFqRH2b
mierLT6RcKgJHYr/Vt6SwP8NCCawCrvhQ4NZcuB49Hr/2AiGHzmf86/lG/c+lhmH
gyqPb1kDghsVxi/GNs9i7AgniZikqT8OTp0INmmCgZtJn1Jo615Iu/tFiC8Sfhhg
QHmTDLjgx1oP1kvZV2PE5UUN/oC05Zup8f31LksXZwpazZKwYC/LbN96HdqgVQ9K
S8e/4I7MJQmPmLIsLp3sdL2FiDGML3smAi0CAwEAAaAmMCQGCSqGSIb3DQEJDjEX
MBUwEwYDVR0lBAwwCgYIKwYBBQUHAwIwDQYJKoZIhvcNAQELBQADggEBAOxSR8Fs
Tdjfu9e0vRNqKWd09ISmYDQc3qnSbLRlYZyMK4pguALq310h/1nNgURWESbNJPOp
FkBWG0XWhWyWP7rTqxo/pk9AKx0TNbHDrS6KiBnKPq0mxjPZsH1L7wNYDc5OANDl
btvn3zT7lMms6z1qM7xUWXR76n2xL/81cdF725nBZ00mWmPW0S1pSmA4EEHCEgNW
0vWQqsIDki3gYc4NCm8OHjx79kcwE+ksyc6vHgMOwsYoOFJnyayhl15oN/3x7hW3
G1xovPupABpfOSNOcTwbgfrfjUDOLx/wirvj9L1N5EGDh4FOLaRZDs+tMrimGBBS
zGU13BnykmQ5jOQ=
-----END CERTIFICATE REQUEST-----
DanielMtzC-picoctf@webshell:~$ 

DESENCRIPCION:0..§0......0<1&0$..U....picoCTF{read_mycert_693f7c03}1.0...U.).	ctfPlayer0.."0
.	*.H.÷
..........0..
.....ú~^àÁÝ.&®KÀ².c?é£!Æ.Yúm¹.	.ëºy.w÷	xJ
üûó.cn.WÛ
..²Lké.&.¡...ù...¨.14Æ£Á£©+¸±2"úª¤.jD}..'«->.p¨	..ÿVÞ.Àÿ
.&°
»áC.YràxôzÿØ...9.ó¯å.÷>....*.oY....Æ/Æ6Ïbì.'..¤©?.N..6i...I.Rhë^H»ûE./.~.`@y..¸àÇZ.ÖKÙWcÄåE
þ.´å.©ñýõ.K.g
ZÍ.°`/Ëlßz.Ú U.JKÇ¿à.Ì%	..²,..ìt½..1./{&.-..... &0$.	*.H.÷
.	.1.0.0...U.%..0
..+.......0
.	*.H.÷
..........ìRGÁlMØß»×´½.j)gtô.¦`4.Þ©Òl´ea..+.`¸.êß]!ÿYÍ.DV.&Í$ó©.@V.EÖ.l.?ºÓ«.?¦O@+..5±Ã.....Ê>.&Æ3Ù°}Kï.X
ÎN.ÐånÛçß4û.É¬ë=j3¼TYt{ê}±/ÿ5qÑ{Û.ÁgM&ZcÖÑ-iJ`8.AÂ..VÒõ.ªÂ..-àaÎ
o..<{öG0.é,ÉÎ¯...ÂÆ(8RgÉ¬¡.^h7ýñî.·.\h¼û©.._9#Nq<..úß.@Î/.ð.»ãô½MäA...N-¤Y.Ï.2¸¦..RÌe5Ü.ò.d9.ä
```
## Notas

## Referencias
https://cyberchef.io/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true)&input=TUlJQ3B6Q0NBWThDQVFBd1BERW1NQ1FHQTFVRUF3d2RjR2xqYjBOVVJudHlaV0ZrWDIxNVkyVnlkRjgyT1RObQpOMk13TTMweEVqQVFCZ05WQkNrTUNXTjBabEJzWVhsbGNqQ0NBU0l3RFFZSktvWklodmNOQVFFQkJRQURnZ0VQCkFEQ0NBUW9DZ2dFQkFQcCtYdURCM1prbXJrdkFzZ3RqUCttakljWURXZnB0dVpzSmlldTZlUmwzOXdsNFNnMzgKKy9PZlkyNExWOXNObWdLeVRHdnBtQ2FVb1pNWWt2a3VsWVNvRnpFMHhxUEJvNmtydUxFeUl2cXFwQUZxUkgyYgptaWVyTFQ2UmNLZ0pIWXIvVnQ2U3dQOE5DQ2F3Q3J2aFE0TlpjdUI0OUhyLzJBaUdIem1mODYvbEcvYytsaG1ICmd5cVBiMWtEZ2hzVnhpL0dOczlpN0FnbmlaaWtxVDhPVHAwSU5tbUNnWnRKbjFKbzYxNUl1L3RGaUM4U2ZoaGcKUUhtVERMamd4MW9QMWt2WlYyUEU1VVVOL29DMDVadXA4ZjMxTGtzWFp3cGF6Wkt3WUMvTGJOOTZIZHFnVlE5SwpTOGUvNEk3TUpRbVBtTElzTHAzc2RMMkZpREdNTDNzbUFpMENBd0VBQWFBbU1DUUdDU3FHU0liM0RRRUpEakVYCk1CVXdFd1lEVlIwbEJBd3dDZ1lJS3dZQkJRVUhBd0l3RFFZSktvWklodmNOQVFFTEJRQURnZ0VCQU94U1I4RnMKVGRqZnU5ZTB2Uk5xS1dkMDlJU21ZRFFjM3FuU2JMUmxZWnlNSzRwZ3VBTHEzMTBoLzFuTmdVUldFU2JOSlBPcApGa0JXRzBYV2hXeVdQN3JUcXhvL3BrOUFLeDBUTmJIRHJTNktpQm5LUHEwbXhqUFpzSDFMN3dOWURjNU9BTkRsCmJ0dm4zelQ3bE1tczZ6MXFNN3hVV1hSNzZuMnhMLzgxY2RGNzI1bkJaMDBtV21QVzBTMXBTbUE0RUVIQ0VnTlcKMHZXUXFzSURraTNnWWM0TkNtOE9Iang3OWtjd0Ura3N5YzZ2SGdNT3dzWW9PRkpueWF5aGwxNW9OLzN4N2hXMwpHMXhvdlB1cEFCcGZPU05PY1R3YmdmcmZqVURPTHgvd2lydmo5TDFONUVHRGg0Rk9MYVJaRHMrdE1yaW1HQkJTCnpHVTEzQm55a21RNWpPUT0