## Data Structures
A data structure is a way of organising and storing data so that it can be efficiently used and manipulated. Think of data structures as containers that hold data and provide methods for interacting with that data. Java provides various built-in data structures that help programmers manage and organise data effectively. Here are some fundamental data structures in Java:

### Array
An **array** is a collection of elements of the same type, stored in contiguous memory locations.

Example: Declaration and Initialization of an Array
```java
public class ArrayExample {
    public static void main(String[] args) {
        // Declaration and initialization of an integer array
        int[] numbers = {1, 2, 3, 4, 5};

        // Accessing elements of the array
        System.out.println("Element at index 2: " + numbers[2]);
    }
}
```

### ArrayList
An **ArrayList** is a dynamic array that can grow or shrink in size.

Example: Using ArrayList to Store Strings
```java
import java.util.ArrayList;

public class ArrayListExample {
    public static void main(String[] args) {
        // Creating an ArrayList of Strings
        ArrayList<String> names = new ArrayList<>();

        // Adding elements to the ArrayList
        names.add("Alice");
        names.add("Bob");
        names.add("Charlie");

        // Accessing elements of the ArrayList
        System.out.println("Element at index 1: " + names.get(1));
    }
}
```

### LinkedList
A **LinkedList** is a collection of elements where each element points to the next element in the list.

Example: Using LinkedList to Store Integers
```java
import java.util.LinkedList;

public class LinkedListExample {
    public static void main(String[] args) {
        // Creating a LinkedList of Integers
        LinkedList<Integer> numbers = new LinkedList<>();

        // Adding elements to the LinkedList
        numbers.add(10);
        numbers.add(20);
        numbers.add(30);

        // Accessing elements of the LinkedList
        System.out.println("First element: " + numbers.getFirst());
    }
}
```

### HashMap
A **HashMap** is a collection of key-value pairs, where each key is unique.

Example: Using HashMap to Store Student Grades
```java
import java.util.HashMap;

public class HashMapExample {
    public static void main(String[] args) {
        // Creating a HashMap to store student grades
        HashMap<String, Integer> studentGrades = new HashMap<>();

        // Adding key-value pairs to the HashMap
        studentGrades.put("Alice", 85);
        studentGrades.put("Bob", 92);
        studentGrades.put("Charlie", 78);

        // Accessing values using keys
        System.out.println("Bob's grade: " + studentGrades.get("Bob"));
    }
}
```

### Stack
A **Stack** is a Last In, First Out (LIFO) data structure where elements are added and removed from the same end.

Example: Using Stack to Reverse a String
```java
import java.util.Stack;

public class StackExample {
    public static void main(String[] args) {
        // Creating a Stack of Characters
        Stack<Character> charStack = new Stack<>();

        // Pushing characters onto the stack
        String input = "Java";
        for (char c : input.toCharArray()) {
            charStack.push(c);
        }

        // Popping characters from the stack to reverse the string
        StringBuilder reversedString = new StringBuilder();
        while (!charStack.isEmpty()) {
            reversedString.append(charStack.pop());
        }

        System.out.println("Reversed String: " + reversedString.toString());
    }
}
```

### Queue
A **Queue** is a First In, First Out (FIFO) data structure where elements are added at the rear and removed from the front.

Example: Using Queue to Implement a Simple Task Queue
```java
import java.util.LinkedList;
import java.util.Queue;

public class QueueExample {
    public static void main(String[] args) {
        // Creating a Queue of Tasks (Strings)
        Queue<String> taskQueue = new LinkedList<>();

        // Enqueuing tasks
        taskQueue.add("Task 1");
        taskQueue.add("Task 2");
        taskQueue.add("Task 3");

        // Dequeuing tasks
        while (!taskQueue.isEmpty()) {
            System.out.println("Processing: " + taskQueue.poll());
        }
    }
}
```

### Set
A **Set** is a collection that does not allow duplicate elements. It models the mathematical set abstraction and is useful when you need to ensure that each element is unique. In Java, there are several implementations of the **Set** interface, such as **HashSet**, **LinkedHashSet**, and **TreeSet**. 

Here's an example using HashSet:
```java
import java.util.HashSet;
import java.util.Set;

public class SetExample {
    public static void main(String[] args) {
        // Creating a HashSet of Strings
        Set<String> fruits = new HashSet<>();

        // Adding elements to the Set
        fruits.add("Apple");
        fruits.add("Banana");
        fruits.add("Orange");

        // Adding a duplicate element (it won't be added)
        fruits.add("Apple");

        // Accessing elements of the Set
        System.out.println("Set of fruits: " + fruits);

        // Checking if an element is present
        String searchFruit = "Banana";
        if (fruits.contains(searchFruit)) {
            System.out.println(searchFruit + " is in the set.");
        } else {
            System.out.println(searchFruit + " is not in the set.");
        }

        // Removing an element
        String removeFruit = "Orange";
        fruits.remove(removeFruit);

        // Displaying the updated Set
        System.out.println("Set after removing " + removeFruit + ": " + fruits);
    }
}
```

In this example, the **HashSet** is used to create a set of fruits. Since a set does not allow duplicates, adding "Apple" again has no effect. It also demonstrates checking for the presence of an element, removing an element, and displaying the final set.

Other implementations of **Set** like **LinkedHashSet** maintain the order of insertion, while **TreeSet** sorts elements in natural order.

Feel free to experiment with different **Set** implementations based on your specific requirements.

