- Les **Optional** sont une classe introduite dans Java 8 pour représenter de manière explicite la présence ou l'absence d'une valeur, et elles sont principalement utilisées pour éviter les problèmes liés aux valeurs nulles (`null`) dans le code.
  Elles sont particulièrement utiles dans les cas où une méthode peut retourner une valeur null, mais vous souhaitez avoir une manière plus sûre de gérer cette éventualité.
-
- ```java
  public class OptionalTest {
  
  public static Optional<String> getOptionalValue() {
    
  	Optional<String> optionalWithValue = Optional.of("String");
    Optional<String> optionalEmpty = Optional.empty();
  
    return optionalWithValue;
    
  }    
    
  public static void main(String[] args) {
    
    Optional<String> optional = getOptionalValue();
  
    // Vérification si une valeur est présente
    if (optional.isPresent()) {
        String value = optional.get();
        System.out.println("Valeur présente : " + value);
    } else {
        System.out.println("Aucune valeur présente");
    }
  
    // Utilisation d'une valeur par défaut
    String defaultValue = "Valeur par défaut";
    String value = optional.orElse(defaultValue);
  
    // Chaînage d'opérations
    String result = optional.map(String::toUpperCase)
                          .orElse("Valeur par défaut si vide");
    
  }
  
  }
  ```
- [[Java]]