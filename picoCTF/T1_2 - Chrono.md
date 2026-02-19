### Chrono

How to automate tasks to run at intervals on linux servers?Use ssh to connect to this server:

```
Server: saturn.picoctf.net
Port: 61827
Username: picoplayer 
Password: bLgSMmbY6X
```
### Solución 1 - Revisando el crontab del sistema


```
picoplayer@challenge:~$ cat /etc/crontab
# picoCTF{Sch3DUL7NG_T45K3_L1NUX_1b4d8744}
```


picoCTF{Sch3DUL7NG_T45K3_L1NUX_1b4d8744}
### Notas
Cron es un proceso en segundo plano que ejecuta comandos en intervalos específicos.
El Crontab del sistema son tareas globales que afectan a todo el servidor.