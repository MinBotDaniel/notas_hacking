### hideme
Every file gets a flag.The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://artifacts.picoctf.net/c/262/flag.png).

### Solución

┌──(kali㉿kali)-[~/Tareas]
└─$ binwalk -e flag.png

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
41            0x29            Zlib compressed data, compressed
39739         0x9B3B          Zip archive data, at least v1.0 to extract, name: secret/
39804         0x9B7C          Zip archive data, at least v2.0 to extract, compressed size: 2959, uncompressed size: 3108, name: secret/flag.png

WARNING: One or more files failed to extract: either no utility was found or it's unimplemented


┌──(kali㉿kali)-[~/Tareas]
└─$ ls
flag.png  _flag.png.extracted

┌──(kali㉿kali)-[~/Tareas]
└─$ cd _flag.png.extracted

┌──(kali㉿kali)-[~/Tareas/_flag.png.extracted]
└─$ ls
29  29.zlib  9B3B.zip  secret

┌──(kali㉿kali)-[~/Tareas/_flag.png.extracted]
└─$ ls -lh      
total 52K
-rw-rw-r-- 1 kali kali    0 May 14 21:44 29
-rw-rw-r-- 1 kali kali  42K May 14 21:44 29.zlib
-rw-rw-r-- 1 kali kali 3.3K May 14 21:44 9B3B.zip
drwxr-xr-x 2 kali kali 4.0K Mar 15  2023 secret

┌──(kali㉿kali)-[~/Tareas/_flag.png.extracted]
└─$ cd secret/

┌──(kali㉿kali)-[~/Tareas/_flag.png.extracted/secret]
└─$ ls flag.png 
flag.png

┌──(kali㉿kali)-[~/Tareas/_flag.png.extracted/secret]
└─$ explorer.exe         
explorer.exe: command not found

┌──(kali㉿kali)-[~/Tareas/_flag.png.extracted/secret]
└─$ explorer.exe flag.png
explorer.exe: command not found

┌──(kali㉿kali)-[~/Tareas/_flag.png.extracted/secret]
└─$ ls         
flag.png

┌──(kali㉿kali)-[~/Tareas/_flag.png.extracted/secret]
└─$ open flag.png 
![[Pasted image 20260514194748.png]]
### Notas

