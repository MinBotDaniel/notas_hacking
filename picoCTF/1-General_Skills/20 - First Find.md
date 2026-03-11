### First Find

Unzip this archive and find the file named 'uber-secret.txt'

- [Download zip file](https://artifacts.picoctf.net/c/501/files.zip)
### Solución 1 - En terminal con grep -r


```
daniel_minbot-picoctf@webshell:~$ cd files/
daniel_minbot-picoctf@webshell:~/files$ ls
13771.txt.utf-8  acceptable_books  satisfactory_books
14789.txt.utf-8  adequate_books
daniel_minbot-picoctf@webshell:~/files$ grep -r 'pico'
adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt:picoCTF{f1nd_15_f457_ab443fd1}
14789.txt.utf-8:brassa un picotin d'orge_. Comme depuis une demi-heure environ c'était
```

picoCTF{f1nd_15_f457_ab443fd1}
### Notas
Se descomprime el zip y se busca en todos los directorios la clave.

