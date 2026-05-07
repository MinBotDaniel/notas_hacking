### Picker IV
Can you figure out how this program works to get the flag?Connect to the program with netcat:`$ nc saturn.picoctf.net 63787`The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/528/picker-IV.c). The binary can be downloaded [here](https://artifacts.picoctf.net/c/528/picker-IV).
### Solución 1
```
┌──(kali㉿kali)-[~/Tareas]
└─$ wget https://artifacts.picoctf.net/c/528/picker-IV  
--2026-05-07 12:53:36--  https://artifacts.picoctf.net/c/528/picker-IV
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.32.104.39, 13.32.104.43, 13.32.104.54, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.32.104.39|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 17272 (17K) [application/octet-stream]
Saving to: ‘picker-IV’

picker-IV                                                           100%[=================================================================================================================================================================>]  16.87K  --.-KB/s    in 0.02s   

2026-05-07 12:53:37 (1018 KB/s) - ‘picker-IV’ saved [17272/17272]

                                                                                                                                                                                                                                                                              
┌──(kali㉿kali)-[~/Tareas]
└─$ ls  
picker-IV
                                                                                                                                                                                                                                                                              
┌──(kali㉿kali)-[~/Tareas]
└─$ nm ./ picker-IV | grep T   
nm: Warning: './' is a directory
00000000004011c0 T _dl_relocate_static_pie
0000000000401448 T _fini
0000000000404000 d _GLOBAL_OFFSET_TABLE_
0000000000401000 T _init
0000000000401440 T __libc_csu_fini
00000000004013d0 T __libc_csu_init
0000000000401334 T main
0000000000401276 T print_segf_message
0000000000401190 T _start
0000000000404080 D __TMC_END__
000000000040129e T win
                                                                                                                                                                                                                                                                              
┌──(kali㉿kali)-[~/Tareas]
└─$ nc saturn.picoctf.net 63787                       
Enter the address in hex to jump to, excluding '0x': 40129e 
You input 0x40129e
You won!
picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_14bc5444}

```

picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_14bc5444}

### Notas

