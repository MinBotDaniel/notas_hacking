### Matryoshka doll

Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one?Image: [dolls.jpg](https://challenge-files.picoctf.net/c_wily_courier/e211d20af86cc82c4622e672d634045f31ec3901d7aa4714393fa9db2d9a3cd3/dolls.jpg)
### Solución 
binwalk para inspeccionar archivos.

```
┌──(kali㉿kali)-[~/problemasPICO/matryoshka/_dolls.jpg.extracted/base_images]
└─$ ls
2_c.jpg  _2_c.jpg.extracted
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/problemasPICO/matryoshka/_dolls.jpg.extracted/base_images]
└─$ cd _2_c.jpg.extracted  
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/matryoshka/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted]
└─$ ls
2DD3B.zip  base_images
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/matryoshka/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted]
└─$ cd base_images       
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└─$ ls
3_c.jpg
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└─$ binwalk -e 3_c.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
123606        0x1E2D6         Zip archive data, at least v2.0 to extract, compressed size: 77633, uncompressed size: 79786, name: base_images/4_c.jpg

WARNING: One or more files failed to extract: either no utility was found or it's unimplemented

                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└─$ ls
3_c.jpg  _3_c.jpg.extracted
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└─$ cd _3_c.jpg.extracted 
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted]
└─$ ls
1E2D6.zip  base_images
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted]
└─$ cd base_images       
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└─$ ls
4_c.jpg
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└─$ binwalk -e 4_c.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
79578         0x136DA         Zip archive data, at least v1.0 to extract, compressed size: 42, uncompressed size: 42, name: flag.txt

WARNING: One or more files failed to extract: either no utility was found or it's unimplemented

                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└─$ ls
4_c.jpg  _4_c.jpg.extracted
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└─$ cd _4_c.jpg.extracted 
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted]
└─$ ls  
136DA.zip  flag.txt
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted]
└─$ cat flag.txt            

```

picoCTF{LL9lb1dR4QbGe4l4iWCvGq9pdtwt7392}

### Notas
se usó el comando binwalk y binwalk -e



