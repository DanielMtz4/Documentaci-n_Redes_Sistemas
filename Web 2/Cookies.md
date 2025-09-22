## Descripción 
Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:6418/](http://mercury.picoctf.net:6418/)
## Hints

## Solución
  ```
  DanielMtzC-picoctf@webshell:~$ for v in {1..30}; do   echo "Probar: $v";   curl -s 
-i --cookie "name=$v" http://mercury.picoctf.net:6418/check | sed -n '1,40p'; done 
| grep pico
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_88acab36}</code></p>
Location: http://mercury.picoctf.net:6418/
Location: http://mercury.picoctf.net:6418/
  ``` 
## Notas

## Referencias

[[Scavenger hunt]]