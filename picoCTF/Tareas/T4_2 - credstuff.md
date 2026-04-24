### credstuff

We found a leak of a blackmarket website's login credentials. Can you find the password of the user `cultiris` and successfully decrypt it?Download the leak [here](https://artifacts.picoctf.net/c/151/leak.tar).The first user in `usernames.txt` corresponds to the first password in `passwords.txt`. The second user corresponds to the second password, and so on.
### Solución 1
Se descomprime el archivo, buscamos el número de línea de `cultiris`, vamos al archivo de passwords y sacas la línea 378 y se descifra el mensaje que está en ROT13.
https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,13)&input=Y3ZwYlBHU3tQN2UxU181NEkzNV83MVozfQ0K&ieol=CRLF&oeol=CRLF

```
┌──(kali㉿kali)-[~/Tareas]
└─$ tar -xvf leak.tar
leak/
leak/passwords.txt
leak/usernames.txt
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/Tareas]
└─$ ls
leak  leak.tar
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/Tareas]
└─$ cd leak        
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/Tareas/leak]
└─$ ls
passwords.txt  usernames.txt
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/Tareas/leak]
└─$ grep -n "cultiris" usernames.txt
378:cultiris
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/Tareas/leak]
└─$ sed -n '378p' passwords.txt
cvpbPGS{P7e1S_54I35_71Z3}

```

picoCTF{C7r1F_54V35_71M3}
### Notas
