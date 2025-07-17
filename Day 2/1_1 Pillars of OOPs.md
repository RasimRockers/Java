# Pillars of OOP

###  The **4 Pillars of OOP (Object-Oriented Programming)** in Java are the foundation of writing structured, reusable, and efficient object-oriented code. 
---

##  1. **Encapsulation**

**Definition:** Wrapping **data** and **methods** together in a single unit (class), and **hiding internal details** from outside access.

### ✅ Key Points:

* Use **private** variables.
* Use **getters and setters** to access them.

###  Example:

```java
class Student {
    private String name;  // data hidden

    // Setter
    public void setName(String n) {
        name = n;
    }

    // Getter
    public String getName() {
        return name;
    }
}

public class Main {
    public static void main(String[] args) {
        Student s = new Student();
        s.setName("Pooja");
        System.out.println("Name: " + s.getName());
    }
}
```

---

##  2. **Inheritance**

**Definition:** One class **inherits** the properties and behaviors of another class using the `extends` keyword.

### ✅ Key Points:

* Promotes **code reusability**.
* `Child` class gets access to `Parent` class methods and fields.

###  Example:

```java
class Animal {
    void sound() {
        System.out.println("Animal makes sound");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog d = new Dog();
        d.sound();  // inherited method
        d.bark();   // own method
    }
}
```

---

##  3. **Polymorphism**

**Definition:** Ability of a method to behave **differently based on the object** that is calling it.

### ✅ Types:

* **Compile-time (Method Overloading)**
* **Runtime (Method Overriding)**

---

### ✅ a) Method Overloading (Same method name, different parameters)

```java
class Calculator {
    int add(int a, int b) {
        return a + b;
    }

    double add(double a, double b) {
        return a + b;
    }
}
```

---

### ✅ b) Method Overriding (Same method in child class)

```java
class Animal {
    void sound() {
        System.out.println("Animal sound");
    }
}

class Cat extends Animal {
    @Override
    void sound() {
        System.out.println("Meow");
    }
}
```

---

##  4. **Abstraction**

**Definition:** Hiding **implementation details** and showing **only the essential features**.

### ✅ Ways to achieve:

* **Abstract Classes**
* **Interfaces**

---

###  Example using Abstract Class:

```java
abstract class Shape {
    abstract void draw();  // abstract method
}

class Circle extends Shape {
    void draw() {
        System.out.println("Drawing Circle");
    }
}
```

---

## ✅ Summary Table

| Pillar        | Purpose                               | Java Feature Used             |
| ------------- | ------------------------------------- | ----------------------------- |
| Encapsulation | Data hiding                           | Private fields, Get/Set       |
| Inheritance   | Code reuse                            | `extends` keyword             |
| Polymorphism  | Dynamic behavior                      | Method Overload/Override      |
| Abstraction   | Hide complexity, show only essentials | `abstract` class, `interface` |

---


