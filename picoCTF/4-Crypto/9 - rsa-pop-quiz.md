### rsa-pop-quiz
Class, take your seats! It's PRIME-time for a quiz...nc fickle-tempest.picoctf.net 55217
### Solución
Se solucionó calculando cada valor de la llave RSA con
```
RSA - llave publica - asimetrico
-------------------------------------------------------------------------
m   - mensaje original o mensaje en texto plano 
c   - mensaje cifrado (ciphertext)
p,q - son dos numeros primos distintos y muy grandes
n   - es el modulo (lo compartes las llaves publica como privada)
tn  - totient n (funcion de euler)
e   - llave public - 65537 (exponente)  2 ^ 16 + 1
d   - llave privada

Calculos
--------------------------------------------------
n  = p * q
tn = (p -1) * (q-1)
d = e ^ -1 (mod tn)     - pow(e, -1, tn)

Cifrar  
--------------------------------------------------
c = m ^ e (mod n)       - pow(m, e, n)

Decifrars
--------------------------------------------------
m = c ^ d (mod n)       - pow(c, d, n)

```

dándonos la bandera:
picoCTF{wA8_th4till3aGal..ob6435DeB}
### Notas
El algoritmo RSA es un ==sistema de cifrado asimétrico (clave pública) fundamental en seguridad digital==, desarrollado por Rivest, Shamir y Adleman. Utiliza una clave pública para cifrar datos y una privada para descifrarlos, basando su seguridad en la dificultad computacional de factorizar números primos grandes. Se usa masivamente en comunicaciones seguras (SSL/TLS), firmas digitales y encriptación de datos.
