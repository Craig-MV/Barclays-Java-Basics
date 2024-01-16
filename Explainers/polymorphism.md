## Polymorphism

Polymorphism is an Object-Oriented Programming (OOP) principle that allows objects of different types to be treated as objects of a common type. There are two types of polymorphism: compile-time polymorphism (method overloading) and runtime polymorphism (method overriding).

Let's use a simple analogy to explain polymorphism:

Imagine you have a remote control that can operate various electronic devices like a TV, a fan, and a music player. Even though each device is different, the remote control allows you to perform common actions like turning them on or off. This flexibility in using the same remote for different devices is similar to polymorphism in programming.

Now, let's represent this concept in Java using method overriding:

```java
// Base class
class Device {
    public void turnOn() {
        System.out.println("Device is turned on");
    }

    public void turnOff() {
        System.out.println("Device is turned off");
    }
}

// Derived class 1
class TV extends Device {
    // Override the turnOn method for TV
    @Override
    public void turnOn() {
        System.out.println("TV is turned on");
    }

    // Additional methods specific to TV can be added here
}

// Derived class 2
class Fan extends Device {
    // Override the turnOff method for Fan
    @Override
    public void turnOff() {
        System.out.println("Fan is turned off");
    }

    // Additional methods specific to Fan can be added here
}
```
Explanation:

- The **Device** class is the base class with methods **turnOn()** and **turnOff()**.
- The **TV** and **Fan** classes are derived from the **Device** class and override the **turnOn()** and **turnOff()** methods, providing specific implementations for each device.
- Now, you can create instances of **TV** and **Fan** and treat them as instances of the common type Device:

```java
public class Main {
    public static void main(String[] args) {
        Device remoteControl;

        // Polymorphism - TV is treated as a Device
        remoteControl = new TV();
        remoteControl.turnOn(); // Calls the overridden method in TV

        // Polymorphism - Fan is treated as a Device
        remoteControl = new Fan();
        remoteControl.turnOff(); // Calls the overridden method in Fan
    }
}
```
In this example, polymorphism allows you to use a common interface (**Device**) to interact with different types of devices (**TV** and **Fan**). The actual method that gets executed is determined at runtime based on the type of the object, demonstrating runtime polymorphism.