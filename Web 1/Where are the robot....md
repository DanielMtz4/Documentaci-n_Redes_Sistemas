## Descripción 
Can you find the robots? `https://jupiter.challenges.picoctf.org/problem/36474/` ([link](https://jupiter.challenges.picoctf.org/problem/36474/)) or http://jupiter.challenges.picoctf.org:36474
## Hints
1. What part of the website could tell you where the creator doesn't want you to look?
## Solución
```
Usar el archivo robots.txt 
User-agent: *
Disallow: /477ce.html
Y esa dirección solo la pego al final para que me redireccione a una sección oculta del programa y obtener la llave
```

## Notas
Archivos robots:  documento de texto que se aloja en la raíz de un sitio web y contiene instrucciones para los rastreadores de motores de búsqueda y otros bots, indicándoles qué partes de un sitio pueden o no rastrear.
## Referencias

[[Logon]]