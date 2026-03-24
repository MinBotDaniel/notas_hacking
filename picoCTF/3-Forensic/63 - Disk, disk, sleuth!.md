### Disk, disk, sleuth!

Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image.[dds1-alpine.flag.img.gz](https://challenge-files.picoctf.net/c_wily_courier/7317ac746dd0d2429c9f16875e0c4b41673375678a980746ea9b618f8ed6aa72/dds1-alpine.flag.img.gz)
### Solución

Nuevamente trabajamos con una imagen de disco. El objetivo es localizar un archivo que contiene la bandera, el cual está "escondido" en algún lugar del sistema de archivos.

Comenzamos analizando las particiones para encontrar el punto de entrada:

┌──(kali㉿kali)-[~/problemasPICO/disk_sleuth]

└─$ `mmls dds1-alpine.flag.img`

Identificamos la partición de Linux y procedemos a listar los archivos desde la raíz. En este reto, la bandera no está en un lugar obvio como `/root`, por lo que debemos navegar por los directorios:

┌──(kali㉿kali)-[~/problemasPICO/disk_sleuth]

└─$ `fls -o [OFFSET] dds1-alpine.flag.img`

Si la lista es muy larga, podemos filtrar la búsqueda con `grep` para encontrar archivos que tengan "flag" en su nombre:

┌──(kali㉿kali)-[~/problemasPICO/disk_sleuth]

└─$ `fls -r -o [OFFSET] dds1-alpine.flag.img | grep flag`

_(El flag `-r` sirve para buscar de forma recursiva en todas las carpetas)._

Tras localizar el archivo (por ejemplo, en `/down-at-the-bottom.txt`), anotamos su número de **inode** y extraemos el contenido:

┌──(kali㉿kali)-[~/problemasPICO/disk_sleuth]

└─$ `icat -o [OFFSET] dds1-alpine.flag.img [INODE]`

El comando nos devolverá la bandera directamente en la terminal.

### Notas

- El uso de `fls -r` (recursivo) es fundamental cuando no conoces la ruta exacta del archivo.
    
- Al ser una imagen basada en **Alpine Linux**, la estructura de archivos es mínima, lo que facilita la búsqueda manual si no quieres usar grep.