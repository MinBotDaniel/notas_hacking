### SQL Direct
Connect to this PostgreSQL server and find the flag!`psql -h saturn.picoctf.net -p 61998 -U postgres pico`Password is `postgres`
### Solución 
Simplemente se realizo una consulta de la tabla existente en la base de datos de postgre.
```
┌──(kali㉿kali)-[~]
└─$ psql -h saturn.picoctf.net -p 61998 -U postgres pico
Password for user postgres: 
psql (18.1 (Debian 18.1-2), server 15.2 (Debian 15.2-1.pgdg110+1))
Type "help" for help.

pico=# \dt
          List of tables
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)

pico=# SELECT * FROM flags;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_73b0678f}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)
```

picoCTF{L3arN_S0m3_5qL_t0d4Y_73b0678f}
### Notas
Se requirio consulta postgreSQL
