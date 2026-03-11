### dont-use-client-side

The factory is hiding things from all of its users.Can you login as Joe and find what they've been looking at? http://fickle-tempest.picoctf.net:58238
### Solución - Verificando en el depurador de javaScript
Aperece un codigo como este
```
function verify() {
    checkpass = document.getElementById("pass").value;
    split = 4;
    if (checkpass.substring(0, split) == 'pico') {
      if (checkpass.substring(split*6, split*7) == 'eb02') {
        if (checkpass.substring(split, split*2) == 'CTF{') {
         if (checkpass.substring(split*4, split*5) == 'ts_p') {
          if (checkpass.substring(split*3, split*4) == 'lien') {
            if (checkpass.substring(split*5, split*6) == 'lz_2') {
              if (checkpass.substring(split*2, split*3) == 'no_c') {
                if (checkpass.substring(split*7, split*8) == 'b45}') {
                  alert("Password Verified")
                  }
                }
              }
      
            }
          }
        }
      }
    }
    else {
      alert("Incorrect password");
    }
    
  }
```

picoCTF{no_clients_plz_2eb02b45}
### Notas
Se fue siguiendo el orden, empieza en 0 a split, luego split a 2, 2 a 3 y asi

