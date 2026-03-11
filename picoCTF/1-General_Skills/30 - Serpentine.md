### Serpentine

Find the flag in the Python script![Download Python script](https://artifacts.picoctf.net/c/37/serpentine.py)
### Solución 1 - Se ejecuta con python


```
daniel_minbot-picoctf@webshell:~$ nano serpentine.py 

~~Internamente se realizaron los siguientes cambios~~
elif choice == 'b':
      print_flag()
      #print('\nOops! I must have misplaced the print_flag function! Check my source code!\n\n')


daniel_minbot-picoctf@webshell:~$ python serpentine.py

    Y
  .-^-.
 /     \      .- ~ ~ -.
()     ()    /   _ _   `.                     _ _ _
 \_   _/    /  /     \   \                . ~  _ _  ~ .
   | |     /  /       \   \             .' .~       ~-. `.
   | |    /  /         )   )           /  /             `.`.
   \ \_ _/  /         /   /           /  /                `'
    \_ _ _.'         /   /           (  (
                    /   /             \  \
                   /   /               \  \
                  /   /                 )  )
                 (   (                 /  /
                  `.  `.             .'  /
                    `.   ~ - - - - ~   .'
                       ~ . _ _ _ _ . ~

Welcome to the serpentine encourager!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) b
picoCTF{7h3_r04d_l355_7r4v3l3d_8e47d128}
a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) 
```


picoCTF{7h3_r04d_l355_7r4v3l3d_8e47d128}
### Notas
Internamente solo se comentó la línea que decía que se había olvidado la contraseña y se mandó a llamar la funcion que imprime la bandera.
