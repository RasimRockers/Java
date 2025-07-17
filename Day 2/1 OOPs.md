

##  OOPs in Java

**Object-Oriented Programming (OOP)** is a programming paradigm based on the concept of **"objects"**, which contain **data (fields)** and **methods (functions)**.

Java is a **purely object-oriented language** (except for primitive data types).

---



## 📘 1. **Class** in Java

A **class** is a **blueprint** or **template** from which objects are created. It defines **fields (variables)** and **methods (functions)**.

### ✅ Syntax:

```java
class ClassName {
    // fields (variables)
    // methods (functions)
}
```

### ✅ Example:

```java
class Car {
    String color;  // field
    void drive() { // method
        System.out.println("Car is driving");
    }
}
```

---

## 🚗 2. **Object** in Java

An **object** is a **real-world instance** of a class. It has **state** (data) and **behavior** (methods).

### ✅ How to create an object:

```java
Car myCar = new Car(); // object creation
```

### ✅ Example using object:

```java
myCar.color = "Red";
myCar.drive();   // Output: Car is driving
```

---

## 🧱 3. **Constructor** in Java

A **constructor** is a **special method** that is automatically called **when an object is created**.

### ✅ Features of Constructors:

* Has the **same name as the class**
* **No return type** (not even void)
* Can be **default**, **parameterized**, or **overloaded**

---

## 🔹 Types of Constructors

### 1. **Default Constructor**

Created automatically if no constructor is defined.

```java
class Bike {
    Bike() {
        System.out.println("Bike is created");
    }
}

public class Main {
    public static void main(String[] args) {
        Bike b = new Bike(); // calls default constructor
    }
}
```

---

### 2. **Parameterized Constructor**

Used to pass values at the time of object creation.

```java
class Student {
    String name;
    int age;

    Student(String n, int a) {  // parameterized constructor
        name = n;
        age = a;
    }

    void display() {
        System.out.println(name + " is " + age + " years old");
    }
}

public class Main {
    public static void main(String[] args) {
        Student s1 = new Student("Alice", 20);
        s1.display();
    }
}
```

---


## 💡 Class, Object, Constructor Together — Simple Program

```java
class Person {
    String name;
    int age;

    // Constructor
    Person(String n, int a) {
        name = n;
        age = a;
    }

    // Method
    void showDetails() {
        System.out.println(name + " is " + age + " years old");
    }
}

public class Main {
    public static void main(String[] args) {
        Person p1 = new Person("John", 25);  // object created with constructor
        p1.showDetails();  // method call
    }
}
```

---

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



