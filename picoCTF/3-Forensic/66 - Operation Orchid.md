### Operation Orchid
Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/137/disk.flag.img.gz)
### Solución

En este reto, la bandera ha sido encriptada. Debemos explorar la imagen de disco para encontrar el archivo, la llave y el método de cifrado.

Primero, analizamos las particiones para localizar el sistema de archivos principal:

┌──(kali㉿kali)-[~/problemasPICO/orchid] └─$ `mmls disk.flag.img`

Identificamos la partición de Linux (usualmente la última y más grande). Listamos los archivos buscando rastros de actividad del usuario, especialmente en la carpeta `/root`:

┌──(kali㉿kali)-[~/problemasPICO/orchid] └─$ `fls -o [OFFSET] disk.flag.img [INODE_ROOT]`

Encontramos un archivo llamado `flag.txt.enc` y, muy importante, el archivo `.bash_history`. Revisamos el historial de comandos para ver qué hizo el usuario:

┌──(kali㉿kali)-[~/problemasPICO/orchid] └─$ `icat -o [OFFSET] disk.flag.img [INODE_BASH_HISTORY]`

El historial revela el comando exacto usado para cifrar la bandera: `openssl aes256 -salt -in flag.txt -out flag.txt.enc -k unbreakablepassword1234567`

Extraemos el archivo encriptado a nuestra máquina:

┌──(kali㉿kali)-[~/problemasPICO/orchid] └─$ `icat -o [OFFSET] disk.flag.img [INODE_FLAG_ENC] > flag.txt.enc`

Finalmente, usamos la misma herramienta y contraseña descubierta para desencriptar:

┌──(kali㉿kali)-[~/problemasPICO/orchid] └─$ `openssl aes256 -d -salt -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567`

Abrimos el archivo resultante para obtener la bandera:

┌──(kali㉿kali)-[~/problemasPICO/orchid] └─$ `cat flag.txt`

### Notas

- Se utilizó `fls` e `icat` para explorar y extraer archivos de la imagen.
    
- El análisis del `.bash_history` fue clave para encontrar la metodología de cifrado (AES-256) y la contraseña.