## Data Types

Data types are used to define the types of values that variables can hold. They specify the size and type of data that a variable can store. Let's explore some common data types in Java:

### 1. Primitive Data Types:

A. **Integer Types**:

- **int**: Represents whole numbers (integers).
```java
int age = 16;
```

- **long**: Represents larger whole numbers.
```java
long population = 7000000000L;
```

B. **Floating-Point Types**:

- **float**: Represents decimal numbers with single precision. (32 bits)
```java
float pi = 3.14f;
```

- **double**: Represents decimal numbers with double precision. (64 bits)
```java
double price = 19.99;
```

C. **char**: Represents a single character.
```java
char grade = 'A';
```

D. **boolean**: Represents a binary value, typically used for true/false conditions.
```java
boolean isStudent = true;
```

### 2. Reference Data Types:

A. **String**: Represents a sequence of characters.
```java
String greeting = "Hello, World!";
```

B. **Arrays** are collections of elements of the same data type.
```java
int[] numbers = {1, 2, 3, 4, 5};
```

C. **Classes and Objects** User-defined data types created using classes. Objects are instances of these classes.:
```java
class Person {
    String name;
    int age;
}

// Creating an object of the Person class
Person student = new Person();
student.name = "John";
student.age = 16;
```
### Full Java example

```java
public class DataTypesExample {
    public static void main(String[] args) {
        // Primitive Data Types
        int myAge = 16;
        long worldPopulation = 7000000000L;
        float piValue = 3.14f;
        double productPrice = 19.99;
        char grade = 'A';
        boolean isStudent = true;

        // Reference Data Types
        String greeting = "Hello, World!";
        
        int[] numbers = {1, 2, 3, 4, 5};

        // Creating an object of the Person class
        Person student = new Person();
        student.name = "John";
        student.age = 16;
    }
}
```

In this example, we have variables of different data types, including primitive types (**int**, **long**, **float**, **double**, **char**, **boolean**) and reference types (**String**, **int[]**, **Person**). Each data type is used for storing specific types of values, and the appropriate type must be chosen based on the nature of the data you want to work with in your program.