### Big Zip

Unzip this archive and find the flag.

- [Download zip file](https://artifacts.picoctf.net/c/504/big-zip-files.zip)
### Solución 1 - En terminal con grep


```
daniel_minbot-picoctf@webshell:~/big-zip-files$ grep -r 'pico' 
folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt:information on the record will last a billion years. Genes and brains and books encode picoCTF{gr3p_15_m4g1c_ef8790dc}
```
picoCTF{gr3p_15_m4g1c_ef8790dc}
### Notas
Se usa el subparametro -r en grep para buscar en todos los directorios.

