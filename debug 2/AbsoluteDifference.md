
---

### **Java Program to Compute Absolute Difference**
```java
// Importing Scanner class to take user input
import java.util.Scanner;

public class AbsoluteDifference {
    public static void main(String[] args) {
        // Creating a Scanner object to read input
        Scanner sc = new Scanner(System.in);
        
        // Accepting two integers as input
        int num1 = sc.nextInt();
        int num2 = sc.nextInt();
        
        // Calculating the absolute difference using Math.abs()
        int result = Math.abs(num1 - num2);
        
        // Printing the absolute difference
        System.out.println(result);
        
        // Closing the Scanner
        sc.close();
    }
}
```

---

### **Line-by-Line Explanation**
1. **`import java.util.Scanner;`** → Imports `Scanner` to read user input.  
2. **`public class AbsoluteDifference {`** → Defines a class named `AbsoluteDifference`.  
3. **`public static void main(String[] args) {`** → Main method where execution starts.  
4. **`Scanner sc = new Scanner(System.in);`** → Creates a `Scanner` object.  
5. **`int num1 = sc.nextInt();`** → Reads the first integer input.  
6. **`int num2 = sc.nextInt();`** → Reads the second integer input.  
7. **`int result = Math.abs(num1 - num2);`** → Computes the absolute difference.  
8. **`System.out.println(result);`** → Prints the absolute difference.  
9. **`sc.close();`** → Closes the `Scanner` to free resources.  

---

### **Why This Code Works Well**
✅ Uses **`Math.abs()`** to ensure the result is always positive.  
✅ **Minimal and efficient** for simple input and output operations.  
✅ **Properly closes `Scanner`** to prevent resource leaks.  

