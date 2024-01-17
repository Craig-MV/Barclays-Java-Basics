## Methods in Java:
Methods are pieces of reusable code that perform specific tasks. They allow you to break down a program into smaller, manageable parts. Methods are blocks of code that perform a specific task and are defined within a class. Methods are invoked by calling their name.

**Example 1: Simple Method without Parameters and Return Value**
```java
public class SimpleMethodExample {
    // A simple method without parameters that displays a value
    static void sayHello() {
        System.out.println("Hello, World!");
    }

    public static void main(String[] args) {
        // Calling the method
        sayHello();
    }
}
```

**Example 2: Method with Parameters and Return Value**
```java
public class Calculator {
    // A method that takes two parameters and returns their sum
    static int add(int num1, int num2) {
        return num1 + num2;
    }

    public static void main(String[] args) {
        // Calling the method with arguments and storing the result
        int result = add(5, 3);

        // Displaying the result
        System.out.println("Sum: " + result);
    }
}
```

**Example 3: Method Overloading**

Method overloading allows you to define multiple methods with the same name but different parameter lists.
```java
public class OverloadingExample {
    // Method with two integers
    static int add(int a, int b) {
        return a + b;
    }

    // Method with three integers
    static int add(int a, int b, int c) {
        return a + b + c;
    }

    public static void main(String[] args) {
        // Calling the overloaded methods
        System.out.println("Sum (2 numbers): " + add(5, 3));
        System.out.println("Sum (3 numbers): " + add(5, 3, 2));
    }
}
```

## Calling methods from different classes
Calling a method from a different class involves using the **dot notation**. The **dot notation** is a way to access members (**fields** or **methods**) of an **object** or **class**. It involves using the **dot (.)** operator to connect the object or class reference with the member you want to access.

Let's go through an example to illustrate how to call a method from a different class using dot notation:

**Example 1 - Method is Static**
```java
// ClassB.java
public class ClassB {
    public static void displayMessage() {
        System.out.println("Hello from ClassB!");
    }
}

```
Then, in **ClassA**, you can call it directly using the class name:
```java
// ClassA.java
public class ClassA {
    public static void main(String[] args) {
        // Calling the static displayMessage method from ClassB
        ClassB.displayMessage();
    }
}
```

**Example 2 - Method is Not Static**
If the **displayMessage** method is not static, you need to create an instance of **ClassB** and use it to call the method:
```java
// ClassB.java
public class ClassB {
    public void displayMessage() {
        System.out.println("Hello from ClassB!");
    }
}
```
```java
// ClassA.java
public class ClassA {
    public static void main(String[] args) {
        // Creating an instance of ClassB
        ClassB objectB = new ClassB();

        // Calling the displayMessage method from ClassB using an instance
        objectB.displayMessage();
    }
}
```
In this case, without the **static** keyword, you need to instantiate an object of **ClassB** before calling the **displayMessage** method.

So, depending on whether the method is static or not, the way you call it may vary.

## Methods and Functions:
People will often use the term "function" it is commonly used interchangeably with "method." Methods in Java essentially serve the same purpose as functions in other programming languages.

## Key points
- Methods/functions allow you to break down complex problems into smaller, manageable pieces of code.
- They enhance code reusability and maintainability.
- Methods can have parameters (inputs) and return values (outputs).
- Method overloading allows you to define multiple methods with the same name but different parameter lists.