### Java Code Analysis
BookShelf Pico, my premium online book-reading service.I believe that my website is super secure. I challenge you to prove me wrong by reading the 'Flag' book!Here are the credentials to get you started:

- Username: "user"
- Password: "user"

Source code can be downloaded [here](https://artifacts.picoctf.net/c/482/bookshelf-pico.zip).Website can be accessed [here!](http://saturn.picoctf.net:49585/).
### Solución 
Si indagamos en el archivo dado, encontramos la clave para posteriormente edita nuestra key.
```
┌──(kali㉿kali)-[~/…/github/nandandesai/pico/security]
└─$ cat SecretGenerator.java               
package io.github.nandandesai.pico.security;

import io.github.nandandesai.pico.configs.UserDataPaths;
import io.github.nandandesai.pico.utils.FileOperation;
import org.slf4j.Logger;
import org.slf4j.LoggerFactory;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Service;

import java.io.IOException;
import java.nio.charset.Charset;

@Service
class SecretGenerator {
    private Logger logger = LoggerFactory.getLogger(SecretGenerator.class);
    private static final String SERVER_SECRET_FILENAME = "server_secret.txt";

    @Autowired
    private UserDataPaths userDataPaths;

    private String generateRandomString(int len) {
        // not so random
        return "1234";
    }

    String getServerSecret() {
        try {
            String secret = new String(FileOperation.readFile(userDataPaths.getCurrentJarPath(), SERVER_SECRET_FILENAME), Charset.defaultCharset());
            logger.info("Server secret successfully read from the filesystem. Using the same for this runtime.");
            return secret;
        }catch (IOException e){
            logger.info(SERVER_SECRET_FILENAME+" file doesn't exists or something went wrong in reading that file. Generating a new secret for the server.");
            String newSecret = generateRandomString(32);
            try {
                FileOperation.writeFile(userDataPaths.getCurrentJarPath(), SERVER_SECRET_FILENAME, newSecret.getBytes());
            } catch (IOException ex) {
                ex.printStackTrace();
            }
            logger.info("Newly generated secret is now written to the filesystem for persistence.");
            return newSecret;
        }
    }
}

```

Inspeccionamos la pagina, vamos a storage y en local storage copiamos la key que nos da y modificamos los valores en jwt.io

![[Pasted image 20260322145023.png]]
De este modo al ingresar al libro flag, ya no esta restringido y nos da la bandera.
```
Great job! Here’s your flag:picoCTF{w34k_jwt_n0t_g00d_d72df65e}                                     
```
picoCTF{w34k_jwt_n0t_g00d_d72df65e}
### Notas
Se resolvio modificando nuestro rol de usuario.
### Referencias
https://www.jwt.io/