### Collaborative Development

My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/71/challenge.zip)
### Solución 1 - Usando git branch -a y git checkout


```
daniel_minbot-picoctf@webshell:~$ unzip -q challenge.zip 
daniel_minbot-picoctf@webshell:~$ ls
README.txt  challenge.zip  drop-in
daniel_minbot-picoctf@webshell:~$ cd drop-in/
daniel_minbot-picoctf@webshell:~/drop-in$ ls
flag.py
daniel_minbot-picoctf@webshell:~/drop-in$ git branch -a

feature/part-1
  feature/part-2
  feature/part-3
* main
  
daniel_minbot-picoctf@webshell:~/drop-in$ git checkout feature/part-1
Switched to branch 'feature/part-1'
daniel_minbot-picoctf@webshell:~/drop-in$ cat flag.py 
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')
daniel_minbot-picoctf@webshell:~/drop-in$ git checkout feature/part-2
Switched to branch 'feature/part-2'
daniel_minbot-picoctf@webshell:~/drop-in$ cat flag.py 
print("Printing the flag...")

print("m@k3s_th3_dr3@m_", end='')
daniel_minbot-picoctf@webshell:~/drop-in$ git checkout feature/part-3
Switched to branch 'feature/part-3'
daniel_minbot-picoctf@webshell:~/drop-in$ cat flag.py 
print("Printing the flag...")

print("w0rk_4c24302f}")

```

picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_4c24302f}

### Notas
Se usó el comando git branch -a para detectar las branch que estaban disponibles y con git checkout 'branch' se pudo ir por cada parte de la bandera.