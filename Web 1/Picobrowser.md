## Descripción 
This website can be rendered only by **picobrowser**, go and catch the flag! `https://jupiter.challenges.picoctf.org/problem/26704/` ([link](https://jupiter.challenges.picoctf.org/problem/26704/)) or http://jupiter.challenges.picoctf.org:26704
## Hints
You don't need to download a new web browser
## Solución
```
DanielMtzC-picoctf@webshell:~$ curl -s https://jupiter.challenges.picoctf.org/problem/26704/flag -H "User-Agent: picobrowser" | grep picoCTF
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{p1c0_s3cr3t_ag3nt_e9b160d0}</code></p>
```
## Notas
curl -s: es hacer una petición al sitio web en modo silencioso
## Referencias

[[Client-side-again]]