### Commitment Issues

I accidentally wrote the flag down. Good thing I deleted it!You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/77/challenge.zip)
### Solución 1 - Usando comandos de git


```
daniel_minbot-picoctf@webshell:~/drop-in$ git init
daniel_minbot-picoctf@webshell:~/drop-in$ git log
daniel_minbot-picoctf@webshell:~/drop-in$ git checkout 3d5ec8a26ee7b092a1760fea18f384c35e435139

daniel_minbot-picoctf@webshell:~/drop-in$ cat message.txt 
picoCTF{s@n1t1z3_30e86d36}
```


picoCTF{s@n1t1z3_30e86d36}
### Notas
Se usó el comando git log para revisar los push anteriores y de esta manera obtener el ID para posteriormente realizar un git checkout 'ID', así se accede a una versión anterior y solo se hizo cat message.txt para obtener el mensaje en aquel momento.