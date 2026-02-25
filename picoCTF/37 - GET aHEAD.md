### GET aHEAD

Find the flag being held on this server to get ahead of the competitionhttp://wily-courier.picoctf.net:49259/
### Solución - Mediante terminal
Obteniendo con el metodo HEAD desde la terminal de kali.
```
┌──(kali㉿kali)-[~]
└─$ curl -I HEAD http://wily-courier.picoctf.net:49259/index.php
curl: (6) Could not resolve host: HEAD
HTTP/1.1 200 OK
Date: Wed, 25 Feb 2026 21:12:57 GMT
Server: Apache/2.4.38 (Debian)
X-Powered-By: PHP/7.2.34
flag: picoCTF{r3j3ct_th3_du4l1ty_8b13f07}
Content-Type: text/html; charset=UTF-8

```


picoCTF{r3j3ct_th3_du4l1ty_8b13f07}
### Notas
HTTP request methods indican indican una accion para un metodo dado.


