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

## arrays

- borders with a definite size

```java
/*
1. Create a program, where user can provide a title and a small text below the title.
Title should be wrapped with ====== at top and bottom, based on the title length.
Example: 
System asks for title and user provides "WoTech and Java is easy"
System asks for description and user provides "I have been learning Java for 6 weeks now."

Result: 
=======================
WoTech and Java is easy
=======================

I have been learning Java for 6 weeks now.
*/

/*
1. Create a program, where user can provide a title and a small text below the title.
Title should be wrapped with ====== at top and bottom, based on the title length.
Example: 
System asks for title and user provides "WoTech and Java is easy"
System asks for description and user provides "I have been learning Java for 6 weeks now."

Result: 
=======================
WoTech and Java is easy
=======================

I have been learning Java for 6 weeks now.
*/

import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
    Scanner input = new Scanner(System.in);
    System.out.println("Enter title: ");
    String title = input.nextLine();
    System.out.println("Enter description: ");
    String description = input.nextLine();
    int length = title.length();

    System.out.println("\n\n");
    printBorder(title);
    System.out.println(title);
    printBorder(title);
    System.out.println("\n");
    System.out.println(description);
  }

  public static void printBorder(String text) {
     int length = text.length();
    for (int i = 0; i < length; i++) {
      System.out.print("=");
    }
    System.out.println();
  

  }

}
```
## for loops

```java



import java.util.Random;
import java.util.Scanner;



public class Main {
  public static void main(String[] args) {

    /*

    Fill the array with random numbers

    Find the sum of all elements in the array.
    For example in an array like this:
    [2, 3, 5, 1]
    Result: 11 (2 + 3 + 5 + 1)
    
      */ 
    
    int[] arr = new int[10];
    int sum = 0;
    

    Random randomNumber = new Random();
System.out.println("Random numbers: ");
    for (int i = 0; i < arr.length; i++) {
      arr[i] = randomNumber.nextInt(-50,50);
      sum = sum + arr[i];
      System.out.println(arr[i]);
      

    }
   
    
    System.out.println("The sum of random numbers: " + sum);

    /* Find all the elements in the array that is below 0
      [-2, 3, -5, 1]
      Result:
      -2
      -5

*/ 
    System.out.println("Negative numbers: ");
    
    for (int i = 0; i < arr.length; i++) {
      if (arr[i] < 0) {
        System.out.println(arr[i]);
      }
      
    }

/*
    Fill the party list with people you would like to invite to the party.
    Check whether or not "Anna" is in the array.
    Check whether or not "Maris" is in the array.
    ["Oskars", "Anna", "Andris"]
    Result: 
    "Anna is in the party list"
    "Maris is not in the party list"
      */
    Scanner input = new Scanner(System.in);
    String[] partyList = {"Oskars", "Anna", "Andris"};
    boolean isInPartyList = false;

    System.out.println("Enter a name: ");
    String inputName = input.nextLine();

    for (String name : partyList) {
      if (name.equals(inputName)) {
        isInPartyList = true; 
        break;
      }
    }
    if (isInPartyList) {
      System.out.println(inputName + " is in the party list");
    }
    else {
        System.out.println(inputName + " is not in the party list"); }  
    
    
  }


}

```

## methods

```java


public class Main {
  public static void main(String[] args) {
    int number = 51;

    checkNumber(number);

    int number2 = 49;

    checkNumber(number2);
    }

  // void is just for action
  // int is for returning a number
  // String is for returning a string
  // double is for returning a double
  // boolean is for returning a boolean
  // good practice is to use return type and use systemoutprintln only in the main method
  public static void checkNumber (int value) {
    if(value > 50) {
      System.out.println("The number is greater than 50");
    } else if (value < 50) {
      System.out.println("The number is less than 50");
    } else {
      System.out.println("The number is equal to 50");
      }
  }
}

```

```java

public class Main {
  public static void main(String[] args) {
    int number1 = 7;
    int number2 = 12;
    int number3 = 18;

    int result = sum(number1, number2);
    int finalResult = sum(result, number3);

    System.out.println(finalResult);
    
  }
public static int sum(int a, int b) {
  return a + b;
}
  
}

```
# get numbers + methods

