```java
import java.util.Scanner;

public class HCF {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        
        int x = scan.nextInt(); // Read first number
        int y = scan.nextInt(); // Read second number
        
        // Finding HCF using the Euclidean Algorithm
        while (y != 0) {
            int temp = y;
            y = x % y;
            x = temp;
        }
        
        scan.close();
        System.out.println(x); // Print HCF
    }
}
```
---

## **Understanding the Code**
This Java program finds the **Highest Common Factor (HCF)** (also called **Greatest Common Divisor (GCD)**) of two numbers using the **Euclidean Algorithm**.

---

### **Step-by-Step Explanation**
#### **1. Import Scanner for Input**
```java
import java.util.Scanner;
```
- We need to take user input, so we import `Scanner` from `java.util` package.

---

#### **2. Define the Main Class and Method**
```java
public class HCF {
    public static void main(String[] args) {
```
- We create a **class** named `HCF`.
- Inside it, we define the `main` method, which is the **starting point** of the program.

---

#### **3. Create Scanner for Input**
```java
Scanner scan = new Scanner(System.in);
```
- `Scanner` is an object that helps us read input from the user.

---

#### **4. Read Two Numbers from User**
```java
int x = scan.nextInt(); // Read first number
int y = scan.nextInt(); // Read second number
```
- The user enters two numbers, which we store in variables **x** and **y**.

---

#### **5. Apply the Euclidean Algorithm**
```java
while (y != 0) {
    int temp = y;
    y = x % y;
    x = temp;
}
```
This loop finds the **HCF** of `x` and `y` using the **Euclidean Algorithm**:
- Keep repeating until `y` becomes **0**.
- In each step:
  1. Store the value of `y` in `temp` (temporary variable).
  2. Replace `y` with `x % y` (**remainder when x is divided by y**).
  3. Assign `x` the value of `temp`.

> 💡 **The process stops when `y = 0`, and `x` will contain the HCF.**

---

#### **6. Close Scanner and Print the Result**
```java
scan.close();
System.out.println(x); // Print HCF
```
- We **close** the scanner to free up system resources.
- Finally, print `x`, which contains the **HCF**.

---

### **Example Walkthrough**
Let's go through an example to see how it works.

#### **Example 1**
**Input:**  
```
12 18
```
**Step-by-Step Execution:**
| Iteration | x  | y  | x % y  | Explanation |
|-----------|----|----|--------|-------------|
| Start     | 12 | 18 |        | Initial values |
| 1         | 18 | 12 | 6      | x becomes 18, y becomes 12 (remainder of 18 ÷ 12) |
| 2         | 12 | 6  | 0      | x becomes 12, y becomes 6 (remainder of 12 ÷ 6) |
| 3         | 6  | 0  |        | y is now 0, loop stops. **HCF = 6** |

**Output:**  
```
6
```

---

#### **Example 2**
**Input:**  
```
20 28
```
**Step-by-Step Execution:**
| Iteration | x  | y  | x % y | Explanation |
|-----------|----|----|--------|-------------|
| Start     | 20 | 28 |        | Initial values |
| 1         | 28 | 20 | 8      | x becomes 28, y becomes 20 (remainder of 28 ÷ 20) |
| 2         | 20 | 8  | 4      | x becomes 20, y becomes 8 (remainder of 20 ÷ 8) |
| 3         | 8  | 4  | 0      | x becomes 8, y becomes 4 (remainder of 8 ÷ 4) |
| 4         | 4  | 0  |        | y is now 0, loop stops. **HCF = 4** |

**Output:**  
```
4
```

---

### **Summary**
1. **Take input** for two numbers.
2. **Use Euclidean Algorithm**:
   - Swap `x` and `y` while `y ≠ 0`.
   - Replace `y` with `x % y` until `y = 0`.
   - The last value of `x` is the **HCF**.
3. **Print the result**.

---

