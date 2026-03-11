### Plumbing

Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag?Connect to fickle-tempest.picoctf.net 63610.
### Solución 1 - Con | grep pico
```
daniel_minbot-picoctf@webshell:~$ nc fickle-tempest.picoctf.net 63610 | grep pico
picoCTF{digital_plumb3r_0BAc587E}
```

### Solución 2 - Pasando a un archivo y buscando con grep
```
daniel_minbot-picoctf@webshell:~$ nc fickle-tempest.picoctf.net 63610 > salida    
^C
daniel_minbot-picoctf@webshell:~$ ls
README.txt  file  salida
daniel_minbot-picoctf@webshell:~$ grep pico salida
picoCTF{digital_plumb3r_0BAc587E}
```



picoCTF{digital_plumb3r_0BAc587E}

### Notas
Se usa | grep pico, pues con | se pueden poner varios comandos en una linea.
Tambien se puede pasar el resultado a un archivo con > nombreArchivo y buscando con grep

