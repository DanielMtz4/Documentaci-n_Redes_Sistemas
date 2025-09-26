## Descripción 
There is a website running at `https://jupiter.challenges.picoctf.org/problem/50009/` ([link](https://jupiter.challenges.picoctf.org/problem/50009/)) or http://jupiter.challenges.picoctf.org:50009. Do you think you can log us in? Try to see if you can login!
## Hints
1. There doesn't seem to be many ways to interact with this. I wonder if the users are kept in a database?
2. Try to think about how the website verifies your login.
## Solución
```
Se hace una inyeccion SQL en la contraseña, dado que la sentencia SQL solamente está concatenada, haciendo posible que en la contraseña pueda poner 
password = ' or 1=1; 
Lo que me dio acceso a la página que contenia la bandera

```
## Notas

## Referencias
