- Les instructions `switch` en Java sont utilisées pour prendre une décision basée sur la valeur d'une expression.
  Elles permettent de choisir parmi plusieurs cas (ou branches) en fonction de la valeur de l'expression, ce qui rend le code plus lisible que l'utilisation de plusieurs instructions `if-else` imbriquées.
-
- **Implémentation**
	-
	- ```Java
	  public class SwitchDemo {
	  
	  public static void main(String[] args) {
	      
	  		int dayOfWeek = 3;
	        switch (dayOfWeek) {
	            case 1:
	                System.out.println("Lundi");
	                break;
	            case 2:
	                System.out.println("Mardi");
	                break;
	            case 3:
	                System.out.println("Mercredi");
	                break;
	            case 4:
	                System.out.println("Jeudi");
	                break;
	            case 5:
	                System.out.println("Vendredi");
	                break;
	            case 6:
	                System.out.println("Samedi");
	                break;
	            case 7:
	                System.out.println("Dimanche");
	                break;
	            default:
	                System.out.println("Jour invalide");
	        }
	      
	    }
	  
	  }
	  ```
-
- **Évolution**
	- Java 7 : Prend désormais en charge les expressions de type ``int`, `char`, `byte`, `short`, `String`, `enum` et quelques autres types primitifs. Ne prenait que `int` ou `char`.
	- Java 12 : Dans Java 12, une nouvelle fonctionnalité appelée "Switch Expressions" a été introduite en tant qu'aperçu. Elle permet d'utiliser l'instruction `switch` comme une expression, ce qui signifie que vous pouvez l'utiliser pour retourner une valeur. Cela simplifie le code et le rend plus concis.
		- ```java
		  int dayOfWeek = 3;
		  String dayName = switch (dayOfWeek) {
		    case 1 -> "Lundi";
		    case 2 -> "Mardi";
		    case 3 -> "Mercredi";
		    // ... d'autres cas ...
		    default -> "Jour invalide";
		  };
		  System.out.println(dayName);
		  ```
	-
	- Java 14 : Les "Switch Expressions" sont devenues une fonctionnalité standard de Java dans la version 14. Cela signifie que vous pouvez maintenant utiliser l'instruction `switch` comme une expression dans le code Java.
	- Java 15 : Java 15 a introduit la possibilité d'utiliser des expressions `yield` dans les "Switch Expressions" pour retourner une valeur de la branche `case`.
		- ```java
		  int dayOfWeek = 3;
		  String dayName = switch (dayOfWeek) {
		    case 1 -> "Lundi";
		    case 2 -> "Mardi";
		    case 3 -> {
		        yield "Mercredi";
		    }
		    // ... d'autres cas ...
		    default -> "Jour invalide";
		  };
		  System.out.println(dayName);
		  ```
	-
- [[Java]]