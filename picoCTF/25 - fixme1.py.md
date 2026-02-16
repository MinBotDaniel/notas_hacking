### fixme1.py

Fix the syntax error in this Python script to print the flag.
### Solución 1 - Se ejecuta con python


```
daniel_minbot-picoctf@webshell:~$ wget -q https://artifacts.picoctf.net/c/25/fixme1.py
daniel_minbot-picoctf@webshell:~$ ls
README.txt  fixme1.py
daniel_minbot-picoctf@webshell:~$ python.py fixme1.py
-bash: python.py: command not found
daniel_minbot-picoctf@webshell:~$ python fixme1.py
  File "/home/daniel_minbot-picoctf/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
daniel_minbot-picoctf@webshell:~$ nano fixme1.py 
daniel_minbot-picoctf@webshell:~$ python fixme1.py
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_6a476c8f}
```

picoCTF{1nd3nt1ty_cr1515_6a476c8f}

### Notas
Había un print mal indentado

