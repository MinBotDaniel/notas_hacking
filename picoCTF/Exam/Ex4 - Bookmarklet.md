### Bookmarklet
Why search for the flag when I can make a bookmarklet to print it for me?Browse [here](http://titan.picoctf.net:53790/), and find the flag!
### Solución 
La página nos da un código javascript que contiene un bookmark
```
        javascript:(function() {
            var encryptedFlag = "àÒÆÞ¦È¬ëÙ£ÖÓÚåÛÑ¢ÕÓÉÕËÆÒÇÚËí";
            var key = "picoctf";
            var decryptedFlag = "";
            for (var i = 0; i < encryptedFlag.length; i++) {
                decryptedFlag += String.fromCharCode((encryptedFlag.charCodeAt(i) - key.charCodeAt(i % key.length) + 256) % 256);
            }
            alert(decryptedFlag);
        })();
```

Al ejecutarlo en la consola del navegador nos arroja la bandera.

![[Pasted image 20260322121800.png]]
picoCTF{p@g3_turn3r_cebccdfe}
### Notas
Un **bookmarklet** es básicamente un marcador (bookmark) en tu navegador web, pero con un giro interesante. En lugar de guardar una dirección web normal (como `https://...`), guarda un fragmento de código JavaScript (que suele empezar con `javascript:`). Cuando haces clic en ese marcador, el navegador ejecuta el código directamente sobre la página en la que te encuentras en ese momento.
