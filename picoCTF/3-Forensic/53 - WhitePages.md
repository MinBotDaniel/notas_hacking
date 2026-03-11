### WhitePages

I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://challenge-files.picoctf.net/c_fickle_tempest/3ba37d6bee0d96d5e3783ba94da753407f9168b61d796797f0816db5aaa86136/whitepages.txt) is all blank!
### Solución 
Se realizo el siguiente codigo en python
```
from pwn import *
file = open('whitepages.txt', 'rb')
data = bytearray(file.read())
data = data.replace(b'\xe2\x80\x83', b'0')
data = data.replace(b'\x20', b'1')
data = data.decode('ascii')
data = unbits(data)
print(data)
```
mas tarde se ejecuta en la terminal
```
┌──(kali㉿kali)-[~/problemasPICO/whitepages]
└─$ python exp.py | grep pico    
b'\npicoCTF\n\nSEE PUBLIC RECORDS & BACKGROUND REPORT\n5000 Forbes Ave, Pittsburgh, PA 15213\npicoCTF{not_all_spaces_are_created_equal_f62118c302bc9c9791e81915c805af3d}\n'
```


picoCTF{not_all_spaces_are_created_equal_f62118c302bc9c9791e81915c805af3d}

### Notas
Unicode es un estándar de codificación de caracteres diseñado para facilitar el tratamiento informático, transmisión y visualización de textos de numerosos idiomas y disciplinas técnicas, además de textos clásicos de lenguas muertas.

Se instalo y uso pwntools.
Si no deja instalar, se usa python3 -m pip install pwntools --break-system-packages



