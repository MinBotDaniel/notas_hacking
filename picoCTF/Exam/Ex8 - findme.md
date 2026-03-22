### findme
Help us test the form by submiting the username as `test` and password as `test!`

Additional details will be available after launching your challenge instance.
### Solución 
Cuando inicias sesión con las credenciales que te da la plataforma (suele ser el usuario `test` y la contraseña `test!`), el servidor no te lleva directamente a la página de inicio. Por debajo, hace un par de "saltos" o redirecciones (códigos de estado HTTP `302`) muy rápidas antes de dejarte en la página final.

Usando burp suite para ver este rastro
![[Pasted image 20260322131122.png]]

En el id de los GET se puede ver que hay una cadena en base 64 dividida en 2, al decodificarla obtenemos la bandera. 
```
┌──(kali㉿kali)-[~]
└─$ echo "bF90aGVfd2F5XzI1YmJhZTlhfQ==" | base64 -d                       
l_the_way_25bbae9a}                                                                     
┌──(kali㉿kali)-[~]
└─$ echo "cGljb0NURntwcm94aWVzX2Fs" | base64 -d 
picoCTF{proxies_al                                                                 
```
picoCTF{proxies_all_the_way_25bbae9a}
### Notas
Se resolvio analizando tráfico de red