- Les `streams` sont un concept introduit dans Java 8 pour simplifier et améliorer la manipulation de collections de données, en particulier les listes, les tableaux et d'autres types de séquences. 
  Les `streams` permettent d'effectuer des opérations de manière plus expressive, concise et parallèle sur ces collections de données.
-
- **Quelques opérations intermédiaires** qui produisent un nouveau stream
	- `filter(Predicate<T> predicate)`: Cette opération intermédiaire permet de filtrer les éléments du stream en fonction d'un prédicat donné. Seuls les éléments qui satisfont la condition sont transmis au prochain stade du traitement.
	- `map(Function<T, R> mapper)`: Cette opération intermédiaire permet de transformer chaque élément du stream en un autre type d'objet en appliquant une fonction.
	- `distinct()`: Cette opération supprime les éléments en double du stream, en se basant sur leur égalité selon la méthode `equals`.
	- `sorted()`: Cette opération intermédiaire trie les éléments du stream en utilisant l'ordre naturel des éléments ou un comparateur personnalisé.
	- `limit(long maxSize)`: Cette opération intermédiaire limite le nombre d'éléments du stream aux `maxSize` premiers éléments du flux.
- **Quelques opérations terminales** qui produisent un résultat final, une valeur
	- `forEach(Consumer<T> action)`: Cette opération terminale itère sur chaque élément du stream et exécute une action donnée pour chaque élément. C'est principalement utilisé pour les effets de bord.
	- `collect(Collector<T, A, R> collector)`: Cette opération terminale permet de collecter les éléments du stream en utilisant un `Collector` personnalisé pour produire un résultat sous forme de liste, de carte, ou tout autre objet souhaité.
	- `reduce(T identity, BinaryOperator<T> accumulator)`: Cette opération terminale effectue une réduction des éléments du stream en utilisant un opérateur binaire, permettant de réaliser des opérations comme la somme, le produit, ou d'autres opérations de réduction.
	- `count()`: Cette opération terminale renvoie le nombre d'éléments dans le stream en tant que résultat final.
	- `anyMatch(Predicate<T> predicate)`: Cette opération terminale vérifie si au moins un élément du stream satisfait un prédicat donné, et renvoie un résultat booléen.
	-
- **Implémentation**
	- ```java
	  import java.util.*;
	  
	  public class StreamTest {
	  
	  	List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8, 9, 10);
	  
	    List<Integer> evenNumbers = numbers.stream()
	        .filter(n -> n % 2 == 0)
	        .collect(Collectors.toList());
	  
	  }
	  ```
- [[Java]]