read me file uses markdown syntax to edit any text, formulas or codes.

# java


## understanding class and methods
```java
public class Main {

  static int sharedValue = 200;
  
  public static void main(String[] args) {
    int mainValue = 14;
    System.out.println(mainValue);
    method1();
    System.out.println(sharedValue);

  }
  
  public static void method1(){
    int firstValue = 50;
    System.out.println(firstValue);
    method2();
  
  }
  
  public static void method2(){
    int secondValue = 100;
    System.out.println(secondValue);
  }
  
}
```

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
- fridge example
  
```java

public class Main {
  public static void main(String[] args) {
    System.out.println("Let's go and check out what is in the fridge!");
    var isFridgeOpen = true;
    String result;

    if (isFridgeOpen) {
      var item1 = "Cheese";
      var item2 = "Milk";
      var item3 = "Eggs";
      result = item1 + item2 + item3;
    } else {
      result = "Fridge is closed, open the fridge";
    }

    System.out.println(result);
    // ERROR System.out.println(item1);
  }
}

```

## story using scanner

```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {

    Scanner input = new Scanner(System.in);
    System.out.println("Who are you?");
    String name = input.nextLine();
    System.out.println("Hello " + name + "!");
    System.out.println("\nWhat is your favourite colour?");
    String colour = input.nextLine();
    System.out.println("Cool! I love " + colour + " too!");
    System.out.println("\nWhat is your favourite animal?");
    String animal = input.nextLine();
    System.out.println("I think " + animal + " is a wonderful creature!");
    System.out.println("\nWhat is your favourite activity?");
    String activity = input.nextLine();
    System.out.println("Ahh, " + activity + ", lovely!");
    System.out.println("\nWhat is your favourite day?");
    String day = input.nextLine();
    System.out.println(day + "s are the best!");
    System.out.println("\nWhat is your favourite season?");
    String season = input.nextLine();
    System.out.println("Let's go, " + season + " fans!");

    System.out.println("\nLet me tell you a little story. On a calm " + season + " " + day + ","
+ name + " was walking down a path to engage in " + activity + ", when they noticed a "
+ colour + " " + animal + ". 'Oh my god,' " + name + " gasped in admiration. 'I must bring this
magical creature with me to do some " + activity + " and I will remember this beautiful " + season +
" day forever.' From here until eternity, " + name + " and their " + animal + " do everything together.");

    input.close();

  }
}
```
