### tunn3l v1s10n

We found this file. Recover the flag.[tunn3l_v1s10n](https://challenge-files.picoctf.net/c_wily_courier/626df9feed926c1e1280804f5d87fde5576e266ff250a819a5528b0471b0f3f7/tunn3l_v1s10n)
### Solución 
Si vemos én la cabecera dice que es un BM

```
┌──(kali㉿kali)-[~/problemasPICO/tunnelvision]
└─$ xxd tunn3l_v1s10n | head
00000000: 424d 8e26 2c00 0000 0000 bad0 0000 bad0  BM.&,...........
00000010: 0000 6e04 0000 3201 0000 0100 1800 0000  ..n...2.........
00000020: 0000 5826 2c00 2516 0000 2516 0000 0000  ..X&,.%...%.....
00000030: 0000 0000 0000 231a 1727 1e1b 2920 1d2a  ......#..'..) .*
00000040: 211e 261d 1a31 2825 352c 2933 2a27 382f  !.&..1(%5,)3*'8/
00000050: 2c2f 2623 332a 262d 2420 3b32 2e32 2925  ,/&#3*&-$ ;2.2)%
00000060: 3027 2333 2a26 382c 2836 2b27 392d 2b2f  0'#3*&8,(6+'9-+/
00000070: 2623 1d12 0e23 1711 2916 0e55 3d31 9776  &#...#..)..U=1.v
00000080: 668b 6652 996d 569e 7058 9e6f 549c 6f54  f.fR.mV.pX.oT.oT
00000090: ab7e 63ba 8c6d bd8a 69c8 9771 c193 71c1  .~c..m..i..q..q.
```

Con hexeditor buscamos el offset con ctl + T y ponemos  0e y ponemos 28 00 y buscamos el 0a e igual ponemos 28 00. Finalmente cambiamos el tamaño de la imagen en el offset 16 poniendo 40 04 y nos da la bandera
![[Pasted image 20260318101227.png]]

picoCTF{qu1t3_a_v13w_2020}

### Notas
Un archivo **BMP** (Bitmap o mapa de bits) es un ==formato de imagen rasterizada== desarrollado por Microsoft que almacena imágenes digitales bidimensionales sin compresión. Se caracteriza por guardar cada píxel de forma independiente, lo que mantiene una alta calidad y detalle, pero resulta en tamaños de archivo grandes.



