## Conditionals

Conditionals in programming are structures that allow you to make decisions based on certain conditions. They help control the flow of a program by executing different blocks of code depending on whether a specified condition evaluates to true or false. In Java, two common conditional statements are the **if** statement and the **switch** statement.

### If Statement
The **if** statement is used to execute a block of code only if a specified condition is true.

Example: Checking if a Number is Even or Odd
```java
import java.util.Scanner;

public class IfStatementExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter a number: ");
        int number = scanner.nextInt();

        if (number % 2 == 0) {
            System.out.println(number + " is even.");
        } else {
            System.out.println(number + " is odd.");
        }

        scanner.close();
    }
}
```
In this example, the **if** statement checks whether the entered number is even (**number % 2 == 0**). If the condition is true, it prints a message stating that the number is even; otherwise, it prints a message stating that the number is odd.

### If-Else Else-If Statement
You can use **else if** clauses to check multiple conditions in a sequence.

Example: Determining Grade Based on Score
```java
import java.util.Scanner;

public class GradeExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter your score: ");
        int score = scanner.nextInt();

        if (score >= 90) {
            System.out.println("Grade: A");
        } else if (score >= 80) {
            System.out.println("Grade: B");
        } else if (score >= 70) {
            System.out.println("Grade: C");
        } else if (score >= 60) {
            System.out.println("Grade: D");
        } else {
            System.out.println("Grade: F");
        }

        scanner.close();
    }
}
```
In this example, the program checks the score against multiple conditions using **else if** clauses to determine the corresponding grade.

### Switch Statement
The **switch** statement is used to perform different actions based on the value of an expression.

Example: Day of the Week
```java
import java.util.Scanner;

public class SwitchStatementExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter a day number (1-7): ");
        int dayNumber = scanner.nextInt();

        String dayName;

        switch (dayNumber) {
            case 1:
                dayName = "Sunday";
                break;
            case 2:
                dayName = "Monday";
                break;
            case 3:
                dayName = "Tuesday";
                break;
            case 4:
                dayName = "Wednesday";
                break;
            case 5:
                dayName = "Thursday";
                break;
            case 6:
                dayName = "Friday";
                break;
            case 7:
                dayName = "Saturday";
                break;
            default:
                dayName = "Invalid day number";
        }

        System.out.println("Day of the week: " + dayName);

        scanner.close();
    }
}
```
In this example, the **switch** statement is used to assign the name of the day of the week based on the entered day number.

### Key Points
- Conditionals are used to make decisions in a program.
- The **if** statement is used to execute a block of code if a condition is true.
- The **else if** clause allows checking multiple conditions in sequence.
- The **switch** statement is used to perform actions based on the value of an expression.
- Conditions are evaluated as true or false, and the corresponding block of code is executed accordingly.

Understanding conditionals is crucial for writing programs that can make decisions and adapt their behavior based on different scenarios.