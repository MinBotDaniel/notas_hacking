### CanYouSee
How about some hide and seek?Download this file [here](https://artifacts.picoctf.net/c_titan/130/unknown.zip).
### Solución

┌──(kali㉿kali)-[~/Tareas]
└─$ unzip unknown.zip 
Archive:  unknown.zip
  inflating: ukn_reality.jpg         

┌──(kali㉿kali)-[~/Tareas]
└─$ ls
ukn_reality.jpg  unknown.zip

┌──(kali㉿kali)-[~/Tareas]
└─$ open ukn_reality.jpg 

┌──(kali㉿kali)-[~/Tareas]
└─$ exiftool ukn_reality.jpg
ExifTool Version Number         : 13.44
File Name                       : ukn_reality.jpg
Directory                       : .
File Size                       : 2.3 MB
File Modification Date/Time     : 2024:02:15 17:40:21-05:00
File Access Date/Time           : 2026:05:14 21:56:15-04:00
File Inode Change Date/Time     : 2026:05:14 21:55:55-04:00
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
Y Cb Cr Sub Sampling            : YC


┌──(kali㉿kali)-[~/Tareas]
└─$ echo "cGljb0NURntNRTc0RDQ3QV9ISUREM05fYTZkZjhkYjh9Cg==" | base64 -d               
picoCTF{ME74D47A_HIDD3N_a6df8db8}

### Notas
