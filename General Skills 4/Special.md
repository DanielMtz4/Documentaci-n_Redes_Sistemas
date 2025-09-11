## Descripción 
Don't power users get tired of making spelling mistakes in the shell? Not anymore! Enter Special, the Spell Checked Interface for Affecting Linux. Now, every word is properly spelled and capitalized... automatically and behind-the-scenes! Be the first to test Special in beta, and feel free to tell us all about how Special streamlines every development process that you face. When your co-workers see your amazing shell interface, just tell them: That's Special (TM)Start your instance to see connection details.

Additional details will be available after launching your challenge instance.
## Hints
1. Experiment with different shell syntax

## Solución
```
Special$ find .
Find . 
sh: 1: Find: not found
Special$ Find .
Find . 
sh: 1: Find: not found
Special$ Clear
Clear 
sh: 1: Clear: not found
Special$ Clear ls
Clear is 
sh: 1: Clear: not found
Special$ Clear is        
Clear is 
sh: 1: Clear: not found
Special$ Clear & find .
Clear & find . 
sh: 1: Clear: not found
.
./blargh
./blargh/flag.txt
./.cache
./.cache/motd.legal-displayed
Special$ Clear & cat ./blargh/flag.txt
Clear & cat ./blargh/flag.txt 
sh: 1: Clear: not found
picoCTF{5p311ch3ck_15_7h3_w0r57_f578af59}Special$ Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.
DanielMtzC-picoctf@webshell:~$ 
```
## Notas

## Referencias
