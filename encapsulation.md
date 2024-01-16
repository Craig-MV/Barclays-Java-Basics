## Encapsulation

Encapsulation involves bundling the data (attributes) and methods (functions) that operate on the data into a single unit called a class. It also restricts access to some of the object's components, protecting the integrity of the data. Think of it like a capsule that encapsulates the internal workings of an object.

Let's use a real-world analogy to explain encapsulation:

Imagine you have a television remote control. The remote control has buttons on the outside that you can press to perform actions like changing channels or adjusting the volume. However, you don't need to know the complex electronics inside the remote; you only interact with the buttons. This separation of the internal workings from the external interface is similar to encapsulation in programming.

Now, let's represent this concept in Java:

```java
// Class representing a Television
class Television {
    // Private attributes (encapsulated)
    private int channel;
    private int volume;

    // Public methods to interact with the Television (external interface)
    public void turnOn() {
        System.out.println("Television is turned on");
    }

    public void changeChannel(int newChannel) {
        if (newChannel > 0 && newChannel <= 100) {
            this.channel = newChannel;
            System.out.println("Channel changed to " + newChannel);
        } else {
            System.out.println("Invalid channel");
        }
    }

    public void adjustVolume(int newVolume) {
        if (newVolume >= 0 && newVolume <= 100) {
            this.volume = newVolume;
            System.out.println("Volume adjusted to " + newVolume);
        } else {
            System.out.println("Invalid volume level");
        }
    }

    public void turnOff() {
        System.out.println("Television is turned off");
    }
}
```

Explanation:

- The **Television** class encapsulates the internal attributes (**channel** and **volume**) by marking them as private. This means they cannot be accessed directly from outside the class.
- Public methods (**turnOn()**, **changeChannel()**, **adjustVolume()**, **turnOff()**) provide a controlled way to interact with the Television. These methods allow you to perform actions on the Television while ensuring that the internal data is accessed and modified in a controlled manner.
- The encapsulation helps in hiding the internal details of the Television, providing a clear and well-defined interface for external use.

Now, you can use the **Television** class in another class:

```java
public class Main {
    public static void main(String[] args) {
        Television myTV = new Television();
        myTV.turnOn();
        myTV.changeChannel(5);
        myTV.adjustVolume(20);
        myTV.turnOff();
    }
}
```

In this example, the user interacts with the **Television** using its public methods, and the internal details (attributes) are encapsulated within the class. This helps in organizing the code and maintaining a clear separation between the external interface and the internal implementation.