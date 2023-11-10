- Le "pattern matching" (ou correspondance de motifs) est une technique de programmation qui permet de rechercher et d'extraire des parties de données structurées en fonction de modèles spécifiques. Il est souvent utilisé pour simplifier et rendre plus lisible le code lors de la manipulation de données complexes, telles que les structures de données, les chaînes de caractères, les listes, les arbres, etc.
-
- **Cas d'utilisation**
	- Un cas d'utilisation courant du pattern matching est la manipulation de structures de données complexes, telles que des arbres.
	  Par exemple, supposons que l'on ait un arbre binaire où chaque nœud peut être soit un nœud "intérieur" contenant une valeur et deux sous-arbres, soit une feuille contenant une valeur.
	  On peut utiliser le pattern matching pour parcourir cet arbre et effectuer des opérations spécifiques sur les nœuds intérieurs ou les feuilles, en fonction de leur structure.
-
- **Implémentation**
	- Java
		- ```java
		  public class MatchingPattern {
		    public static void main(String[] args) {
		        Object obj = "Hello, World";
		  
		        if (obj instanceof String str) {
		            System.out.println("C'est une chaîne de caractères : " + str);
		        } else if (obj instanceof Integer integer) {
		            System.out.println("C'est un entier : " + integer);
		        } else {
		            System.out.println("Type non géré : " + obj);
		        }
		    }
		  }
		  ```
-
- [[Traitement des données]]