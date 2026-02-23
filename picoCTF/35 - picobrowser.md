### picobrowser

This website can be rendered only by picobrowser, go and catch the flag!http://fickle-tempest.picoctf.net:61253
### Solución - Ingresando el agente de usuario correcto
Al inspeccionar la pagina nos percatamos que en User-Agent aparece 
```
user-agent

Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/145.0.0.0 Safari/537.36
```
Sin embargo, la respuesta es que nos solicita que usemos picobrowser. Solo se modifica este dato en la consola.

```
┌──(kali㉿kali)-[~]
└─$ curl -s http://fickle-tempest.picoctf.net:61253/flag -H "User-Agent: picobrowser" | grep picoCTF
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{p1c0_s3cr3t_ag3nt_fba5c48f}</code></p>

```

picoCTF{p1c0_s3cr3t_ag3nt_fba5c48f}
### Notas
UserAgent le permite al servidor y a la red identificarse entre si.
El comando curl nos ayuda a modificar aspectos del codigo fuente de una pagina.

