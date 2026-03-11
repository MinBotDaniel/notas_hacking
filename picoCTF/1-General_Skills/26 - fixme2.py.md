### fixme2.py

Fix the syntax error in the Python script to print the flag.
### Solución 1 - Se ejecuta con python


```
daniel_minbot-picoctf@webshell:~$ wget -q https://artifacts.picoctf.net/c/6/fixme2.py
daniel_minbot-picoctf@webshell:~$ ls
README.txt  fixme2.py
daniel_minbot-picoctf@webshell:~$ python fixme2.py
  File "/home/daniel_minbot-picoctf/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
daniel_minbot-picoctf@webshell:~$ nano fixme2.py
daniel_minbot-picoctf@webshell:~$ python fixme2.py 
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
```

picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}

### Notas
En el if había un = de asignacion y no de comparación.

