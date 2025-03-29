Here is the complete Java program with the condition for checking if the **10th digit** is odd:  

### **Java Program**
```java
import java.util.Scanner;

public class Hello {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();  // Read input number

        // Extract the 10th digit from the right and check if it's odd
        if ((Math.abs(num) / 1000000000) % 10 % 2 == 1) {
            System.out.print("yes");
        } else {
            System.out.print("no");
        }

        sc.close();  // Close the scanner
    }
}
```

---

### **Simple Explanation**
1. **`Math.abs(num)`** → Converts negative numbers to positive so we don’t get errors when extracting digits.  
2. **`/ 1000000000`** → Moves the **10th digit** to the unit place by removing the last 9 digits.  
3. **`% 10`** → Extracts the **last digit** (which is now the 10th digit of the original number).  
4. **`% 2 == 1`** → Checks if the extracted digit is **odd**.  

If the 10th digit is odd, it prints **"yes"**, otherwise, it prints **"no"**.  

