### PW Crack 2

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/15/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/15/level2.flag.txt.enc) in the same directory too.
### Solución 1 - Se ejecuta con python


```
daniel_minbot-picoctf@webshell:~$ ls 
README.txt  level2.flag.txt.enc  level2.py
daniel_minbot-picoctf@webshell:~$ nano level2.py
daniel_minbot-picoctf@webshell:~$ nano level2.py
daniel_minbot-picoctf@webshell:~$ python level2.py 
39ce
Please enter correct password for flag: 39ce
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_502ec42e}
```

picoCTF{tr45h_51ng1ng_502ec42e}

### Notas
Se imprime primero la contraseña poniendo la contraseña antes de entrar al if
