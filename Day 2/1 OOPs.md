

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

