### MacroHard WeakEdge

I've hidden a flag in this file. Can you find it?[Forensics_is_fun.pptm](https://challenge-files.picoctf.net/c_wily_courier/d78815176c19ddc85a1388233268d2f4c459fcbbaab197b4a29ebafc88294c54/Forensics_is_fun.pptm)
### Solución 
hacemos unzip del ppt 

```
┌──(kali㉿kali)-[~/problemasPICO/macrohard]
└─$ unzip Forensics_is_fun.pptm 
```

y abrimos VS code con el comando code . en la carpeta que se desea:
```
──(kali㉿kali)-[~/problemasPICO/macrohard]
└─$ code .      
               
```

Si buscamos con VS code, encontramos el archivo con la bandera.

![[Pasted image 20260318105710.png]]

ahi hay una cadena en base 64, solo de decodifica:
```
┌──(kali㉿kali)-[~/problemasPICO/macrohard]
└─$ echo 'Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q' | tr -d " " | base64 -d
flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5} 
```

picoCTF{D1d_u_kn0w_ppts_r_z1p5}
### Notas
Se usó VS code.
