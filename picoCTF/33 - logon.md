### logon

The factory is hiding things from all of its users.Can you login as Joe and find what they've been looking at? http://fickle-tempest.picoctf.net:58238
### Solución
Se uso un editor de cookies para poner el valor de admin en True y nos arrojara la bandera


picoCTF{th3_c0nsp1r4cy_l1v3s_4d184b0d}
### Notas
En teoria se puede editar la cookie con la terminal poniendo: curl http://fickle-tempest.picoctf.net:58238 -H "Cookie: username=admin; password=holamundo; admin=True" | grep pico. Sin embargo a mi no me funciono este metodo.

