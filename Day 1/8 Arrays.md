

## 📦 Array in Java?

An **array** in Java is a **collection of similar data types** stored in **contiguous memory locations**.

* Arrays are **fixed in size**
* They can hold **primitive types** (`int`, `char`, etc.) or **objects**
* The index of arrays starts at **0**

---

## ✅ Syntax for Array Declaration

```java
// Declaration
datatype[] arrayName;

// Creation
arrayName = new datatype[size];

// Declaration + Creation
datatype[] arrayName = new datatype[size];

// Declaration + Creation + Initialization
datatype[] arrayName = {value1, value2, value3};
```

✅ Example:

```java
int[] numbers = new int[5];           // Creates an array of size 5
int[] scores = {90, 85, 70, 88, 76};  // Initializes with values
```

---

## 🧱 Types of Arrays in Java

### 🔹 1. **Single-Dimensional Array**

```java
int[] arr = {1, 2, 3, 4, 5};
```

### 🔹 2. **Multi-Dimensional Array (Matrix)**

```java
int[][] matrix = {
    {1, 2},
    {3, 4}
};
System.out.println(matrix[1][0]);  // Output: 3
```

---

## 🧪 Example Program: Array Basics

```java
public class ArrayExample {
    public static void main(String[] args) {
        int[] marks = new int[3];

        marks[0] = 85;
        marks[1] = 90;
        marks[2] = 95;

        System.out.println("Student Marks:");
        for (int i = 0; i < marks.length; i++) {
            System.out.println("Subject " + (i + 1) + ": " + marks[i]);
        }
    }
}
```

---



## ⚙️ Array Operations in Java

Java provides powerful ways to **create**, **access**, **manipulate**, and **process** arrays.

---

### ✅ 1. **Declare and Initialize Arrays**

```java
int[] nums = {10, 20, 30, 40, 50};
```

OR

```java
int[] nums = new int[5];
nums[0] = 10; // and so on
```

---

### ✅ 2. **Access Elements by Index**

```java
System.out.println(nums[2]);  // Output: 30
```

---

### ✅ 3. **Update Array Elements**

```java
nums[1] = 25;  // Updates index 1 to 25
```

---

### ✅ 4. **Find Length of an Array**

```java
int length = nums.length;
System.out.println("Length: " + length);
```

---

### ✅ 5. **Traverse an Array**

#### a) Using `for` loop:

```java
for (int i = 0; i < nums.length; i++) {
    System.out.println(nums[i]);
}
```

#### b) Using `for-each` loop:

```java
for (int num : nums) {
    System.out.println(num);
}
```

---

### ✅ 6. **Sum of Elements**

```java
int sum = 0;
for (int num : nums) {
    sum += num;
}
System.out.println("Sum: " + sum);
```

---

### ✅ 7. **Find Maximum Element**

```java
int max = nums[0];
for (int num : nums) {
    if (num > max) max = num;
}
System.out.println("Max: " + max);
```

---

### ✅ 8. **Find Minimum Element**

```java
int min = nums[0];
for (int num : nums) {
    if (num < min) min = num;
}
System.out.println("Min: " + min);
```

---

### ✅ 9. **Sort an Array**

Using built-in method:

```java
import java.util.Arrays;

Arrays.sort(nums);
System.out.println("Sorted: " + Arrays.toString(nums));
```

---

### ✅ 10. **Search for an Element**

#### a) Linear Search:

```java
int target = 30;
boolean found = false;
for (int num : nums) {
    if (num == target) {
        found = true;
        break;
    }
}
System.out.println(found ? "Found" : "Not Found");
```

#### b) Binary Search (array must be sorted):

```java
int index = Arrays.binarySearch(nums, 30);
System.out.println(index >= 0 ? "Found at index " + index : "Not Found");
```

---

##  Reverse an Array

```java
for (int i = 0; i < nums.length / 2; i++) {
    int temp = nums[i];
    nums[i] = nums[nums.length - 1 - i];
    nums[nums.length - 1 - i] = temp;
}
System.out.println("Reversed: " + Arrays.toString(nums));
```

---

