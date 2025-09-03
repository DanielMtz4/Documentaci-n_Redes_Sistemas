## Descripción 
Can you make sense of this file?Download the file [here](https://artifacts.picoctf.net/c/476/enc_flag).
## Hints
Multiple decoding is always good
## Solución
```
DanielMtzC-picoctf@webshell:~$ ls
README.txt  enc_flag
DanielMtzC-picoctf@webshell:~$ cat enc_flag 
VmpGU1EyRXlUWGxTYmxKVVYwZFNWbGxyV21GV1JteDBUbFpPYWxKdFVsaFpWVlUxWVZaS1ZWWnVh
RmRXZWtab1dWWmtSMk5yTlZWWApiVVpUVm10d1VWZFdVa2RpYlZaWFZtNVdVZ3BpU0VKeldWUkNk
MlZXVlhoWGJYQk9VbFJXU0ZkcVRuTldaM0JZVWpGS2VWWkdaSGRXCk1sWnpWV3hhVm1KRk5XOVVW
VkpEVGxaYVdFMVhSbFZrTTBKVVZXMTRWMDVHV2toalJYUlhDazFyV25sVVZXaHpWakpHZEdWRlZs
aGkKYlRrelZERldUMkpzUWxWTlJYTkxDZz09Cg==
DanielMtzC-picoctf@webshell:~$ string enc_flag 
-bash: string: command not found
DanielMtzC-picoctf@webshell:~$ cat enc_flag | base64 -d 
VjFSQ2EyTXlSblJUV0dSVllrWmFWRmx0TlZOalJtUlhZVVU1YVZKVVZuaFdWekZoWVZkR2NrNVVX
bUZTVmtwUVdWUkdibVZXVm5WUgpiSEJzWVRCd2VWVXhXbXBOUlRWSFdqTnNWZ3BYUjFKeVZGZHdW
MlZzVWxaVmJFNW9UVVJDTlZaWE1XRlVkM0JUVW14V05GWkhjRXRXCk1rWnlUVWhzVjJGdGVFVlhi
bTkzVDFWT2JsQlVNRXNLCg==
DanielMtzC-picoctf@webshell:~$ cat enc_flag | base64 -d | base64 -d | base64 -d| base64 -d
Y0dsamIwTlVSbnRpWVhObE5qUmZiak56ZEROa1gyUnBZekJrSVc0NFgyUXdkMjVzTURSa00yUmZO
RFUxTjJWak0yVjlDZz09Cg==
DanielMtzC-picoctf@webshell:~$ cat enc_flag | base64 -d | base64 -d | base64 -d| base64 -d | base64 -d
cGljb0NURntiYXNlNjRfbjNzdDNkX2RpYzBkIW44X2Qwd25sMDRkM2RfNDU1N2VjM2V9Cg==
DanielMtzC-picoctf@webshell:~$ cat enc_flag | base64 -d | base64 -d | base64 -d| base64 -d | base64 -d | base64 -d
picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_4557ec3e}
DanielMtzC-picoctf@webshell:~$ 
```
## Notas
base64 -d: Desencripta un código en base 64
## Referencias
