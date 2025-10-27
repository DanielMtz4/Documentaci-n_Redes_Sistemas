## Descripción 
How about some hide and seek?Download this file [here](https://artifacts.picoctf.net/c_titan/6/unknown.zip).
## Hints
1. If something isn't in the expected form, maybe it deserves attention?
2. How can you view the information about the picture?
## Solución
```
anielMtzC-picoctf@webshell:~$ unzip unknown.zip 
Archive:  unknown.zip
  inflating: ukn_reality.jpg         
DanielMtzC-picoctf@webshell:~$ exiftool 
.bash_history    .config/         .python_history  ukn_reality.jpg
.bash_logout     .gitconfig       .ssh/            unknown.zip
.bashrc          .lesshst         .wget-hsts       
.cache/          .local/          README.txt       
.cargo/          .profile         exploit.py       
DanielMtzC-picoctf@webshell:~$ exiftool ukn_reality.jpg 
ExifTool Version Number         : 12.40
File Name                       : ukn_reality.jpg
Directory                       : .
File Size                       : 2.2 MiB
File Modification Date/Time     : 2024:02:15 22:40:21+00:00
File Access Date/Time           : 2024:02:15 22:40:21+00:00
File Inode Change Date/Time     : 2025:10:27 05:45:35+00:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Resolution Unit                 : inches
X Resolution                    : 72
Y Resolution                    : 72
XMP Toolkit                     : Image::ExifTool 11.88
Attribution URL                 : cGljb0NURntNRTc0RDQ3QV9ISUREM05fYTZkZjhkYjh9Cg==
Image Width                     : 4308
Image Height                    : 2875
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 4308x2875
Megapixels                      : 12.4
DanielMtzC-picoctf@webshell:~$ 
flag: picoCTF{ME74D47A_HIDD3N_a6df8db8}
```
## Notas

## Referencias
