### Information
Files can always be changed in a secret way. Can you find the flag?[cat.jpg](https://challenge-files.picoctf.net/c_wily_courier/76e95e3e6ee69b4f82b3cea25051f5a9a5918b57809a1f90b29b06b776c73bc7/cat.jpg)

### Solución

[](https://github.com/JorgeAlamillo/Fundamentos_de_la_Seguridad_de_la_Informacion/blob/master/picoCTF/Tarea-4/01-information.md#soluci%C3%B3n)

┌──(-[~/information] └─$ wget [https://challenge-files.picoctf.net/c_wily_courier/76e95e3e6ee69b4f82b3cea25051f5a9a5918b57809a1f90b29b06b776c73bc7/cat.jpg](https://challenge-files.picoctf.net/c_wily_courier/76e95e3e6ee69b4f82b3cea25051f5a9a5918b57809a1f90b29b06b776c73bc7/cat.jpg) --2026-03-23 12:16:11-- [https://challenge-files.picoctf.net/c_wily_courier/76e95e3e6ee69b4f82b3cea25051f5a9a5918b57809a1f90b29b06b776c73bc7/cat.jpg](https://challenge-files.picoctf.net/c_wily_courier/76e95e3e6ee69b4f82b3cea25051f5a9a5918b57809a1f90b29b06b776c73bc7/cat.jpg) Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.161.44.61, 3.161.44.84, 3.161.44.22, ... Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.161.44.61|:443... connected. HTTP request sent, awaiting response... 200 OK Length: 878136 (858K) [application/octet-stream] Saving to: ‘cat.jpg’

cat.jpg 100%[=================================================>] 857.55K 682KB/s in 1.3s

2026-03-23 12:16:18 (682 KB/s) - ‘cat.jpg’ saved [878136/878136]


┌──(-[~/information] └─$ echo "cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9" | base64 -d picoCTF{the_m3tadata_1s_modified}

### Notas