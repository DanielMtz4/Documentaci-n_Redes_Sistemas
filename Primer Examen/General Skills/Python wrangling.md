## Descripción 
Python scripts are invoked kind of like programs in the Terminal... Can you run [this Python script](https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/ende.py) using [this password](https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/pw.txt) to get [the flag](https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/flag.txt.en)?
## Hints
1. Get the Python script accessible in your shell by entering the following command in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/ende.py`
2. $ man python
## Solución
```
DanielMtzC-picoctf@webshell:~$ ls
README.txt  ende.py  flag.txt.en  pw.txt
DanielMtzC-picoctf@webshell:~$ cat pw.txt 
67c6cc9667c6cc9667c6cc9667c6cc96
DanielMtzC-picoctf@webshell:~$ python ende.py -d flag.txt.en
Please enter the password:https://mercury.picoctf.net/static/b351a89e0bc6745b007168                          
Traceback (most recent call last):
  File "/home/DanielMtzC-picoctf/ende.py", line 44, in <module>
    c = Fernet(ssb_b64)
  File "/usr/local/lib/python3.10/dist-packages/cryptography/fernet.py", line 40, in __init__
    raise ValueError(
ValueError: Fernet key must be 32 url-safe base64-encoded bytes.
DanielMtzC-picoctf@webshell:~$ python ende.py -d flag.txt.en
Please enter the password:67c6cc9667c6cc9667c6cc9667c6cc96
picoCTF{4p0110_1n_7h3_h0us3_67c6cc96}
```
## Notas

## Referencias
