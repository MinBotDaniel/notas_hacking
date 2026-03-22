### Cookie Monster Secret Recipe
Cookie Monster has hidden his top-secret cookie recipe somewhere on his website. As an aspiring cookie detective, your mission is to uncover this delectable secret. Can you outsmart Cookie Monster and find the hidden recipe?You can access the Cookie Monster [here](http://verbal-sleep.picoctf.net:62792/) and good luck
### Solución 
La página nos ofrece una cookie llamada secret_recipe con el valor: cGljb0NURntjMDBrMWVfbTBuc3Rlcl9sMHZlc19jMDBraWVzXzJDODA0MEVGfQ%3D%3D que es un codificado en base 64, por lo que solo se decodifica.

```
┌──(kali㉿kali)-[~]
└─$ echo cGljb0NURntjMDBrMWVfbTBuc3Rlcl9sMHZlc19jMDBraWVzXzJDODA0MEVGfQ%3D%3D | base64 -d                                             
picoCTF{c00k1e_m0nster_l0ves_c00kies_2C8040EF}base64: invalid input

```

picoCTF{c00k1e_m0nster_l0ves_c00kies_2C8040EF}
### Notas
Se usó cookie editor.