## Descripción 
What was I last working on? I remember writing a note to help me remember...You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/163/challenge.zip)
## Hints
	1. The `cat` command will let you read a file, but that won't help you here!
	2. Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control).
	3. When committing a file with git, a message can (and should) be included.
## Solución
```
DanielMtzC-picoctf@webshell:~/drop-in$ ls
message.txt
DanielMtzC-picoctf@webshell:~/drop-in$ cat message.txt 
This is what I was working on, but I'd need to look at my commit history to know why...DanielMtzC-picoctf@webshell:~/drop-in$ git log message.txt
DanielMtzC-picoctf@webshell:~/drop-in$ 
```
## Notas

## Referencias
