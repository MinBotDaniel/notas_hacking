### WebNet1

We found this [packet capture](https://challenge-files.picoctf.net/c_fickle_tempest/d1e9add4e31989553f239ebf71ba5972f9bed7bd4932f931e14bfba80d75f815/capture.pcap) and [key](https://challenge-files.picoctf.net/c_fickle_tempest/d1e9add4e31989553f239ebf71ba5972f9bed7bd4932f931e14bfba80d75f815/picopico.key). Recover the flag.

### Solución 
Se abre wireshark para el la captura pcap, con esto seguimos los TLS.
Notaremos que están encriptados. Vamos a edit, preferences y en protocols buscamos TLS, y en RSA keys list Edit y buscamos la key que descargamos.
Al inspeccionar el paquete 47 exportamos como HTTP el 91 y lo guardamos, al dar el comando strings para la imagen, encontramos la bandera

```
┌──(kali㉿kali)-[~/problemasPICO/webnet1]
└─$ strings vulture.jpg | grep pico
picoCTF{honey.roasted.peanuts}

```

picoCTF{honey.roasted.peanuts}

### Notas
TLS (Transport Layer Security) es el ==protocolo criptográfico estándar para asegurar comunicaciones en Internet==, encriptando datos entre un navegador y un servidor. Sucesor de SSL, garantiza la privacidad, integridad y autenticación de la información, permitiendo conexiones HTTPS seguras. Evita el robo de datos y mejora el posicionamiento SEO.



