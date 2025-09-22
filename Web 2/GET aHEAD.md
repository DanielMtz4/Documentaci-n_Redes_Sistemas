## Descripción 
Find the flag being held on this server to get ahead of the competition http://mercury.picoctf.net:28916/
## Hints
1. Maybe you have more than 2 choices
2. Check out tools like Burpsuite to modify your requests and look at the responses
## Solución
```
curl -I http://mercury.picoctf.net:28916/index.php
HTTP/1.1 200 OK
flag: picoCTF{r3j3ct_th3_du4l1ty_70bc61c4}
Content-type: text/html; charset=UTF-8
```
## Notas
METODOS DE PETICION
GET: Solicita una representacion de un recurso específico.Las peticiones que usan el método GET sólo debe recuperar datos 

POST: Se usa para enviar una entidad a un recurso específica. Causando a menudo un cambio en el estado o efetos secundarios en el servidor
## Referencias
http://mercury.picoctf.net:28916/

[[Cookies]]




