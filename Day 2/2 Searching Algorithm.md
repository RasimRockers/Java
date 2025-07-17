

# Searching in Java

**Searching** is the process of finding a specific element in a collection like an array or list.

---

##  Common Searching Algorithms in Java

| Algorithm         | Works on        | Time Complexity |
| ----------------- | --------------- | --------------- |
| **Linear Search** | Unsorted/sorted | O(n)            |
| **Binary Search** | Sorted only     | O(log n)        |

---

## ✅ 1. Linear Search in Java

Linear Search checks each element one by one.

### 🔹 Code:

```java
public class LinearSearch {
    public static void main(String[] args) {
        int[] arr = {10, 25, 30, 45, 50};
        int key = 30;
        boolean found = false;

        for (int i = 0; i < arr.length; i++) {
            if (arr[i] == key) {
                System.out.println("Element found at index: " + i);
                found = true;
                break;
            }
        }

        if (!found) {
            System.out.println("Element not found");
        }
    }
}
```

### ✅ Output:

```
Element found at index: 2
```

---

## ✅ 2. Binary Search in Java

Binary Search divides the sorted array and searches efficiently.

> ⚠️ **Works only on sorted arrays**

### 🔹 Code:

```java
import java.util.Arrays;

public class BinarySearch {
    public static void main(String[] args) {
        int[] arr = {10, 20, 30, 40, 50};
        int key = 40;
        int low = 0, high = arr.length - 1;

        while (low <= high) {
            int mid = (low + high) / 2;

            if (arr[mid] == key) {
                System.out.println("Element found at index: " + mid);
                return;
            } else if (arr[mid] < key) {
                low = mid + 1;
            } else {
                high = mid - 1;
            }
        }

        System.out.println("Element not found");
    }
}
```

### ✅ Output:

```
Element found at index: 3
```

---

## ✅ 3. Binary Search Using Java Library

Java has a built-in method: `Arrays.binarySearch()`

```java
import java.util.Arrays;

public class BinarySearchLibrary {
    public static void main(String[] args) {
        int[] arr = {5, 10, 20, 30, 40};
        int index = Arrays.binarySearch(arr, 20);
        
        if (index >= 0) {
            System.out.println("Element found at index: " + index);
        } else {
            System.out.println("Element not found");
        }
    }
}
```

---



