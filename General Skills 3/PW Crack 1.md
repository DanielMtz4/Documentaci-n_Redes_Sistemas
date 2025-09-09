## Descripción 
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/12/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/12/level1.flag.txt.enc) in the same directory too.
## Hints
1. To view the file in the webshell, do: `$ nano level1.py`
2. To exit `nano`, press Ctrl and x and follow the on-screen prompts.
3. The `str_xor` function does not need to be reverse engineered for this challenge.
## Solución
```
DanielMtzC-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/12/level1.py
--2025-09-09 17:01:27--  https://artifacts.picoctf.net/c/12/level1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.72, 3.170.131.77, 3.170.131.33, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.72|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 876 [application/octet-stream]
Saving to: 'level1.py'

level1.py            100%[=====================>]     876  --.-KB/s    in 0s      

2025-09-09 17:01:27 (213 MB/s) - 'level1.py' saved [876/876]

DanielMtzC-picoctf@webshell:~$ cat 
.bash_history    .config/         .ssh/            files.zip
.bash_logout     .local/          .wget-hsts       level1.py
.bashrc          .profile         README.txt       
.cache/          .python_history  files/           
DanielMtzC-picoctf@webshell:~$ cat level1.py 
### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
###############################################################################


flag_enc = open('level1.flag.txt.enc', 'rb').read()



def level_1_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == "8713"):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")



level_1_pw_check()
DanielMtzC-picoctf@webshell:~$ python3 level1.py 
Traceback (most recent call last):
  File "/home/DanielMtzC-picoctf/level1.py", line 13, in <module>
    flag_enc = open('level1.flag.txt.enc', 'rb').read()
FileNotFoundError: [Errno 2] No such file or directory: 'level1.flag.txt.enc'
DanielMtzC-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/12/level1.flag.txt.enc
--2025-09-09 17:02:38--  https://artifacts.picoctf.net/c/12/level1.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.77, 3.170.131.72, 3.170.131.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.77|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 30 [application/octet-stream]
Saving to: 'level1.flag.txt.enc'

level1.flag.txt.enc  100%[=====================>]      30  --.-KB/s    in 0.04s   

2025-09-09 17:02:38 (721 B/s) - 'level1.flag.txt.enc' saved [30/30]

DanielMtzC-picoctf@webshell:~$ python3 level1.py 
Please enter correct password for flag: 8713
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_1b2fd683}
```
## Notas

## Referencias
