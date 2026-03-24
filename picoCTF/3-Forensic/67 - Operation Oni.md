### Operation Oni
Download this disk image, find the key and log into the remote machine.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download disk image](https://artifacts.picoctf.net/c/69/disk.img.gz)
- Remote machine: `ssh -i key_file -p 64258 ctf-player@saturn.picoctf.net`
### Solución

En este reto se nos entrega una imagen de disco y una dirección de un servidor remoto. El objetivo es encontrar una llave privada SSH dentro del disco para poder loguearnos al servidor y leer la bandera.

Primero, analizamos las particiones del disco:

┌──(kali㉿kali)-[~/problemasPICO/oni]

└─$ `mmls disk.img`

Identificamos la partición principal (Linux). Luego, listamos los archivos buscando el directorio del usuario. En retos de este tipo, las llaves suelen estar en `.ssh`:

┌──(kali㉿kali)-[~/problemasPICO/oni]

└─$ `fls -o [OFFSET] disk.img [INODE_DEL_HOME_O_ROOT]`

Buscamos dentro de la carpeta `.ssh` (usando su número de inode) y localizamos un archivo llamado `id_ed25519` o `id_rsa`. Lo extraemos a nuestra máquina local:

┌──(kali㉿kali)-[~/problemasPICO/oni]

└─$ `icat -o [OFFSET] disk.img [INODE_DE_LA_LLAVE] > id_ed25519`

Cambiamos los permisos del archivo de la llave para que SSH nos permita usarlo (permisos de lectura solo para el dueño):

┌──(kali㉿kali)-[~/problemasPICO/oni]

└─$ `chmod 600 id_ed25519`

Finalmente, nos conectamos al servidor remoto usando la llave extraída:

┌──(kali㉿kali)-[~/problemasPICO/oni]

└─$ `ssh -i id_ed25519 -p [PUERTO] ctf-player@saturn.picoctf.net`

Una vez dentro del servidor, listamos los archivos y leemos la bandera:

`ctf-player@pico-server:~$ ls`

`ctf-player@pico-server:~$ cat flag.txt`

### Notas

- Se utilizó `icat` para recuperar la llave privada directamente desde los sectores del disco sin montar la imagen.
    
- El comando `chmod 600` es obligatorio; de lo contrario, SSH rechazará la llave por ser "demasiado abierta".