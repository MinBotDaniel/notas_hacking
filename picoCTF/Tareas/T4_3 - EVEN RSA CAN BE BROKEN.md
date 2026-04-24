### EVEN RSA CAN BE BROKEN???

This service provides you an encrypted flag. Can you decrypt it with just N & e?Connect to the program with netcat:`$ nc verbal-sleep.picoctf.net 52528`The program's source code can be downloaded [here](https://challenge-files.picoctf.net/c_verbal_sleep/c798cbe85b3e431345406f393827b9b905481b5fcd6d4b4a845527ee0602da9b/encrypt.py).
### Solución 1
Nos metemos a la conexión para obtener los datos.

```
┌──(kali㉿kali)-[~/Tareas]
└─$ nc verbal-sleep.picoctf.net 52528 
N: 17681111459803207224577120160344423739497719865764697733752619172317142782910167419560966900397519233064913923036750164897964571843021042757112693200664826
e: 65537
cyphertext: 6923703894130988471678648525836455221581350036345593097583476279507226808570130339090287217067132386445725003856544219084021818771543126551148484721956423
```
ejecutamos el siguiente código para obtener la bandera.
```
from Crypto.Util.number import long_to_bytes, inverse

# Datos de tu sesión de Kali
n = 17681111459803207224577120160344423739497719865764697733752619172317142782910167419560966900397519233064913923036750164897964571843021042757112693200664826
e = 65537
c = 6923703894130988471678648525836455221581350036345593097583476279507226808570130339090287217067132386445725003856544219084021818771543126551148484721956423

# 1. Factorizamos N
p = 2
q = n // p

# 2. Calculamos phi(n) = (p-1)*(q-1)
phi = (p - 1) * (q - 1)

# 3. Calculamos la d (llave privada)
d = inverse(e, phi)

# 4. Desciframos
m = pow(c, d, n)

# 5. Pasamos de número a texto
flag = long_to_bytes(m)
print(f"Tu flag es: {flag.decode()}")
```

Tu flag es: picoCTF{tw0_1$_pr!m341c6ed35}
### Notas
