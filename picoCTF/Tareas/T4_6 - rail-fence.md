### rail-fence

A type of transposition cipher is the rail fence cipher, which is described [here](https://en.wikipedia.org/wiki/Rail_fence_cipher). Here is one such cipher encrypted using the rail fence with 4 rails. Can you decrypt it?Download the message [here](https://artifacts.picoctf.net/c/188/message.txt).Put the decoded message in the picoCTF flag format, `picoCTF{decoded_message}`.
### Solución 1
Se realizó con el siguiente exploid.
```
def decrypt_rail_fence(cipher, rails):
    # Creamos una matriz vacía para marcar el patrón
    fence = [['\n' for _ in range(len(cipher))] for _ in range(rails)]
    
    # Determinamos el patrón de zigzag
    rail = 0
    direction = 1 # 1 para bajar, -1 para subir
    for i in range(len(cipher)):
        fence[rail][i] = '*'
        rail += direction
        if rail == rails - 1 or rail == 0:
            direction *= -1
            
    # Llenamos el patrón con los caracteres del mensaje cifrado
    index = 0
    for r in range(rails):
        for c in range(len(cipher)):
            if fence[r][c] == '*' and index < len(cipher):
                fence[r][c] = cipher[index]
                index += 1
                
    # Leemos en zigzag para recuperar el mensaje original
    result = []
    rail = 0
    direction = 1
    for i in range(len(cipher)):
        result.append(fence[rail][i])
        rail += direction
        if rail == rails - 1 or rail == 0:
            direction *= -1
            
    return "".join(result)

# Pega aquí el texto que viene en tu archivo descargado
ciphertext = "Ta _7N6D49hlg:W3D_H3C31N__A97ef sHR053F38N43D7B i33___N6 " 
rails = 4

print(f"picoCTF{{{decrypt_rail_fence(ciphertext, rails)}}}")
```
```
┌──(kali㉿kali)-[~/Tareas]
└─$ python3 exp.py
picoCTF{Theiflag 3s: WH3R3_D0_5_7H3_F3NC3_8361NN4ND_36D_4A7 B997 }

```

picoCTF{WH3R3_D035_7H3_F3NC3_8361N_4ND_3ND_4A76B997}
### Notas
El cifrado de **Rail Fence** (o cifrado de zigzag) es pura transposición, **papichulo**. A diferencia de los que hemos visto (como ROT13 o RSA), aquí no se cambian las letras, solo se desordenan siguiendo un patrón de "valla" o "serpiente".