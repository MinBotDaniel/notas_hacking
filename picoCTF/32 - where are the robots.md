### where are the robots

Can you find the robots?http://fickle-tempest.picoctf.net:56140
### Solución
Se buscó un archivo robots poniendo al final de la liga de la página un /robots.txt
Dentro había un mensaje que decía User-agent: *
Disallow: /cc6b1.html
Donde nos prohíbe ver esta parte de la página. Se borra el /robots.txt de la liga y se pone /cc6b1.html para que nos muestre la bandera.

picoCTF{ca1cu1at1ng_Mach1n3s_cc6b1}
### Notas
A `robots.txt` file is a plain text file located in a website's root directory (`example.com/robots.txt`) that instructs search engine crawlers which pages or files they can or cannot crawl.
