## Descripción 
Run the `runme.py` script to get the flag. Download the script with your browser or with `wget` in the webshell.[Download runme.py Python script](https://artifacts.picoctf.net/c/34/runme.py)
## Hints
1. If you have Python on your computer, you can download the script normally and run it. Otherwise, use the `wget` command in the webshell.
2. To use `wget` in the webshell, first right click on the download link and select 'Copy Link' or 'Copy Link Address'
3. Type everything after the dollar sign in the webshell: `$ wget` , then paste the link after the space after `wget` and press enter. This will download the script for you in the webshell so you can run it!
4. inally, to run the script, type everything after the dollar sign and then press enter: `$ python3 runme.py` You should have the flag now!
## Solución
```
DanielMtzC-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/34/runme.py
--2025-09-09 19:06:07--  https://artifacts.picoctf.net/c/34/runme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.77, 3.170.131.33, 3.170.131.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.77|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: 'runme.py'

runme.py             100%[=====================>]     270  --.-KB/s    in 0s      

2025-09-09 19:06:07 (75.6 MB/s) - 'runme.py' saved [270/270]

DanielMtzC-picoctf@webshell:~$ ls
README.txt  runme.py
DanielMtzC-picoctf@webshell:~$ python3 runme.py 
picoCTF{run_s4n1ty_run}
DanielMtzC-picoctf@webshell:~$ 

```
## Notas

## Referencias
