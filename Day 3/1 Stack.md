

## ✅ Stack

A **Stack** is a linear data structure that follows the **LIFO (Last In, First Out)** principle.

---

## 📌 Stack Operations

| Operation   | Description             |
| ----------- | ----------------------- |
| `push()`    | Insert an element       |
| `pop()`     | Remove top element      |
| `peek()`    | View top element        |
| `isEmpty()` | Check if stack is empty |
| `isFull()`  | Check if stack is full  |

---

## 🧪 Java Code: Stack Using Array

```java
public class StackUsingArray {
    int top;
    int size;
    int[] stack;

    // Constructor
    public StackUsingArray(int size) {
        this.size = size;
        stack = new int[size];
        top = -1;
    }

    // Push operation
    public void push(int value) {
        if (isFull()) {
            System.out.println("Stack Overflow!");
        } else {
            stack[++top] = value;
            System.out.println(value + " pushed to stack.");
        }
    }

    // Pop operation
    public int pop() {
        if (isEmpty()) {
            System.out.println("Stack Underflow!");
            return -1;
        } else {
            return stack[top--];
        }
    }

    // Peek operation
    public int peek() {
        if (isEmpty()) {
            System.out.println("Stack is empty!");
            return -1;
        } else {
            return stack[top];
        }
    }

    // Check if stack is empty
    public boolean isEmpty() {
        return top == -1;
    }

    // Check if stack is full
    public boolean isFull() {
        return top == size - 1;
    }

    // Display stack
    public void display() {
        if (isEmpty()) {
            System.out.println("Stack is empty!");
        } else {
            System.out.print("Stack elements: ");
            for (int i = 0; i <= top; i++) {
                System.out.print(stack[i] + " ");
            }
            System.out.println();
        }
    }

    // Main method to test
    public static void main(String[] args) {
        StackUsingArray s = new StackUsingArray(5);

        s.push(10);
        s.push(20);
        s.push(30);
        s.display();            // Output: 10 20 30
        System.out.println("Top: " + s.peek());
        System.out.println("Popped: " + s.pop());
        s.display();            // Output: 10 20
    }
}
```

---

## ✅ Output

```
10 pushed to stack.
20 pushed to stack.
30 pushed to stack.
Stack elements: 10 20 30 
Top: 30
Popped: 30
Stack elements: 10 20 
```

---


