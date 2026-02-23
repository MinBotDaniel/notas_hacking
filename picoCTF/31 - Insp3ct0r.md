### Insp3ct0r

Kishor Balan tipped us off that the following code may need inspection:http://fickle-tempest.picoctf.net:57437
### Solución
Parte 1, clic derecho y view page source.
En un comentario dice:
<!-- Html is neat. Anyways have 1/3 of the flag: picoCTF{tru3_d3 -->
Luego en la línea: <link rel="stylesheet" type="text/css" href="[mycss.css](http://fickle-tempest.picoctf.net:57437/mycss.css)">
redirige a otro código donde hay otro comentario:
/* You need CSS to make pretty pages. Here's part 2/3 of the flag: t3ct1ve_0r_ju5t */

Despues en la línea: <script type="application/javascript" src="[myjs.js](http://fickle-tempest.picoctf.net:57437/myjs.js)"></script>
Dejaron otro comentario que dice:
/* Javascript sure is neat. Anyways part 3/3 of the flag: _lucky?302945a7} */

picoCTF{tru3_d3t3ct1ve_0r_ju5t_lucky?302945a7}
### Notas
Solo se fue enlazando la bandera
