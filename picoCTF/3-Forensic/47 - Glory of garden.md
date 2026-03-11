### Glory of garden

This file contains more than it seems.Get the flag from [garden.jpg](https://challenge-files.picoctf.net/c_fickle_tempest/19722024edeecca10f263776ab05c8b1235b136dcf25aa6e976d3860513ffcd5/garden.jpg).
### Solución 
Mediante el comando strings
```
┌──(kali㉿kali)-[~]
└─$ strings garden.jpg | grep pico
Here is a flag: picoCTF{more_than_m33ts_the_3y37fde8891}
```

picoCTF{more_than_m33ts_the_3y37fde8891}
### Notas
The `strings` command in Linux is ==a utility used to **extract printable character sequences from binary files** and other non-text files==.