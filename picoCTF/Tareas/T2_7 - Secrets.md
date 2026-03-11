### Secrets

We have several pages hidden. Can you find the one with the flag?The website is running [here](http://saturn.picoctf.net:62005/).
### Solución 1
vemos el codigo fuente de la pagina, nos habla sobre una carpeta /secret/
luego inspeccionamos esta nueva pagina y ahora veremos una carpeta hidden, por lo que ahora ponemos /secret/hidden/
Ahora al inspeccionar veremos que hay otra que se llama superhidden, por lo que se pone /secret/hidden/superhidden/
y al darel de nuevo ctrl + u, veremos 

```
<!DOCTYPE html> <html> <head> <title></title> <link rel="stylesheet" href="[mycss.css](view-source:http://saturn.picoctf.net:62005/secret/hidden/superhidden/mycss.css)" /> </head> <body> <h1>Finally. You found me. But can you see me</h1> <h3 class="flag">picoCTF{succ3ss_@h3n1c@10n_39849bcf}</h3> </body> </html>
```

Aqui esta la bandera. 

picoCTF{succ3ss_@h3n1c@10n_39849bcf}
### Notas
se buscó entre carpetas que aparecen en los links.
