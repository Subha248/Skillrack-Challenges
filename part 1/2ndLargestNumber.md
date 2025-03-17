
---

### **Java Program: Find the Second Largest Number**
```java
import java.util.Scanner; // Import Scanner class for input

public class Hello { // Class declaration
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in); // Create Scanner object to read input
        
        int N = scan.nextInt(); // Read the number of elements
        
        // Initialize variables to store the largest and second largest numbers
        int largest = Integer.MIN_VALUE;
        int secondLargest = Integer.MIN_VALUE;

        for (int i = 0; i < N; i++) { // Loop through N elements
            int num = scan.nextInt(); // Read the next integer

            if (num > largest) { 
                secondLargest = largest; // Update second largest before updating largest
                largest = num;  // Update largest
            } 
            else if (num > secondLargest && num != largest) { 
                secondLargest = num; // Update second largest if it's smaller than largest
            }
        }

        scan.close(); // Close the scanner to prevent memory leaks
        System.out.println(secondLargest); // Print the second largest number
    }
}
```
---

### **Step-by-Step Explanation:**
1. **Read the number of elements (`N`)** from the user.
2. **Initialize** two variables:
   - `largest`: Holds the **largest number** (initially set to `Integer.MIN_VALUE`).
   - `secondLargest`: Holds the **second largest number** (also set to `Integer.MIN_VALUE`).
3. **Loop through `N` numbers**:
   - If the number is **greater than `largest`**, update `secondLargest` before updating `largest`.
   - Otherwise, if the number is **greater than `secondLargest` but not equal to `largest`**, update `secondLargest`.
4. **Print `secondLargest`** as the final output.

---

### **Example Input & Output**
#### ✅ **Example 1**
```
Input:
3
100
2200
345

Output:
345
```
#### ✅ **Example 2**
```
Input:
5
10
20
5
30
25

Output:
25
```

---

### **Why This Works?**
- Ensures that the **largest** and **second largest** values are always correctly updated.
- Uses **only one loop** for efficiency (**O(N) complexity**).
- Handles **negative numbers** and **repeated values** properly.
Here’s a **test case table** showing how the program processes input step by step.  

---

### **Example 1: Finding the Second Largest Number**  
#### **Input:**
```
5
10
20
5
30
25
```

#### **Step-by-Step Execution:**
| Iteration | Input Number | Largest (`largest`) | Second Largest (`secondLargest`) | Explanation |
|-----------|-------------|----------------------|----------------------|-------------|
| 1         | 10          | 10                   | MIN_VALUE            | First number, update `largest` |
| 2         | 20          | 20                   | 10                   | 20 > 10, update `largest`, `secondLargest` becomes 10 |
| 3         | 5           | 20                   | 10                   | 5 < secondLargest (10), no change |
| 4         | 30          | 30                   | 20                   | 30 > 20, update `largest`, `secondLargest` becomes 20 |
| 5         | 25          | 30                   | 25                   | 25 > 20, update `secondLargest` |

#### **Final Output:**  
```
25
```

---

### **Example 2: Handling Duplicates**  
#### **Input:**
```
4
50
50
20
10
```

#### **Step-by-Step Execution:**
| Iteration | Input Number | Largest (`largest`) | Second Largest (`secondLargest`) | Explanation |
|-----------|-------------|----------------------|----------------------|-------------|
| 1         | 50          | 50                   | MIN_VALUE            | First number, update `largest` |
| 2         | 50          | 50                   | MIN_VALUE            | Duplicate of `largest`, ignore |
| 3         | 20          | 50                   | 20                   | 20 < 50, update `secondLargest` |
| 4         | 10          | 50                   | 20                   | 10 < secondLargest, no change |

#### **Final Output:**  
```
20
```

---

