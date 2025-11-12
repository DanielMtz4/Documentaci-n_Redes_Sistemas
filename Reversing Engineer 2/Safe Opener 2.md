## Descripción 
What can you do with this file?I forgot the key to my safe but this [file](https://artifacts.picoctf.net/c/292/SafeOpener.class) is supposed to help me with retrieving the lost key. Can you help me unlock my safe?
## Hints
1. Download and try to decompile the file.
## Solución
```
DanielMtzC-picoctf@webshell:~$ cat SafeOpener.class 
4
CDE     FG
H
I
JL      FN
OP
Q
RS
.T
OU
VW
X
Y
[
]
R`ab<init>()VCodeLineNumberTableLocalVariableTablethis
                                                      LSafeOpener;main([Ljava/lang/String;)VisOpenZargs[Ljava/lang/StringkeyboardLjava/io/BufferedReader;encodercEncoder
                                                                                                                                                                        InnerClassesLjava/util/Base64$Encoder;
StackMapTable*Dcdang/String;keyiI
ExceptionsopenSafe(Ljava/lang/String;)password
SourceFileSafeOpener.java
                         java/io/BufferedReaderjava/io/InputStreamReaderf
                                                                         gh
                                                                           i
                                                                            jk
                                                                              lm
                                                                                noEnter password for the safe: p
                                                                                                                qr
                                                                                                                  std
                                                                                                                     uv
                                                                                                                       wx
                                                                                                                         yr
                                                                                                                           >?java/lang/StringBuilder
You have  
          z{
            z| attempt(s) left
                              }t,picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_0e57c117}
                                                                             ~
                                                                              Sesame openPassword is incorrect

SafeOpenerjava/lang/Objectjava/util/Base64$Encoderjava/lang/Stringjava/io/IOExceptionjava/lang/SysteminLjava/io/InputStream;(Ljava/io/InputStream;)V(Ljava/io/Reader;)Vjava/util/Base64
getEncoder()Ljava/util/Base64$Encoder;outLjava/io/PrintStream;java/io/PrintStreamprint(Ljava/lang/String;)readLine()Ljava/lang/StringgetBytes()[BencodeToString([B)Ljava/lang/String;printlnappend-(Ljava/lang/String;)Ljava/lang/StringBuilder;(I)Ljava/lang/StringBuildertoStringequals(Ljava/lang/Object;)Z! /*!"
                                                                                                                        #$      %& <xYYL:6T

+
&.4>EKPqtw"HK,'(!)*f+,b-1_23[43 X567 89:;;V<=   >? uL*+
                 "#&'"@323;AB0
                 
Flag: picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_0e57c117}
```
## Notas

## Referencias
