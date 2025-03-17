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

The condition:  

```java
if (Character.isUpperCase(S.charAt(i)))
```

### **Explanation (Step by Step)**  

1. **`S.charAt(i)`**  
   - This extracts the character at index `i` from the string `S`.  
   - Example: If `S = "VfCtorY"`, then:  
     - `S.charAt(0)` → `'V'`  
     - `S.charAt(1)` → `'f'`  
     - `S.charAt(2)` → `'C'`  
   
2. **`Character.isUpperCase(...)`**  
   - This is a built-in Java method that checks if a given character is an uppercase letter (A-Z).  
   - It returns **`true`** if the character is uppercase and **`false`** otherwise.  

### **Example Execution**  
If the input is:  
```plaintext
VfCtorY
```
The loop will process each character:

| `i` | `S.charAt(i)` | `Character.isUpperCase(S.charAt(i))` |
|----|--------------|--------------------------------|
| 0  | `'V'`       | `true`  (count = 1) |
| 1  | `'f'`       | `false` |
| 2  | `'C'`       | `true`  (count = 2) |
| 3  | `'t'`       | `false` |
| 4  | `'o'`       | `false` |
| 5  | `'r'`       | `false` |
| 6  | `'Y'`       | `true`  (count = 3) |

Final Output:  
```plaintext
3
```

### **Summary**  
✅ `Character.isUpperCase(S.charAt(i))` checks whether each character in the string is uppercase.  
✅ If true, it increments the `count` variable.  
✅ Finally, the program prints the total count of uppercase letters. 
