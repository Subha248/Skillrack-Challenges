Here is a **simple Java program** that accepts a string and prints its last **three characters**. If the string has less than three characters, it prints the entire string.  

---

### **Code:**
```java
import java.util.Scanner;

public class LastThreeCharacters {
    public static void main(String[] args) {
        // Create Scanner object to take input
        Scanner sc = new Scanner(System.in);

        // Accept the string input
        System.out.print("Enter a string: ");
        String s = sc.nextLine();

        // Check if string length is less than or equal to 3
        String result = (s.length() <= 3) ? s : s.substring(s.length() - 3);

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

3. **Ternary Condition:**  
   ```java
   String result = (s.length() <= 3) ? s : s.substring(s.length() - 3);
   ```
   - If the **length of `s` is 3 or less**, print the full string.  
   - Otherwise, extract the **last three characters** using `s.substring(s.length() - 3)`.  

4. **`System.out.println("Output: " + result);`**  
   - Prints the extracted part of the string.  

5. **`sc.close();`**  
   - Closes the scanner to prevent memory leaks.  

---

### **Example Runs:**

**Input 1:**  
```
Enter a string: HelloWorld
```
**Output:**  
```
Output: rld
```

---

**Input 2:**  
```
Enter a string: Hi
```
**Output:**  
```
Output: Hi
```
(Since "Hi" has less than 3 characters, the full string is printed.)

---

Let me know if you need any clarifications! 😊
