### Wave a flag
Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information...[warm](https://challenge-files.picoctf.net/c_wily_courier/11d04620d1b8e59680f745f5e3d3957d48628b1e3e7c56c74c0030e82a778d63/warm)
### Solución 1 - Comando -h


```
daniel_minbot-picoctf@webshell:~$ wget https://challenge-files.picoctf.net/c_wily_courier/11d04620d1b8e59680f745f5e3d3957d48628b1e3e7c56c74c0030e82a778d63/warm
--2026-02-11 16:02:48--  https://challenge-files.picoctf.net/c_wily_courier/11d04620d1b8e59680f745f5e3d3957d48628b1e3e7c56c74c0030e82a778d63/warm
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.40, 3.160.5.95, 3.160.5.64, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 19312 (19K) [application/octet-stream]
Saving to: 'warm'

warm                100%[================>]  18.86K  --.-KB/s    in 0.006s  

2026-02-11 16:02:48 (3.28 MB/s) - 'warm' saved [19312/19312]
daniel_minbot-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_ac5832c}
```


picoCTF{b1scu1ts_4nd_gr4vy_ac5832c}

### Notas
Se usa el comando chmod +x para darle permiso al archivo de ser ejecutable y se realizo ./warm -h para ver informacion del ejecutable.