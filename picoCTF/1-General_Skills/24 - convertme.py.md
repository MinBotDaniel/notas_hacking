### convertme.py

Run the Python script and convert the given number from decimal to binary to get the flag.[Download Python script](https://artifacts.picoctf.net/c/22/convertme.py)
### Solución 1 - Se ejecuta con python


```
daniel_minbot-picoctf@webshell:~$ wget -q  https://artifacts.picoctf.net/c/22/convertme.py
daniel_minbot-picoctf@webshell:~$ ls
README.txt  code.py  codebook.txt  convertme.py
daniel_minbot-picoctf@webshell:~$ python convertme.py 
If 18 is in decimal base, what is it in binary base?
Answer: 00010010
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_762f748e}
```

picoCTF{4ll_y0ur_b4535_762f748e}

Se requirió de cyberChef para convertir el numero de decimal a binario:
https://gchq.github.io/CyberChef/#recipe=To_Base(2)&input=MTg
### Notas
Todo se ejecutó en la terminal

