### So Meta

Find the flag in this [picture](https://challenge-files.picoctf.net/c_fickle_tempest/010f805d3d59e58913240f26904349f886a0ee71c205d46185ada895377818af/pico_img.png).
### Solución 
Mediante el comando strings
```
┌──(kali㉿kali)-[~]
└─$ strings pico_img.png | grep pico
picoCTF{s0_m3ta_19ebefe2}

```

picoCTF{s0_m3ta_19ebefe2}
### Notas
The `strings` command in Linux is ==a utility used to **extract printable character sequences from binary files** and other non-text files==.