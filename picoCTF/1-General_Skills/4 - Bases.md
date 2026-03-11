### Bases

What does this bDNhcm5fdGgzX3IwcDM1 mean? I think it has something to do with bases.

### Solución 1 - Python
```
>>> import base64
>>> base64.b64decode('bDNhcm5fdGgzX3IwcDM1')
b'l3arn_th3_r0p35'
```

### Solucion 2 - CyberChef

### Solucion 3 - comandos de consola en Linux
```
daniel_minbot-picoctf@webshell:~$ echo 'bDNhcm5fdGgzX3IwcDM1' | base64 -d
l3arn_th3_r0p35
```


picoCTF{l3arn_th3_r0p35}

### Notas
En python se importa con import base64
base64.b64decode() - decodifica en base 64

en la consola de linux, se ponde -d porque es decodificacion

### Referencias
https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=YkROaGNtNWZkR2d6WDNJd2NETTE