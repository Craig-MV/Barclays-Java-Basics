## Iteration

Certainly! Iteration, in programming, refers to the process of repeatedly executing a block of code. It allows you to perform the same set of instructions multiple times, which is particularly useful when dealing with repetitive tasks or when working with collections of data.

There are three common types of iteration in Java: **for** loop, **while** loop and **do-while** loop.

### For Loop
The **for** loop is used when you know in advance how many times you want to repeat a block of code.

Example: Printing Numbers 1 to 5
```java
// for loop syntax
// for(start; limit; increment)
public class ForLoopExample {
    public static void main(String[] args) {
        // Using a for loop to iterate from 1 to 5
        for (int i = 1; i <= 5; i++) {
            System.out.println(i);
        }
    }
}
```
In this example, the **for** loop starts with **int i = 1**, repeats the block of code inside the loop as long as **i** is less than or equal to 5, and increments **i** by 1 in each iteration.

### While Loop
The **while** loop is used when you want to repeat a block of code as long as a certain condition is true.

Example: Printing Numbers 1 to 5 using While Loop
```java
public class WhileLoopExample {
    public static void main(String[] args) {
        int i = 1;
        
        // Using a while loop to iterate from 1 to 5
        while (i <= 5) {
            System.out.println(i);
            i++; // Incrementing i in each iteration
        }
    }
}
```
Here, the **while** loop continues to execute the code block as long as the condition **i <= 5** is true. The variable **i** is incremented in each iteration.

### Do-While Loop
The **do-while** loop is similar to the **while** loop, but it guarantees that the code inside the loop is executed at least once before checking the loop condition.

Example: Reading Input Until a Valid Number is Entered
```java
import java.util.Scanner;

public class DoWhileLoopExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int userInput;

        do {
            System.out.print("Enter a number (0 to exit): ");
            userInput = scanner.nextInt();
            System.out.println("You entered: " + userInput);
        } while (userInput != 0);

        System.out.println("Exited the loop.");
        scanner.close();
    }
}
```
In this example, the **do-while** loop will always execute at least once because the condition is checked after the code block is executed.

### Key Points
- Iteration allows you to repeat a set of instructions.
- **for** loop is used when the number of iterations is known in advance.
- **while** loop is used when the number of iterations is not known in advance.
- **do-while** loop is similar to **while** loop but guarantees at least one execution of the code block.

These loops are fundamental constructs in programming and are used extensively in various scenarios to solve different kinds of problems.