```java


import java.util.Scanner;
public class Main {
  public static void main(String[] args) {
    /*
    1. Create a function that returns smallest number of 2 numbers.

    For example:
    User provides 5
    User provides 7

    Function returns 5
    Main function prints out:
    5 is the smallest number
      */
    Scanner input = new Scanner(System.in);
    System.out.println("Enter a number: ");
    int number1 = getNumber();
    System.out.println("Enter another number: ");
    int number2 = getNumber();
    int result = smallestNumber(number1, number2);
    System.out.println("The smallest number is " + result);

    smallestNumber(number1, number2);
    
    }
    public static int getNumber() {
  Scanner input = new Scanner(System.in);
  int number = input.nextInt();
  return number;

}
    public static int smallestNumber(int a, int b) {
      if (a < b) {
        return a;
      }
      else {
        return b;
      }
  }

  
}

```

```java

import java.util.Scanner;

public class Main {
  public static void main(String[] args) {

    
Scanner input = new Scanner(System.in);
    System.out.println("Enter number: ");
    int num1 = getNumber();
    System.out.println("Enter number: ");
    int num2 = getNumber();
    System.out.println("Enter number: ");
    int num3 = getNumber();
    int result = multiply(num1, num2, num3);

    System.out.println(num1 + " * " + num2 + " * " + num3 + " = " + result);
  }


  public static int getNumber() {
Scanner input = new Scanner(System.in);
    int num = input.nextInt();
    return num;

    
   }

  public static int multiply(int num1, int num2, int num3) {
    int sum = num1 * num2 * num3;
    return sum;
  }

}

```

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


# function of calling a name using methods

```java

import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
    /*
    3. Create a function that returns a combination of first name and last name
    User provides "Oskars"
    User provides "Klaumanis"

    Function receives both of the names and returns "Oskars Klaumanis"
    Main function prints out the result
      */
  Scanner input = new Scanner(System.in);
    System.out.println("Enter your first name: ");
    String firstName = getName();
   System.out.println("Enter your surname: ");
    String surName = getName();

    String result = namesCombined(firstName, surName);
    System.out.println("Your name is " + result);
  }
  
  public static String getName() {
Scanner input = new Scanner (System.in);
    String name = input.nextLine();
      
      return name;
    
  }
public static String namesCombined(String firstName, String surName) {
  return firstName + " " + surName;
}

}

```

## rock, paper, scissors

```java

import java.util.Scanner;
import java.util.Random;

public class Main {
  public static void main(String[] args) {
    
  
  Scanner input = new Scanner(System.in);
  System.out.println("Let's play Rock, Paper, Scissors!");
  System.out.println("Enter your choice (rock, paper, scissors): ");
 
  String playerChoice = getPlayerChoice();
  System.out.println("You chose: " + playerChoice);



  String computerChoice = getComputerChoice();
  System.out.println("Computer chose: " + computerChoice);

  String result = getResult(playerChoice, computerChoice);
  System.out.print(result);

  

    }
  
public static String getPlayerChoice () {
  Scanner input = new Scanner(System.in);
  String playerChoice = input.nextLine().toLowerCase();
  return playerChoice;


}

public static String getComputerChoice () {
String[] choices = {"rock", "paper", "scissors"};
  Random compRandom = new Random();
  int randomIndex = compRandom.nextInt(choices.length);
  return choices[randomIndex];
  
}

public static String getResult (String playerChoice, String computerChoice) {
  
if (playerChoice.equals(computerChoice)) {
  return "It's a tie!";
}
  else if ((playerChoice.equals("rock") && computerChoice.equals("scissors")) || (playerChoice.equals("paper") && computerChoice.equals("rock")) || (playerChoice.equals("scissors") && computerChoice.equals("paper"))) {
    return "You win!";
    }
  else {
    return "Computer wins!";
  }
  
  }
}
```

## arrays

```java

import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in); //

    int[] arr = new int[5]; // Bounds is from 0 to 4
    // We ask the computer to create a closet
    //Where we could put 5 different boxes of a number
    arr[0] = 5;
    arr[1] = 8;
    arr[2] = 13;
    arr[3] = 54;
    arr[4] = 80;
    // arr[5] Index out of bounds

    for (int i = 0; i < arr.length; i++) { // 0 ... 1 -> 4
      //int number = scanner.nextInt();
      //arr[5] = scanner.nextInt();
      arr[i] = i; // We are overwriting the value of array with i (0, 1, 2, 3, 4)

    }

    for (int i = 0; i < arr.length; i++) { // 0 -> 4
      System.out.println(arr[i]); // We are accessing arr[3]
    }

    scanner.close();//
  }
}

```

