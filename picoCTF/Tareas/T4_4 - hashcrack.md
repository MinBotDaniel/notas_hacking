### hashcrack

A company stored a secret message on a server which got breached due to the admin using weakly hashed passwords. Can you gain access to the secret stored within the server?Access the server using `nc verbal-sleep.picoctf.net 51536`
### Solución 1
Nos metemos a la conexión para obtener el hash y poder sacar la contraseña, esta vez crackeando con los formatos MD5(32), SHA1(40) Y SHA256(64)

```
┌──(kali㉿kali)-[~]
└─$ echo "482c811da5d5b4bc6d497ffa98491e38" > hash.txt
                                 
┌──(kali㉿kali)-[~]
└─$ john --format=Raw-MD5 --wordlist=/usr/share/wordlists/rockyou.txt hash.txt
Using default input encoding: UTF-8
Loaded 1 password hash (Raw-MD5 [MD5 256/256 AVX2 8x3])
Warning: no OpenMP support for this hash type, consider --fork=2
Press 'q' or Ctrl-C to abort, almost any other key for status
password123      (?)     
1g 0:00:00:00 DONE (2026-04-23 23:16) 20.00g/s 30720p/s 30720c/s 30720C/s 753951..mexico1
Use the "--show --format=Raw-MD5" options to display all of the cracked passwords reliably
Session completed. 

┌──(kali㉿kali)-[~]
└─$ echo "b7a875fc1ea228b9061041b7cec4bd3c52ab3ce3" > hash.txt

┌──(kali㉿kali)-[~]
└─$ john --format=raw-sha1 --wordlist=/usr/share/wordlists/rockyou.txt hash.txt
Using default input encoding: UTF-8
Loaded 1 password hash (Raw-SHA1 [SHA1 256/256 AVX2 8x])
Warning: no OpenMP support for this hash type, consider --fork=2
Press 'q' or Ctrl-C to abort, almost any other key for status
letmein          (?)     
1g 0:00:00:00 DONE (2026-04-23 23:22) 12.50g/s 6400p/s 6400c/s 6400C/s stupid..letmein
Use the "--show --format=Raw-SHA1" options to display all of the cracked passwords reliably
Session completed.

┌──(kali㉿kali)-[~]
└─$ echo "916e8c4f79b25028c9e467f1eb8eee6d6bbdff965f9928310ad30a8d88697745" > hash.txt
                                   
┌──(kali㉿kali)-[~]
└─$ john --format=raw-sha256 --wordlist=/usr/share/wordlists/rockyou.txt hash.txt    
Using default input encoding: UTF-8
Loaded 1 password hash (Raw-SHA256 [SHA256 256/256 AVX2 8x])
Warning: poor OpenMP scalability for this hash type, consider --fork=2
Will run 2 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status
qwerty098        (?)     
1g 0:00:00:00 DONE (2026-04-23 23:23) 16.66g/s 10376Kp/s 10376Kc/s 10376KC/s sammy987..magl3181
Use the "--show --format=Raw-SHA256" options to display all of the cracked passwords reliably
Session completed. 

```

picoCTF{UseStr0nG_h@shEs_&PaSswDs!_ccc21957}


