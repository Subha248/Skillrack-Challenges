### **Problem Statement**  
Write a program that takes an integer **N** as input and prints the first **N** terms of the Fibonacci sequence.

---

### **Code (Java)**
```java
import java.util.Scanner;

public class FibonacciSequence {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        
        int N = scan.nextInt(); // Read the number of terms
        int a = 0, b = 1; // First two Fibonacci numbers
        
        for (int i = 0; i < N; i++) { 
            System.out.print(a + " "); // Print current Fibonacci number
            int next = a + b; // Calculate next number
            a = b;  // Shift a to b
            b = next; // Shift b to next
        }
        
        scan.close();
    }
}
```

---

### **Explanation (Step by Step)**
1. **Input Reading:**  
   - The program reads an integer **N**, which represents how many Fibonacci numbers to print.

2. **Variable Initialization:**  
   - `a = 0` and `b = 1` → These are the first two Fibonacci numbers.

3. **Loop Execution (for first N terms):**  
   - Print `a` (current Fibonacci number).  
   - Compute the next number: `next = a + b`.  
   - Shift values:  
     - `a` takes the value of `b`.  
     - `b` takes the value of `next`.  

4. **Example Execution:**
   - **Input:** `N = 5`  
   - **Output:** `0 1 1 2 3`

---

