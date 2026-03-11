### shark on wire 2

We found this [packet capture](https://challenge-files.picoctf.net/c_fickle_tempest/4d884ac4c144f7871b97b96ae69a31a8483651db7929cd4ecb05d7447832f87c/capture.pcap). Recover the flag.
### Solución 
Se abre la captura de paquetes y encontramos que en el flujo 32 de un paquete UDP se encuentra la pista start
![[Pasted image 20260311171733.png]]
Mientras que en el flujo 60 se encuentra el end
![[Pasted image 20260311171755.png]]
Se sabe que estan en el puerto 22, se automatiza el proceso, pues todo coincide que si se quita el puerto 5000, queda el codigo ascii de la bandera.
```
from scapy.all import *
flag = ''
packets = rdpcap('capture.pcap')

for p in packets:
    if UDP in p and p[UDP].dport == 22:
        if p[UDP].sport > 5000:
            flag += chr(p[UDP].sport - 5000)
print(flag)

```

Al ejecutarlo, deja la bandera:
```
┌──(kali㉿kali)-[~/problemasPICO/sharkonwire2]
└─$ python exp.py
picoCTF{p1LLf3r3d_data_v1a_st3g0}
```

picoCTF{p1LLf3r3d_data_v1a_st3g0}

### Notas
Scapy es una herramienta de manipulación de paquetes para redes informáticas, escrita originalmente en Python por Philippe Biondi. Puede falsificar o decodificar paquetes, enviarlos por cable, capturarlos y unir solicitudes y respuestas.



