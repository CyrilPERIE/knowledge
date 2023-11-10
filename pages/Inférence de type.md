- L'inférence de type de variables locales nous permet de demander au compilateur de déterminer ce type pour nous, plutôt que de nous obliger à le fournir explicitement. 
  Le type est déduit du contexte par le compilateur.
-
- **Implémentation**
	- Java
		- ```java
		  import java.util.*;
		  public class TypeInference {
		  public static void main(String... args) {
		        ArrayList<Integer> arr = new ArrayList<Integer>();
		        ArrayList<Integer> inference = new ArrayList<>();
		        var inference2 = new ArrayList<Integer>();
		        System.out.println(inference.getClass() == arr.getClass() & inference2.getClass() == arr.getClass()); //print: true
		        inference2.add(1); //print: true
		        nums.add("2"); //Doesn't compile
		        inference2.add(2);
		        inference2.add(3);
		        for(Integer num: inference2) System.out.print(num); //print: 123
		    }
		  }
		  ```
- [[Java]]