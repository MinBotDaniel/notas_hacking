### substitution1

A second message has come in the mail, and it seems almost identical to the first one. Maybe the same thing will work again.Download the message [here](https://artifacts.picoctf.net/c/181/message.txt).
### Solución 1
Como sugiere el hint, este reto se resuelve por **frecuencia de letras**. En inglés, la letra más común es la **E**, seguida de la **T**, **A**, **O**, etc. (el famoso _ETAOIN SHRDLU_).

Estructura:

- **`ZWDg`** aparece al principio. En el contexto de estas competencias, es obvio que significa **`CTFs`**.
    
- Esto nos da una base: `Z=C`, `W=T`, `D=F`, `g=s`.
    
- Luego dice **`(gejfw djf zacwpfx wex dqar)`**. Si `ZWDg` es `CTFs`, lo que está en paréntesis es la definición: **`(short for capture the flag)`**.

Al ir sustituyendo las letras más comunes y palabras cortas (como `wex` que claramente es `the`), obtenemos el abecedario completo:

|**Cifrado**|**Real**|
|---|---|
|**c**|**p**|
|**b**|**i**|
|**z**|**c**|
|**j**|**o**|
|**Z**|**C**|
|**W**|**T**|
|**D**|**F**|
|**x**|**e**|
|**f**|**r**|
Si aplicamos este mapeo a la cadena final:

`cbzjZWD{DF3LP3VZS_4774ZN5_4F3_Z001_4871X6DT}`

1. `cbzjZWD` → **`picoCTF`**
    
2. `DF3LP3VZS` → **`FR3QU3NCY`** (`D=F`, `F=R`, `L=Q`, `P=U`, `V=N`, `Z=C`, `S=Y`)
    
3. `4774ZN5` → **`4774CK5`** (`Z=C`, `N=K`)
    
4. `4F3` → **`4R3`** (`F=R`)
    
5. `Z001` → **`C001`** (o **`C00L`**, pero en estos retos los números suelen quedarse como números)
    
6. `4871X6DT` → **`4871E6FB`** (`X=E`, `D=F`, `T=B`)

picoCTF{5UB5717U710N_3V0LU710N_357BF9FF}
### Notas
