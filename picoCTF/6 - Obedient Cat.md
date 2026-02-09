### Obedient Cat

This file has a flag in plain sight (aka "in-the-clear").
### Solución 1 - Comando cat
```
daniel_minbot-picoctf@webshell:~$ wget https://challenge-files.picoctf.net/c_wily_courier/8d63e440ec205416efd07e5c9f9ea0ab050fe3f4c8fc30bebfcca22f0c902491/flag
--2026-02-09 18:45:12--  https://challenge-files.picoctf.net/c_wily_courier/8d63e440ec205416efd07e5c9f9ea0ab050fe3f4c8fc30bebfcca22f0c902491/flag
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.40, 3.160.5.64, 3.160.5.95, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34 [application/octet-stream]
Saving to: 'flag.1'

flag.1              100%[================>]      34  --.-KB/s    in 0s      

2026-02-09 18:45:12 (695 KB/s) - 'flag.1' saved [34/34]

daniel_minbot-picoctf@webshell:~$ ls  
README.txt  flag  flag.1
daniel_minbot-picoctf@webshell:~$ cat flag.1
picoCTF{s4n1ty_v3r1f13d_9b8fa0bc}
```


picoCTF{s4n1ty_v3r1f13d_9b8fa0bc}

### Notas
Para mostrar un archivo de texto plano se ingresa cat archivo

