### Time machine

What was I last working on? I remember writing a note to help me remember...You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/161/challenge.zip)
### Solución 1 - Usando comandos de git


```
daniel_minbot-picoctf@webshell:~/drop-in$ wget -q https://artifacts.picoctf.net/c_titan/161/challenge.zip
daniel_minbot-picoctf@webshell:~/drop-in$ ls
challenge.zip  message.txt
daniel_minbot-picoctf@webshell:~/drop-in$ unzip -q challenge.zip 
daniel_minbot-picoctf@webshell:~/drop-in$ ls
challenge.zip  drop-in  message.txt
daniel_minbot-picoctf@webshell:~/drop-in$ cd drop-in/
daniel_minbot-picoctf@webshell:~/drop-in/drop-in$ ls
message.txt
daniel_minbot-picoctf@webshell:~/drop-in/drop-in$ cat message.txt 
This is what I was working on, but I'd need to look at my commit history to know why...daniel_minbot-picoctf@webshell:~/drop-in/drop-in$ git log

commit 10228f3d6437701ef5aaac04213757031f30ebec (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:24 2024 +0000

    picoCTF{t1m3m@ch1n3_8defe16a}
(END)

```


picoCTF{t1m3m@ch1n3_8defe16a}
### Notas
Mismo procedimiento que el anterior pero usando solo git log.