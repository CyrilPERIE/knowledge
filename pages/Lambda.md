- Implémentation d'une interface fonctionnelle
-
- ```java
  import java.util.*;
  import java.util.function.*;
  
  public class LambdaTest {
  
    public static void main(String... args) {
      
        List<String> list = Arrays.asList("Java", "C++", "Python", "Ruby");
  Collections.sort(list, (a, b) -> a.compareTo(b));
      
      	List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8, 9, 10);
  numbers.stream()
         .filter(n -> n % 2 == 0)
         .forEach(System.out::println);
  
      
    }
  
  }
  ```
- [[Java]]