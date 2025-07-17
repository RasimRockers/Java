#  `static` in Java

The keyword **`static`** in Java is used to **create fields, methods, blocks, or nested classes** that belong **to the class itself, not to any specific object**.

It means:

* You **don’t need to create an object** to use static members.
* Static members are **shared across all instances** of the class.

---

## 📦 Where can we use `static`?

| Use Case              | Meaning                                  |
| --------------------- | ---------------------------------------- |
| `static` **variable** | Shared variable for all objects          |
| `static` **method**   | Method that can be called without object |
| `static` **block**    | Runs once when class is loaded           |
| `static` **class**    | Nested class (inside another class)      |

---

## ✅ 1. `static` **Variable**

Shared among all objects of a class.

```java
class Counter {
    static int count = 0;  // static variable

    Counter() {
        count++;
        System.out.println("Count = " + count);
    }
}

public class Main {
    public static void main(String[] args) {
        Counter c1 = new Counter();  // Count = 1
        Counter c2 = new Counter();  // Count = 2
        Counter c3 = new Counter();  // Count = 3
    }
}
```

---

## ✅ 2. `static` **Method**

Called without creating an object.

```java
class MathUtil {
    static int square(int x) {
        return x * x;
    }
}

public class Main {
    public static void main(String[] args) {
        int result = MathUtil.square(5);  // no object needed
        System.out.println("Square = " + result);  // Output: 25
    }
}
```

> ❗ Static methods **cannot access non-static members** directly.

---

## ✅ 3. `static` **Block**

Runs **only once** when the class is loaded.

```java
class Demo {
    static {
        System.out.println("Static block executed");
    }

    Demo() {
        System.out.println("Constructor called");
    }
}

public class Main {
    public static void main(String[] args) {
        Demo d1 = new Demo();
        Demo d2 = new Demo();
    }
}
```

**Output:**

```
Static block executed
Constructor called
Constructor called
```

---

## ✅ 4. `static` **Nested Class**

A class inside another class can be static.

```java
class Outer {
    static class Inner {
        void show() {
            System.out.println("Inside static nested class");
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Outer.Inner obj = new Outer.Inner();  // no Outer object needed
        obj.show();
    }
}
```



---

## 💡 When to use `static`?

* When a method or variable should be **shared** across all instances
* Utility methods (like `Math.sqrt()` or `main()`)
* For constants (`static final`)

---




