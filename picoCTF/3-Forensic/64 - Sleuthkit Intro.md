### Sleuthkit Intro

Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.[Download disk image](https://artifacts.picoctf.net/c/164/disk.img.gz)Access checker program: `nc saturn.picoctf.net 53153`
### Solución

En este reto se nos proporciona un archivo de imagen de disco comprimido. El objetivo es encontrar el tamaño de la partición de Linux para obtener la bandera a través de un servidor remoto.

Primero, descargamos y descomprimimos el archivo:

┌──(kali㉿kali)-[~/problemasPICO/sleuthkit]

└─$ `unzip disk.img.gz`

Utilizamos la herramienta `mmls` de **The Sleuth Kit** para visualizar la tabla de particiones del archivo de imagen:

┌──(kali㉿kali)-[~/problemasPICO/sleuthkit]

└─$ `mmls disk.img`

En la salida del comando, identificamos la partición de tipo **Linux (0x83)** y tomamos nota de su longitud o sector de inicio según lo solicite el reto. Finalmente, nos conectamos al servidor proporcionado para entregar el valor y recibir la bandera:

┌──(kali㉿kali)-[~/problemasPICO/sleuthkit]

└─$ `nc saturn.picoctf.net [PUERTO]`

$\text{picoCTF\{mm15\_f7w1\}}$
### Notas

- Se utilizó `mmls` para listar los contenidos de la tabla de particiones.
    
- Es necesario tener instalado el paquete `sleuthkit` en Kali.