- Les variables "var" en Java ont été introduites dans Java 10 pour simplifier la déclaration des variables locales en inférant automatiquement leur type. Elles permettent de réduire la verbosité du code en évitant la répétition du type de données lors de la déclaration d'une variable.
-
- **Cas d'utilisation**
	- L'utilisation la plus courante des variables "var" est pour la déclaration de variables locales, telles que les variables à l'intérieur d'une méthode. Cela rend le code plus lisible en réduisant la duplication du type.
	-
- **Implémentation**
	-
	- ```Java
	  import java.util.*;
	  
	  public class Var {
	  
	  public static void main(String[] args) {
	      
	  		// Avant l'introduction de "var" (Java 9 et versions antérieures)
	        String message = "Hello, world!";
	        List<String> names = new ArrayList<String>();
	  
	        // Avec l'utilisation de "var" (Java 10+)
	        var message = "Hello, world!";
	        var names = new ArrayList<String>();
	  
	        // Déclaration d'une variable dans une boucle
	        for (var i = 0; i < 5; i++) {
	            System.out.println(i);
	        }    
	      
	    }
	  
	  }
	  ```
-
- **Évolution**
	-
	- Java 10 : Introduction de "var" pour les variables locales.
	- Java 11 : "var" a été étendu pour permettre son utilisation dans les paramètres de boucle for.
	- Java 14 : "var" peut maintenant être utilisé dans les expressions de type de données complexes, telles que les lambdas.
	- Java 16 : "var" peut être utilisé avec les expressions "instanceof".
	- Java 17 : Améliorations mineures pour une utilisation plus cohérente de "var" dans les expressions lambda et les cas avec plusieurs déclarations sur la même ligne.
	-
- [[Java]]