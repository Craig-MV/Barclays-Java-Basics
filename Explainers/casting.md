## Casting

**Implicit Casting** (Widening):
Implicit casting occurs when you convert a smaller data type to a larger data type. Java does this automatically, and it's considered safe because it doesn't result in any loss of data.

```java
public class ImplicitCastingExample {
    public static void main(String[] args) {
        int intValue = 42;
        long longValue = intValue; // Implicit casting from int to long

        System.out.println("int value: " + intValue);
        System.out.println("long value: " + longValue);
    }
}
```

In this example, the **int** value is implicitly cast to a **long** value without any explicit conversion.

**Explicit Casting** (Narrowing):
Explicit casting is required when you convert a larger data type to a smaller data type. This can result in data loss, so you need to explicitly specify the casting.

```java
public class ExplicitCastingExample {
    public static void main(String[] args) {
        double doubleValue = 3.14;
        int intValue = (int) doubleValue; // Explicit casting from double to int

        System.out.println("double value: " + doubleValue);
        System.out.println("int value: " + intValue);
    }
}
```

In this example, the **double** value is explicitly cast to an **int** value. Note that the fractional part is truncated, and data loss occurs.

**Important Points**

**Upcasting** (Implicit Casting): Automatically converting a smaller data type to a larger data type is safe and doesn't require explicit casting.

**Downcasting** (Explicit Casting): Manually converting a larger data type to a smaller data type requires explicit casting, and it may result in data loss.

**Loss of Precision**: When downcasting, be aware of the potential loss of precision. For example, converting a **double** to an **int** may result in the loss of decimal values.

```java
double value = 123.456;
int intValue = (int) value; // intValue will be 123, and the fractional part is truncated.
```