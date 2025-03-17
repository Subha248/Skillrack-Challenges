Here is a **simple Java program** that accepts a string `s` and an integer `n`, then prints the first `n` characters of the string. If `n` is greater than the length of the string, it prints the entire string.  

---

### **Code:**
```java
import java.util.Scanner;

public class PrintNCharacters {
    public static void main(String[] args) {
        // Create Scanner object to take input
        Scanner sc = new Scanner(System.in);

        // Accept the string input
        System.out.print("Enter a string: ");
        String s = sc.nextLine();

        // Accept the integer input
        System.out.print("Enter a number (n): ");
        int n = sc.nextInt();

        // Check if n is greater than the string length
        String result = (n <= s.length()) ? s.substring(0, n) : s;

        // Print the result
        System.out.println("Output: " + result);

        // Close scanner
        sc.close();
    }
}
```

---

### **Explanation (Line-by-line):**  
1. **`Scanner sc = new Scanner(System.in);`**  
   - Creates a Scanner object to read input from the user.  

2. **`String s = sc.nextLine();`**  
   - Reads the entire string input from the user.  

3. **`int n = sc.nextInt();`**  
   - Reads an integer input (`n`) from the user.  

4. **Ternary Condition:**  
   ```java
   String result = (n <= s.length()) ? s.substring(0, n) : s;
   ```
   - If `n` is **less than or equal to the length of `s`**, extract the first `n` characters using `s.substring(0, n)`.  
   - If `n` is **greater than the length of `s`**, print the whole string `s` (to avoid an error).  

5. **`System.out.println("Output: " + result);`**  
   - Prints the extracted part of the string.  

6. **`sc.close();`**  
   - Closes the scanner to prevent memory leaks.  

---

### **Example Runs:**

**Input 1:**  
```
Enter a string: HelloWorld
Enter a number (n): 5
```
**Output:**  
```
Output: Hello
```

---

**Input 2:**  
```
Enter a string: Java
Enter a number (n): 10
```
**Output:**  
```
Output: Java
```
(Since `n` is greater than the length of "Java", it prints the full string.)

---

Let me know if you need any more explanations! 😊
