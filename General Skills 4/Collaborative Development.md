## Descripción 
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/69/challenge.zip)
	
## Hints
1. `git branch -a` will let you see available branches
2. How can file 'diffs' be brought to the main branch? Don't forget to `git config`!
3. Merge conflicts can be tricky! Try a text editor like nano, emacs, or vim.
## Solución
```
DanielMtzC-picoctf@webshell:~$ ls
README.txt  challenge.zip  drop-in
DanielMtzC-picoctf@webshell:~$ cd drop-in/
DanielMtzC-picoctf@webshell:~/drop-in$ git merge feature/part-1
Updating eb4de2a..ad37f59
Fast-forward
 flag.py | 1 +
 1 file changed, 1 insertion(+)
DanielMtzC-picoctf@webshell:~/drop-in$ cat flag.py 
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')DanielMtzC-picoctf@webshell:~/drop-in$ git merge feature/part-2
Committer identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got 'DanielMtzC-picoctf@webshell.(none)')
DanielMtzC-picoctf@webshell:~/drop-in$ git --global
unknown option: --global
usage: git [--version] [--help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           [--super-prefix=<path>] [--config-env=<name>=<envvar>]
           <command> [<args>]
DanielMtzC-picoctf@webshell:~/drop-in$ git config --global user.name random
DanielMtzC-picoctf@webshell:~/drop-in$ git config --global user.gmail random@gmail.com
DanielMtzC-picoctf@webshell:~/drop-in$ git merge feature/part-2
Committer identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got 'DanielMtzC-picoctf@webshell.(none)')
DanielMtzC-picoctf@webshell:~/drop-in$ git config --global user.gmail picoctf@webshell
DanielMtzC-picoctf@webshell:~/drop-in$ git config --global user.name DanielMtzC
DanielMtzC-picoctf@webshell:~/drop-in$ git merge feature/part-2
Committer identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got 'DanielMtzC-picoctf@webshell.(none)')
DanielMtzC-picoctf@webshell:~/drop-in$ git config --global user.name "DanielMtzC"
DanielMtzC-picoctf@webshell:~/drop-in$ git config --global user.gmail "picoctf@webshell"
DanielMtzC-picoctf@webshell:~/drop-in$ git config --list
DanielMtzC-picoctf@webshell:~/drop-in$ git merge feature/part-2
Committer identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got 'DanielMtzC-picoctf@webshell.(none)')
DanielMtzC-picoctf@webshell:~/drop-in$ git config --list
DanielMtzC-picoctf@webshell:~/drop-in$ 
DanielMtzC-picoctf@webshell:~/drop-in$ git merge feature/part-2
Committer identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got 'DanielMtzC-picoctf@webshell.(none)')
DanielMtzC-picoctf@webshell:~/drop-in$ git config user.email "picoctf@webshell"
DanielMtzC-picoctf@webshell:~/drop-in$ git config user.name "DanielMtzC"
DanielMtzC-picoctf@webshell:~/drop-in$ git merge feature/part-2
Auto-merging flag.py
CONFLICT (content): Merge conflict in flag.py
Automatic merge failed; fix conflicts and then commit the result.
DanielMtzC-picoctf@webshell:~/drop-in$ git add flag.py 
DanielMtzC-picoctf@webshell:~/drop-in$ git commit -m merge 
[main 38bdca0] merge
DanielMtzC-picoctf@webshell:~/drop-in$ git merge feature/part-3
Auto-merging flag.py
CONFLICT (content): Merge conflict in flag.py
Automatic merge failed; fix conflicts and then commit the result.
DanielMtzC-picoctf@webshell:~/drop-in$ git add flag.py 
DanielMtzC-picoctf@webshell:~/drop-in$ git commit -m merge
[main 390958c] merge
DanielMtzC-picoctf@webshell:~/drop-in$ cat f
cat: f: No such file or directory
DanielMtzC-picoctf@webshell:~/drop-in$ cat flag.py 
print("Printing the flag...")
<<<<<<< HEAD
<<<<<<< HEAD
print("picoCTF{t3@mw0rk_", end='')
=======

print("m@k3s_th3_dr3@m_", end='')
>>>>>>> feature/part-2
=======

print("w0rk_e4b79efb}")
>>>>>>> feature/part-3
```
## Notas
- `git config` → configurar identidad.
- `git merge` → combinar ramas.
- `git add` → preparar cambios.
- `git commit` → guardar cambios en el historial.
- `git config --list` → ver configuraciones.
- `cat` → ver contenido de un archivo.
## Referencias
