### substitution2
It seems that another encrypted message has been intercepted. The encryptor seems to have learned their lesson though and now there isn't any punctuation! Can you still crack the cipher?Download the message [here](https://artifacts.picoctf.net/c/112/message.txt).
### Solución 1
Aunque el texto parece una sopa de letras, hay patrones que se repiten constantemente. Por ejemplo, la cadena **`nafy`** o **`naf`** aparece muchísimas veces al inicio de las oraciones. En inglés, la palabra más común de tres letras es **"the"**.

Si mapeamos `naf` → `the`:

- `n` = `t`
    
- `a` = `h`
    
- `f` = `e`
    

Esto nos da una base sólida. Si seguimos este hilo y analizamos el bloque de la flag, podemos reconstruir el alfabeto.


picoCTF{N6R4M_4N41Y515_15_73D10U5_8E1BF808}
### Notas
