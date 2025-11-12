## Descripción 
Can you figure out how this program works to get the flag?Connect to the program with netcat:`$ nc saturn.picoctf.net 59152`The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/527/picker-IV.c). The binary can be downloaded [here](https://artifacts.picoctf.net/c/527/picker-IV).
## Hints
1. With Python, there are no binaries. With compiled languages like C, there is source code, and there are binaries. Binaries are created from source code, they are a conversion from the human-readable source code, to the highly efficient machine language, in this case: x86_64.
2. How can you find the address that `win` is at?
## Solución
```
DanielMtzC-picoctf@webshell:~$ nc saturn.picoctf.net 60680
Enter the address in hex to jump to, excluding '0x': 40129E
You input 0x40129e
You won!
picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_01672a61}

//----- (000000000040129E) ----------------------------------------------------
int win()
{
  FILE *stream; // [rsp+0h] [rbp-10h]
  char i; // [rsp+Fh] [rbp-1h]

  puts("You won!");
  stream = fopen("flag.txt", "r");
  if ( !stream )
  {
    puts("Cannot open file.");
    exit(0);
  }
  for ( i = fgetc(stream); i != -1; i = fgetc(stream) )
    putchar(i);
  putchar(10);
  return fclose(stream);
}
```
## Notas

## Referencias
https://dogbolt.org/?id=547a0af6-2d2f-4986-9199-14045ab5a2fd#Hex-Rays=229