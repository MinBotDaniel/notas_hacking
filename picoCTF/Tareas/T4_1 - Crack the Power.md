### Crack the Power

We received an encrypted message. The modulus is built from primes large enough that factoring them isn’t an option, at least not today. See if you can make sense of the numbers and reveal the flag.Download the [message](https://challenge-files.picoctf.net/c_amiable_citadel/03d301dd23ffd797f69f0455c954caf1ac883a876ef4c26f3e60bfac12581cbb/message.txt).
### Solución 1
Se realizó el siguiente código para obtener la bandera.

```
def integer_nth_root(n, e):
    low = 0
    high = n
    while low <= high:
        mid = (low + high) // 2
        if mid**e < n:
            low = mid + 1
        elif mid**e > n:
            high = mid - 1
        else:
            return mid
    return high

# Reemplaza con los valores de tu archivo 'message.txt'
c = 64063743081040685750056670209627408012372374820768642038157947527305937807645895825264608452210412137964776518409031003168093019478452163390659639208000653671701516776987238400389204376950106633618024600291814065796738728662875496>
e = 20 # El exponente que te da el reto

# 1. Calculamos la raíz
m = integer_nth_root(c, e)

# 2. Convertimos el número resultante a texto (bytes)
flag = bytes.fromhex(hex(m)[2:]).decode('utf-8')

print(f"La flag es: {flag}")
```

La flag es: picoCTF{t1ny_e_63ab67e3}
### Notas
**Coppersmith's attack** describes a class of [cryptographic attacks](https://en.wikipedia.org/wiki/Cryptographic_attack "Cryptographic attack") on the [public-key cryptosystem](https://en.wikipedia.org/wiki/Public-key_cryptography "Public-key cryptography") [RSA](https://en.wikipedia.org/wiki/RSA_\(algorithm\) "RSA (algorithm)") based on the [Coppersmith method](https://en.wikipedia.org/wiki/Coppersmith_method "Coppersmith method"). Particular applications of the Coppersmith method for attacking RSA include cases when the public exponent _e_ is small or when partial knowledge of a prime factor of the secret key is available.