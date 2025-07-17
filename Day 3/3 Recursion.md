# **Recursion in Java**

**Recursion** is a technique in Java where a method calls **itself** to solve a problem.

---

###  Why use Recursion?

* Solves problems that can be **broken into smaller subproblems**.
* Common in:

  * Factorial calculation
  * Fibonacci series
  * Tree traversal
  * Tower of Hanoi
  * Backtracking problems

---

### ✅ Basic Syntax

```java
returnType methodName(parameters) {
    if (base_condition) {
        // stop recursion
        return result;
    } else {
        // recursive call
        return methodName(smaller_parameters);
    }
}
```

---

### 🔹 Example 1: Factorial using Recursion

```java
public class RecursionExample {
    static int factorial(int n) {
        if (n == 0)  // base case
            return 1;
        else
            return n * factorial(n - 1);  // recursive call
    }

    public static void main(String[] args) {
        int result = factorial(5);
        System.out.println("Factorial of 5 is: " + result);
    }
}
```

**Output:**

```
Factorial of 5 is: 120
```

---

### 🔹 Example 2: Fibonacci Series using Recursion

```java
public class FibonacciRecursion {
    static int fib(int n) {
        if (n <= 1) return n;  // base case
        return fib(n - 1) + fib(n - 2);  // recursive call
    }

    public static void main(String[] args) {
        int n = 7;
        System.out.print("Fibonacci Series: ");
        for (int i = 0; i < n; i++) {
            System.out.print(fib(i) + " ");
        }
    }
}
```

**Output:**

```
Fibonacci Series: 0 1 1 2 3 5 8
```

---

### 📌 Key Concepts

| Term               | Meaning                                      |
| ------------------ | -------------------------------------------- |
| **Base Case**      | The condition where recursion **stops**      |
| **Recursive Case** | Where function calls **itself**              |
| **Stack Overflow** | Happens if base case is missing or incorrect |

---


