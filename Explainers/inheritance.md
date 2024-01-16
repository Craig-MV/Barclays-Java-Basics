## Inheritance

Inheritance allows a class to inherit properties and behaviors from another class. It promotes code reuse and helps create a hierarchy of classes.

Let's use a simple analogy to explain inheritance:

Imagine you have a base class called **Vehicle**. This class represents common features of all vehicles, such as having a speed and a method to move. Now, you want to create more specific types of vehicles like **Car** and **Bicycle**.

```java
// Base class
class Vehicle {
    int speed;

    // Constructor
    public Vehicle(int speed) {
        this.speed = speed;
    }

    // Method to move
    public void move() {
        System.out.println("Vehicle is moving at a speed of " + speed + " mph");
    }
}

// Derived class 1
class Car extends Vehicle {
    // Additional properties specific to Car can be added here

    // Constructor
    public Car(int speed) {
        super(speed); // Call the constructor of the base class
    }

    // Additional methods specific to Car can be added here
}

// Derived class 2
class Bicycle extends Vehicle {
    // Additional properties specific to Bicycle can be added here

    // Constructor
    public Bicycle(int speed) {
        super(speed); // Call the constructor of the base class
    }

    // Additional methods specific to Bicycle can be added here
}
```

Explanation:

- The **Vehicle** class is the base class, and it has a property **speed** and a method **move**.
- The **Car** and **Bicycle** classes are derived from the **Vehicle** class using the **extends** keyword. This means they inherit the properties and methods of the **Vehicle** class.
- The **super(speed)** in the constructors of **Car** and **Bicycle** calls the constructor of the base class **(Vehicle)** to initialize the **speed** property.
- Derived classes (**Car** and **Bicycle**) can have their own additional properties and methods in addition to those inherited from the base class.

With this setup, you can create instances of **Car** and **Bicycle** and use both the common **move** method from the base class and any additional methods specific to each derived class. This promotes code reuse and a clear organization of your code.