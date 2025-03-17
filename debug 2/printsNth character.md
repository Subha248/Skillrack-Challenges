Here is a **Java program** that accepts a string `s` and an integer `n`, then prints the **nth character** of the string.  

---

### **Java Code**
```java
import java.util.Scanner;

public class NthCharacter {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        String s = scan.nextLine(); // Accept string input
        int n = scan.nextInt(); // Accept integer input

        // Check if n is valid
        if (n > 0 && n <= s.length()) {
            System.out.println(s.charAt(n - 1)); // Print nth character (1-based index)
        } else {
            System.out.println("Invalid input. N is out of range.");
        }
        
        scan.close();
    }
}
```

---

### **Explanation**
1. **Read Input:**  
   - `scan.nextLine()` reads the full string `s`.
   - `scan.nextInt()` reads the integer `n`.
2. **Check Validity:**  
   - Ensure `n` is between `1` and `s.length()`.  
3. **Extract Character:**  
   - `s.charAt(n - 1)` gives the **nth character** (since indexing starts from 0).  
4. **Print the Result.**

---

### **Example**
#### **Input**
```
HelloWorld
4
```
#### **Processing**
- `s.charAt(4 - 1) = s.charAt(3) = 'l'`
#### **Output**
```
l
```

---

Let me know if you need any changes! 😊
