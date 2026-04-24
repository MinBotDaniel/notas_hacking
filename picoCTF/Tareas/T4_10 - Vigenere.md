### Vigenere
Can you decrypt this message?Decrypt this [message](https://artifacts.picoctf.net/c/159/cipher.txt) using this key "CYLAB".
### Solución 1
Obtenemos la clave cifrada:
```
┌──(kali㉿kali)-[~/Tareas]
└─$ cat cipher.txt                                           
rgnoDVD{O0NU_WQ3_G1G3O3T3_A1AH3S_f85729e7}
```
Se soluciona con el siguiente exploid:
```
def vigenere_decrypt(ciphertext, key):
    decrypted = ""
    key = key.upper()
    key_index = 0
    
    for char in ciphertext:
        if char.isalpha():
            # Determinar si es mayúscula o minúscula
            start = ord('A') if char.isupper() else ord('a')
            # Calcular el desplazamiento de la llave
            shift = ord(key[key_index % len(key)]) - ord('A')
            # Descifrar
            decrypted += chr((ord(char) - start - shift) % 26 + start)
            key_index += 1
        else:
            # Los números y símbolos se quedan igual y NO avanzan la llave
            decrypted += char
            
    return decrypted

cipher = "rgnoDVD{O0NU_WQ3_G1G3O3T3_A1AH3S_f85729e7}"
key = "CYLAB"
print(f"Flag: {vigenere_decrypt(cipher, key)}")
```


picoCTF{D0NT_US3_V1G3N3R3_C1PH3R_d85729g7}

### Notas
The **Vigenère cipher** (French pronunciation: [[viʒnɛːʁ]](https://en.wikipedia.org/wiki/Help:IPA/French "Help:IPA/French")) is a method of [encrypting](https://en.wikipedia.org/wiki/Encryption "Encryption") alphabetic text where each letter of the [plaintext](https://en.wikipedia.org/wiki/Plaintext "Plaintext") is encoded with a different [Caesar cipher](https://en.wikipedia.org/wiki/Caesar_cipher "Caesar cipher"), whose increment is determined by the corresponding letter of another text, the [key](https://en.wikipedia.org/wiki/Key_\(cryptography\) "Key (cryptography)"). In a [Caesar cipher](https://en.wikipedia.org/wiki/Caesar_cipher "Caesar cipher"), each letter of the alphabet is shifted along some number of places. In a Caesar cipher of shift 3, `a` would become `D`, `b` would become `E`, `y` would become `B` and so on. The Vigenère cipher has several Caesar ciphers in sequence with different shift values.