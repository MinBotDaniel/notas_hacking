### Safe Opener 2
What can you do with this file?I forgot the key to my safe but this [file](https://artifacts.picoctf.net/c/289/SafeOpener.class) is supposed to help me with retrieving the lost key. Can you help me unlock my safe?
### Solución 1
Usamos un decompiler online y nos da el código fuente de la clase, en el que se ve la comparación realizada.
```
    import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.Base64;

public class SafeOpener {
   public static void main(String[] args) throws IOException {
      BufferedReader keyboard = new BufferedReader(new InputStreamReader(System.in));
      Base64.Encoder encoder = Base64.getEncoder();
      String encodedkey = "";
      String key = "";

      for(int i = 0; i < 3; ++i) {
         System.out.print("Enter password for the safe: ");
         key = keyboard.readLine();
         encodedkey = encoder.encodeToString(key.getBytes());
         System.out.println(encodedkey);
         boolean isOpen = openSafe(encodedkey);
         if (isOpen) {
            break;
         }

         System.out.println("You have  " + (2 - i) + " attempt(s) left");
      }

   }

   public static boolean openSafe(String password) {
      String encodedkey = "picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_de45efd6}";
      if (password.equals(encodedkey)) {
         System.out.println("Sesame open");
         return true;
      } else {
         System.out.println("Password is incorrect\n");
         return false;
      }
   }
}          
```


picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_de45efd6}
### Notas
Descompilar es el ==proceso de ingeniería inversa que convierte código binario (ejecutable o bytecode) de vuelta a un lenguaje de alto nivel legible por humanos==, como Java, C# o Python. Se utiliza principalmente para recuperar código fuente perdido, analizar malware, mejorar la seguridad y la interoperabilidad.

### Referencias
https://www.decompiler.com/jar/beba6d132ddc3ff8b344b0e1b38c54a8/SafeOpener.java