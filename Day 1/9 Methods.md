

## 🔧 Methods in Java

A **method** in Java is a **block of code** that performs a specific task. Methods are used to:

* **Organize code** into reusable blocks
* **Avoid repetition**
* Improve **readability and maintainability**

---

## 🧠 Syntax of a Method

```java
returnType methodName(parameter1, parameter2, ...) {
    // method body
    return value; // if returnType is not void
}
```

✅ Example:

```java
int add(int a, int b) {
    return a + b;
}
```

---

## ✅ Types of Methods in Java

### 🔹 1. **Predefined Methods**

These are built-in methods provided by Java.

✅ Examples:

```java
System.out.println("Hello");         // println() is predefined
String name = "Java";
int len = name.length();             // length() is predefined
```

---

### 🔹 2. **User-Defined Methods**

Methods you create based on your logic.

---

## 🔧 Example: User-Defined Methods

```java
public class MethodExample {

    // method without return and without parameters
    void greet() {
        System.out.println("Welcome to Java!");
    }

    // method with return and parameters
    int add(int x, int y) {
        return x + y;
    }

    public static void main(String[] args) {
        MethodExample obj = new MethodExample();

        obj.greet();  // calling method

        int sum = obj.add(10, 20);  // calling with parameters
        System.out.println("Sum = " + sum);
    }
}
```

---

## 📦 Method Categories by Return and Parameter

| Type                        | Example                     |
| --------------------------- | --------------------------- |
| No return, no parameter     | `void show()`               |
| No return, with parameter   | `void display(String name)` |
| With return, no parameter   | `int getValue()`            |
| With return, with parameter | `int sum(int a, int b)`     |

---

