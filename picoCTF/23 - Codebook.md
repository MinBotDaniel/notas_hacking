### Codebook
Run the Python script `code.py` in the same directory as `codebook.txt`.
### Solución 1 - Se ejecuta con python


```
daniel_minbot-picoctf@webshell:~$ wget -q https://artifacts.picoctf.net/c/3/code.py
daniel_minbot-picoctf@webshell:~$ ls     
README.txt  code.py
daniel_minbot-picoctf@webshell:~$ python code.py 
Couldn't find codebook.txt. Did you download that file into the same directory as this script?
daniel_minbot-picoctf@webshell:~$ wget -q https://artifacts.picoctf.net/c/3/codebook.txt
daniel_minbot-picoctf@webshell:~$ ls
README.txt  code.py  codebook.txt
daniel_minbot-picoctf@webshell:~$ python code.py 
picoCTF{c0d3b00k_455157_197a982c}
```

picoCTF{c0d3b00k_455157_197a982c}
### Notas
Todo se ejecutó en la terminal

