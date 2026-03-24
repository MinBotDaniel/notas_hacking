### Sleuthkit Apprentice
Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/137/disk.flag.img.gz)
### Solución

Este reto requiere navegar por el sistema de archivos de una imagen de disco más compleja para encontrar un archivo oculto.

Iniciamos analizando las particiones para identificar dónde está instalado el sistema operativo:

┌──(kali㉿kali)-[~/problemasPICO/apprentice]

└─$ `mmls disk.flag.img`

Buscamos la partición más grande (donde reside el sistema de archivos principal). Una vez identificada, usamos `fls` para listar los archivos y directorios. Es probable que debas explorar de forma recursiva o buscar en directorios específicos como `/root`:

┌──(kali㉿kali)-[~/problemasPICO/apprentice]

└─$ `fls -o [OFFSET] disk.flag.img`

_(Donde OFFSET es el sector de inicio de la partición detectada)_.

Si encontramos un directorio interesante, listamos su contenido usando su número de **inode**:

┌──(kali㉿kali)-[~/problemasPICO/apprentice]

└─$ `fls -o [OFFSET] disk.flag.img [INODE]`

Tras encontrar el archivo `flag.txt`, utilizamos `icat` junto con su número de inode para visualizar el contenido y obtener la bandera:

┌──(kali㉿kali)-[~/problemasPICO/apprentice]

└─$ `icat -o [OFFSET] disk.flag.img [INODE_DE_FLAG]`

$\text{picoCTF\{y0u\_p4wn3d\_4nd\_sk1llz\_5f97371a\}}$

### Notas

- `fls` permite listar archivos, incluso los borrados, dentro de una imagen.
    
- `icat` muestra el contenido de un archivo basándose en su número de inode, sin necesidad de montar la imagen.