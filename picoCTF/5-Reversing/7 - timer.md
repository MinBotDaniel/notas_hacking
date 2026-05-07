### timer
You will find the flag after analysing this apkDownload [here](https://artifacts.picoctf.net/c/449/timer.apk).
### Solución 1
Usamos un decompiler online y nos da el código fuente de la clase, en el que se ve la comparación realizada.
```
┌──(kali㉿kali)-[~/Tareas]
└─$ unzip timer.apk 

┌──(kali㉿kali)-[~/Tareas]
└─$ strings classes3.dex | grep pico
*picoCTF{t1m3r_r3v3rs3d_succ355fully_17496}         
```

picoCTF{t1m3r_r3v3rs3d_succ355fully_17496} 
### Notas
Los archivos APK (**Android Package Kit**) ==son el formato estándar que utiliza Android para distribuir e instalar aplicaciones==, equivalentes a los `.exe` en Windows. Contienen todo el código, recursos y certificados necesarios para la app. Permiten instalar aplicaciones fuera de Google Play Store (sideloading)

### Referencias
https://www.decompiler.com/jar/beba6d132ddc3ff8b344b0e1b38c54a8/SafeOpener.java