### Local Authority

Can you get the flag?Go to this [website](http://saturn.picoctf.net:64967/) and see what you can discover
### Solución 1
Inspeccionamos el código fuente de la página y de este modo aparece un script en el que nos dice la contraseña y usuario a usar.

```
function checkPassword(username, password)
{
  if( username === 'admin' && password === 'strongPassword098765' )
  {
    return true;
  }
  else
  {
    return false;
  }
}
```
picoCTF{j5_15_7r4n5p4r3n7_a8788e61}
### Notas
solo se copia y pegan los datos.
