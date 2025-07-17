# Sorting Methods in Java
---
In Java, **sorting** is the process of arranging data in a particular order (ascending or descending). Java provides several **sorting methods** using built-in libraries and custom logic.

---


## 🔸 1. **Bubble Sort**

Compares each pair and swaps if needed.

```java
public class BubbleSort {
    public static void main(String[] args) {
        int[] arr = {5, 2, 8, 1, 3};

        for (int i = 0; i < arr.length - 1; i++) {
            for (int j = 0; j < arr.length - i - 1; j++) {
                if (arr[j] > arr[j + 1]) {
                    // Swap
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }
            }
        }

        for (int num : arr) {
            System.out.print(num + " ");
        }
    }
}
```

---

## 🔸 2. **Selection Sort**

Selects the smallest element and places it at the front.

```java
public class SelectionSort {
    public static void main(String[] args) {
        int[] arr = {4, 1, 3, 9, 2};

        for (int i = 0; i < arr.length - 1; i++) {
            int minIdx = i;

            for (int j = i + 1; j < arr.length; j++) {
                if (arr[j] < arr[minIdx]) {
                    minIdx = j;
                }
            }

            // Swap
            int temp = arr[i];
            arr[i] = arr[minIdx];
            arr[minIdx] = temp;
        }

        for (int num : arr) {
            System.out.print(num + " ");
        }
    }
}
```

---

