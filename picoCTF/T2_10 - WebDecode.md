### WebDecode

Do you know how to use the web inspector?Start searching [here](http://titan.picoctf.net:54462/) to find the flag
### Solución 1
En la página en about, se encuentra una cadena en base 64, al desglosarla en terminal nos da la bandera.

```
┌──(kali㉿kali)-[~]
└─$ echo cGljb0NURnt3ZWJfc3VjYzNzc2Z1bGx5X2QzYzBkZWRfMTBmOTM3NmZ9 | base64 -d
picoCTF{web_succ3ssfully_d3c0ded_10f9376f} 
```

picoCTF{web_succ3ssfully_d3c0ded_10f9376f}
### Notas
Se usó inspect en las 3 opciones de la página, se encontró en about.
