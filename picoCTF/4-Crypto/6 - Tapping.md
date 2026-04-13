### Tapping
Theres tapping coming in from the wires.What's it saying nc fickle-tempest.picoctf.net 60844.
### Solución
Entramos a la conexión dada y obtenemos un código morse a descifrar.
```
┌──(kali㉿kali)-[~/problemasPICO/easy]
└─$ nc fickle-tempest.picoctf.net 60844
.--. .. -.-. --- -.-. - ..-. { -- ----- .-. ... ...-- -.-. ----- -.. ...-- .---- ... ..-. ..- -. ---.. ....- ---.. ----- .- ..-. ----. -.... } 
```
Que de nuevo se puede decodificar en cyberchef.
https://gchq.github.io/CyberChef/#recipe=From_Morse_Code('Space','Line%20feed')&input=Li0tLiAuLiAtLi0uIC0tLSAtLi0uIC0gLi4tLiB7IC0tIC0tLS0tIC4tLiAuLi4gLi4uLS0gLS4tLiAtLS0tLSAtLi4gLi4uLS0gLi0tLS0gLi4uIC4uLS4gLi4tIC0uIC0tLS4uIC4uLi4tIC0tLS4uIC0tLS0tIC4tIC4uLS4gLS0tLS4gLS4uLi4gfSA
PICOCTF{M0RS3C0D31SFUN8480AF96}

### Notas
El **código morse,** también conocido como **alfabeto morse** o **clave morse**, es un sistema de representación de letras y números mediante señales emitidas de forma intermitente.
