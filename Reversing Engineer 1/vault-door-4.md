## Descripción 
This vault uses ASCII encoding for the password.The source code for this vault is here: [VaultDoor4.java](https://challenge-files.picoctf.net/c_fickle_tempest/1f1763f633d961f780c72e411eba52fa8f26aeb37842ce96ae94c69eadf9ce11/VaultDoor4.java)

## Hints
1. Use a search engine to find an "ASCII table"
2. You will also need to know the difference between octal, decimal, and hexadecimal numbers.
## Solución
```
console.log(String.fromCharCode(106 , 85  , 53  , 116 , 95  , 52  , 95  , 98  ,
            0x55, 0x6e, 0x43, 0x68, 0x5f, 0x30, 0x66, 0x5f,
            0142, 0131, 0164, 063 , 0163, 0137, 061 , 062) +
            ['6' , '5' , '3' , '7' , '5' , '3' , '9' , '2'].join(''))

picoCTF{jU5t_4_bUnCh_0f_bYt3s_1265375392}
```
## Notas

## Referencias
