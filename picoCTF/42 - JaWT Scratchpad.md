### JaWT Scratchpad

Check the admin scratchpad! http://fickle-tempest.picoctf.net:51363
### Solución 

```
┌──(kali㉿kali)-[~]
└─$ ls
Desktop    Downloads  Music     Public     Videos
Documents  eltoken    Pictures  Templates
                                                                             
┌──(kali㉿kali)-[~]
└─$ john eltoken 
Created directory: /home/kali/.john
Using default input encoding: UTF-8
Loaded 1 password hash (HMAC-SHA256 [password is key, SHA256 256/256 AVX2 8x])
Will run 2 OpenMP threads
Proceeding with single, rules:Single
Press 'q' or Ctrl-C to abort, almost any other key for status
Almost done: Processing the remaining buffered candidate passwords, if any.
Proceeding with wordlist:/usr/share/john/password.lst
Proceeding with incremental:ASCII
0g 0:00:00:40  3/3 0g/s 4295Kp/s 4295Kc/s 4295KC/s gn627t..gcsd1m
Session aborted

HEADER:ALGORITHM & TOKEN TYPE

{

  "typ": "JWT",

  "alg": "HS256"

}

PAYLOAD:DATA

{

  "user": "admin"

}

VERIFY SIGNATURE

HMACSHA256(
  base64UrlEncode(header) + "." +
  base64UrlEncode(payload),
  
) secret base64 encoded

```

picoCTF{jawt_was_just_what_you_thought_bbb82bd4a57564aefb32d69dafb60583}
### Notas
Token jwt, Un archivo JSON es una cadena de caracteres separada por 3 puntos. La primera tiene el algoritmo de encriptacion. 


https://jwt.lannysport.net/


