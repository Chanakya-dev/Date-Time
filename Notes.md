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
  ```java
  import java.time.LocalTime;
    public class LocalTimeExample {
    public static void main(String[] args) {
        LocalTime now = LocalTime.now();
        System.out.println("Current time: " + now);
        
        LocalTime specificTime = LocalTime.of(14, 30, 0); // 2:30 PM
        System.out.println("Specific time: " + specificTime);
        
        // Adding hours
        LocalTime nextHour = now.plusHours(1);
        System.out.println("Next hour: " + nextHour);
    }
    }    ```

- Local DateTime

  ```java
  import java.time.LocalDateTime;

    public class LocalDateTimeExample {
    public static void main(String[] args) {
        LocalDateTime now = LocalDateTime.now();
        System.out.println("Current date and time: " + now);
        
        LocalDateTime specificDateTime = LocalDateTime.of(2024, 8, 25, 14, 30);
        System.out.println("Specific date and time: " + specificDateTime);
        
        // Adding days and hours
        LocalDateTime futureDateTime = now.plusDays(5).plusHours(3);
        System.out.println("Future date and time: " + futureDateTime);
    }
    }

  ```
- ZonedDateTime
  ```java
  import java.time.ZonedDateTime;
    import java.time.ZoneId;

    public class ZonedDateTimeExample {
    public static void main(String[] args) {
        ZonedDateTime zonedNow = ZonedDateTime.now();
        System.out.println("Current date and time with zone: " + zonedNow);
        
        ZonedDateTime zonedDateTime = ZonedDateTime.of(2024, 8, 25, 14, 30, 0, 0, ZoneId.of("America/New_York"));
        System.out.println("Specific date and time in New York: " + zonedDateTime);
        
        // Changing time zone
        ZonedDateTime zonedInLondon = zonedDateTime.withZoneSameInstant(ZoneId.of("Europe/London"));
        System.out.println("Same instant in London: " + zonedInLondon);
    }
    }
    ``` 
-  Duration and Period
  ```java
import java.time.Duration;
import java.time.LocalDate;
import java.time.LocalTime;
import java.time.Period;

public class DurationPeriodExample {
    public static void main(String[] args) {
        // Duration
        LocalTime startTime = LocalTime.of(10, 0);
        LocalTime endTime = LocalTime.of(12, 30);
        Duration duration = Duration.between(startTime, endTime);
        System.out.println("Duration: " + duration.toHours() + " hours");

        // Period
        LocalDate startDate = LocalDate.of(2024, 8, 25);
        LocalDate endDate = LocalDate.of(2025, 8, 25);
        Period period = Period.between(startDate, endDate);
        System.out.println("Period: " + period.getYears() + " years, " + period.getMonths() + " months, " + period.getDays() + " days");
    }
}
```
- Date and Time Formatter

  ```java
  import java.time.LocalDate;
    import java.time.format.DateTimeFormatter;

    public class DateTimeFormatterExample {
    public static void main(String[] args) {
        DateTimeFormatter formatter = DateTimeFormatter.ofPattern("dd-MM-yyyy");
        
        // Formatting
        LocalDate date = LocalDate.now();
        String formattedDate = date.format(formatter);
        System.out.println("Formatted date: " + formattedDate);
        
        // Parsing
        LocalDate parsedDate = LocalDate.parse("25-08-2024", formatter);
        System.out.println("Parsed date: " + parsedDate);
    }
    }
    ```
 - Time Zones

   ```java
   import java.time.ZonedDateTime;
    import java.time.ZoneId;

    public class TimeZoneExample {
    public static void main(String[] args) {
        ZonedDateTime zonedDateTime = ZonedDateTime.now(ZoneId.of("Asia/Tokyo"));
        System.out.println("Current date and time in Tokyo: " + zonedDateTime);
        
        ZonedDateTime newYorkTime = zonedDateTime.withZoneSameInstant(ZoneId.of("America/New_York"));
        System.out.println("Same moment in New York: " + newYorkTime);
    }
    }
   ```
