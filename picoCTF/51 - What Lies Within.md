### What Lies Within

There's something in the [building](https://challenge-files.picoctf.net/c_fickle_tempest/c0eec6af0f04316e2bdc4a9f095afd0e2d0121f5e543dbc4a65bb0038d72a993/buildings.png). Can you retrieve the flag?
### Solución 
Se uso zsteg para encontrar la bandera oculta en la imagen.
```
┌──(kali㉿kali)-[~/problemasPICO/whatLiesWithin]
└─$ zsteg -a buildings.png | grep picoCTF
b1,rgb,lsb,xy       .. text: "picoCTF{h1d1ng_1n_th3_b1t5}"
  
```

picoCTF{h1d1ng_1n_th3_b1t5}

### Notas
La esteganografia es ocultar informacion en un archivo.
