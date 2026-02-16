### PW Crack 1

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/10/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/10/level1.flag.txt.enc) in the same directory too.
### Solución 1 - Se ejecuta con python


```
daniel_minbot-picoctf@webshell:~$ wget -q https://artifacts.picoctf.net/c/10/level1.py
daniel_minbot-picoctf@webshell:~$ wget -q https://artifacts.picoctf.net/c/10/level1.flag.txt.enc
daniel_minbot-picoctf@webshell:~$ ls
README.txt  level1.flag.txt.enc  level1.py
daniel_minbot-picoctf@webshell:~$ nano level1.py
daniel_minbot-picoctf@webshell:~$ python level1.py
Please enter correct password for flag: 691d
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_56891419}
```

picoCTF{545h_r1ng1ng_56891419}

### Notas
Dentro del codigo se encuentra la password.

