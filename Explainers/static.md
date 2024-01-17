## Static
 In Java, the **static** keyword is used to declare members (**variables** and **methods**) that belong to the class itself, rather than to instances of the class. This means that static members are shared among all instances of the class, and you can access them using the class name without creating an instance.

### Static Variables
- A static variable is a variable that is associated with the class rather than with instances of the class.
- It is shared among all instances of the class.
- Declared using the static keyword.
```java
public class MyClass {
    static int staticVariable = 10;

    // Other non-static members...
}
```

### Static Methods
- A static method is a method that belongs to the class rather than to instances of the class.
- It can be called using the class name without creating an instance.
- Cannot access instance-level variables directly (non-static variables), as they are associated with instances.
```java
public class MyClass {
    static void staticMethod() {
        // Code for the static method
    }

    // Other non-static methods...
}
```

### Use cases for static
- Constants: You can declare constants as static final variables.
- Utility Methods: Methods that don't depend on instance-specific data.
- Counters or Shared Resources: Variables that need to be shared among all instances.
- Factory Methods: Methods that create and return instances of the class.

Here's an example that demonstrates the use of **static** in a class:

```java
public class StaticExample {
    static int staticVariable = 5; // Static variable

    int instanceVariable = 10; // Non-static variable

    static void staticMethod() {
        System.out.println("Static method called");
        // You can only access staticVariable directly here
        // instanceVariable is not accessible as it is not static
    }

    void instanceMethod() {
        System.out.println("Instance method called");
        // Both staticVariable and instanceVariable can be accessed here
    }

    public static void main(String[] args) {
        // Accessing static members without creating an instance
        System.out.println("Static Variable: " + StaticExample.staticVariable);
        StaticExample.staticMethod();

        // Creating an instance to access non-static members
        StaticExample instance = new StaticExample();
        System.out.println("Instance Variable: " + instance.instanceVariable);
        instance.instanceMethod();
    }
}
```
In the example, **staticVariable** and **staticMethod** are associated with the class itself, while **instanceVariable** and **instanceMethod** are specific to instances of the class. The **main** method demonstrates how to access both static and non-static members.
