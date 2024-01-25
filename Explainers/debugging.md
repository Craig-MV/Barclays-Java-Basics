## Debugging

Debugging is the process of finding and fixing errors, or bugs, in a program. It involves identifying and correcting issues that cause the program to behave unexpectedly or not as intended. In Java, you can use debugging tools and techniques to analyse your code and locate errors. Let's explore the basics of debugging with examples.

**Example scenario**
Let's say you have the following Java program that is supposed to calculate and print the average of an array of numbers:
```java
public class AverageCalculator {
    public static void main(String[] args) {
        int[] numbers = {5, 10, 15, 20, 25};
        int sum = 0;

        // Calculate the sum of numbers
        for (int i = 1; i <= numbers.length; i++) {
            sum += numbers[i];
        }

        // Calculate the average
        double average = sum / numbers.length;

        // Print the result
        System.out.println("Average: " + average);
    }
}
```

**Debugging Steps:**
1. Identify the Issue:
Run the program and observe any error messages or unexpected behavior.
In this case, the program might throw an **ArrayIndexOutOfBoundsException** because the loop is attempting to access an element beyond the array's bounds.

2. Use Print Statements:
Insert print statements to display intermediate values and track the flow of the program.
Add **System.out.println()** statements at different points in your code.

```java
public class AverageCalculator {
    public static void main(String[] args) {
        int[] numbers = {5, 10, 15, 20, 25};
        int sum = 0;

        // Calculate the sum of numbers
        for (int i = 1; i <= numbers.length; i++) {
            System.out.println("Adding: " + numbers[i]); // Debugging print statement
            sum += numbers[i];
        }

        // Calculate the average
        double average = sum / numbers.length;

        // Print the result
        System.out.println("Average: " + average);
    }
}
```

3. Use a Debugger:
Most integrated development environments (IDEs) have built-in debuggers. Set breakpoints at critical points in your code to pause execution and inspect variables.

4. Fix the Issue:
Identify the root cause of the problem and make the necessary corrections.

**Corrected Code**:
```java
public class AverageCalculator {
    public static void main(String[] args) {
        int[] numbers = {5, 10, 15, 20, 25};
        int sum = 0;

        // Calculate the sum of numbers
        for (int i = 0; i < numbers.length; i++) { // Fix: Use i < numbers.length
            sum += numbers[i];
        }

        // Calculate the average
        double average = (double) sum / numbers.length; // Fix: Cast sum to double for accurate division

        // Print the result
        System.out.println("Average: " + average);
    }
}
```

**Debugging Summary**:
- Identify issues by running the program and observing behavior.
- Use print statements to display intermediate values.
- Utilise debugging tools, such as breakpoints in an IDE.
- Make corrections based on your findings.