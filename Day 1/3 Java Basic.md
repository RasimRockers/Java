
## 📝 Comments in Java

**Comments** are **non-executable lines** in Java code meant for **documentation, explanation, or disabling code** during testing. The compiler **ignores** them.

---

### 1. **Single-Line Comment (`//`)**

* Starts with `//`
* Used for short explanations or quick notes

✅ **Example:**

```java
int age = 20; // This stores the user's age
```

---

### 2. **Multi-Line Comment (`/* ... */`)**

* Starts with `/*` and ends with `*/`
* Used for block comments, usually over multiple lines

✅ **Example:**

```java
/* This is a multi-line comment
   explaining the purpose of the following code block */
int sum = a + b;
```

---

## ✅ Best Practices for Using Comments

* Use comments to **explain why**, not what
  *(The code tells what it does, comments explain why it does that)*
* Keep them **short and meaningful**
* Avoid **over-commenting** obvious code
* Use Javadoc for **API-level documentation**

---


---

## 🔁 Input and Output Operations in Java

Java provides powerful and flexible methods for handling **input** (reading data) and **output** (displaying data). I/O operations are done using:

* **Standard I/O (console-based)**
* **File I/O (file-based)** – optional for advanced learners

We'll focus here on **console-based I/O** using classes from the `java.util` and `java.io` packages.

---

## ✅ **1. Output in Java** – `System.out`

### 🖨️ Using `System.out.println()` and `System.out.print()`

| Method      | Description                 |
| ----------- | --------------------------- |
| `println()` | Prints data with a newline  |
| `print()`   | Prints data without newline |

✅ **Example:**

```java
System.out.println("Welcome to Java!");  // With newline
System.out.print("Hello");               // Without newline
System.out.print(" World");              // Continues on same line
```

---

## ✅ **2. Input in Java** – Using `Scanner` Class

### 📥 Using `Scanner` (from `java.util` package)

#### ➤ Step 1: Import the Scanner class

```java
import java.util.Scanner;
```

#### ➤ Step 2: Create Scanner object

```java
Scanner input = new Scanner(System.in);
```
To get **input from the user** in Java (console-based), the most common and modern way is using the **`Scanner` class**.

---




---

### 🔹step 3:  **Use Scanner Methods to Read Input**

| Method          | Data Type     | Example Input |
| --------------- | ------------- | ------------- |
| `nextInt()`     | Integer       | `23`          |
| `nextFloat()`   | Float         | `12.5f`       |
| `nextDouble()`  | Double        | `45.67`       |
| `next()`        | Single word   | `John`        |
| `nextLine()`    | Full sentence | `John Smith`  |
| `nextBoolean()` | true/false    | `true`        |

---

## 🎯 Example Program – Read Name and Age

```java
import java.util.Scanner;

public class InputExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in); // Step 1: Create scanner

        System.out.print("Enter your name: "); 
        String name = sc.nextLine();           // Step 2: Read string

        System.out.print("Enter your age: ");
        int age = sc.nextInt();                // Step 3: Read integer

        System.out.println("Hello " + name + "! You are " + age + " years old.");

        sc.close(); // Step 4: Close scanner
    }
}
```

---

