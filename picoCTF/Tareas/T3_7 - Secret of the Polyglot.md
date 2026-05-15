### Secret of the Polyglot

The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file?Download the suspicious file [here](https://artifacts.picoctf.net/c_titan/99/flag2of2-final.pdf).

### Solución

┌──(kali㉿kali)-[~/Tareas]
└─$ ls
flag2of2-final.pdf

┌──(kali㉿kali)-[~/Tareas]
└─$ file flag2of2-final.pdf 
flag2of2-final.pdf: PNG image data, 50 x 50, 8-bit/color RGBA, non-interlaced

┌──(kali㉿kali)-[~/Tareas]
└─$ cp flag2of2-final.pdf
cp: missing destination file operand after 'flag2of2-final.pdf'
Try 'cp --help' for more information.

┌──(kali㉿kali)-[~/Tareas]
└─$ cp flag2of2-final.pdf parte1.png                     

┌──(kali㉿kali)-[~/Tareas]
└─$ ls
flag2of2-final.pdf  parte1.png

┌──(kali㉿kali)-[~/Tareas]
└─$ explorer.exe         
explorer.exe: command not found

┌──(kali㉿kali)-[~/Tareas]
└─$ ls
flag2of2-final.pdf  parte1.png

┌──(kali㉿kali)-[~/Tareas]
└─$ open parte1.png     

┌──(kali㉿kali)-[~/Tareas]
└─$ strings flag2of2-final.pdf | grep -i "pico"

┌──(kali㉿kali)-[~/Tareas]
└─$ xdg-open parte1.png

┌──(kali㉿kali)-[~/Tareas]
└─$ open flag2of2-final.pdf 

┌──(kali㉿kali)-[~/Tareas]
└─$ open parte1.png  
picoCTF{f1u3n7_1n_pn9_&_pdf_2a6a1ea8}
### Notas
