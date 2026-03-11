### m00nwalk

Decode this [message](https://challenge-files.picoctf.net/c_fickle_tempest/5593bde2464fd1977048cba02daa086d1fbc0fada1ef8521169ccdad2f19c6fc/message.wav) from the moon.
### Solución 
Con la herramienta sstv en kali
```
┌──(kali㉿kali)-[~/problemasPICO/moonwalk]
└─$ ls
flag.png  message.wav
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/problemasPICO/moonwalk]
└─$ open flag.png   
  
```
Nos deja una imagen que contiene la bandera

picoCTF{beep_boop_im_in_space}

### Notas
El formato ssv codifica mensajes en un audio.

### Referencias
https://github.com/colaclanth/sstv
