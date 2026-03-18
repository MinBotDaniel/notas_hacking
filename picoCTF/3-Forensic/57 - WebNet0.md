### WebNet0

We found this [packet capture](https://challenge-files.picoctf.net/c_fickle_tempest/66113619363fca174ef6bf56587007af1626f99c44fc5cf92333f9fd8876ce9a/capture.pcap) and [key](https://challenge-files.picoctf.net/c_fickle_tempest/66113619363fca174ef6bf56587007af1626f99c44fc5cf92333f9fd8876ce9a/picopico.key). Recover the flag.
### Solución 
Se abre wireshark para el la captura pcap, con esto seguimos los TLS.
Notaremos que están encriptados. Vamos a edit, preferences y en protocols buscamos TLS, y en RSA keys list Edit y buscamos la key que descargamos.
Al inspeccionar el primer paquete que se pone en ver encontramos la bandera.

picoCTF{nongshim.shrimp.crackers}

### Notas
TLS (Transport Layer Security) es el ==protocolo criptográfico estándar para asegurar comunicaciones en Internet==, encriptando datos entre un navegador y un servidor. Sucesor de SSL, garantiza la privacidad, integridad y autenticación de la información, permitiendo conexiones HTTPS seguras. Evita el robo de datos y mejora el posicionamiento SEO.



