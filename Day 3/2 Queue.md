

## ✅ Queue

A **Queue** is a linear data structure that follows the **FIFO (First In, First Out)** principle.

---

## 📌 Queue Operations

| Operation   | Description                      |
| ----------- | -------------------------------- |
| `enqueue()` | Insert an element into the queue |
| `dequeue()` | Remove the front element         |
| `peek()`    | View the front element           |
| `isEmpty()` | Check if the queue is empty      |
| `isFull()`  | Check if the queue is full       |

---

## 🔹 Java Code: Queue Using Array

```java
public class QueueUsingArray {
    int front, rear, size;
    int capacity;
    int[] queue;

    // Constructor
    public QueueUsingArray(int capacity) {
        this.capacity = capacity;
        queue = new int[capacity];
        front = 0;
        rear = -1;
        size = 0;
    }

    // Enqueue operation
    public void enqueue(int item) {
        if (isFull()) {
            System.out.println("Queue Overflow! Cannot insert " + item);
            return;
        }
        rear = (rear + 1) % capacity;
        queue[rear] = item;
        size++;
        System.out.println(item + " enqueued to queue.");
    }

    // Dequeue operation
    public int dequeue() {
        if (isEmpty()) {
            System.out.println("Queue Underflow! Cannot dequeue.");
            return -1;
        }
        int item = queue[front];
        front = (front + 1) % capacity;
        size--;
        return item;
    }

    // Peek operation
    public int peek() {
        if (isEmpty()) {
            System.out.println("Queue is empty!");
            return -1;
        }
        return queue[front];
    }

    // Check if queue is empty
    public boolean isEmpty() {
        return size == 0;
    }

    // Check if queue is full
    public boolean isFull() {
        return size == capacity;
    }

    // Display queue
    public void display() {
        if (isEmpty()) {
            System.out.println("Queue is empty!");
            return;
        }
        System.out.print("Queue elements: ");
        for (int i = 0; i < size; i++) {
            System.out.print(queue[(front + i) % capacity] + " ");
        }
        System.out.println();
    }

    // Main method to test the queue
    public static void main(String[] args) {
        QueueUsingArray q = new QueueUsingArray(5);

        q.enqueue(10);
        q.enqueue(20);
        q.enqueue(30);
        q.enqueue(40);
        q.display();  // Output: 10 20 30 40

        System.out.println("Dequeued: " + q.dequeue());
        q.display();  // Output: 20 30 40

        q.enqueue(50);
        q.enqueue(60);
        q.display();  // Output: 20 30 40 50 60

        System.out.println("Front: " + q.peek());
        q.enqueue(70); // Queue full
    }
}
```

---

## ✅ Output

```
10 enqueued to queue.
20 enqueued to queue.
30 enqueued to queue.
40 enqueued to queue.
Queue elements: 10 20 30 40 
Dequeued: 10
Queue elements: 20 30 40 
50 enqueued to queue.
60 enqueued to queue.
Queue elements: 20 30 40 50 60 
Front: 20
Queue Overflow! Cannot insert 70
```

---

