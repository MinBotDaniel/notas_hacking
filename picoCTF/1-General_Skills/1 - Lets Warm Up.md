### Lets Warm Up

If I told you a word started with 0x70 in hexadecimal, what would it start with in ASCII?

### Solucion 1 - Usando cyberchef

[https://gchq.github.io/CyberChef/#recipe=From_Hex('Auto')&input=MHg3MA](https://gchq.github.io/CyberChef/#recipe=From_Hex\('Auto'\)&input=MHg3MA "https://gchq.github.io/CyberChef/#recipe=From_Hex('Auto')&input=MHg3MA
(https://gchq.github.io/CyberChef/#recipe=From_Hex('Auto')&input=MHg3MA)") p picoCTF{p}

### Solucion 2 - Usando Python

```
>>> int(0x70) 112
>>> chr(112) 'p'
```
### Notas

- Cyberchef  permite decodificar diferentes tipos de formatos

### Referencias

- [https://gchq.github.io/CyberChef](https://gchq.github.io/CyberChef "https://gchq.github.io/CyberChef
