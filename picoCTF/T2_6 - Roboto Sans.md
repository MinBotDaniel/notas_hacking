### Roboto Sans

The flag is somewhere on this web application not necessarily on the website. Find it.Check [this](http://saturn.picoctf.net:58617/) out.
### Solución 1
ponemos al final de la liga un /robots.txt
asi obtenemos lo siguiente

```
User-agent *
Disallow: /cgi-bin/
Think you have seen your flag or want to keep looking.

ZmxhZzEudHh0;anMvbXlmaW
anMvbXlmaWxlLnR4dA==
svssshjweuiwl;oiho.bsvdaslejg
Disallow: /wp-admin/
```

si decodificamos 
```
┌──(kali㉿kali)-[~]
└─$ echo anMvbXlmaWxlLnR4dA== | base64 -d
js/myfile.txt  
```
ponemos al final de la liga, nos da la bandera.

picoCTF{Who_D03sN7_L1k5_90B0T5_22ce1f22}
### Notas
se buscó un archivo tipo robots.txt