## arrays, cities

```java

import java.util.Scanner;

public class Main {
  public static void main(String[] args) {

    String[] cities = new String[5];

    Scanner input = new Scanner(System.in);
    System.out.println("Enter 5 cities: ");

    for (int i = 0; i < cities.length; i++) {
      System.out.println("City " + (i + 1) + ": ");
      cities[i] = input.nextLine();
    }

  System.out.println("Cities entered: ");

    for (int i = 0; i < cities.length; i++) {
      System.out.println(cities[i]);
    }

      input.close();
    
  }


}

```

```java

import java.util.Scanner; 

public class Main {
  public static void main(String[] args) {
    
    Scanner input = new Scanner(System.in);
    int[] numbers = new int[5];
    
    System.out.println("Enter 5 numbers:");
    for (int i = 0; i < numbers.length; i++) { 
      numbers[i] = input.nextInt();
    }


    int largestNumber = numbers[0];
    for (int i = 0; i < numbers.length; i++) {
      if (numbers[i] > largestNumber) {
        largestNumber = numbers[i];
      }
    }
    System.out.println("The largest number is " + largestNumber);

    int smallestNumber = numbers[0];
    for (int i = 0; i < numbers.length; i++) {
      if (numbers[i] < smallestNumber) {
        smallestNumber = numbers[i];
      }
    }
    System.out.println("The smallest number is " + smallestNumber);

    input.close();
  }
}

```

## for loops

```java

import java.util.Scanner;

public class Main {
  public static void main(String[] args) {

    int[] numbers = { 1, 3, 4, 2, 5, 8 }; // numbers.length = size of the numbers = 6

    System.out.println("Please write your favourite number: ");

    Scanner input = new Scanner(System.in);
    int favouriteNumber = input.nextInt();

    boolean isFound = false;

    for (int i = 0; i < numbers.length; i++) {

      if (numbers[i] == favouriteNumber) {
        isFound = true;
        break; //EXITS THE FOR LOOP ALTOGETHER, ignoring the i < numbers.length
      }

    }
    if(isFound){
      System.out.println("Your favourite number " + favouriteNumber + " is in the array");
    } else {
      System.out.println("Your favourite number " + favouriteNumber + " is NOT FOUND!");
    }

    input.close();
  }
}

```


## arrays, for loops

```java



public class Main {
  public static void main(String[] args) {
    
    /* 
    1. Go through the array - for loop
    2. Find a number less than our number - if
    3. Increment index by 1
    4. Return index
    5. If we can't find the number that is less than our number, return total count +1

    */

    int[] arr = {8, 7, 5, 3, 2, 1}; // current race results
    int number = 1; // hardcoded number = our result
    int place = getThePlace(arr, number);
    System.out.println("Our place in the race is " + place);
  
  } 

  public static int getThePlace(int[] arr, int number) {
    for (int i = 0; i < arr.length; i++) {
      if (arr[i] < number) {
        return i + 1; // return index + 1
      }
    }
    return arr.length + 1; //return total count + 1 
    }
  
}

```

## prime numbers

```java


   /*
1. Go through the numbers from 2 to (numer -1)
2. check whether or ot it is dividable (number % i == 0)
3. if the 2nd point is true, then it is a prime number
4. if the 2nd point is false then it is not a prime number
5. print the result
    */
    public class Main {
        public static void main(String[] args) {
            for(int i = 0; i < 100; i++){
                boolean isAPrimeNumber = isPrime(i);
                System.out.println(i + " is a prime number - " + isAPrimeNumber);
            }
        }

        public static boolean isPrime(int number){
            for(int i = 2; i < number; i++){
                if(number % i == 0){
                    return false;
                }
            }
            return true;
        }
    }

```
## 2D arrays

```java

public class Main {
    public static void main(String[] args) {
        int[][] array = new int[5][5];
     int counter = 1;
        for (int i = 0; i < array.length; i++) {
            
            for (int j = 0; j < array[i].length; j++) {
                array[i][j] = counter;
                counter++;
            }
          
        }

      for(int i = 0; i < array.length; i++){
          for(int j = 0; j < array[i].length; j++){
              if(array[i][j] < 10){
                  System.out.print(array[i][j] + "  ");
              }
              else{
                  System.out.print(array[i][j] + " ");
              }
          }
          System.out.println();
      }
        
    }
}

```

