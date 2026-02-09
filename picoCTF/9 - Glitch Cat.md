### Glitch Cat

Our flag printing service has started glitching!`$ nc saturn.picoctf.net 54286`
### Solución 1
```
daniel_minbot-picoctf@webshell:~$ nc saturn.picoctf.net 54286
'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'

daniel_minbot-picoctf@webshell:~$ python
Python 3.10.12 (main, Feb  4 2025, 14:57:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'
'picoCTF{gl17ch_m3_n07_a4392d2e}'
```




picoCTF{gl17ch_m3_n07_a4392d2e}

### Notas
La clave contenia una concatenacion de cadenas que en conjunto mostraba la clave

