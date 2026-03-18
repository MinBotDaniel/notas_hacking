### flag_shop
There's a flag shop selling stuff, can you buy a flag?[Source](https://challenge-files.picoctf.net/c_fickle_tempest/8ff1a012a01d1cbdaff34d98276201480b3a664509284c48bb108e0e01d3551d/store.c). Connect with nc fickle-tempest.picoctf.net 61718.
### Solución 
Tenemos que comprar banderas y poner una cantidad enorme para 
```
┌──(kali㉿kali)-[~/problemasPICO/flagshop]
└─$ nc fickle-tempest.picoctf.net 61718                                                                                                  
Welcome to the flag exchange
We sell flags

1. Check Account Balance

2. Buy Flags

3. Exit

 Enter a menu selection
2
Currently for sale
1. Defintely not the flag Flag
2. 1337 Flag
1
These knockoff Flags cost 900 each, enter desired quantity
1110000000

The final cost is: -1727379968

Your current balance after transaction: 1727381068

Welcome to the flag exchange
We sell flags

1. Check Account Balance

2. Buy Flags

3. Exit

 Enter a menu selection
2
Currently for sale
1. Defintely not the flag Flag
2. 1337 Flag
2
1337 flags cost 100000 dollars, and we only have 1 in stock
Enter 1 to buy one1
YOUR FLAG IS: picoCTF{m0n3y_bag5_4E85dfe5}

```


picoCTF{m0n3y_bag5_4E85dfe5}
### Notas
El programa hará esta operación: `costo = cantidad * precio_por_unidad`.

Al ser una cantidad tan grande, el resultado superará el límite de los enteros y el `costo` se volverá un **número negativo gigante** (ej: $-2,000,000,000$).

Cuando el programa haga: `balance = balance - costo`, en realidad estará haciendo `balance - (-2,000,000,000)`, lo que se traduce en **sumarte** esa millonada a tu cuenta.
