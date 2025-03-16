### **Java Program to Count Uppercase Letters in a String**  

#### **Code:**
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        String S = scan.nextLine(); // Read input string

        int count = 0; // Initialize count for uppercase letters

        for (int i = 0; i < S.length(); i++) { // Loop through each character
            if (Character.isUpperCase(S.charAt(i))) { // Check if character is uppercase
                count++; // Increment count
            }
        }

        System.out.println(count); // Print the count of uppercase letters
        scan.close();
    }
}
```

#### **Explanation (Step-by-Step Execution)**  
1. **Take Input:**  
   - Read a string `S` from the user.  

2. **Initialize Count:**  
   - Set `count = 0` to track uppercase letters.  

3. **Loop Through String:**  
   - Check each character in `S` using `Character.isUpperCase(S.charAt(i))`.  
   - If uppercase, increase `count`.  

4. **Output Result:**  
   - Print the final `count`.  

#### **Example Execution:**  
**Input:**  
```
VfCtorY
```
**Processing:**  
- 'V' (uppercase) → count = 1  
- 'f' (lowercase) → count = 1  
- 'C' (uppercase) → count = 2  
- 't' (lowercase) → count = 2  
- 'o' (lowercase) → count = 2  
- 'r' (lowercase) → count = 2  
- 'Y' (uppercase) → count = 3  

**Output:**  
```
3
```