```java



public class Main {
  public static void main(String[] args) {
  
    int[][] array = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
    };

    for(int i = 0; i < array.length; i++){
        //array[0] = {1, 2, 3}
        //array[0].length = 3
        int[] row = array[i]; // {1, 2, 3} OR {4, 5, 6} OR, {7, 8, 9}
        for(int j = 0; j < row.length; j++){
            System.out.print(row[j]);
        }



    }  
  }


}

```

```java

public class Main {
    public static void main(String[] args) {
        int[][] array = new int[5][5];

        for (int i = 0; i < array.length; i++) {
            int[] row = array[i];
            for (int j = 0; j < row.length; j++) {
                row[j] = i;
            }
        }

        for(int i = 0; i < array.length; i++){
            for(int j = 0; j < array[i].length; j++){
                System.out.print(array[i][j] + "|");
            }
            System.out.println();
            System.out.println("----------");
        }
    }
}

```

```java

public class Main {
    public static void main(String[] args) {
        int[][] array = new int[10][10];

        for (int i = 0; i < array.length; i++) {
            int[] row = array[i];
            for (int j = 0; j < row.length; j++) {
                row[j] = i*j;
            }
        }

        for(int i = 0; i < array.length; i++){
            for(int j = 0; j < array[i].length; j++){
                if(array[i][j] < 10){
                    System.out.print(array[i][j] + "  ");
                }
                else{
                    System.out.print(array[i][j] + " ");
                }
            }
            System.out.println();
        }
    }
}

```


# 3 x 3 grid 2D array

```java

import java.util.Random;

public class Main {
  public static void main(String[] args) {
int[][] grid = new int[3][3];
    Random randomNumber = new Random();
    int randomIndex = randomNumber.nextInt(grid.length);

    for (int i = 0; i < grid.length; i++) {
      for (int j = 0; j < grid[i].length; j++) {
        grid[i][j] = randomNumber.nextInt(9) + 1;
      } 
      
    }
    
    for(int i = 0; i < grid.length; i++){
        for(int j = 0; j < grid[i].length; j++){
            if(grid[i][j] < 10){
                System.out.print(grid[i][j] + "  ");
            }
            else{
                System.out.print(grid[i][j] + " ");
            }
        }
        System.out.println();
    }
  }
}

```

# 2D array - bombing of ships game

```java

public class Main {
    public static void main(String[] args) { // Main method
        int size = 10;
        int[][] grid = new int[size][size];
        int bombColumn = 1;
        int bombRow = 0;
        // 1 1 1 0 0 0 0 0 0 0
        // 1 5 1 0 0 0 0 0 0 0
        // 1 1 1 0 0 0 0 0 0 0
        // 0 0 0 0 0 0 0 0 0 0
        // .... times 10

        grid[bombRow][bombColumn] = 5; // Center
        if(bombRow != 0) {
            grid[bombRow - 1][bombColumn] = 1; // Top middle
            grid[bombRow - 1][bombColumn - 1] = 1; // top left
            grid[bombRow - 1][bombColumn + 1] = 1; // top right
        }
      if(bombRow != size - 1){
        grid[bombRow + 1][bombColumn] = 1; // bottom middle
        grid[bombRow + 1][bombColumn - 1] = 1; //bottom left
        grid[bombRow + 1][bombColumn + 1] = 1; //bottom right
        }
        grid[bombRow + 1][bombColumn] = 1; // bottom middle
        grid[bombRow + 1][bombColumn - 1] = 1; //bottom left
        grid[bombRow + 1][bombColumn + 1] = 1; //bottom right

        grid[bombRow][bombColumn - 1] = 1; // middle left
        grid[bombRow][bombColumn + 1] = 1; //middle right


        printArray(grid, size);
    }

    public static void printArray(int[][] array, int size) {
        for (int i = 0; i < size; i++) {
            for (int j = 0; j < size; j++) {
                System.out.print(array[i][j] + " ");
            }
            System.out.println();
        }
    }
}

```

## triangle

