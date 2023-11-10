- Interface avec une seule fonction abstraite, cette fonction sera ensuite implémentée par une [[Lambda]]
- Quelques Interfaces fonctionnelles à connaître
	- `Function<T, R>` : Cette interface fonctionnelle prend un argument de type `T` et renvoie un résultat de type `R`. Elle est utilisée pour représenter une fonction qui effectue une opération sur `T` et renvoie `R`.
	- `Predicate<T>` : Cette interface fonctionnelle prend un argument de type `T` et renvoie un booléen. Elle est utilisée pour représenter une condition ou un prédicat.
	- `Consumer<T>` : Cette interface fonctionnelle prend un argument de type `T` et ne renvoie rien. Elle est utilisée pour représenter une opération qui consomme un objet de type `T`.
	- `UnaryOperator<T>` : Cette interface fonctionnelle prend un argument de type `T` et renvoie un résultat de type `T`. Elle est utilisée pour représenter une opération qui transforme un objet de type `T` en un autre objet de type `T`.
	- `Supplier<T>` : Cette interface fonctionnelle ne prend pas d'argument, mais renvoie un résultat de type `T`. Elle est utilisée pour représenter une source de données ou une valeur produite.
	- `Comparator<T>` : Cette interface fonctionnelle  prend deux arguments de type `T` et renvoie un résultat de type `int`. Cette interface est largement utilisée pour trier des collections d'objets en fonction de critères spécifiques. Elle renvoie un entier négatif si le premier objet est inférieur au second, zéro s'ils sont égaux, et un entier positif si le premier objet est supérieur au second.
		- ```java
		  //Permet d'inverser une liste
		  Comparator c = (a,b) -> -1;
		  Collections.sort(list, c);
		  ```
	-
- ```java
  /**
  * Bloque la compilation si l'interface ne respecte pas 
  * le contrat d'une interface fonctionnelle.
  **/
  @FunctionalInterface 
  interface ITest {
  
    public void test();
  
  }
  
  public class Test {
      
    public static void main(String[] args) {
  
        ITest i = () -> System.out.println("Test");
        i.test();
  
    }
  
  } 
  ```
- [[Java]]
-