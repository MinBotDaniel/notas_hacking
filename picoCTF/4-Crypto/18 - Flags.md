### Flags
What do the [flags](https://challenge-files.picoctf.net/c_fickle_tempest/214c9d918be75903d4183c35fa4b94ef60dba05fc4df37c97cf0868087067372/flag.png) mean?
### Solución
Si traducimos la secuencia de banderas nos queda:

```
Cuadro azul/blanco	P
Amarillo con círculo negro	I
Franjas azul, blanco, rojo	C
Amarillo y rojo diagonal	O
Franjas azul, blanco, rojo	C
Franjas vertical rojo, blanco, azul	T
Blanca con rombo rojo	F
Símbolo	{
Blanca con rombo rojo	F
Roja con franja amarilla	1 (Representa el 1 en este set)
Blanca y azul con muesca	A
Franjas amarillas y azules	G
Cruz azul sobre fondo amarillo	S
Blanca y azul con muesca (muesca invertida)	A
Cuadros azules y blancos	N
Franja azul sobre fondo amarillo	D
Cruz amarilla sobre fondo azul	S
Franjas vertical rojo, blanco, azul	T
Cuadros rojos y blancos	U
Blanca con rombo rojo	F
Blanca con rombo rojo	F
Símbolo
```
Encontramos la bandera

**`picoCTF{F1AG5AND5TUFF}`**
### Notas
Los certificados utilizan un estándar llamado **X.509**. A menudo, estos retos esconden información en los campos "Subject" (Sujeto), "Issuer" (Emisor) o en las extensiones personalizadas del certificado.