read me file uses markdown syntax to edit any text, formulas or codes.

# java

##  if, else if, else
```java


public class Main {
  public static void main(String[] args) {
    // System.out.println("Hello world!");
    // winter, spring, summer, autumn
    // warm jacket, t-shirt, swimming suit, raincoat
    String season = "qwerty";

    if (season == "winter") {
      System.out.println("Wear a warm jacket!");
    } else if (season == "spring") {
      System.out.println("Wear a T-shirt!");
    } else if (season == "summer") {
      System.out.println("Wear a swimming suit!");
    } else if (season == "autumn") {
      System.out.println("Wear a raincoat!");
    } else {
      System.out.println("I do not recongnize this season!");
    }

    

    // winter, spring, summer, autumn


String season = "qwerty";

    if (season == "winter") {
      System.out.println("Wear a warm jacket!");
    } else if (season == "spring") {
      System.out.println("Wear a T-shirt!");
    } else if (season == "summer") {
      System.out.println("Wear a swimming suite!");
    } else if (season == "autumn") {
      System.out.println("Wear a rain coat!");
    } else {
      System.out.println("I do not recongnize this season!");
    }

    
    // warm jacket, t-shirt, swimming suit, raincoat



    int temperature = -5;

    if (temperature < 5) {
      System.out.println("Wear a warm jacket!");
    } else if (temperature >= 5 && temperature < 15) {
      System.out.println("Wear a jacket!");
    } else if (temperature >= 15 && temperature < 30) {
      System.out.println("Wear a t-shirt!");
    } else (temperature >= 30) {
      System.out.println("Wear nothing!");
    }
   
    }

  
}
```

## logical operations

- AND logical operator - if both conditions are true
```java  
    int temp = 10;
    if (temp > 30) {
    System.out.println("It's a hot day");
     }

     else if (temp >= 20 && temp <= 30) {
     System.out.println("It's warm outside");
     }
     else {
     System.out.println("It's cold outside");
     }
```
- OR logical operator - if one of the conditions is true<
```java
    int age1 = 6;
    int age2 = 67;

    if (age1 >=10 || age2 <= 18) {
    System.out.println("You can enter the party!");
     }
     else {
    System.out.println("You can go to another party!");
     }
```
  
- NOT - the opposite of the condition
```java
    int a = 4;
    int b = 6;
    boolean c = !(a < b);

    System.out.println(c);
```
