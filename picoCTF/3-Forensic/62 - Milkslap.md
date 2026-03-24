### Milkslap

🥛http://wily-courier.picoctf.net:64549/
### Solución

Primero, entramos al enlace del reto. No hay un archivo directo para descargar, pero al inspeccionar la página o el código fuente, encontramos un archivo de imagen PNG que se comporta como un GIF al interactuar con él.

Descargamos la imagen directamente desde el servidor:

┌──(kali㉿kali)-[~/problemasPICO/milkslap]

└─$ `wget [URL_DE_LA_IMAGEN_CON_EL_GIF]`

Como se trata de un archivo **PNG**, utilizamos la herramienta `zsteg` (recordando que `steghide` es para JPG y `zsteg` es ideal para PNG) para buscar datos ocultos mediante esteganografía:

┌──(kali㉿kali)-[~/problemasPICO/milkslap]

└─$ `zsteg concat_v.png`

Al ejecutar el comando, la herramienta escanea los bits de la imagen y revela la bandera que estaba embebida en los datos:

**picoCTF{imag3_m4n1pul4t10n_sl4p5}**

### Notas

- Se usó `zsteg` para la extracción de metadatos y esteganografía en el PNG.
    
- Si no tienes la herramienta, se instala con `gem install zsteg`.