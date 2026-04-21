### b00tl3gRSA2
In RSA d is a lot bigger than e, why don't we use d to encrypt instead of e?
Connect with nc fickle-tempest.picoctf.net 57593.
### Solución
Vemos que N es muy chico por lo que se factoriza
```
┌──(kali㉿kali)-[~/PICOCTF/mindpsqs]
└─$ cat values            
Decrypt my super sick RSA:
c: 15341890103764929939105506004034128738090325640037083301857608662849501626260517
n: 948406957756830799684818171639547165784816468744946013083947881743680617123566349
e: 65537
```
https://factordb.com/index.php?query=948406957756830799684818171639547165784816468744946013083947881743680617123566349
del que sacamos p y q para implementar el siguiente código:
```
>>> from Crypto.Util.number import long_to_bytes
>>> from Crypto.Util.number import inverse
>>> c = 15341890103764929939105506004034128738090325640037083301857608662849501626260517
>>> e = 65537
>>> p = 1891771437429478964908181306574287207137
>>> q = 501332739776173570344039681219489434626477
>>> n = p * q
>>> tn = (p -1) * (q-1)
>>> d = inverse(e,tn)
>>> m = pow(c, d, n)
>>> long_to_bytes(m)
b'\n}19ea7cd1_do0g_0n_N_11ams{FTCocip'
```
dándonos la bandera:
picoCTF{sma11_N_n0_g0od_1dc7ae91}

### Notas


