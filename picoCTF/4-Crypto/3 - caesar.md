### caesar
Decrypt this message.Message: [message](https://challenge-files.picoctf.net/c_fickle_tempest/bfd7c036228a50ff9e76dfc29ac6cec116f209f0db26506497997f0aca083105/data.enc)
### Solución
Descargamo el mensaje y al hacer cat, vemos que está cifrado la parte dentro de las llaves de la bandera.
```
┌──(kali㉿kali)-[~/problemasPICO/caesar]
└─$ cat data.enc 
picoCTF{dspttjohuifsvcjdpohatwvibg}
```

En cyberchef ponemos el ROT13 para ir incrementando las posiciones de desplazamiento y encontrar el encriptado.
https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,25)&input=ZHNwdHRqb2h1aWZzdmNqZHBvaGF0d3ZpYmc
En este caso de 25.

picoCTF{crossingtherubicongzsvuhaf}

### Notas
El _cifrado_ César consiste en sustituir cada letra del abecedario por una letra desplazada un número determinado de posiciones (clave).