```java

    import java.util.Scanner;

    public class Main {
        public static void main(String[] args) {
            Scanner scanner = new Scanner(System.in);
            System.out.print("Enter the number of lines for the triangle: ");
            int lines = scanner.nextInt();

            for (int i = 1; i <= lines; i++ {
                for (int j = 1; j <= i; j++) {
                    System.out.print("_");
                }
                System.out.println(); // Move to the next line after printing each line
            }
            scanner.close();
        }
    }

```

## guess the number 

```java

import java.util.Scanner;




public class Main {
  public static void main(String[] args) {

    Scanner input = new Scanner(System.in);
    int guess;
    int answer = 44;

    boolean correctGuess = true;

    
  while (correctGuess) {
    System.out.println("Guess a number between 1 and 100: ");
    guess = input.nextInt();
  if (guess < answer) {
      System.out.println("Too low! Try again.");
  } else if (guess > answer) {
      System.out.println("Too high! Try again.");
  } else {
      System.out.println("Congratulations! You've guessed the number!");
  break;
  }
    }
  
  }


}
```
## borders 

```java

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter the text: ");
        String text = scanner.nextLine();

        int length = text.length();
        int maxLength = length + 8;

        // Print the top border
        printBorder(maxLength);

        // Print the text with side borders
        System.out.println("|   " + text + "   |");

        // Print the bottom border
        printBorder(maxLength);
    }

    public static void printBorder(int length) {
        System.out.print("=");
        for (int i = 0; i < length - 2; i++) {
            System.out.print("=");
        }
        System.out.println("=");
    }
}

```

```java

public class Main {
  public static void main(String[] args) {
    printOutABorder();
    System.out.println("Hello, you!");
    int number = getARandomNumber();
    System.out.println(number);

    int number1 = 5;
    int number2 = 7;
    int result = sum(number1, number2);
      System.out.println(result);
    printOutABorder();

  }

  public static void printOutABorder() {
    System.out.println("===========");
  }

  public static int getARandomNumber() {
    return 5;
  }
  public static int sum(int number1, int number2) {
    return number1 + number2;
  }
}

```

## boolean methods callback

```java

/*
Write a name and check whether or not it is atleast 3 char long
Write a surname and check whether or not it is atleast 3 char long
If it's not, then say. Sorry, your name is too short.
If both of them are valid, say. Thank you, your information has been registered!
  */

public class Main {
  public static void main(String[] args) {
    String name = "Oskars";
    String surname = "Klaumanis";
    boolean isUserNameValid = isNameValid(name);
    boolean isUserSurnameValid = isNameValid(surname);

    if(isUserNameValid && isUserSurnameValid) {
      System.out.println("Thank you, your information has been registered!");
    } else {
      System.out.println("Sorry, check your information.");
    }
  }

public static boolean isNameValid(String nameValue) {
  if(nameValue.length() < 3) {
    System.out.println("Sorry, your name is too short.");
      return false;
  }
  return true;
}
}

```

## collections

```java

import java.util.ArrayList;
import java.util.stream.Collectors;
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
    ArrayList<String> shopItems = new ArrayList<String>();

    shopItems.add("Glass Table");
    shopItems.add("Wooden Table");
    shopItems.add("Round Table");
    shopItems.add("Doors");
    shopItems.add("Trapdoor");
    shopItems.add("Couch");
    shopItems.add("Bed");
    shopItems.add("Sofa");



    
    shopItems
      .stream() //in between stream and collect, can do actions
      .filter(item -> item.contains("Table"))
      // .skip(3) // can skip first 3 items
      // .limit(2) // taking only the remaining first two items
      .forEach(item -> print("TEST " + item));
      

    
    
  }

  public static void print(String text) {
    System.out.println();
    System.out.println(text);
  }

}

```

## arraylists

