## Date and Time

- Local Date
```java
import java.time.LocalDate;

public class LocalDateExample {
    public static void main(String[] args) {
        LocalDate today = LocalDate.now();
        System.out.println("Today's date: " + today);

        LocalDate specificDate = LocalDate.of(2024, 8, 25);
        System.out.println("Specific date: " + specificDate);
        
        // Adding days
        LocalDate nextWeek = today.plusDays(7);
        System.out.println("Next week's date: " + nextWeek);
    }
}
```
- Local Time
  
