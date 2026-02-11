### Tab, Tab, Attack
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames.[Addadshashanammu.zip](https://challenge-files.picoctf.net/c_wily_courier/c090282eec93405912f926586287741dd5b9bd24cbdf8f3555c53902d556e508/Addadshashanammu.zip)


### Solución 1 - En terminal de Linux


```
daniel_minbot-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilka
la/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ strings fang-of-haynekhtnamet | grep 'pico' 
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_fc588427}
```


picoCTF{l3v3l_up!_t4k3_4_r35t!_fc588427}
### Notas
Se realizo el ingreso a cada directorio autocompletando el nombre complejo con TAB, llegando al requerido se hace una busqueda en el archivo binario con strings y grep.

