### Blame Game

Someone's commits seems to be preventing the program from working. Who is it?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/74/challenge.zip)
### Solución 1 - Usando git log y un grep


```
daniel_minbot-picoctf@webshell:~/drop-in$ git log
daniel_minbot-picoctf@webshell:~/drop-in$ git log | grep "picoCTF"

```

### Solución 2 - Usando git blame

```
daniel_minbot-picoctf@webshell:~/drop-in$ git blame message.py
0fe87f16 (picoCTF{@sk_th3_1nt3rn_ea346835} 2024-03-09 21:09:25 +0000 1) print("Hello, World!"
```
picoCTF{@sk_th3_1nt3rn_ea346835}
### Notas
git log mas un grep para buscar la bandera en el nombre de los usuarios que modificaron el archivo, también se puede con el comando git blame que devuelve el usuario que realizó la última modificación del archivo