### Notas
[MD5](https://www.google.com/search?q=MD5&sca_esv=e42243e293ad428e&sxsrf=ANbL-n6Br0oadMZ9Qoj7FAsfobPUnNzXJQ%3A1777001168262&ei=0OLqacLKD5mHp84P1eSCgQ0&biw=1707&bih=817&ved=2ahUKEwj38PacxYWUAxXQHNAFHUNXCpIQgK4QegQIARAB&uact=5&oq=MD5%2C+SHA1%2C+SHA256&gs_lp=Egxnd3Mtd2l6LXNlcnAiEU1ENSwgU0hBMSwgU0hBMjU2MgUQABiABDIGEAAYFhgeMgYQABgWGB4yBhAAGBYYHjIGEAAYFhgeMgYQABgWGB4yBhAAGBYYHjIGEAAYFhgeMgYQABgWGB4yBhAAGBYYHkiLDlDJBVjVC3ABeAGQAQCYAW6gAYgEqgEDMi4zuAEDyAEA-AEBmAIGoAKfBMICChAAGLADGNYEGEfCAg4QABiwAxjkAhjWBNgBAcICFxAuGLADGLgGGNgCGMgDGNoGGNwG2AEBwgIEECMYJ8ICBRAAGO8FwgIIEAAYgAQYogTCAggQABiiBBiJBZgDAIgGAZAGDroGBggBEAEYCZIHAzIuNKAHhR6yBwMxLjS4B5oEwgcFMC40LjLIBxGACAA&sclient=gws-wiz-serp&mstk=AUtExfC3dCxNqD5bDgzHM7bKrOKNFG0JjtFHb-V9Nf-HNafOqfHNgqe9sJ55RjUlr-vMR8rCfre3us5UNym3r8fjjEd8zWLbyC1ctLGg2Qg-pZnAogpSU9fHNxW3RnhdHw6WOF8tvqOyF6lyvTY2o5oETIbqFAiZrve2KHbD2LTHW_0dGKNU0D2WhnqUIrU6w45iOtPxAK_FNRCXFwFHM_qYEkVWP-c3EJt5eD6gEPLtN779QZQ7MPjjM8uv1TnhtOnd8NSw0w-zi5HgXHgVbFPmjuCn&csui=3), [SHA1](https://www.google.com/search?q=SHA1&sca_esv=e42243e293ad428e&sxsrf=ANbL-n6Br0oadMZ9Qoj7FAsfobPUnNzXJQ%3A1777001168262&ei=0OLqacLKD5mHp84P1eSCgQ0&biw=1707&bih=817&ved=2ahUKEwj38PacxYWUAxXQHNAFHUNXCpIQgK4QegQIARAC&uact=5&oq=MD5%2C+SHA1%2C+SHA256&gs_lp=Egxnd3Mtd2l6LXNlcnAiEU1ENSwgU0hBMSwgU0hBMjU2MgUQABiABDIGEAAYFhgeMgYQABgWGB4yBhAAGBYYHjIGEAAYFhgeMgYQABgWGB4yBhAAGBYYHjIGEAAYFhgeMgYQABgWGB4yBhAAGBYYHkiLDlDJBVjVC3ABeAGQAQCYAW6gAYgEqgEDMi4zuAEDyAEA-AEBmAIGoAKfBMICChAAGLADGNYEGEfCAg4QABiwAxjkAhjWBNgBAcICFxAuGLADGLgGGNgCGMgDGNoGGNwG2AEBwgIEECMYJ8ICBRAAGO8FwgIIEAAYgAQYogTCAggQABiiBBiJBZgDAIgGAZAGDroGBggBEAEYCZIHAzIuNKAHhR6yBwMxLjS4B5oEwgcFMC40LjLIBxGACAA&sclient=gws-wiz-serp&mstk=AUtExfC3dCxNqD5bDgzHM7bKrOKNFG0JjtFHb-V9Nf-HNafOqfHNgqe9sJ55RjUlr-vMR8rCfre3us5UNym3r8fjjEd8zWLbyC1ctLGg2Qg-pZnAogpSU9fHNxW3RnhdHw6WOF8tvqOyF6lyvTY2o5oETIbqFAiZrve2KHbD2LTHW_0dGKNU0D2WhnqUIrU6w45iOtPxAK_FNRCXFwFHM_qYEkVWP-c3EJt5eD6gEPLtN779QZQ7MPjjM8uv1TnhtOnd8NSw0w-zi5HgXHgVbFPmjuCn&csui=3), and [SHA256](https://www.google.com/search?q=SHA256&sca_esv=e42243e293ad428e&sxsrf=ANbL-n6Br0oadMZ9Qoj7FAsfobPUnNzXJQ%3A1777001168262&ei=0OLqacLKD5mHp84P1eSCgQ0&biw=1707&bih=817&ved=2ahUKEwj38PacxYWUAxXQHNAFHUNXCpIQgK4QegQIARAD&uact=5&oq=MD5%2C+SHA1%2C+SHA256&gs_lp=Egxnd3Mtd2l6LXNlcnAiEU1ENSwgU0hBMSwgU0hBMjU2MgUQABiABDIGEAAYFhgeMgYQABgWGB4yBhAAGBYYHjIGEAAYFhgeMgYQABgWGB4yBhAAGBYYHjIGEAAYFhgeMgYQABgWGB4yBhAAGBYYHkiLDlDJBVjVC3ABeAGQAQCYAW6gAYgEqgEDMi4zuAEDyAEA-AEBmAIGoAKfBMICChAAGLADGNYEGEfCAg4QABiwAxjkAhjWBNgBAcICFxAuGLADGLgGGNgCGMgDGNoGGNwG2AEBwgIEECMYJ8ICBRAAGO8FwgIIEAAYgAQYogTCAggQABiiBBiJBZgDAIgGAZAGDroGBggBEAEYCZIHAzIuNKAHhR6yBwMxLjS4B5oEwgcFMC40LjLIBxGACAA&sclient=gws-wiz-serp&mstk=AUtExfC3dCxNqD5bDgzHM7bKrOKNFG0JjtFHb-V9Nf-HNafOqfHNgqe9sJ55RjUlr-vMR8rCfre3us5UNym3r8fjjEd8zWLbyC1ctLGg2Qg-pZnAogpSU9fHNxW3RnhdHw6WOF8tvqOyF6lyvTY2o5oETIbqFAiZrve2KHbD2LTHW_0dGKNU0D2WhnqUIrU6w45iOtPxAK_FNRCXFwFHM_qYEkVWP-c3EJt5eD6gEPLtN779QZQ7MPjjM8uv1TnhtOnd8NSw0w-zi5HgXHgVbFPmjuCn&csui=3) are ==cryptographic hash functions that convert input data into fixed-length, unique hexadecimal strings==. SHA256 is the modern standard for security, while MD5 (128-bit) and SHA1 (160-bit) are considered insecure, legacy algorithms vulnerable to collisions. Use SHA256 for password storage and integrity checks