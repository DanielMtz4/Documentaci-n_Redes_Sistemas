## Descripción 
You will find the flag after analysing this apkDownload [here](https://artifacts.picoctf.net/c/449/timer.apk).
## Hints
1. Decompile
2. mobsf or jadx
## Solución
```
**Bandera:** `picoCTF{t1m3r_r3v3rs3d_succ355fully_17496}`

**Dónde estaba:** dentro del archivo `classes3.dex` del APK que subiste.

Si quieres verificarlo tú mismo en tu máquina, aquí tienes comandos útiles:

Linux / macOS (en terminal):

`# listar archivos del APK unzip -l 2dea19b4-b2a4-4a89-ba5f-4414c1397cf1.apk  # buscar la bandera directamente dentro del dex sin extraer: unzip -p 2dea19b4-b2a4-4a89-ba5f-4414c1397cf1.apk classes3.dex | strings | grep -i "picoCTF"`

Windows PowerShell:

`# usar 7z para listar & 'C:\Program Files\7-Zip\7z.exe' l 2dea19b4-b2a4-4a89-ba5f-4414c1397cf1.apk  # extraer y buscar (requiere 7z y findstr) & 'C:\Program Files\7-Zip\7z.exe' x 2dea19b4-b2a4-4a89-ba5f-4414c1397cf1.apk -oc:\tmp_apk strings C:\tmp_apk\classes3.dex | findstr /I "picoCTF"`
```
## Notas

## Referencias