```java

import java.util.ArrayList;
import java.util.stream.Collectors; 
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
// initialising arraylist
    ArrayList<String> shopItems = new ArrayList<String>();

    Scanner input = new Scanner(System.in);

   

    while (true) {
      System.out.println("Enter item to the store: ");
      String item = input.nextLine();

      if(item.equals("exit")) {
        break;
      }
      
      addItems(shopItems, item);

      }

    printArrayList(shopItems);
    System.out.println("Enter items to remove: ");
    String itemToRemove = input.nextLine();

    shopItems.removeIf(item -> item.equals(itemToRemove));

    printArrayList(shopItems);

    ArrayList<String> filteredArrayList = new ArrayList<String>();

    for (String item: shopItems) {
      if(item.length() <= 5){
        filteredArrayList.add(item);
      }

    printArrayList(filteredArrayList);
      
    }
    
    
    // initialise arraylist
    // create an element in the arraylist
    // remove an element
    // get the elements
    
  }

  public static void printArrayList(ArrayList<String> items) {
    clearConsole();
    System.out.println("Items in the store: ");
    for (String item : items)
      {System.out.println(item);
        }
  }

  public static void addItems(ArrayList<String> shopItems, String item) {
    clearConsole();
    shopItems.add(item);
    System.out.println(item + " has been added to the store.");
  }

  public static void clearConsole(){
      System.out.print("\033[H\033[2J");
      System.out.flush();
  }
  
}

```

## arraylist homework 22052024

```java

/*Easy: Create an arrayList for integers
Add 5 numbers.

Filter the arrayList and print out only numbers that divide by 2 
(number % 2 == 0)


  */

import java.util.ArrayList;
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {

    ArrayList<Integer> numbers = new ArrayList<Integer>();
    ArrayList<Integer> filteredNumbers = new ArrayList<Integer>();
    Scanner input = new Scanner(System.in);

    for (int i = 0; i < 5; i++) {
        System.out.println("Enter a number: ");
        int number = input.nextInt();
        addNumbers(numbers, number);
    }

    System.out.println(numbers);

    for (int number : numbers) {
      if (number % 2 == 0) {
      filteredNumbers.add(number);
      }
    }

  System.out.println(filteredNumbers);
    
    
  }

  public static void addNumbers(ArrayList<Integer> numbers, int number) {
    numbers.add(number);
  }
}

```

## book application
Main.Java:
```java

import java.util.ArrayList;
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {

    Scanner input = new Scanner(System.in);
    ArrayList<Book> books = new ArrayList<Book>();
   
    
    System.out.println("Welcome to the book management app!");
    
    
    while (true) {
      
      System.out.println();
      System.out.println("What would you like to do?");
      System.out.println("1. Add a book");
      System.out.println("2. Remove a book");
      System.out.println("3. View your books");
      System.out.println("4. Exit");
      System.out.println("Please choose a number from 1 to 4.");
      System.out.println();

      int userChoice = input.nextInt();
      input.nextLine();

      
      if (userChoice == 1) {
        addBook(books);
        
      }
      else if (userChoice == 2) {
        removeBook(books);
        
      }
      else if (userChoice == 3) {
        viewBooks(books);
        
      }
      else if (userChoice == 4) {
        System.out.println("Thank you for using the book management app!");
        break;
      }
      else {
        System.out.println("Invalid input. Please choose a number from 1 to 4.");
      }
    } 
  

  }
  public static void addBook(ArrayList<Book> books) {
    Scanner addBook = new Scanner(System.in);
    System.out.println("Enter the title of the book: ");
    
    String title = addBook.nextLine();
    System.out.println("Enter the author of the book: ");
    String author = addBook.nextLine();
    System.out.println("Enter the year the book was published: ");
    int year = addBook.nextInt();
    

    Book book = new Book(title, author, year);
    books.add(book);
    System.out.println();
    System.out.println("The book has been added to your library.");
  }

  public static void removeBook(ArrayList<Book> books) {
  Scanner removeBook = new Scanner(System.in);
  System.out.println("Enter the title of the book you would like to remove: ");
  String removeTitle = removeBook.nextLine();

if (books.removeIf(book -> book.getTitle().equalsIgnoreCase(removeTitle))) {
  System.out.println();
  System.out.println("The book has been removed from your library."); }

else {
  System.out.println();
  System.out.println("This book is not in your library. Try again.");
}
    }

  public static void viewBooks(ArrayList<Book> books) {
    System.out.println("Your books: ");
   for (Book book : books) {
     System.out.println(book.showBooks());
   } 
  }


}

```
Book.Java:
```java
public class Book{
  public String title;
  public String author;
  public int year;


  public Book(String title, String author, int year) {
    this.title = title;
    this.author = author;
    this.year = year;
  }

  public String getTitle() {
    return title;
  }

  public String getAuthor() {
    return author;
  }

  public int getYear() {
    return year;
  }

  public String showBooks() {
    return title + " by " + author + " (" + year + ")";
  }
  
}
```
