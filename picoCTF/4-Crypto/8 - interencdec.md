### interencdec
Can you get the real meaning from this file.Download the file [here](https://artifacts.picoctf.net/c_titan/3/enc_flag).
### Solución
Descargamos el archivo y lo desencriptamos en base 64 dos veces
```
┌──(kali㉿kali)-[~/problemasPICO/interedcec]
└─$ cat enc_flag 
YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclgya3lNRFJvYTJvMmZRPT0nCg==
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/problemasPICO/interedcec]
└─$ echo "YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclgya3lNRFJvYTJvMmZRPT0nCg==" | base64 -d | tr -d "b'" | base64 -d
wpjvJAM{jhlzhy_k3jy9wa3k_i204hkj6}   
```
Lo obtenido lo pasamos en cyberchef para descifrado cesar con desplazamiento de 19.
[https://www.guballa.de/substitution-solver](https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,19)&input=d3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX2kyMDRoa2o2fQ&ieol=CRLF)
picoCTF{caesar_d3cr9pt3d_b204adc6}
### Notas

