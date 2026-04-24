### substitution0

A message has come in but it seems to be all scrambled. Luckily it seems to have the key at the beginning. Can you crack this substitution cipher?Download the message [here](https://artifacts.picoctf.net/c/154/message.txt).
### Solución 1
Es el mapeo directo del abecedario estándar. Funciona así:

- La **A** se convierte en **Z**
    
- La **B** se convierte en **G**
    
- La **C** se convierte en **S**
    
- ...y así sucesivamente.

```
- **r** → Está en la posición 15 de la llave. La letra 16 del abecedario es la **p**.
    
- **u** → Está en la posición 8. La letra 9 es la **i**.
    
- **s** → Está en la posición 2. La letra 3 es la **c**.
    
- **e** → Está en la posición 14. La letra 15 es la **o**.
    
- **S** → Posición 2 → **C**.
    
- **W** → Posición 19 → **T**.
    
- **X** → Posición 5 → **F**.
  
- `5NG5717N710L` → **5UB5717U710N** (SUBSTITUTION)
    
- `3A0MN710L` → **3V0LU710N** (EVOLUTION)
    
- `357GX9XX` → **357BF9FF** **La flag final es:** **`picoCTF{5UB5717U710N_3V0LU710N_357BF9FF}`**

```

picoCTF{5UB5717U710N_3V0LU710N_357BF9FF}
### Notas
