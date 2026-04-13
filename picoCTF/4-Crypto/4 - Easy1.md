### Easy1
The one time pad can be cryptographically secure, but not when you know the key. Can you solve this?We've given you the encrypted flag, key, and a table to help UFJKXQZQUNB with the key of SOLVECRYPTO. Can you use this [table](https://challenge-files.picoctf.net/c_fickle_tempest/859ffc313a4d8b63149f144745043a7312fc4f993e405eeeb8ee5ae6ca8444a8/table.txt) to solve it?.
### Solución
La bandera cifrada es UFJKXQZQUNB y la llave es SOLVECRYPTO. Se puede hacer a mano con el archivo table que nos da el problema o mediante cyberchef.

https://gchq.github.io/CyberChef/#recipe=Vigen%C3%A8re_Decode('SOLVECRYPTO')&input=VUZKS1hRWlFVTkI

picoCTF{CRYPTOISFUN}

### Notas
En [criptografía](https://es.wikipedia.org/wiki/Criptograf%C3%ADa "Criptografía"), la **libreta de uso único**, también llamado **libreta de un solo uso** (del inglés _one-time pad_), es un tipo de [algoritmos](https://es.wikipedia.org/wiki/Algoritmos "Algoritmos") de [cifrado](https://es.wikipedia.org/wiki/Cifrado_\(criptograf%C3%ADa\) "Cifrado (criptografía)") por el que el [texto en claro](https://es.wikipedia.org/wiki/Texto_en_claro "Texto en claro") se combina con una clave aleatoria o «libreta» igual de larga que el texto en claro y que sólo se utiliza una vez.

El cifrado de Vigenère es un ==método de cifrado polialfabético clásico que utiliza una palabra clave para aplicar múltiples cifrados César a un texto, haciendo que una misma letra original se cifre con letras diferentes==.
