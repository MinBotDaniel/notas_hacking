### Static ain't always noise
Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information...[warm](https://challenge-files.picoctf.net/c_wily_courier/11d04620d1b8e59680f745f5e3d3957d48628b1e3e7c56c74c0030e82a778d63/warm)
### Solución 1 - Comando strings


```
daniel_minbot-picoctf@webshell:~$ strings static | grep 'pico' 
picoCTF{d15a5m_t34s3r_20335e41}
```


picoCTF{d15a5m_t34s3r_20335e41}

### Notas
Se usa el comando strings usado en ejercicios anteriores