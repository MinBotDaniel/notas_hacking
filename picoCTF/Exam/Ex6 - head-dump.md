### head-dump
Welcome to the challenge! In this challenge, you will explore a web application and find an endpoint that exposes a file containing a hidden flag.
The application is a simple blog website where you can read articles about various topics, including an article about API Documentation. Your goal is to explore the application and find the endpoint that generates files holding the server’s memory, where a secret flag is hidden.
The website is running picoCTF News.
### Solución 
En la URL de la página ponemos /api-docs/ al final y nos redirige a una página de testeo de APIs de los desarrolladores, hasta abajo encontramos el heapdump o volcado de memoria, que contiene la bandera.
Se copia el curl que nos da, pero ponemos un grep para la bandera. Se usa el -s para que no nos arroje basura.

```
┌──(kali㉿kali)-[~/Downloads]
└─$ curl -s http://verbal-sleep.picoctf.net:49415/heapdump | grep -oE "picoCTF\{.*?\}"
picoCTF{Pat!3nt_15_Th3_K3y_871ffa9a}
```

picoCTF{Pat!3nt_15_Th3_K3y_871ffa9a}
### Notas
El **heapdump hacking** (o explotación de volcados de memoria dinámica) es una ==técnica de ciberataque que consiste en obtener y analizar una instantánea (snapshot) de la memoria RAM de una aplicación en ejecución para robar información confidencial==.